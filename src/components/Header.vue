<template>
<header class="bg-deep-ocean fixed z-10 w-full">
      <div class="px-6 my-4 md:my-0 relative flex justify-between max-w-7xl xl:mx-auto">
        <div class="flex">
          <div class="relative flex items-center ">
            <a href="#home">
              <svg class="h-8 w-8 md:h-10 md:w-10 fill-current text-gray-100 hover:text-gray-500" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><path d="M22.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 2.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 22.25 15z"></path><path d="M27.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 7.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 27.25 15z"></path></g></svg>
            </a>
            <button @click="menuOpen = !menuOpen" type="button" class="absolute pl-8 w-full h-full md:hidden focus:outline-none">
              <svg class="h-5 w-5 fill-current text-gray-100" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><path d="M14.25 6.507L9.003 11.75 3.75 6.5" stroke-width="1.5" stroke="currentColor" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"></path></svg>
            </button>
          </div>
          <nav class="hidden md:block flex w-full">
              <div class="ml-8 py-4 md:py-6 inline-block border-b-2 border-teal-400 w-auto">
                <a href="#" class="text-gray-500 hover:text-gray-300 font-semibold">Home</a>
              </div>
              <div class="ml-8 py-4 md:py-6 inline-block">
                <a href="#" class="text-gray-500 hover:text-gray-300 font-semibold">Library</a>
              </div>
              <div class="ml-8 py-4 md:py-6 inline-block">
                <a href="#" class="text-gray-500 hover:text-gray-300 font-semibold">Releases</a>
              </div>
              <div class="ml-8 py-4 md:py-6 inline-block">
                <a href="#" class="text-gray-500 hover:text-gray-300 font-semibold">Samples</a>
              </div>
          </nav>
        </div>

        <transition
          enter-active-class="transition-all transition-fastest ease-out-quad"
          leave-active-class="transition-all transition-faster ease-in-quad"
          enter-class="opacity-0 scale-70"
          enter-to-class="opacity-100 scale-100"
          leave-class="opacity-100 scale-100"
          leave-to-class="opacity-0 scale-70"
        >
          <div v-if="menuOpen" class="origin-top-left md:origin-top-right absolute top-0 left-0 mt-10 md:mt-16 md:left-auto md:right-0 w-screen sm:w-auto">
            <div class="mx-6  bg-white rounded-sm sm:w-64 shadow-xl overflow-y-hidden">
              <nav class="py-4 px-6 overflow-y-auto h-102 sm:h-auto">
                <div class="flex justify-between items-center">
                  <span class="text-sm font-semibold">User Name</span>
                  <img class="w-10 h-10 rounded-full md:hidden" src="@/assets/img/Profile.jpg" alt="Profile image">
                </div>
                <div class="pb-2 border-b">
                  <p class="text-sm text-gray-600">
                    Advanced<span class="mx-1">&middot;</span><a href="#" class="text-teal-500">Upgrade</a>
                  </p>
                </div>
                <div class="py-2 md:hidden border-b flex flex-col">
                  <a href="#" class="py-2 hover:text-teal-400">Home</a>
                  <a href="#" class="py-2 hover:text-teal-400">Library</a>
                  <a href="#" class="py-2 hover:text-teal-400">Releases</a>
                  <a href="#" class="py-2 hover:text-teal-400">Samples</a>
                </div>
                <div class="py-2 border-b flex flex-col">
                  <a href="#" class="py-2 hover:text-teal-400">Account settings</a>
                </div>
                <div class="py-2 border-b flex flex-col">
                  <a href="#" class="py-2 hover:text-teal-400">Desktop app</a>
                  <a href="#" class="py-2 hover:text-teal-400">Blog</a>
                  <a href="#" class="py-2 hover:text-teal-400">Pricing</a>
                  <a href="#" class="py-2 hover:text-teal-400">Help</a>
                  <a href="#" class="py-2 hover:text-teal-400">Give Feedback
                    <span class="py-1 px-2 ml-2 bg-indigo-700 text-xs text-white uppercase rounded">new</span>
                    </a>
                </div>
                <div class="py-2">
                  <button type="button" class="py-1 hover:text-teal-400">Log out</button>
                </div>
              </nav>
            </div>
          </div>
        </transition>

        <div class="flex items-center">
          <div @click="toggle" class="relative">
            <button type="button" class="focus:outline-none">
              <svg class="h-6 w-6 fill-current text-gray-100 hover:text-gray-500" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M14 5c-.294-1.162-1.081-2-2.006-2-.913 0-1.69.864-1.994 2" fill="currentColor"></path><path d="M9 17.25a3 3 0 0 0 6 0" stroke="currentColor" stroke-width="1.5"></path><path d="M17.25 13.248l.503 1c.827 0 1.497.666 1.497 1.5 0 .83-.68 1.502-1.497 1.502H6.247a1.495 1.495 0 0 1-1.497-1.501c0-.83.68-1.501 1.497-1.501l.503-1v-2.994c0-3.04 2.24-5.504 5.004-5.504h.492c2.764 0 5.004 2.471 5.004 5.504v2.994z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path></g></svg>
            </button>
            <transition
              enter-active-class="transition-all transition-fastest ease-out-quad"
              leave-active-class="transition-all transition-faster ease-in-quad"
              enter-class="opacity-0 scale-70"
              enter-to-class="opacity-100 scale-100"
              leave-class="opacity-100 scale-100"
              leave-to-class="opacity-0 scale-70"
            >
            <div v-if="notificationsOpen" class="origin-top-right absolute top-0 right-0 -mr-6 md:mr-0 mt-6 w-screen sm:w-96">
              <div class="mt-4 bg-white rounded-sm shadow-xl overflow-y-hidden ">
                <div class="p-4 flex justify-between items-center">
                  <span class="font-semibold">Notifications</span>
                  <button class="font-semibold" type="button">Mark all as seen</button>
                </div>
                <div class="with_scrollbar overflow-y-auto h-96">
                  <div v-bind:key="notification.id" v-for="(notification, i) in notifications" :class="{'border-t' : i === 0 }" class="border-b">
                      <Notification :notification="notification"/>
                  </div>
                </div>
              </div>
            </div>
            </transition>
          </div>
          <button @click="menuOpen = !menuOpen" type="button" class="hidden rounded-full focus:outline-none focus:shadow-outline md:block relative ml-6 ">
            <img class="w-10 h-10 rounded-full" src="@/assets/img/Profile.jpg" alt="Profile image">
          </button>
        </div>

      </div>
    </header>
    
