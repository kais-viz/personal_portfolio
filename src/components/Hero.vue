<template>
    <section id="about">
        <div class="bg-white dark:bg-gray-900">
            <header class="absolute inset-x-0 top-0 z-50">
            <Dialog class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
                <div class="fixed inset-0 z-50" />
                <DialogPanel class="fixed inset-y-0 right-0 z-50 w-full px-6 py-6 overflow-y-auto bg-white sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
                <div class="flex items-center justify-between">
                    <a href="#" class="-m-1.5 p-1.5">
                    <span class="sr-only">Your Company</span>
                    <img class="w-auto h-8" src="https://tailwindcss.com/plus-assets/img/logos/mark.svg?color=indigo&shade=600" alt="" />
                    </a>
                    <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
                    <span class="sr-only">Close menu</span>
                    <XMarkIcon class="size-6" aria-hidden="true" />
                    </button>
                </div>
                <div class="flow-root mt-6">
                    <div class="-my-6 divide-y divide-gray-500/10">
                    <div class="py-6 space-y-2">
                        <a v-for="item in navigation" :key="item.name" :href="item.href" class="block px-3 py-2 -mx-3 font-semibold text-gray-900 rounded-lg dark:text-white text-base/7 hover:bg-gray-50 dark:hover:bg-gray-800">{{ item.name }}</a>
                    </div>
                    <div class="py-6">
                        <a href="#" class="-mx-3 block rounded-lg px-3 py-2.5 text-base/7 font-semibold text-gray-900 dark:text-white hover:bg-gray-50 dark:hover:bg-gray-800">Log in</a>
                    </div>
                    </div>
                </div>
                </DialogPanel>
            </Dialog>
            </header>
            <div class="relative overflow-hidden isolate pt-14">
            <div class="px-6 py-32 mx-auto max-w-7xl sm:py-40 lg:px-8">
                <div class="max-w-2xl mx-auto lg:mx-0 lg:grid lg:max-w-none lg:grid-cols-2 lg:gap-x-16 lg:gap-y-8 xl:grid-cols-1 xl:grid-rows-1 xl:gap-x-8">
                <h1 class="max-w-2xl text-5xl font-semibold tracking-tight text-gray-900 dark:text-white text-balance sm:text-7xl lg:col-span-2 xl:col-auto">We’re changing the way people connect</h1>
                <div class="max-w-xl mt-6 lg:mt-0 xl:col-end-1 xl:row-start-1">
                    <p class="text-lg font-medium text-gray-500 dark:text-gray-300 text-pretty sm:text-xl/8">Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui lorem cupidatat commodo. Elit sunt amet fugiat veniam occaecat fugiat aliqua. Anim aute id magna aliqua ad ad non deserunt sunt. Qui irure qui lorem cupidatat commodo.</p>
                    <div class="flex items-center mt-10 gap-x-6">
                    <a href="#" class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Get started</a>
                    <a href="#" class="font-semibold text-gray-900 dark:text-white text-sm/6">Learn more <span aria-hidden="true">→</span></a>
                    </div>
                </div>
                <img src="/kais.jpg" alt="Kais Kawar" class="mt-10 aspect-[6/5] w-full max-w-xl rounded-2xl object-cover sm:mt-16 lg:mt-0 lg:max-w-none xl:row-span-2 xl:row-end-2   
        xl:mt-36" />
                </div>
            </div>
            <div class="absolute inset-x-0 bottom-0 h-24 -z-10 bg-gradient-to-t from-white dark:from-gray-900 sm:h-32" />
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'

const navigation = [


  { name: 'Product', href: '#' },
  { name: 'Features', href: '#' },
  { name: 'Marketplace', href: '#' },
  { name: 'Company', href: '#' },
]

const mobileMenuOpen = ref(false)
</script>
