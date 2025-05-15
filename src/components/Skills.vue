<template>
  <div>
    <h3 class="text-base font-semibold text-gray-900">Technical Skills</h3>
    <dl class="grid grid-cols-1 mt-5 overflow-hidden bg-white divide-y divide-gray-200 rounded-lg shadow md:grid-cols-4 md:divide-x md:divide-y-0">
      <div v-for="skill in skills" :key="skill.name" class="px-4 py-5 sm:p-6">
        <dt class="text-base font-normal text-gray-900">{{ skill.name }}</dt>
        <dd class="flex items-center justify-center mt-4">
          <img :src="skill.logo" :alt="skill.name" class="w-16 h-16" />
        </dd>
      </div>
    </dl>
  </div>
</template>

<script setup>
const skills = [
  { 
    name: 'Python', 
    logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg'
  },
  { 
    name: 'Vue.js', 
    logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg'
  },
  { 
    name: 'Nuxt.js', 
    logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nuxtjs/nuxtjs-original.svg'
  },
  { 
    name: 'MySQL', 
    logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg'
  },
  { 
    name: 'AWS', 
    logo: 'https://www.svgrepo.com/show/353443/aws.svg'
  },
  { 
    name: 'Azure', 
    logo: 'https://cdn.jsdelivr.net/gh/devicons/devicon/icons/azure/azure-original.svg'
  }
]
</script>
