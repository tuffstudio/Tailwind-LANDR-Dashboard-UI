<template>
<header class="bg-deep-ocean fixed z-10 w-full">
      <div class="px-6 relative flex justify-between max-w-7xl xl:mx-auto">
        <div class="flex">
          <div class="relative flex items-center ">
            <a href="#home">
              <svg class="h-8 w-8 md:h-10 md:w-10 fill-current text-gray-100 hover:text-gray-500" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><path d="M22.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 2.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 22.25 15z"></path><path d="M27.25 15a9.749 9.749 0 0 1-9.75 9.75A9.749 9.749 0 0 1 7.75 15a9.749 9.749 0 0 1 9.75-9.75A9.749 9.749 0 0 1 27.25 15z"></path></g></svg>
            </a>
            <button @click="menuOpen = !menuOpen" type="button" class="absolute pl-8 w-full h-full md:hidden">
              <svg class="h-5 w-5 fill-current text-gray-100" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><path d="M14.25 6.507L9.003 11.75 3.75 6.5" stroke-width="1.5" stroke="currentColor" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"></path></svg>
            </button>
          </div>
          <nav class="invisible md:visible flex w-full">
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

        <div v-if="menuOpen" class="absolute top-0 left-0 mt-12 md:mt-16 md:left-auto md:right-0 w-screen sm:w-auto">
          <div class="mx-6  bg-white rounded-sm sm:w-64 shadow-xl overflow-y-hidden">
            <nav class="py-4 px-6 overflow-y-auto">
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

        <div class="flex items-center">
          <div @click="notificationsOpen = !notificationsOpen" class="relative">
            <button type="button">
              <svg class="h-6 w-6 fill-current text-gray-100 hover:text-gray-500" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M14 5c-.294-1.162-1.081-2-2.006-2-.913 0-1.69.864-1.994 2" fill="currentColor"></path><path d="M9 17.25a3 3 0 0 0 6 0" stroke="currentColor" stroke-width="1.5"></path><path d="M17.25 13.248l.503 1c.827 0 1.497.666 1.497 1.5 0 .83-.68 1.502-1.497 1.502H6.247a1.495 1.495 0 0 1-1.497-1.501c0-.83.68-1.501 1.497-1.501l.503-1v-2.994c0-3.04 2.24-5.504 5.004-5.504h.492c2.764 0 5.004 2.471 5.004 5.504v2.994z" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path></g></svg>
            </button>
            <div v-if="notificationsOpen" class="absolute right-0">
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
          </div>
          <button @click="menuOpen = !menuOpen" type="button" class="hidden md:block relative ml-6">
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
    },
    
}
</script>

