<template>
  <section id="experience" class="py-10">
    <h2 class="mb-6 text-2xl font-bold dark:text-white">Experience</h2>
    <div class="flow-root">
      <ul role="list" class="-mb-8">
        <li v-for="(job, jobIdx) in jobs" :key="job.id">
          <div class="relative pb-8">
            <span v-if="jobIdx !== jobs.length - 1" class="absolute left-5 top-5 -ml-px h-full w-0.5 bg-gray-200 dark:bg-gray-700" aria-hidden="true" />
            <div class="relative flex items-start space-x-3">
              <div class="relative">
                <img class="flex items-center justify-center bg-gray-100 rounded-full dark:bg-gray-800 size-8 ring-2 ring-white dark:ring-gray-900" :src="job.companyLogo" alt="" />
              </div>
              <div class="flex-1 min-w-0">
                <div>
                  <div class="text-sm">
                    <span class="font-medium text-gray-900 dark:text-white">{{ job.position }}</span> - 
                    <span class="font-medium text-gray-900 dark:text-white">{{ job.company }}</span>
                  </div>
                  <p class="mt-0.5 text-sm text-gray-500 dark:text-gray-400">{{ job.location }} | {{ job.period }}</p>
                </div>
                <div class="mt-2 text-sm text-gray-700 dark:text-gray-300">
                  <p>{{ job.description }}</p>
                </div>
              </div>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<script setup>
const jobs = [
  {
    id: 1,
    position: 'Full Stack Software Developer',
    company: 'StellarNurse',
    companyLogo: '/omi-test.png',
    description: 'Led development of a cloud-based SaaS platform. Implemented CI/CD pipelines and microservices architecture. Mentored junior developers and conducted code reviews.',
    location: 'The Netherlands',
    period: 'Jun 2021 - Present',
  },
  {
    id: 2,
    position: 'Full Stack Software Developer',
    company: 'Omi Health',
    companyLogo: '/omi.svg',
    description: 'Developed responsive web applications using Vue.js and Node.js. Designed and implemented RESTful APIs. Collaborated with UX designers to improve user experience.',
    location: 'The Netherlands',
    period: 'Dec 2020 - May 2021',
  },
  {
    id: 3,
    position: 'Software Developer',
    company: 'Freelancer',
    companyLogo: '/omi-test.png',
    description: 'Built interactive user interfaces using modern JavaScript frameworks. Optimized application performance and implemented responsive designs. Participated in agile development processes.',
    location: 'Remote',
    period: 'Jun 2016 - Feb 2018',
  },
]
</script>
