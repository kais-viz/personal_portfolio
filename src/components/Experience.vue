<template>
  <section id="experience" class="py-16 bg-white dark:bg-gray-900 sm:py-20">
    <div class="px-6 mx-auto max-w-7xl lg:px-8">
      <h2 class="mb-6 text-2xl font-bold dark:text-white">Experience</h2>
    <div class="flow-root">
      <ul role="list" class="-mb-8">
        <li v-for="(job, jobIdx) in jobs" :key="job.id">
          <div class="relative pb-8">
            <span v-if="jobIdx !== jobs.length - 1" class="absolute left-4 top-4 -ml-px h-full w-0.5 bg-gray-200 dark:bg-gray-700" aria-hidden="true" />
            <div class="relative flex items-start space-x-3">
              <div class="relative flex items-center justify-center flex-shrink-0 mt-1 bg-indigo-100 rounded-full dark:bg-indigo-900 size-9">
                <span class="text-xs font-medium text-indigo-600 dark:text-indigo-300">{{ job.company.charAt(0) }}</span>
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
                  <ul v-if="job.bullets && job.bullets.length" class="mt-2 ml-5 space-y-1 list-disc">
                    <li v-for="(bullet, index) in job.bullets" :key="index">{{ bullet }}</li>
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
const jobs = [
  {
    id: 1,
    position: 'Full Stack Software Developer',
    company: 'StellarNurse',
    description: '',
    bullets: [
      "Designed scalable cloud-base application for job collection system, utilising Python, AWS's SQS and Lambda functions, Serverless Framework, and MySQL",
      "Led the integration of job data from Google Jobs and agencies using DataForSEO and a pretrained Llama model, ensuring efficient data storage and processing using an innovative approach",
      "Developed an anonymous email sending service to mask sender and receiver identities using Python and AWS SES, ensuring 100% anonymity for all users",
      "Adopted a Test-Driven Development (TDD) approach using pytest for unit testing, improving code coverage and helped reduce post-deployment bugs",
      "Developed a responsive frontend using VueJS and NuxtJS, naturally improving page load speeds"
    ],
    location: 'The Netherlands',
    period: 'Jun 2021 - Present',
  },
  {
    id: 2,
    position: 'Full Stack Software Developer',
    company: 'Omi Health',
    description: '',
    bullets: [
      "Developed and deployed a data-driven, Dash-powered website on GCP, allowing for real-time predictive COVID-19 insights",
      "Developed Python ETL scripts for automated data transformation and optimized data storage in MySQL",
      "Architected and implemented a scalable technology stack to enhance cost efficiency and mitigate vendor-locking risks, demonstrating flexibility in leading the migration from GCP to AWS and reducing infrastructure costs by 75%",
      "Designed and developed a modern frontend using VueJS and NuxtJS, achieving a 150% improvement in page load speed",
      "Implemented AWS RDS for a scalable database solution and leveraged Docker Swarm for an efficient deployment"
    ],
    location: 'The Netherlands',
    period: 'Dec 2020 - May 2021',
  },
  {
    id: 3,
    position: 'Software Developer',
    company: 'Freelancer',
    description: 'Built interactive user interfaces using modern JavaScript frameworks.',
    bullets: [
      "Independently managed the development of MailAwesome, a SaaS CRM helpdesk solution designed to streamline business operations by integrating Gmail for team collaboration; aimed at small-to-medium businesses",
      "Developed backend services for ticket automation using Gmail API and Java Spring Framework, leveraging MongoDB's NoSQL capabilities for efficient data modeling and querying",
      "Designed data visualization dashboards and reports, working on a contract basis with Foresite, my previous employer, utilising D3/DC.js",
      "Independently managed project planning, product development, and research initiatives from scratch, demonstrating business development skills",
      "Demonstrated creativity and adaptability by self-publishing and selling over 5,000 public domain books on Amazon Kindle Digital Publishing, leveraging data from Goodreads, Wikipedia, and Amazon API"
    ],
    location: 'Remote',
    period: 'Sep 2016 - Mar 2019',
  },
  {
    id: 4,
    position: 'Frontend Web Developer',
    company: 'Foresite Web Design',
    description: '',
    bullets: [
      "Developed user-focused Drupal websites using JavaScript, PHP, and Python",
      "Worked in a collaborative team setting to deliver client projects; some are featured on the company's website"
    ],
    location: 'Jordan',
    period: 'Oct 2013 - Aug 2016',
  },
]
</script>
