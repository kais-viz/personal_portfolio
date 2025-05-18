<template>
  <section id="contact">
    <div class="px-6 py-16 pb-24 mx-auto bg-white sm:pb-32 dark:bg-gray-900 isolate sm:py-20 max-w-7xl lg:px-8">
      <div class="max-w-2xl mx-auto text-center">
        <h2 class="text-4xl font-semibold tracking-tight text-gray-900 dark:text-white text-balance sm:text-5xl">Let's Connect</h2>
      </div>
      <div v-if="formSubmitted" class="max-w-xl mx-auto mt-16 text-center sm:mt-10">
        <h3 class="mb-4 text-2xl font-medium text-gray-900 dark:text-white">Thank you!</h3>
        <p class="text-lg text-gray-600 dark:text-gray-300">I will get back to you as soon as possible.</p>
      </div>
      <form v-else class="max-w-xl mx-auto mt-16 sm:mt-10" @submit.prevent="handleSubmit">
        <div class="grid grid-cols-1 gap-x-8 gap-y-6 sm:grid-cols-2">
          <div class="sm:col-span-2">
            <label for="email" class="block font-semibold text-gray-900 dark:text-white text-sm/6">Email</label>
            <div class="mt-2.5">
              <input type="email" name="email" id="email" autocomplete="email" class="block w-full rounded-md bg-white dark:bg-gray-800 px-3.5 py-2 text-base text-gray-900 dark:text-white outline outline-1 -outline-offset-1 outline-gray-300 dark:outline-gray-600 placeholder:text-gray-400 dark:placeholder:text-gray-500 focus:outline focus:outline-2 focus:-outline-offset-2 focus:outline-indigo-600" />
            </div>
          </div>
          <div class="sm:col-span-2">
            <label for="message" class="block font-semibold text-gray-900 dark:text-white text-sm/6">Message</label>
            <div class="mt-2.5">
              <textarea name="message" id="message" rows="4" class="block w-full rounded-md bg-white dark:bg-gray-800 px-3.5 py-2 text-base text-gray-900 dark:text-white outline outline-1 -outline-offset-1 outline-gray-300 dark:outline-gray-600 placeholder:text-gray-400 dark:placeholder:text-gray-500 focus:outline focus:outline-2 focus:-outline-offset-2 focus:outline-indigo-600" />
            </div>
          </div>
        </div>
        <div class="mt-10">
          <button type="submit" class="block w-full rounded-md bg-indigo-600 px-3.5 py-2.5 text-center text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Submit</button>
        </div>
      </form>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const formSubmitted = ref(false)

const handleSubmit = async (e) => {
  const formData = new FormData(e.target);
  
  try {
    const response = await fetch('https://formspree.io/f/xqaqnwjk', {
      method: 'POST',
      body: formData,
      headers: {
        'Accept': 'application/json'
      }
    });
    
    if (response.ok) {
      formSubmitted.value = true;
    } else {
      alert('There was a problem submitting your form. Please try again.');
    }
  } catch (error) {
    console.error('Error submitting form:', error);
    alert('There was a problem submitting your form. Please try again.');
  }
}
</script>
