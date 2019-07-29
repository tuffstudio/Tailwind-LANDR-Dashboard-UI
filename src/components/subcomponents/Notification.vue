<template>
    <div class="notification flex items-center justify-between hover:bg-gray-100">
        <div class="px-4 py-6">
            <svg width="36" height="36" viewBox="0 0 36 36" xmlns="http://www.w3.org/2000/svg"><g stroke="currentColor" stroke-width="1.5" fill="none" fill-rule="evenodd"><path d="M26.75 18c0 6.628-5.372 12-12 12s-12-5.372-12-12 5.372-12 12-12 12 5.372 12 12z"></path><path d="M33.25 18c0 6.628-5.372 12-12 12s-12-5.372-12-12 5.372-12 12-12 12 5.372 12 12z"></path></g></svg>
        </div>
        <div class="w-full text-left leading-tight">
            <h3 class="text-sm">
                <p> <strong>{{notification.notificationTitle}}</strong> {{notification.notificationText}}
                <a class="text-teal-500 underline hover:no-underline" href="#">{{ notification.notificationLink }}</a>
                </p>
            </h3>
            <span class="text-sm text-gray-500">{{ notification.notificationDate }} </span>
        </div>
        <div>
            <svg class="mr-4 invisible cursor-pointer" width="18" height="18" viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg"><path d="M14.25 3.75l-6.297 10.5-4.203-4.2" stroke-width="1.5" stroke="currentColor" fill="none" fill-rule="evenodd" stroke-linecap="round" stroke-linejoin="round"></path></svg>
        </div>
    </div>
</template>

<script>
export default {
  props: [ 'notification' ],
}
</script>
