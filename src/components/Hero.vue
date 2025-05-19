<template>
<section id="about">
  <div class="bg-white dark:bg-gray-900">
    <div class="relative pt-8 overflow-hidden isolate sm:pt-14">
      <div class="px-6 py-12 mx-auto max-w-7xl sm:py-16 lg:px-8">
        <div class="flex flex-col items-start gap-8 md:flex-row">
          <!-- Left side content -->
          <div class="w-full space-y-6 md:w-1/2">          
            <h1 class="text-4xl font-bold text-gray-800 dark:text-white md:text-4xl -ml-0.5">Delivering High-Impact Software Solutions</h1>
            <p class="text-2xl text-gray-600 dark:text-gray-300">I'm <span @click="incrementClicks" class="transition-colors cursor-pointer ">Kais Kawar</span>, a Full Stack Software Developer specializing in building robust, data-driven, and scalable cloud-based applications.</p>
            <p class="text-lg text-gray-600 dark:text-gray-300">I leverage Python, Node.js, Vue.js, and AWS to deliver robust solutions, from reliable ETL pipelines to high-performance web applications, ensuring your data works for you and your systems scale smoothly.</p>
            
            <!-- Social media icons and CV download -->
            <div class="flex flex-wrap items-center gap-x-6 gap-y-4">
              <a href="https://linkedin.com/in/kaiskawar" target="_blank" rel="noopener noreferrer" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                <span class="sr-only">LinkedIn</span>
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                </svg>
              </a>
              <a href="https://github.com/kais-viz" target="_blank" rel="noopener noreferrer" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                <span class="sr-only">GitHub</span>
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                  <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd" />
                </svg>
              </a>
              <a href="https://medium.com/@kaiskawar" target="_blank" rel="noopener noreferrer" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-300">
                <span class="sr-only">Medium</span>
                <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                  <path d="M13.54 12a6.8 6.8 0 01-6.77 6.82A6.8 6.8 0 010 12a6.8 6.8 0 016.77-6.82A6.8 6.8 0 0113.54 12zM20.96 12c0 3.54-1.51 6.42-3.38 6.42-1.87 0-3.39-2.88-3.39-6.42s1.52-6.42 3.39-6.42 3.38 2.88 3.38 6.42M24 12c0 3.17-.53 5.75-1.19 5.75-.66 0-1.19-2.58-1.19-5.75s.53-5.75 1.19-5.75C23.47 6.25 24 8.83 24 12z"/>
                </svg>
              </a>
              <a href="/KaisKawar_CV.pdf" download class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Download CV</a>
            </div>
          </div>
          <!-- Right side image -->
          <div class="flex justify-center w-full md:w-1/2">
            <img
              src="/kais.jpg"
              alt="Kais Kawar"
              class="h-auto max-w-full rounded-lg shadow-lg"
            />
          </div>
        </div>
        
        <div v-if="showSimba" class="p-6 mt-12 transition-all duration-500 transform bg-gray-100 rounded-lg shadow-lg dark:bg-gray-800 animate-fade-in">
          <div class="flex flex-col items-center gap-8 md:flex-row">
            <div class="w-full md:w-1/2">
              <h3 class="mb-4 text-2xl font-bold text-gray-800 dark:text-white">I like your curiousity, just like Simba!</h3>
              <p class="text-lg text-gray-600 dark:text-gray-300">
                He's my coding companion who supervises every line of code with silent judgement.
                Known for his curious nature and occasional keyboard contributions. 😸
              </p>
            </div>
            <div class="flex justify-center w-full md:w-1/2">
              <img
                src="/simba.jpg"
                alt="Simba the cat"
                class="h-auto max-w-full rounded-lg shadow-lg"
              />
            </div>
          </div>
        </div>
      </div>
      <div class="absolute inset-x-0 bottom-0 h-24 -z-10 bg-gradient-to-t from-white dark:from-gray-900 sm:h-32" />
    </div>
  </div>
</section>
</template>
<script>
export default {
  name: 'HeroNew',
  data() {
    return {
      clickCount: 0,
      showSimba: false
    }
  },
  methods: {
    incrementClicks() {
      this.clickCount++;
      if (this.clickCount >= 5) {
        this.showSimba = true;
      }
    }
  }
}
</script>

<style scoped>
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-fade-in {
  animation: fadeIn 0.5s ease-out forwards;
}
</style>
