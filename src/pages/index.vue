<script lang="ts" setup>
import HoneyMainImg from "@/public/honey-preview-3.jpg"
import HoneyImg from "@/public/honey-preview-special.png"
import HoneyPreview1 from "@/public/honey-preview-1.jpg"
import HoneyPreview2 from "@/public/honey-preview-2.jpg"
import HoneyPreview4 from "@/public/honey-preview-4.jpg"
import SpacePlus from "@/public/space-plus.png"
import Fly from "@/public/fly.png"
import Beach from "@/public/preview-beach.png"
import Avatar from "@/public/avatar.png"
import Newyork from "@/public/new-york.png"
import Paris from "@/public/paris.png"
import LakeLouise from "@/public/lake-louise.png"
import Tokyo from "@/public/tokyo.png"

</script>

<template>
    <Distributor />
    <div class="flex justify-center items-center py-14">
        <div class="w-65% flex flex-col items-center gap-16px">
            <SharedBox note="CATEGORY" title="We Offer Best Services" class="h-480px">
                <template #content>
                    <Category />
                </template>
            </SharedBox>
        </div>
    </div>
    <div class="flex justify-center items-center ">
        <div class="w-70% flex items-center gap-16">
            <div class="flex-1 relative flex justify-end ">
                <div class="vertical-text">Honeymoon Packages</div>
                <div class="honey-img">
                    <img :src="HoneyImg" alt="honey-preview absolute">
                </div>
                <img :src="HoneyPreview1" alt="honey-preview-1"
                    class="absolute rounded-full w-230px h-230px object-cover object-center left-8%" />
                <img :src="HoneyPreview2" alt="honey-preview-2"
                    class="absolute rounded-full w-141px h-141px object-cover object-center left-0 top-248px" />
                <img :src="HoneyPreview4" alt="honey-preview-4"
                    class="absolute rounded-full w-74px h-74px object-cover object-center left-44% top-0" />
            </div>
            <div class="flex-1">
                <SharedInforImage note="Honeymoon Specials" title="Our Romantic Tropical Destinations" des="labore
                    harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos.
                    Non
                    quis eius quo eligendi corrupti et fugiat nulla qui soluta recusandae in maxime quasi aut ducimus
                    illum
                    aut optio quibusdam!" :isShowButton="true" />
            </div>
        </div>
    </div>
    <div class="flex justify-center">
        <img :src="SpacePlus" alt="space-plus">
    </div>
    <div class="flex justify-center items-center h-800px">
        <div class="w-80% flex items-center gap-16 relative">
            <div class="flex-1">
                <SharedInforImage note="Fast & Easy" title="Get Your Favourite Resort Bookings">
                    <template #custom>
                        <div class="flex gap-20px flex-col">
                            <div class="flex gap-4">
                                <div>
                                    <div class="w-[47px] h-12 relative">
                                        <div
                                            class="w-[47px] h-12 left-0 top-0 absolute bg-amber-400 rounded-[13px] flex justify-center items-center text-white text-20px">
                                            <i class='bx bx-square'></i>
                                        </div>
                                    </div>
                                </div>
                                <div>
                                    <div class="text-gray-500 text-base font-bold font-['Poppins'] leading-tight">Choose
                                        Destination</div>
                                    <div class="text-gray-500 text-base font-normal font-['Poppins'] leading-tight">Lorem
                                        ipsum dolor sit amet, consectetur <br />adipiscing elit. Urna, tortor tempus. </div>
                                </div>
                            </div>
                            <div class="flex gap-4">
                                <div>
                                    <div class="w-[47px] h-12 relative">
                                        <div class="w-[47px] h-12 left-0 top-0 absolute bg-orange-600 rounded-[13px]"></div>
                                        <div
                                            class="w-[22.05px] h-[17.86px] left-[12.97px] top-[14.07px] absolute flex justify-center items-center text-white text-20px">
                                            <i class='bx bx-swim'></i>
                                        </div>
                                    </div>
                                </div>
                                <div>
                                    <div class="text-gray-500 text-base font-bold font-['Poppins'] leading-tight">Check
                                        Availability</div>
                                    <div class="text-gray-500 text-base font-normal font-['Poppins'] leading-tight">Lorem
                                        ipsum dolor sit amet, consectetur <br />adipiscing elit. Urna, tortor tempus. </div>
                                </div>
                            </div>
                            <div class="flex gap-4">
                                <div>
                                    <div class="w-[47px] h-12 relative">
                                        <div class="w-[47px] h-12 left-0 top-0 absolute bg-sky-800 rounded-[13px]"></div>
                                        <div
                                            class="w-[22.50px] h-[18.75px] left-[12.75px] top-[15.62px] absolute flex justify-center items-center text-white text-20px">
                                            <i class='bx bxs-car-wash'></i>
                                        </div>
                                    </div>
                                </div>
                                <div>
                                    <div class="text-gray-500 text-base font-bold font-['Poppins'] leading-tight">Let’s Go
                                    </div>
                                    <div class="text-gray-500 text-base font-normal font-['Poppins'] leading-tight">Lorem
                                        ipsum dolor sit amet, consectetur <br />adipiscing elit. Urna, tortor tempus. </div>
                                </div>
                            </div>
                        </div>
                    </template>
                </SharedInforImage>
            </div>
            <div class="flex-1 relative h-454px">
                <img :src="Fly" alt="fly-img" class="top-0 right-0 absolute w-692px h-385px" />
                <div
                    class="w-[300px] h-[250px] opacity-80 bg-blue-400 rounded-full blur-[150px] absolute left--120px bottom-0">
                </div>
                <div
                    class="w-[350px] h-[380px] bg-white rounded-[26px] shadow absolute bottom--90px left-0 flex items-center flex-col">
                    <img class="w-[321px] h-[161px] rounded-[26px] mt-20px" :src="Beach" />
                    <div class="w-full p-20px relative">
                        <div class="text-zinc-950 text-lg font-semibold font-['Poppins'] leading-snug tracking-tight">Trip
                            to
                            Hawaii
                        </div>
                        <div class="flex gap-1 items-center py-4">
                            <div class="text-slate-500 text-base font-medium font-['Poppins'] leading-tight">14-29 June
                            </div>|
                            <div class="text-slate-500 text-base font-medium font-['Poppins'] leading-tight">by JR Martinax
                            </div>
                        </div>
                        <div class="flex gap-2">
                            <div class="w-9 h-9 bg-neutral-100 rounded-full flex justify-center items-center">
                                <i class='bx bxs-leaf text-#84829A'></i>
                            </div>
                            <div class="w-9 h-9 bg-neutral-100 rounded-full flex justify-center items-center">
                                <i class='bx bx-map-alt text-#84829A'></i>
                            </div>
                            <div class="w-9 h-9 bg-neutral-100 rounded-full flex justify-center items-center">
                                <i class='bx bx-send text-#84829A'></i>
                            </div>

                        </div>
                        <div class="w-[263px] h-[129px] bg-white rounded-[18px] shadow absolute right--140px top-20px flex">
                            <img :src="Avatar" alt="avatar" class="w-50px h-50px rounded-full m-20px ">
                            <div class="mt-20px">
                                <div class="text-slate-500 text-sm font-medium font-['Poppins'] leading-[17.43px]">Ongoing
                                </div>
                                <div class="text-zinc-950 text-lg font-semibold font-['Poppins'] leading-snug">Trip to rome
                                </div>
                                <div><span
                                        style="text-red-400 text-sm font-semibold font-['Poppins'] leading-[17.43px]">40%</span><span
                                        style="text-zinc-950 text-sm font-semibold font-['Poppins'] leading-[17.43px]">
                                        completed</span></div>
                                <div class="w-[156px] h-[5px] relative">
                                    <div class="w-[156px] h-[5px] left-0 top-0 absolute bg-neutral-100 rounded-[30px]">
                                    </div>
                                    <div class="w-[73px] h-[5px] left-0 top-0 absolute bg-red-400 rounded-[30px]"></div>
                                </div>
                            </div>
                        </div>

                        <div class="flex justify-between pt-6 items-center">
                            <i class='bx bx-building-house text-20px text-#84829A'></i>
                            <div class="text-slate-500 text-base font-semibold leading-tight">60 people are interested</div>
                            <i class='bx bx-heart text-20px text-#DF6951'></i>
                        </div>

                        <div class="origin-top-left rotate-90 w-[153px] h-[166px] relative z--8 bottom-52px left-68px">
                            <div
                                class="left-0 top-0 absolute origin-top-left rotate-90 text-red-400 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[35px] top-[-0px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[70px] top-[-0px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-0 top-[35px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[35px] top-[35px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[70px] top-[35px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[105px] top-[35px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-0 top-[70px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[35px] top-[70px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[70px] top-[70px] absolute origin-top-left rotate-90 text-indigo-600 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[105px] top-[70px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[140px] top-[70px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-0 top-[105px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[35px] top-[105px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[70px] top-[105px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[105px] top-[105px] absolute origin-top-left rotate-90 text-red-400 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[140px] top-[105px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-0 top-[140px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[35px] top-[140px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[70px] top-[140px] absolute origin-top-left rotate-90 text-red-400 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[105px] top-[140px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                            <div
                                class="left-[140px] top-[140px] absolute origin-top-left rotate-90 text-neutral-200 text-[22px] font-normal font-['Roboto']">
                                +</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="mt-20" />
    <SharedSepratir :img="Newyork" text="Let’s make your next holiday amazing" />

    <div class="flex justify-center items-center h-800px">
        <div class="w-80% flex items-center justify-between relative">
            <div>
                <SharedInforImage note="Promotion" title="We Provide You Best Europe Sightseeing Tours" :isShowButton="true"
                    des="Et labore harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos. Non quis eius quo eligendi corrupti et fugiat nulla qui soluta recusandae in maxime quasi aut ducimus illum aut optio quibusdam!" />
                <SharedDestination />
            </div>
            <div class="flex">
                <img :src="Paris" class="min-w-400px" />
                <div class="vertical-text">Breath Taking Viewes</div>
            </div>
        </div>
    </div>

    <div class="flex pt-40 relative">
        <SharedPromotion :image="LakeLouise" note="Promotion" title="Explore Nature" />
        <SharedPromotion :image="Tokyo" note="Promotion" title="Explore Cities" />
    </div>

    <div class="flex justify-center items-center pt-40">
        <div class="w-80% flex flex-col items-center relative">
            <SharedInforImage note="Trendy" title="Our Trending Tour Packages" :is-center="true">
                <template #custom>
                    <Carousel />
                </template>
            </SharedInforImage>
        </div>
    </div>
</template>

<style scoped>
.honey-img {
    height: 690px;
    width: 474px;
    overflow: hidden;
}

.vertical-text {
    writing-mode: vertical-rl;
    text-orientation: mixed;
    transform: rotate(180deg);
    white-space: nowrap;
    font-family: Arial, sans-serif;
    font-size: 51px;
    color: #E6E6E6;
    font-weight: bold;
}

</style>