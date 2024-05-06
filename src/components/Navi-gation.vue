<template>
    <div class="nav">
        <ul class="md:flex  space-x-6 hidden">
            <li>
                <router-link to="/" class="text-lg al">About</router-link>
            </li>
            <li>
                <router-link to="/" class="text-lg al">Features</router-link>
            </li>
            <li>
                <router-link to="/" class="text-lg al">Pricing</router-link>
            </li>
            <li>
                <router-link to="/" class="text-lg al">Testimonial</router-link>
            </li>
            <li>
                <router-link to="/" class="text-lg al">Contact</router-link>
            </li>
        </ul>



    </div>
</template>

<script setup>

</script>

<style  scoped>
.al {
    position: relative;
    color: gray;

}

.al::after {
    content: "";
    position: absolute;
    background-color:#4ADE80;
    height: 1px;
    width: 0;
    left: 0;
    bottom: -10px;
    transition: 0.3s;

}

.al:hover:after {
    width: 100%;

}

.al:hover {
    color:black;
}

</style>