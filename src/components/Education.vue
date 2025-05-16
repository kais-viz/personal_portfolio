<template>
  <section id="education" class="py-16 bg-white dark:bg-gray-900 sm:py-20">
    <div class="px-6 mx-auto max-w-7xl lg:px-8">
      <h2 class="mb-6 text-2xl font-bold dark:text-white">Education</h2>
    <div class="flow-root">
      <ul role="list" class="-mb-8">
        <li v-for="(education, educationIdx) in educations" :key="education.id">
          <div class="relative pb-8">
            <span v-if="educationIdx !== educations.length - 1" class="absolute left-5 top-5 -ml-px h-full w-0.5 bg-gray-200 dark:bg-gray-700" aria-hidden="true" />
            <div class="relative flex items-start space-x-3">
              <div class="relative">
                <img class="flex items-center justify-center bg-gray-100 rounded-full dark:bg-gray-800 size-9 ring-6 ring-white dark:ring-gray-900" :src="education.schoolLogo" alt="" />
              </div>
              <div class="flex-1 min-w-0">
                <div>
                  <div class="text-sm">
                    <span class="font-medium text-gray-900 dark:text-white">{{ education.degree }}</span> at 
                    <span class="font-medium text-gray-900 dark:text-white">{{ education.school }}</span>
                  </div>
                  <p class="mt-0.5 text-sm text-gray-500 dark:text-gray-400">{{ education.location }} | {{ education.period }}</p>
                </div>
                <div class="mt-2 text-sm text-gray-700 dark:text-gray-300">
                  <p>{{ education.description }}</p>
                  <ul v-if="education.bullets && education.bullets.length" class="mt-2 ml-5 space-y-1 list-disc">
                    <li v-for="(bullet, index) in education.bullets" :key="index">{{ bullet }}</li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </li>
      </ul>
      </div>
    </div>
  </section>
</template>

<script setup>
const educations = [
  {
    id: 1,
    degree: 'Data Analytics and Machine Learning',
    school: 'Ubiqum Code Academy',
    schoolLogo: '/ubiqum.jpeg',
    description: 'Five-month full-time project-based bootcamp using realistic business cases and datasets (see RPubs). During the course, I built machine learning pipelines and models for multiple projects. The following are some highlights:',
    bullets: [
      "Predicted purchasing trends using R for market basket analysis utilising historical transaction records",
      "Analysed energy consumption patterns, reducing consumption by up to 26%",
      "Conducted sentiment analysis for iPhone vs Samsung Galaxy. Automation of web-scraping using Common Crawl, task distribution using Amazon EMR, and analysing the text to data solutions using R",
      "Developed an indoor positioning system by leveraging WiFi fingerprinting; reducing the error to 8m",
      "Created compelling visualisations with ggplot and plotly for each project, helping communicate insights to the team effictively"
    ],
    location: 'Amsterdam, The Netherlands',
    period: 'Mar 2019 - Sep 2019',
  },
  {
    id: 2,
    degree: 'Master of Science in Computer Science',
    school: 'University of Liverpool',
    schoolLogo: '/uni_of_liverpool.jpeg',
    description: 'Thesis: Developed and designed an iOS recipe app, built with Objective C and CodeIgniter.',
    bullets: [],
    location: 'Liverpool, United Kingdom',
    period: '2012 - 2013',
  },
  {
    id: 3,
    degree: 'Bachelor of Engineering in Civil Engineering',
    school: 'University of Liverpool',
    schoolLogo: '/uni_of_liverpool.jpeg',
    description: 'Thesis: Modelled residual pollution from the Mersey Estuary and impact on the estuary.',
    bullets: [],
    location: 'Liverpool, United Kingdom',
    period: '2009 - 2012',
  },
]
</script>
