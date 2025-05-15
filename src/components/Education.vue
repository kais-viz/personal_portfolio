<template>
  <section id="education" class="py-10">
    <h2 class="text-2xl font-bold mb-6 dark:text-white">Education</h2>
    <div class="flow-root">
      <ul role="list" class="-mb-8">
        <li v-for="(education, educationIdx) in educations" :key="education.id">
          <div class="relative pb-8">
            <span v-if="educationIdx !== educations.length - 1" class="absolute left-5 top-5 -ml-px h-full w-0.5 bg-gray-200 dark:bg-gray-700" aria-hidden="true" />
            <div class="relative flex items-start space-x-3">
              <div class="relative">
                <img class="flex items-center justify-center bg-gray-100 dark:bg-gray-800 rounded-full size-10 ring-8 ring-white dark:ring-gray-900" :src="education.schoolLogo" alt="" />
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
const educations = [
  {
    id: 1,
    degree: 'Master of Computer Science',
    school: 'Stanford University',
    schoolLogo: 'https://images.unsplash.com/photo-1522071820081-009f0129c71c?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=8&w=256&h=256&q=80',
    description: 'Specialized in Artificial Intelligence and Machine Learning. Completed thesis on neural network optimization techniques. Participated in research projects and published papers in international conferences.',
    location: 'Stanford, CA',
    period: '2018 - 2020',
  },
  {
    id: 2,
    degree: 'Bachelor of Science in Computer Engineering',
    school: 'MIT',
    schoolLogo: 'https://images.unsplash.com/photo-1507537297725-24a1c029d3ca?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=8&w=256&h=256&q=80',
    description: 'Graduated with honors. Focused on software engineering and systems design. Completed capstone project on distributed systems. Active member of the Robotics Club.',
    location: 'Cambridge, MA',
    period: '2014 - 2018',
  },
  {
    id: 3,
    degree: 'High School Diploma',
    school: 'Tech Preparatory Academy',
    schoolLogo: 'https://images.unsplash.com/photo-1519389950473-47ba0277781c?ixlib=rb-1.2.1&auto=format&fit=facearea&facepad=8&w=256&h=256&q=80',
    description: 'Graduated with highest honors. Participated in national programming competitions. Founded the school\'s Computer Science Club. Received scholarship for academic excellence.',
    location: 'Seattle, WA',
    period: '2010 - 2014',
  },
]
</script>
