<template>
  <div id="app" class="relative bg-gray-100 antialiased text-gray-800">

    <header class="h-16">
      <div class="px-6 py-4 flex justify-between bg-deep-ocean fixed z-10 w-full">
        <button class="flex items-center ">
          <svg class="h-8 w-8 fill-current text-gray-100" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><path d="M22.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 2.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 22.25 15z"></path><path d="M27.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 7.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 27.25 15z"></path></g></svg>
          <svg class="h-5 w-5 fill-current text-gray-100" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><path d="M14.25 6.507L9.003 11.75 3.75 6.5" stroke-width="1.5" stroke="currentColor" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"></path></svg>
        </button>
        <button class="">
          <svg class="h-6 w-6 fill-current text-gray-100" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M14 5c-.294-1.162-1.081-2-2.006-2-.913 0-1.69.864-1.994 2" fill="currentColor"></path><path d="M9 17.25a3 3 0 0 0 6 0" stroke="currentColor" stroke-width="1.5"></path><path d="M17.25 13.248l.503 1c.827 0 1.497.666 1.497 1.5 0 .83-.68 1.502-1.497 1.502H6.247a1.495 1.495 0 0 1-1.497-1.501c0-.83.68-1.501 1.497-1.501l.503-1v-2.994c0-3.04 2.24-5.504 5.004-5.504h.492c2.764 0 5.004 2.471 5.004 5.504v2.994z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path></g></svg>
        </button>
      </div>
    </header>

    <main class="px-5 py-6">

      <div class="hidden sm:flex justify-between items-center">
        <h1 class="text-2xl font-semibold" >Welcome to LANDR</h1>
        <a class="px-6 py-3 inline-block bg-yellow-500 text-xs leading-none font-semibold text-white rounded-sm" href="#">See Plans</a>
      </div>

      <section class="mt-4 flex shrink-0">
        <div class="relative p-5 w-full">
          <img class="absolute inset-0 h-full w-full rounded object-cover" src="./assets/img/banner-collab.jpg" alt="Guy in the music studio">
          <div class="p-4 w-9/12 relative">
            <h2 class="text-3xl leading-tight text-white font-semibold tracking-wide">Share tracks & ask for opinions.</h2>
            <p class="mt-3 text-white">Take notes for yourself, or ask for feedback after you've mastered.</p>
            <a class="mt-5 inline-block px-8 py-3 bg-gray-100 text-sm text-gray-700 font-semibold rounded-sm" href="#">Get feedback</a>
          </div>
        </div>
      </section>

      <div class="block sm:flex sm:flex-wrap sm:-mx-2">
      
          <section class="mt-4 card text-center sm:w-1/2 sm:px-2">
            <a href="#" class="p-6 bg-white inline-block rounded hover:shadow-lg">
              <h2 class="text-sm text-gray-500">Master</h2>
              <img class="p-12 pb-8" src="./assets/img/ill-empty_state-collab.svg" alt="Cat and human playing on the synth">
              <p class="text-lg font-semibold">Share tracks, get feedback, make better music.</p>
            </a>
          </section>
  
          <section class="mt-4 card text-center sm:w-1/2 sm:px-2">
            <a href="#" class="p-6 bg-white inline-block rounded hover:shadow-lg">
              <h2 class="text-sm text-gray-500">Collaborate</h2>
              <img class="p-12 pb-8" src="./assets/img/ill-empty_state-collab.svg" alt="Cat and human playing on the synth">
              <p class="text-lg font-semibold">Share tracks, get feedback, make better music.</p>
            </a>
          </section>
  
        <section class="mt-4 card text-center sm:w-1/2 sm:px-2">
          <a href="#" class="p-6 bg-white inline-block rounded hover:shadow-lg">
            <h2 class="text-sm text-gray-500">Distriute</h2>
            <img class="p-12 pb-8" src="./assets/img/ill-empty_state-collab.svg" alt="Cat and human playing on the synth">
            <p class="text-lg font-semibold">Share tracks, get feedback, make better music.</p>
          </a>
        </section>
  
        <section class="mt-4 card text-center sm:w-1/2 sm:px-2">
          <a href="#" class="p-6 bg-white inline-block rounded hover:shadow-lg">
            <h2 class="text-sm text-gray-500">Promote</h2>
            <img class="p-12 pb-8" src="./assets/img/ill-empty_state-collab.svg" alt="Cat and human playing on the synth">
            <p class="text-lg font-semibold">Share tracks, get feedback, make better music.</p>
          </a>
        </section>
      </div>

      <section class="mt-4 bg-white rounded">
        <div class="p-6 inline-block w-full">
          <h2 class="text-sm text-gray-500">Recent work</h2>
            
            <div class="mt-8">

              <div class="flex items-center border-t border-b cursor-pointer">
                <div class="pl-0 pr-4 py-4">
                  <svg class="h-8 w-8" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><circle cx="9.5" cy="20.5" r="1.75"></circle><circle cx="19" cy="19" r="1.75"></circle><path d="M11.25 20v-6.5M20.75 18.25V11.5" stroke-linecap="square"></path><path stroke-linejoin="round" d="M11.25 9.75l9.5-2v5l-9.5 2z"></path><rect x="3.75" y="3.75" width="22.5" height="22.5" rx="1.25"></rect></g></svg>
                </div>
                <div class="leading-tight">
                  <div class="flex items-end">
                    <h3 class="font-semibold hover:underline">Moon Rising-9e</h3>
                    <svg class="w-4 h-4 ml-1 fill-current text-gray-500" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M6.563 13.827a6 6 0 1 1 7.403-5.188 2.001 2.001 0 0 0-3.274 2.111H8.256c-1.12 0-2.006.895-2.006 2 0 .398.115.767.313 1.077zM8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" fill="currentColor"></path><path d="M8.5 12.75h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"></path><path stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" d="M12.75 10.25l2.5 2.5-2.5 2.5"></path></g></svg>
                  </div>
                  <span class="text-sm text-gray-500">Jul 5, 2019 &middot; 1 Master</span>
                </div>
              </div>
  
              <div class="flex items-center border-b cursor-pointer">
                <div class="pl-0 pr-4 py-4">
                  <svg class="h-8 w-8" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><circle cx="9.5" cy="20.5" r="1.75"></circle><circle cx="19" cy="19" r="1.75"></circle><path d="M11.25 20v-6.5M20.75 18.25V11.5" stroke-linecap="square"></path><path stroke-linejoin="round" d="M11.25 9.75l9.5-2v5l-9.5 2z"></path><rect x="3.75" y="3.75" width="22.5" height="22.5" rx="1.25"></rect></g></svg>
                </div>
                <div class="leading-tight">
                  <div class="flex items-end">
                    <h3 class="font-semibold hover:underline">MR-Master FREE VSTs - no</h3>
                    <svg class="w-4 h-4 ml-1 fill-current text-gray-500" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M6.563 13.827a6 6 0 1 1 7.403-5.188 2.001 2.001 0 0 0-3.274 2.111H8.256c-1.12 0-2.006.895-2.006 2 0 .398.115.767.313 1.077zM8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" fill="currentColor"></path><path d="M8.5 12.75h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"></path><path stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" d="M12.75 10.25l2.5 2.5-2.5 2.5"></path></g></svg>
                  </div>
                  <span class="text-sm text-gray-500">Jul 5, 2019 &middot; 1 Master</span>
                </div>
              </div>

              <div class="flex items-center border-b cursor-pointer">
                <div class="pl-0 pr-4 py-4">
                  <svg class="h-8 w-8" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><circle cx="9.5" cy="20.5" r="1.75"></circle><circle cx="19" cy="19" r="1.75"></circle><path d="M11.25 20v-6.5M20.75 18.25V11.5" stroke-linecap="square"></path><path stroke-linejoin="round" d="M11.25 9.75l9.5-2v5l-9.5 2z"></path><rect x="3.75" y="3.75" width="22.5" height="22.5" rx="1.25"></rect></g></svg>
                </div>
                <div class="leading-tight">
                  <div class="flex items-end">
                    <h3 class="font-semibold hover:underline">MR-Master-9c-NO_LIMIT</h3>
                    <svg class="w-4 h-4 ml-1 fill-current text-gray-500" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M6.563 13.827a6 6 0 1 1 7.403-5.188 2.001 2.001 0 0 0-3.274 2.111H8.256c-1.12 0-2.006.895-2.006 2 0 .398.115.767.313 1.077zM8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" fill="currentColor"></path><path d="M8.5 12.75h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"></path><path stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" d="M12.75 10.25l2.5 2.5-2.5 2.5"></path></g></svg>
                  </div>
                  <span class="text-sm text-gray-500">Jul 5, 2019 &middot; 1 Master</span>
                </div>
              </div>

              <div class="flex items-center border-b cursor-pointer">
                <div class="pl-0 pr-4 py-4">
                  <svg class="h-8 w-8" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><circle cx="9.5" cy="20.5" r="1.75"></circle><circle cx="19" cy="19" r="1.75"></circle><path d="M11.25 20v-6.5M20.75 18.25V11.5" stroke-linecap="square"></path><path stroke-linejoin="round" d="M11.25 9.75l9.5-2v5l-9.5 2z"></path><rect x="3.75" y="3.75" width="22.5" height="22.5" rx="1.25"></rect></g></svg>
                </div>
                <div class="leading-tight">
                  <div class="flex items-end">
                    <h3 class="font-semibold hover:underline">Moon Rising-9c</h3>
                    <svg class="w-4 h-4 ml-1 fill-current text-gray-500" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M6.563 13.827a6 6 0 1 1 7.403-5.188 2.001 2.001 0 0 0-3.274 2.111H8.256c-1.12 0-2.006.895-2.006 2 0 .398.115.767.313 1.077zM8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" fill="currentColor"></path><path d="M8.5 12.75h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"></path><path stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" d="M12.75 10.25l2.5 2.5-2.5 2.5"></path></g></svg>
                  </div>
                  <span class="text-sm text-gray-500">Jul 5, 2019 &middot; 1 Master</span>
                </div>
              </div>

              <div class="flex items-center border-b cursor-pointer">
                <div class="pl-0 pr-4 py-4">
                  <svg class="h-8 w-8" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><circle cx="9.5" cy="20.5" r="1.75"></circle><circle cx="19" cy="19" r="1.75"></circle><path d="M11.25 20v-6.5M20.75 18.25V11.5" stroke-linecap="square"></path><path stroke-linejoin="round" d="M11.25 9.75l9.5-2v5l-9.5 2z"></path><rect x="3.75" y="3.75" width="22.5" height="22.5" rx="1.25"></rect></g></svg>
                </div>
                <div class="leading-tight">
                  <div class="flex items-end">
                    <h3 class="font-semibold hover:underline">Moon Rising-9b</h3>
                    <svg class="w-4 h-4 ml-1 fill-current text-gray-500" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M6.563 13.827a6 6 0 1 1 7.403-5.188 2.001 2.001 0 0 0-3.274 2.111H8.256c-1.12 0-2.006.895-2.006 2 0 .398.115.767.313 1.077zM8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" fill="currentColor"></path><path d="M8.5 12.75h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"></path><path stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" d="M12.75 10.25l2.5 2.5-2.5 2.5"></path></g></svg>
                  </div>
                  <span class="text-sm text-gray-500">Jul 5, 2019 &middot; 1 Master</span>
                </div>
              </div>

              <div class="flex items-center border-b cursor-pointer">
                <div class="pl-0 pr-4 py-4">
                  <svg class="h-8 w-8" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><circle cx="9.5" cy="20.5" r="1.75"></circle><circle cx="19" cy="19" r="1.75"></circle><path d="M11.25 20v-6.5M20.75 18.25V11.5" stroke-linecap="square"></path><path stroke-linejoin="round" d="M11.25 9.75l9.5-2v5l-9.5 2z"></path><rect x="3.75" y="3.75" width="22.5" height="22.5" rx="1.25"></rect></g></svg>
                </div>
                <div class="leading-tight">
                  <div class="flex items-end">
                    <h3 class="font-semibold hover:underline">Moon Rising-9a test2</h3>
                    <svg class="w-4 h-4 ml-1 fill-current text-gray-500" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M6.563 13.827a6 6 0 1 1 7.403-5.188 2.001 2.001 0 0 0-3.274 2.111H8.256c-1.12 0-2.006.895-2.006 2 0 .398.115.767.313 1.077zM8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" fill="currentColor"></path><path d="M8.5 12.75h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"></path><path stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" d="M12.75 10.25l2.5 2.5-2.5 2.5"></path></g></svg>
                  </div>
                  <span class="text-sm text-gray-500">Jul 5, 2019 &middot; 1 Master</span>
                </div>
              </div>

            </div>

            <a class="mt-1 inline-block text-xs float-right font-semibold" href="#">See all files</a>

        </div>
      </section>

      <section class="mt-4 card bg-white rounded hover:shadow-lg">
        <a href="#" class="p-6 inline-block">
          <h2 class="text-sm text-gray-500">The LANDR Blog</h2>
          <p class="mt-4 text-lg font-semibold">Get the best tools, tips and inspiration you need to grow your music everyday.</p>
        </a>
      </section>

       <section class="mt-4 relative card rounded hover:shadow-lg">
        <div class="p-6 relative z-10 sm:w-7/12">
          <a href="#" class="inline-block">
            <h2 class="text-sm text-gray-500">LANDR Samples</h2>
            <p class="mt-4 text-lg font-semibold">Stay inspired with free curated sample packs from top artists.</p>
          </a>
        </div>
        <img class="absolute inset-0 w-full h-full object-cover" src="./assets/img/samples-background@2x.jpg" alt="Hand playing synth">
      </section>

      <section class="mt-4 p-6 bg-white rounded">
        <h2 class="text-2xl leading-tight font-semibold tracking-wide">Stay in the loop with the LANDR newsletter</h2>
        <p class="mt-4 text-sm text-gray-600">Sing up to get the best music tips, tools and tutorials direct to your inbox.</p>
        
        <form class="w-full mt-12">
          <div class="flex items-center border">
            <input class="py-1 px-4 appearance-none bg-transparent w-full text-gray-700 leading-tight focus:outline-none" type="email" placeholder="Email" aria-label="Email">
            <button class="py-3 px-5 flex-shrink-0 border-l text-sm font-semibold text-teal-400" type="button">
              Subscribe
            </button>
          </div>
        </form>     

      </section>

    </main>
    <footer class="px-4 py-2 border-t sm:flex sm:justify-between">
      <div>
        <a class="text-sm underline hover:no-underline" href="#">Privacy Policy</a>
        <span class="mx-1">-</span>
        <a class="text-sm underline hover:no-underline" href="#">Terms of Service</a>
      </div>
      
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
