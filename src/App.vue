<template>
  <div id="app" class="relative bg-gray-100 antialiased text-gray-800">

    <header class="bg-deep-ocean fixed z-10 w-full">
      <div class="px-6 flex justify-between max-w-7xl xl:mx-auto">
        <div class="flex">
          <div class="relative flex items-center ">
            <a href="#home">
              <svg class="h-8 w-8 md:h-10 md:w-10 fill-current text-gray-100 hover:text-gray-500" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><path d="M22.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 2.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 22.25 15z"></path><path d="M27.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 7.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 27.25 15z"></path></g></svg>
            </a>
            <button class="absolute pl-8 w-full h-full md:hidden">
              <svg class="h-5 w-5 fill-current text-gray-100" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><path d="M14.25 6.507L9.003 11.75 3.75 6.5" stroke-width="1.5" stroke="currentColor" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"></path></svg>
            </button>
          </div>
          <nav class="invisible md:visible flex w-full">
              <div class="ml-8 py-4 md:py-6 inline-block border-b-2 border-teal-400 w-auto">
                <a class="text-gray-500 hover:text-gray-300 cursor-pointer font-semibold">Home</a>
              </div>
              <div class="ml-8 py-4 md:py-6 inline-block">
                <a class="text-gray-500 hover:text-gray-300 cursor-pointer font-semibold">Library</a>
              </div>
              <div class="ml-8 py-4 md:py-6 inline-block">
                <a class="text-gray-500 hover:text-gray-300 cursor-pointer font-semibold">Releases</a>
              </div>
              <div class="ml-8 py-4 md:py-6 inline-block">
                <a class="text-gray-500 hover:text-gray-300 cursor-pointer font-semibold">Samples</a>
              </div>
          </nav>
        </div>
        <div class="flex">
          <button class="relative">
            <svg class="h-6 w-6 fill-current text-gray-100 hover:text-gray-500" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M14 5c-.294-1.162-1.081-2-2.006-2-.913 0-1.69.864-1.994 2" fill="currentColor"></path><path d="M9 17.25a3 3 0 0 0 6 0" stroke="currentColor" stroke-width="1.5"></path><path d="M17.25 13.248l.503 1c.827 0 1.497.666 1.497 1.5 0 .83-.68 1.502-1.497 1.502H6.247a1.495 1.495 0 0 1-1.497-1.501c0-.83.68-1.501 1.497-1.501l.503-1v-2.994c0-3.04 2.24-5.504 5.004-5.504h.492c2.764 0 5.004 2.471 5.004 5.504v2.994z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path></g></svg>
            <div class="absolute z-40 right-0">
              <div class="mt-4 bg-white rounded-sm w-96 shadow-xl overflow-y-hidden ">
                <div class="p-4 flex justify-between items-center">
                  <span>Notifications</span>
                  <button type="button">Mark all as seen</button>
                </div>
                <div class="overflow-y-auto h-64">
                  <div v-bind:key="notification.id" v-for="(notification, i) in notifications" :class="{'border-t' : i === 0 }" class="border-b">
  	                  <Notification :notification="notification"/>
  	              </div>
                </div>
              </div>
            </div>
          </button>
          <button class="hidden md:block relative ml-6">
            <img class="w-10 h-10 rounded-full" src="./assets/img/Profile.jpg" alt="">
          </button>
        </div>
      </div>
    </header>

    <main class="px-5 pt-16 sm:pt-20 md:pt-24  pb-6 md:px-10 xl:mx-auto max-w-8xl">

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
<!-- stats -->
      <div class="block lg:flex">
	      <section class="block sm:flex sm:flex-wrap sm:-mx-2 lg:w-1/2">
	        <div v-bind:key="stat.id" v-for="stat in stats" class="card mt-4 text-center sm:w-1/2 sm:px-2">
	          <UserStats :stat="stat"/>
	        </div>
	      </section>
	<!-- tracks -->
	      <section class="mt-4 bg-white rounded lg:w-1/2 lg:ml-4">
	        <div class="p-6 inline-block w-full">
	          <h2 class="text-sm text-gray-500">Recent work</h2>
	            <div class="mt-8">
	                <div v-bind:key="track.id" v-for="(track, i) in tracks" :class="{'border-t' : i === 0 }" class="border-b">
	                  <MasteredTrack :track="track"/>
	                </div>
	            </div>
	            <a class="mt-1 inline-block text-xs float-right font-semibold" href="#">See all files</a>
	        </div>
	      </section>
      </div>

<!-- selecetd posts -->
      <section class="lg:flex lg:-mx-2">
      <!-- blog post-->
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
      <!-- samples post -->
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
   
      <NewsletterSubscribe/>

    </main>
    
      <Footer/>

  </div>
</template>

<script>
import UserStats from "@/components/UserStats.vue";
import MasteredTrack from "@/components/MasteredTrack.vue";
import Notification from "@/components/Notification.vue";
import NewsletterSubscribe from "@/components/NewsletterSubscribe.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: 'app',
  components: {
    UserStats,
    MasteredTrack,
    Notification,
    NewsletterSubscribe,
    Footer,
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
      notifications: [
        {
          notificationTitle: "Moon Rising-9e",
          notificationDate: "Jul 6, 2019",
        },
        {
          notificationTitle: "MR-Master FREE VSTs - no",
          notificationDate: "Jul 6, 2019",
        },
        {
          notificationTitle: "MR-Master-9c-NO_LIMIT",
          notificationDate: "Jul 6, 2019",
        },
        {
          notificationTitle: "Moon Rising-9e",
          notificationDate: "Jul 6, 2019",
        },
        {
          notificationTitle: "Moon Rising-9c",
          notificationDate: "Jul 6, 2019",
        },
        {
          notificationTitle: "Moon Rising-9b",
          notificationDate: "Jul 6, 2019",
        },
      ],
    }
  }
}
</script>

<style src="./assets/css/tailwind.css"></style>
