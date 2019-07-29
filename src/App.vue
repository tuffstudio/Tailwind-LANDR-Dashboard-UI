<template>
  <div id="app" class="relative bg-gray-100 antialiased text-gray-800">
    
    <Header/>

    <main class="px-5 pt-16 sm:pt-20 md:pt-24  pb-6 md:px-10 xl:mx-auto max-w-8xl">

      <section class="hidden sm:flex justify-between items-center">
        <h1 class="text-2xl font-semibold" >Welcome to LANDR</h1>
        <a href="#" class="px-6 py-3 inline-block bg-yellow-500 text-xs leading-none font-semibold text-white rounded-sm">See Plans</a>
      </section>
<!-- banner -->
      <section class="mt-4 md:mt-8 flex shrink-0">
        <div class="relative p-5 md:px-12 md:py-24 w-full">
          <img class="absolute inset-0 h-full w-full rounded object-cover" src="./assets/img/banner-collab.jpg" alt="Guy in the music studio">
          <div class="p-4 md:p-6 w-9/12 max-w-lg relative">
            <h2 class="text-3xl md:text-5xl leading-tight md:leading-none text-white font-semibold tracking-wide">Share tracks & ask for opinions.</h2>
            <p class="mt-3 text-white">Take notes for yourself, or ask for feedback after you've mastered.</p>
            <a href="#" class="mt-5 inline-block px-8 py-3 bg-gray-100 text-sm text-gray-700 font-semibold rounded-sm">Get feedback</a>
          </div>
        </div>
      </section>
<!-- stats -->
      <section class="block lg:flex">
	      <div class="block sm:flex sm:flex-wrap sm:-mx-2 lg:w-1/2">
	        <figure v-bind:key="stat.id" v-for="stat in stats" class="card mt-4 text-center sm:w-1/2 sm:px-2">
	          <UserStats :stat="stat"/>
	        </figure>
	      </div>
	<!-- tracks -->
	      <article class="mt-4 bg-white rounded lg:w-1/2 lg:ml-4">
	        <div class="p-6 inline-block w-full">
	          <h2 class="text-sm text-gray-500">Recent work</h2>
	            <div class="mt-8">
	                <div v-bind:key="track.id" v-for="(track, i) in tracks" :class="{'border-t' : i === 0 }" class="border-b">
	                  <MasteredTrack :track="track"/>
	                </div>
	            </div>
	            <a href="#" class="mt-1 inline-block text-xs float-right font-semibold">See all files</a>
	        </div>
	      </article>
      </section>

<!-- selecetd posts -->
      <aside class="lg:flex lg:-mx-2">
      <!-- blog post-->
        <div class="mt-4 lg:w-1/2 lg:pl-2 lg:pr-4 ">
          <article class="card h-full bg-white rounded hover:shadow-lg">
            <a href="#" class="p-6 inline-block md:flex justify-between">
              <div>
                <h2 class="text-sm text-gray-500">The LANDR Blog</h2>
                <p class="mt-4 text-lg font-semibold">Get the best tools, tips and inspiration you need to grow your music everyday.</p>
              </div>
              <img class="hidden md:block h-24 w-32 p-2" src="./assets/img/ill-empty_state-blog.svg" alt="">
            </a>
          </article>
        </div>
      <!-- samples post -->
        <div class="mt-4 lg:w-1/2 lg:pl-0 lg:pr-2 ">
         <article class="card relative z-0 h-full rounded hover:shadow-lg">
            <div class="p-6 relative sm:w-7/12">
              <a href="#" class="inline-block relative z-10">
                <h2 class="text-sm text-gray-500">LANDR Samples</h2>
                <p class="mt-4 text-lg font-semibold">Stay inspired with free curated sample packs from top artists.</p>
              </a>
            </div>
            <img class="absolute inset-0 w-full h-full object-cover rounded" src="./assets/img/samples-background@2x.jpg" alt="Hand playing synth">
          </article>
        </div>
      </aside>
   
      <aside class="mt-4 p-6 bg-white rounded">
        <NewsletterSubscribe/>
      </aside>

    </main>
    
      <Footer/>

  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import UserStats from "@/components/UserStats.vue";
import MasteredTrack from "@/components/MasteredTrack.vue";
import Notification from "@/components/subcomponents/Notification.vue";
import NewsletterSubscribe from "@/components/NewsletterSubscribe.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: 'app',
  components: {
    Header,
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
      // notifications: [
      //   {
      //     notificationTitle: "Moon Rising-9e",
      //     notificationDate: "Jul 6, 2019",
      //   },
      //   {
      //     notificationTitle: "MR-Master FREE VSTs - no",
      //     notificationDate: "Jul 6, 2019",
      //   },
      //   {
      //     notificationTitle: "MR-Master-9c-NO_LIMIT",
      //     notificationDate: "Jul 6, 2019",
      //   },
      //   {
      //     notificationTitle: "Moon Rising-9e",
      //     notificationDate: "Jul 6, 2019",
      //   },
      //   {
      //     notificationTitle: "Moon Rising-9c",
      //     notificationDate: "Jul 6, 2019",
      //   },
      //   {
      //     notificationTitle: "Moon Rising-9b",
      //     notificationDate: "Jul 6, 2019",
      //   },
      // ],
    }
  }
}
</script>

<style src="./assets/css/tailwind.css"></style>
