<template>
<section id="about">
  <div class="bg-white dark:bg-gray-900">
    <div class="relative pt-8 overflow-hidden isolate sm:pt-14">
      <div class="px-6 py-12 mx-auto max-w-7xl sm:py-16 lg:px-8">
        <div class="flex flex-col items-start gap-8 md:flex-row">
          <!-- Left side content -->
          <div class="w-full space-y-6 md:w-1/2">          
            <h1 class="text-4xl font-bold text-gray-800 dark:text-white md:text-4xl -ml-0.5">Delivering High-Impact Software Solutions.</h1>
            <p class="text-2xl text-gray-600 dark:text-gray-300">I'm Kais Kawar, a Full Stack Software Engineer specializing in building robust, data-driven, and scalable cloud-based applications.</p>
            <p class="text-lg text-gray-600 dark:text-gray-300">Leveraging Python, Node.js, Vue.js, and AWS, I deliver innovative solutions from reliable ETL pipelines to high-performance web applications, ensuring your data works for you and your systems handle growth effortlessly.</p>
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
      </div>
      <div class="absolute inset-x-0 bottom-0 h-24 -z-10 bg-gradient-to-t from-white dark:from-gray-900 sm:h-32" />
    </div>
  </div>
</section>
</template>
<script>
export default {
  name: 'HeroNew'
}
</script>