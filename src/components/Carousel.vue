<script setup lang="ts">
import emblaCarouselVue from 'embla-carousel-vue'
import Autoplay from 'embla-carousel-autoplay'

import Switzerland from "@/public/switzerland.png"
import Amazon from "@/public/amazon.png"
import Giza from "@/public/giza.png"

import LogoSwitzerland from "@/public/logo-switzerland.png"
import LogoAmazon from "@/public/logo-brazil.png"
import LogoGiza from "@/public/logo-egypt.png"


const destinations = [
    {
        img: Switzerland,
        name: 'Switzerland',
        avatar: LogoSwitzerland,
        price: 1000,
        discount: 1200,
        location: 'Europe',
        day: 8,
        people: 25,
        des: 'Nam exercitationem commodi et ducimus quia in dolore animi sit mollitia amet id quod eligendi. Et labore harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos.',
    },
    {
        img: Amazon,
        name: 'Amazon',
        avatar: LogoAmazon,
        price: 1223,
        discount: 1400,
        location: 'Brazil',
        day: 8,
        people: 30,
        des: 'Nam exercitationem commodi et ducimus quia in dolore animi sit mollitia amet id quod eligendi. Et labore harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos.',
    },
    {
        img: Giza,
        name: 'Giza',
        avatar: LogoGiza,
        price: 1200,
        discount: 1500,
        location: 'Egypt',
        day: 8,
        people: 155,
        des: 'Nam exercitationem commodi et ducimus quia in dolore animi sit mollitia amet id quod eligendi. Et labore harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos.',
    },
    {
        img: Switzerland,
        name: 'Switzerland',
        avatar: LogoSwitzerland,
        price: 1000,
        discount: 1200,
        location: 'Europe',
        day: 8,
        people: 25,
        des: 'Nam exercitationem commodi et ducimus quia in dolore animi sit mollitia amet id quod eligendi. Et labore harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos.',
    },
    {
        img: Amazon,
        name: 'Amazon',
        avatar: LogoAmazon,
        price: 1223,
        discount: 1400,
        location: 'Brazil',
        day: 8,
        people: 30,
        des: 'Nam exercitationem commodi et ducimus quia in dolore animi sit mollitia amet id quod eligendi. Et labore harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos.',
    },
    {
        img: Giza,
        name: 'Giza',
        avatar: LogoGiza,
        price: 1200,
        discount: 1500,
        location: 'Egypt',
        day: 8,
        people: 155,
        des: 'Nam exercitationem commodi et ducimus quia in dolore animi sit mollitia amet id quod eligendi. Et labore harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos.',
    },
]

const [emblaRef] = emblaCarouselVue({ loop: true, align: 'start' }, [Autoplay()])
</script>
<template>
    <div class="carousel-container">
        <div class="embla" ref="emblaRef">
            <div class="embla__container">
                <div v-for="(item, index) in destinations" :key="index"
                    class="basis-1/1 py-4 2xl:basis-1/5 lg:basis-1/3 md:basis-1/2 xl:basis-1/4">
                    <div
                        class="card border-border rounded-2xl leading-normal! hover:shadow-lg hover:-translate-y-3 cursor-pointer">
                        <div class="image-container">
                            <img :src="item?.img" class="block w-392px h-312px pixelated">
                            <img :src="item?.avatar" alt="avatar" class="absolute bottom--76px left-0 rounded-full">
                        </div>
                        <div class="flex pt-10 gap-10">
                            <div
                                class="flex gap-1 items-center text-center text-zinc-500 text-[16.81px] font-normal font-['Poppins'] capitalize">
                                <i class='bx bx-calendar-alt'></i>
                                <span>{{ item.day }} Days</span>
                            </div>
                            <div
                                class="flex gap-1 items-center text-center text-zinc-500 text-[16.81px] font-normal font-['Poppins'] capitalize">
                                <i class='bx bx-user'></i>
                                <span>{{ item.people }} People Going</span>
                            </div>
                        </div>

                        <div class="flex justify-between items-center">
                            <div class="text-center text-zinc-800 text-[29.03px] font-bold capitalize">Switzerland</div>
                            <div class="text-yellow-400">
                                <i class='bx bxs-star'></i>
                                <i class='bx bxs-star'></i>
                                <i class='bx bxs-star'></i>
                                <i class='bx bxs-star'></i>
                                <i class='bx bxs-star'></i>
                            </div>
                        </div>

                        <div class="text-zinc-500 flex items-center gap-1">
                            <i class='bx bx-current-location text-28px'></i>
                            <div class="text-center  text-[16.81px] capitalize">{{ item.location }}</div>
                        </div>

                        <div class="flex items-center gap-6 py-4">
                            <div class="text-center text-red-400 text-[29.03px] font-medium capitalize">{{ item.price }} $
                            </div>
                            <div class="text-center text-zinc-500 text-[22px] font-medium line-through capitalize">
                                {{ item.discount }} $</div>
                        </div>
                        <div
                            class="text-start text-black text-xs font-normal font-['Poppins'] leading-normal tracking-wide">
                            {{ item.des }}</div>

                        <div class="flex justify-start pt-4">
                            <el-button size="large" color="#DF6951">
                            <span class="text-white">
                                Explore Now
                            </span>
                        </el-button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
.image-container {
    position: relative;
    display: inline-block;
}

.card {
    height: 700px;
    min-width: 320px;
    border: 1px solid var(--el-border-color);
    box-sizing: border-box;
    text-align: center;
    position: relative;
    transition: all .3s ease-in-out;
    bottom: 0;
    margin: auto;
}

.carousel-container {
    width: 1100px;
    overflow: hidden;
    margin: 0 auto;
}

.embla {
    overflow: hidden;
}

.embla__container {
    display: flex;
    gap: 60px;
}

.embla__slide {
    flex: 0 0 100%;
    min-width: 0;
}

.pixelated {
    image-rendering: pixelated;
}
</style>