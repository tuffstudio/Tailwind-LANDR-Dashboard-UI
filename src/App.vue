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

    <main class="px-5 py-6 md:px-10 max-w-6xl xl:mx-auto">

      <div class="hidden sm:flex justify-between items-center">
        <h1 class="text-2xl font-semibold" >Welcome to LANDR</h1>
        <a class="px-6 py-3 inline-block bg-yellow-500 text-xs leading-none font-semibold text-white rounded-sm" href="#">See Plans</a>
      </div>
<!-- banner -->
      <section class="mt-4 md:mt-8 flex shrink-0">
        <div class="relative p-5 md:px-12 md:py-24 w-full">
          <img class="absolute inset-0 h-full w-full rounded object-cover" src="./assets/img/banner-collab.jpg" alt="Guy in the music studio">
          <div class="p-4 md:p-6 w-9/12 max-w-lg relative">
            <h2 class="text-3xl md:text-5xl leading-tight md:leading-none text-white font-semibold tracking-wide">Share tracks & ask for opinions.</h2>
            <p class="mt-3 text-white">Take notes for yourself, or ask for feedback after you've mastered.</p>
            <a class="mt-5 inline-block px-8 py-3 bg-gray-100 text-sm text-gray-700 font-semibold rounded-sm" href="#">Get feedback</a>
          </div>
        </div>
      </section>

      <div class="block lg:flex">
	<!-- stats -->
	      <section class="block sm:flex sm:flex-wrap sm:-mx-2 lg:w-1/2">
	        <div v-for="(stat, i) in stats" class="card mt-4 text-center sm:w-1/2 sm:px-2">
	          <UserStats :stat="stat"/>
	        </div>
	      </section>
	<!-- tracks -->
	      <section class="mt-4 bg-white rounded lg:w-1/2 lg:ml-4">
	        <div class="p-6 inline-block w-full">
	          <h2 class="text-sm text-gray-500">Recent work</h2>
	            <div class="mt-8">
	                <div v-for="(track, i) in tracks" :class="{'border-t' : i === 0 }" class="border-b">
	                  <MasteredTrack :track="track"/>
	                </div>
	            </div>
	            <a class="mt-1 inline-block text-xs float-right font-semibold" href="#">See all files</a>
	        </div>
	      </section>
      </div>
      <section class="lg:flex lg:-mx-2">
  <!-- blog -->
        <div class="mt-4 lg:w-1/2 lg:pl-2 lg:pr-4 ">
          <section class="card h-full bg-white rounded hover:shadow-lg">
            <a href="#" class="p-6 inline-block md:flex justify-between">
              <div>
                <h2 class="text-sm text-gray-500">The LANDR Blog</h2>
                <p class="mt-4 text-lg font-semibold">Get the best tools, tips and inspiration you need to grow your music everyday.</p>
              </div>
              <img class="hidden md:block h-24 w-32 p-2" src="./assets/img/ill-empty_state-blog.svg" alt="">
            </a>
          </section>
        </div>
  <!-- samples -->
        <div class="mt-4 lg:w-1/2 lg:pl-0 lg:pr-2 ">
         <section class="card relative h-full rounded hover:shadow-lg">
          <div class="p-6 relative z-10 sm:w-7/12">
            <a href="#" class="inline-block">
              <h2 class="text-sm text-gray-500">LANDR Samples</h2>
              <p class="mt-4 text-lg font-semibold">Stay inspired with free curated sample packs from top artists.</p>
            </a>
          </div>
          <img class="absolute inset-0 w-full h-full object-cover rounded" src="./assets/img/samples-background@2x.jpg" alt="Hand playing synth">
        </section>
        </div>
      </section>
<!-- newsletter -->
      <section class="mt-4 p-6 bg-white rounded">

        <div class="md:flex md:items-center md:-mx-2">
          <div class="w-full md:w-1/2 md:px-2">
            <h2 class="text-2xl leading-tight font-semibold tracking-wide">Stay in the loop with the LANDR newsletter</h2>
            <p class="mt-4 text-sm text-gray-600">Sing up to get the best music tips, tools and tutorials direct to your inbox.</p>
          </div>
          
          <div class="w-full md:w-1/2 md:px-2">
            <form class="w-full mt-12 md:mt-0">
              <div class="flex items-center border">
                <input class="py-1 px-4 appearance-none bg-transparent w-full text-gray-700 leading-tight focus:outline-none" type="email" placeholder="Email" aria-label="Email">
                <button class="py-3 px-5 flex-shrink-0 border-l text-sm font-semibold text-teal-400" type="button">
                  Subscribe
                </button>
              </div>
            </form>   
          </div> 
        </div> 

      </section>

    </main>
    <footer class="px-4 py-2 md:px-10 border-t sm:flex sm:justify-between">
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
import UserStats from "@/components/UserStats.vue";
import MasteredTrack from "@/components/MasteredTrack.vue";

export default {
  name: 'app',
  components: {
    UserStats,
    MasteredTrack,
  },
  data(){
    return{
      stats: [
        {
          title: "Master",
          imageUrl: 'https://app.landr.com/images/dashboard/ill-empty_state-collab.svg',
          imageAlt: "Mastering stats",
          tagline: "",
        },
        {
          title: "Collaborate",
          imageUrl: 'https://app.landr.com/images/dashboard/ill-empty_state-collab.svg',
          imageAlt: "Cat and human playin on synth",
          tagline: "Share tracks, get feedback, make better music.",
        },
        {
          title: "Distribute",
          imageUrl: 'https://app.landr.com/images/dashboard/ill-empty_state-collab.svg',
          imageAlt: "Distribution stats",
          tagline: "",
        },
        {
          title: "Promote",
          imageUrl: 'https://app.landr.com/images/dashboard/ill-empty_state-collab.svg',
          imageAlt: "Promotion stats",
          tagline: "",
        },
      ],
      tracks: [
        {
          trackTitle: "Moon Rising-9e",
          masterDate: "Jul 6, 2019",
          masterCount: 2,
        },
        {
          trackTitle: "MR-Master FREE VSTs - no",
          masterDate: "Jul 6, 2019",
          masterCount: 2,
        },
        {
          trackTitle: "MR-Master-9c-NO_LIMIT",
          masterDate: "Jul 6, 2019",
          masterCount: 3,
        },
        {
          trackTitle: "Moon Rising-9e",
          masterDate: "Jul 6, 2019",
          masterCount: 1,
        },
        {
          trackTitle: "Moon Rising-9c",
          masterDate: "Jul 6, 2019",
          masterCount: 2,
        },
        {
          trackTitle: "Moon Rising-9b",
          masterDate: "Jul 6, 2019",
          masterCount: 1,
        },
      ],
    }
  }
}
</script>

<style src="./assets/css/tailwind.css"></style>
