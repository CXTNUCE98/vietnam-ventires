<script setup lang="ts">
import Logo from '@/public/logo.png'
import BgHome from '@/public/bg-home-1.png'
import BgAbout from '@/public/bg-header-about.png'

const route = useRoute()
const nav = ref([
    { label: 'Home', to: '/', active: true },
    { label: 'About', to: '/about' },
    { label: 'Service', to: '/service' },
    { label: 'Upcoming Packages', to: '/packages' },
])

const curRoute = computed(() => {
    return route.path as string
})

const bgHeader = {
    '/': BgHome,
    '/about': BgAbout,
}
const isShowMenu = ref(false)
function toggle() {
    console.log('running');
    isShowMenu.value = !isShowMenu.value
}


const isCenter = computed(() => {
    return curRoute.value !== '/'
})
</script>

<template>
    <nav class="relative border-gray-200 dark:bg-gray-900">
        <img :src="bgHeader[curRoute]" class="absolute inset-0 w-full h-full object-cover z-0" alt="Background Image">
        <div class="relative max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4 z-10">
            <NuxtLink to="/" class="flex items-center space-x-3 rtl:space-x-reverse">
                <img :src="Logo" class="h-16 rounded-full" alt="Logo" />
            </NuxtLink>
            <button @click="toggle" data-collapse-toggle="navbar-default" type="button"
                class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-gray-500 rounded-lg md:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
                aria-controls="navbar-default" aria-expanded="false">
                <span class="sr-only">Open main menu</span>
                <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 17 14">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M1 1h15M1 7h15M1 13h15" />
                </svg>
            </button>
            <div class="hidden w-full md:block md:w-auto" :class="{ '!block': isShowMenu }" id="navbar-default">
                <ul
                    class="font-medium flex flex-col p-4 text-white md:p-0 mt-4 border bg-gray-50 border-gray-100 rounded-lg md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-transparent dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
                    <template v-for="(item, index) in nav" :key="index">
                        <li class="relative flex justify-center">
                            <NuxtLink
                                class="block py-2 px-3 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-#DF6951 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent"
                                :class="{ 'active': item.to === curRoute }" :to="item.to">
                                {{ item.label }}
                            </NuxtLink>
                        </li>
                    </template>
                </ul>
            </div>

            <button class="hidden bg-#DF6951 border-1px outline-none px-4 py-2 rounded-lg text-light md:block">
                Get in touch
            </button>
        </div>

        <div v-if="isCenter" class="absolute flex justify-center items-center w-full h-80% flex-col">
            <div class="text-rose-50 text-lg font-bold font-['Poppins'] uppercase tracking-widest">Read</div>
            <div class="text-white text-38 font-normal yesteryear-regular leading-56">About Us</div>
        </div>
        <div v-else class="absolute ">2</div>
    </nav>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Yesteryear&display=swap');

.yesteryear-regular {
  font-family: "Yesteryear", cursive;
  font-weight: 400;
  font-style: normal;
}
nav {
    height: 766px;
}

.active::before {
    content: '';
    position: absolute;
    border-bottom: 4px solid #DF6951;
    width: 40px;
    bottom: -3px;
    left: 50%;
    transform: translateX(-50%);
}
</style>