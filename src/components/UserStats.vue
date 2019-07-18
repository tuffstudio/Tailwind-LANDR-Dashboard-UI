<template>
    <a href="#" class="p-6 inline-block h-full bg-white rounded hover:shadow-lg">
        <h2 class="text-sm text-gray-500">{{ stat.title }}</h2>
        <img class="p-12 pb-8" :src="stat.imageUrl" :alt="stat.imageAlt">
        <p class="text-lg font-semibold">{{ stat.tagline }}</p>
    </a>
</template>

<script>
export default {
  props: [ 'stat' ],
}
</script>