</template>

<script>
import Notification from "@/components/subcomponents/Notification.vue";

export default {
    components: {
        Notification,
    },
    data(){
        return{
          menuOpen: false,
          notificationsOpen: false,
          notifications: [
            {
              notificationTitle: "High Rise Low Down (Felix Jackson Remix)",
              notificationText: "just got it\'s first play!",
              notificationLink: "See your stats",
              notificationDate: "Jul 18, 2019",
            },
            {
              notificationTitle: "Your track Moon Rising",
              notificationText: "is mastered and ready.",
              notificationLink: "Listen now",
              notificationDate: "Jul 6, 2019",
            },
            {
              notificationTitle: "Your track Rizke - Internationales",
              notificationText: "is mastered and ready.",
              notificationLink: "Listen now",
              notificationDate: "Jul 5, 2019",
            },
            {
              notificationTitle: "Your track Moon Rising-9e",
              notificationText: "is mastered and ready.",
              notificationLink: "Listen now",
              notificationDate: "Jul 5, 2019",
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
    },
    methods: {
    toggle() {
      this.notificationsOpen = !this.notificationsOpen
    },
  },
    
}
</script>

<style>
.origin-top-right {
  transform-origin: top right;
}
.origin-top-left {
  transform-origin: top left;
}
.transition-all {
  transition-property: all;
}
.transition-fastest {
  transition-duration: 50ms;
}
.transition-faster {
  transition-duration: 100ms;
}
.transition-fast {
  transition-duration: 150ms;
}
.transition-medium {
  transition-duration: 200ms;
}
.ease-out-quad {
  transition-timing-function: cubic-bezier(.25, .46, .45, .94);
}
.ease-in-quad {
  transition-timing-function: cubic-bezier(.55, .085, .68, .53);
}
.scale-70 {
  transform: scale(.7);
}
.scale-100 {
  transform: scale(1);
}

 .with_scrollbar::-webkit-scrollbar { width: 5px;}
              /* Track */
 .with_scrollbar::-webkit-scrollbar-track {border-radius: 0;}
              /* Handle */
 .with_scrollbar::-webkit-scrollbar-thumb {background: black; }
 .with_scrollbar::-webkit-scrollbar-thumb:window-inactive {background: black; }

</style>


