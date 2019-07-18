<template>
    <div class="flex items-center cursor-pointer">
        <div class="pl-0 pr-4 py-4">
            <svg class="h-8 w-8" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><circle cx="9.5" cy="20.5" r="1.75"></circle><circle cx="19" cy="19" r="1.75"></circle><path d="M11.25 20v-6.5M20.75 18.25V11.5" stroke-linecap="square"></path><path stroke-linejoin="round" d="M11.25 9.75l9.5-2v5l-9.5 2z"></path><rect x="3.75" y="3.75" width="22.5" height="22.5" rx="1.25"></rect></g></svg>
        </div>
        <div class="leading-tight">
            <div class="flex items-end">
                <h3 class="font-semibold hover:underline">{{ track.trackTitle}}</h3>
                <svg class="w-4 h-4 ml-1 fill-current text-gray-500" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><g fill="none" fill-rule="evenodd"><path d="M6.563 13.827a6 6 0 1 1 7.403-5.188 2.001 2.001 0 0 0-3.274 2.111H8.256c-1.12 0-2.006.895-2.006 2 0 .398.115.767.313 1.077zM8 9.5a1.5 1.5 0 1 0 0-3 1.5 1.5 0 0 0 0 3z" fill="currentColor"></path><path d="M8.5 12.75h6" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"></path><path stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round" d="M12.75 10.25l2.5 2.5-2.5 2.5"></path></g></svg>
            </div>
            <span class="text-sm text-gray-500">{{ track.masterDate }} &middot; {{ track.masterCount }} {{ track.masterCount === 1 ? 'Master' : 'Masters' }} </span>
        </div>
    </div>
</template>

<script>
export default {
  props: [ 'track' ],
}
</script>
