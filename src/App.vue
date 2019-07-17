<template>
  <div id="app" class="bg-gray-100 antialiased text-gray-800">
    <header class="bg-gray-900">
      <div class="px-6 py-4 flex justify-between">
        <button class="flex items-center ">
          <svg class="h-8 w-8 fill-current text-gray-100" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><path d="M22.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 2.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 22.25 15z"></path><path d="M27.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 7.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 27.25 15z"></path></g></svg>
          <svg class="h-5 w-5 fill-current text-gray-100" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><path d="M14.25 6.507L9.003 11.75 3.75 6.5" stroke-width="1.5" stroke="currentColor" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"></path></svg>
        </button>
        <button class="">
          <svg class="h-6 w-6 fill-current text-gray-100" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M14 5c-.294-1.162-1.081-2-2.006-2-.913 0-1.69.864-1.994 2" fill="currentColor"></path><path d="M9 17.25a3 3 0 0 0 6 0" stroke="currentColor" stroke-width="1.5"></path><path d="M17.25 13.248l.503 1c.827 0 1.497.666 1.497 1.5 0 .83-.68 1.502-1.497 1.502H6.247a1.495 1.495 0 0 1-1.497-1.501c0-.83.68-1.501 1.497-1.501l.503-1v-2.994c0-3.04 2.24-5.504 5.004-5.504h.492c2.764 0 5.004 2.471 5.004 5.504v2.994z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path></g></svg>
        </button>
      </div>
    </header>
    <main class="p-4">
      <div class="hidden sm:block">
        <h1>Welcome to LANDR</h1>
        <a href="#">See Plans</a>
      </div>
      <section class="mt-4 flex shrink-0">
        <div class="relative p-5">
          <img class="absolute inset-0 h-full w-full rounded object-cover" src="https://app.landr.com/images/dashboard/banner-collab.jpg" alt="Guy in the music studio">
          <div class="p-4 w-9/12 relative">
            <h2 class="text-3xl leading-tight text-white font-semibold tracking-wide">Share tracks & ask for opinions.</h2>
            <p class="mt-3 text-white text-md">Take notes for yourself, or ask for feedback after you've mastered.</p>
            <a class="mt-5 inline-block px-8 py-3 bg-gray-100 text-sm text-gray-700 font-semibold rounded-sm" href="#">Get feedback</a>
          </div>
        </div>
      </section>
      <section class="mt-4 text-center bg-white rounded">
        <a href="#" class="inline-block p-6 hover:shadow-lg hover:underline">
          <h2 class="text-sm text-gray-500">Collaborate</h2>
          <img class="p-12 pb-8" src="https://app.landr.com/images/dashboard/ill-empty_state-collab.svg" alt="Cat and human playing on the synth">
          <p class="text-lg font-semibold">Share tracks, get feedback, make better music.</p>
        </a>
      </section>
    </main>
    <footer class="px-4 py-2 border-t ">
      <a class="text-sm underline hover:no-underline" href="#">Privacy Policy</a>
      <span>-</span>
      <a class="text-sm underline hover:no-underline" href="#">Terms of Service</a>
      <div class="text-sm flex items-center">
        <span class="text-xs">
          &copy;
        </span>
        <p class="mx-1">
          2019 LANDR. Need help?
        </p>
        <a class="text-teal-400 underline hover:no-underline" href="#">
          Contact support
        </a>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'app',
  components: {}
}
</script>

<style src="./assets/css/tailwind.css"></style>
