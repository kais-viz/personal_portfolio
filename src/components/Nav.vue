<template>                                                                                                                                                    
  <header class="sticky top-0 z-50 bg-white dark:bg-gray-900 shadow-sm dark:shadow-gray-800/10">                                                                                                                  
    <nav class="flex items-center justify-between p-6 mx-auto max-w-7xl lg:px-8" aria-label="Global">                                                         
      <div class="flex items-center">                                                                                                                
        <div class="hidden lg:flex lg:gap-x-12">                                                                                                              
          <a v-for="item in navigation" :key="item.name" :href="item.href" class="font-semibold text-gray-900 text-sm/6 dark:text-white">{{ item.name }}</a>  
        </div>                                                                                                                                                
      </div>                                                                                                                                                  
      <div class="flex lg:hidden">                                                                                                                            
        <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700 dark:text-gray-200" @click="mobileMenuOpen 
= true">                                                                                                                                                      
          <span class="sr-only">Open main menu</span>                                                                                                         
          <Bars3Icon class="size-6" aria-hidden="true" />                                                                                                     
        </button>                                                                                                                                             
      </div>                                                                                                                                                  
      <div class="hidden lg:flex lg:items-center lg:gap-x-6">                                                                                                 
        <!-- Dark mode toggle -->                                                                                                                             
        <button @click="toggleDarkMode" class="p-2 text-gray-500 rounded-full dark:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-700">                   
          <SunIcon v-if="isDarkMode" class="size-5" aria-hidden="true" />                                                                                     
          <MoonIcon v-else class="size-5" aria-hidden="true" />                                                                                               
          <span class="sr-only">Toggle dark mode</span>                                                                                                       
        </button>                                                                                                                                             
      </div>                                                                                                                                                  
    </nav>                                                                                                                                                    
    <Dialog class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">                                                                         
      <div class="fixed inset-0 z-10" />                                                                                                                      
      <DialogPanel class="fixed inset-y-0 right-0 z-10 w-full px-6 py-6 overflow-y-auto bg-white dark:bg-gray-900 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10 dark:sm:ring-gray-100/10">                                                                                                                                    
        <div class="flex items-center justify-between">                                                                                                       
          <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700 dark:text-gray-200" @click="mobileMenuOpen = false">                             
            <span class="sr-only">Close menu</span>                                                                                                           
            <XMarkIcon class="size-6" aria-hidden="true" />                                                                                                   
          </button>                                                                                                                                           
        </div>                                                                                                                                                
        <div class="flow-root mt-6">                                                                                                                          
          <div class="-my-6 divide-y divide-gray-500/10 dark:divide-gray-500/30">                                                                             
            <div class="py-6 space-y-2">                                                                                                                      
              <a v-for="item in navigation" :key="item.name" :href="item.href" class="block px-3 py-2 -mx-3 font-semibold text-gray-900 rounded-lg text-base/7 dark:text-white hover:bg-gray-50 dark:hover:bg-gray-800">{{ item.name }}</a>                                                                                  
            </div>
            <div class="py-6">                                                                                                                                
              <!-- Dark mode toggle in mobile menu -->                                                                                                        
              <button @click="toggleDarkMode" class="-mx-3 flex w-full items-center rounded-lg px-3 py-2.5 text-base/7 font-semibold text-gray-900            
dark:text-white hover:bg-gray-50 dark:hover:bg-gray-800">                                                                                                     
                <span class="mr-3">{{ isDarkMode ? 'Light Mode' : 'Dark Mode' }}</span>                                                                       
                <SunIcon v-if="isDarkMode" class="size-5" aria-hidden="true" />                                                                               
                <MoonIcon v-else class="size-5" aria-hidden="true" />                                                                                         
              </button>
            </div>                                                                                                                                            
          </div>                                                                                                                                              
        </div>                                                                                                                                                
      </DialogPanel>                                                                                                                                          
    </Dialog>                                                                                                                                                 
  </header>                                                                                                                                                   
</template>                                                                                                                                                   
                                                                                                                                                              
<script setup>                                                                                                                                                
import { ref, onMounted } from 'vue'                                                                                                                          
import { Dialog, DialogPanel } from '@headlessui/vue'                                                                                                         
import { Bars3Icon, XMarkIcon, SunIcon, MoonIcon } from '@heroicons/vue/24/outline'                                                                           
                                                                                                                                                              
const navigation = [                                                                                                                                          
  { name: 'About', href: '#about' },                                                                                                                             
  { name: 'Experience', href: '#experience' },   
  { name: 'Skills', href: '#skills' },                                                                                                                          
  { name: 'Education', href: '#education' },                                                                                                                         
  { name: 'Contact', href: '#contact' },                                                                                                                           
]                                                                                                                                                             
                                                                                                                                                              
const mobileMenuOpen = ref(false)                                                                                                                             
const isDarkMode = ref(false)                                                                                                                                 
                                                                                                                                                              
// Function to toggle dark mode                                                                                                                               
const toggleDarkMode = () => {                                                                                                                                
  isDarkMode.value = !isDarkMode.value                                                                                                                        
  if (isDarkMode.value) {                                                                                                                                     
    document.documentElement.classList.add('dark')                                                                                                            
    localStorage.setItem('darkMode', 'true')                                                                                                                  
  } else {                                                                                                                                                    
    document.documentElement.classList.remove('dark')                                                                                                         
    localStorage.setItem('darkMode', 'false')                                                                                                                 
  }                                                                                                                                                           
}                                                                                                                                                             
                                                                                                                                                              
// Check for saved user preference on component mount                                                                                                         
onMounted(() => {                                                                                                                                             
  const savedDarkMode = localStorage.getItem('darkMode')                                                                                                      
  if (savedDarkMode === 'true' ||                                                                                                                             
      (savedDarkMode === null && window.matchMedia('(prefers-color-scheme: dark)').matches)) {                                                                
    isDarkMode.value = true                                                                                                                                   
    document.documentElement.classList.add('dark')                                                                                                            
  }                                                                                                                                                           
})                                                                                                                                                            
</script>
