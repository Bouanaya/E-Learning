<template>
    <div class="grid md:grid-cols-3 gap-8 py-8  ">
        <div class="grid grid-rows-2  rounded-xl bg-white shadow-[rgba(7,_65,_210,_0.1)_0px_9px_30px] p-4 "
            v-for="{ id, img, active, name, star, firstName, lastName, numberClass, numberStudents, prix, cotchImg, NoActive } in form"
            :key="id">
            <div class="">
                <img :src='img' class="rounded-xl" alt="">
            </div>
            <div class="Cs">
                <div class="flex justify-between items-center">
                    <div class="py-2 flex items-center gap-3  ">
                        <div class=" items-center gap-2 bg-primary-100 flex py-2 px-2 rounded-lg">
                            <div class=" w-3 h-3 bg-green-400 rounded-full  " v-show="active"></div>
                            <div class="w-3 h-3 bg-red-500 rounded-full  " v-show="NoActive"></div>
                            <h2 class="text-sm text-gray-600">{{ name }}</h2>
                        </div>
                    </div>
                    <div class=" flex items-center gap-3  ">
                        <div class=" items-center gap-2 bg-green-400 flex py-1 px-2  rounded-lg">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" class="w-5 h-5 text-yellow-400">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M11.48 3.499a.562.562 0 0 1 1.04 0l2.125 5.111a.563.563 0 0 0 .475.345l5.518.442c.499.04.701.663.321.988l-4.204 3.602a.563.563 0 0 0-.182.557l1.285 5.385a.562.562 0 0 1-.84.61l-4.725-2.885a.562.562 0 0 0-.586 0L6.982 20.54a.562.562 0 0 1-.84-.61l1.285-5.386a.562.562 0 0 0-.182-.557l-4.204-3.602a.562.562 0 0 1 .321-.988l5.518-.442a.563.563 0 0 0 .475-.345L11.48 3.5Z" />
                            </svg>
                            <h2>{{ star }}</h2>
                        </div>
                    </div>

                </div>
                <div class="">
                    <h1 class="font-semibold text-xl">{{ firstName }} <br> {{ lastName }}</h1>
                    <div class="flex gap-4 py-3">
                        <nav class="flex gap-2">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" class="w-5 h-5 text-primary-300">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M12 6.042A8.967 8.967 0 0 0 6 3.75c-1.052 0-2.062.18-3 .512v14.25A8.987 8.987 0 0 1 6 18c2.305 0 4.408.867 6 2.292m0-14.25a8.966 8.966 0 0 1 6-2.292c1.052 0 2.062.18 3 .512v14.25A8.987 8.987 0 0 0 18 18a8.967 8.967 0 0 0-6 2.292m0-14.25v14.25" />
                            </svg>
                            <h1 class="text-sm">{{ numberClass }} Classes</h1>

                        </nav>
                        <nav class="flex gap-2">
                            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                                stroke="currentColor" class="w-5 h-5 text-primary-300">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M15 19.128a9.38 9.38 0 0 0 2.625.372 9.337 9.337 0 0 0 4.121-.952 4.125 4.125 0 0 0-7.533-2.493M15 19.128v-.003c0-1.113-.285-2.16-.786-3.07M15 19.128v.106A12.318 12.318 0 0 1 8.624 21c-2.331 0-4.512-.645-6.374-1.766l-.001-.109a6.375 6.375 0 0 1 11.964-3.07M12 6.375a3.375 3.375 0 1 1-6.75 0 3.375 3.375 0 0 1 6.75 0Zm8.25 2.25a2.625 2.625 0 1 1-5.25 0 2.625 2.625 0 0 1 5.25 0Z" />
                            </svg>

                            <h1 class="text-sm">{{ numberStudents }} students</h1>

                        </nav>
                    </div>
                    <div class="pt-5  border-t flex justify-between items-center">
                        <h1 class="font-semibold text-xl md:text-lg">{{ prix }} DH</h1>
                        <nav class="flex items-center gap-2">
                            <img :src="cotchImg" class="w-10 rounded-full" alt="">
                            <button class="text-primary-500"> wade warren</button>
                        </nav>
                    </div>
                </div>
            </div>


        </div>
    </div>

</template>

<script setup>
const form = [
    {
        id: 0,
        img: "/public/imgs/pexels-markusspiske-965345.jpg",
        active: true,
        NoActive: false,

        name: "Web Design",
        star: "4.9",
        firstName: "Web Design &",
        lastName: "Development Course",
        numberClass: "18",
        numberStudents: "160",
        prix: "580",
        cotchImg: "/public/imgs/592b30.webp"
    },
    {
        id: 1,
        img: "/public/imgs/pexels-picjumbo-com-55570-196644.jpg",
        active: true,
        NoActive: false,
        name: "UI/UX Design",
        star: "4.9",
        firstName: "Learn UI/UX and Grow",
        lastName: "Your Career",
        numberClass: "18",
        numberStudents: "160",
        prix: "580",
        cotchImg: "/public/imgs/592b30.webp"
    },
    {
        id: 2,
        img: "/public/imgs/pexels-divinetechygirl-1181671.jpg",
        active: true,
        NoActive: false,
        name: "Data Science",
        star: "4.9",
        firstName: "Python For Data",
        lastName: "science",
        numberClass: "18",
        numberStudents: "160",
        prix: "580",
        cotchImg: "/public/imgs/592b30.webp"
    },
    {
        id: 3,
        img: "/public/imgs/pexels-paduret-1476321.jpg",
        active: false,
        NoActive: true,
        name: "Machine",
        star: "4.9",
        firstName: "Machine Learning,Data",
        lastName: "Science and Deep learning",
        numberClass: "14",
        numberStudents: "160",
        prix: "580",
        cotchImg: "/public/imgs/592b30.webp"
    },
    {
        id: 4,
        img: "/public/imgs/pexels-designecologist-1779487.jpg",
        active:true,
        NoActive:false,
        name: "Design Thinking",
        star: "4.3",
        firstName: "Learn Complete Design",
        lastName: "Thinking Process",
        numberClass: "17",
        numberStudents: "160",
        prix: "280",
        cotchImg: "/public/imgs/592b30.webp"
    },
    {
        id: 5,
        img: "/public/imgs/pexels-pixabay-38544.jpg",
        active: false,
        NoActive: true,
        name: "Banner Design",
        star: "7.1",
        firstName: "Learn Social Media",
        lastName: "Banner Design",
        numberClass: "10",
        numberStudents: "100",
        prix: "780",
        cotchImg: "/public/imgs/592b30.webp"
    },

]

</script>