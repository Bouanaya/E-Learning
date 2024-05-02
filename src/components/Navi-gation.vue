<template>
    <div class="nav">
        <ul class="md:flex  space-x-6 hidden">
            <li>
                <router-link to="/" class="text-lg">About</router-link>
            </li>
            <li>
                <router-link to="/" class="text-lg">Features</router-link>
            </li>
            <li>
                <router-link to="/" class="text-lg">Pricing</router-link>
            </li>
            <li>
                <router-link to="/" class="text-lg">Testimonial</router-link>
            </li>
        </ul>
        <div class="md:hidden flex">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                stroke="currentColor" class="w-8 h-8">
                <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>

        </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>

</style>