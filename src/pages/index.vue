<script lang="ts" setup>
import HoneyMainImg from "@/public/honey-preview-3.jpg"
import HoneyImg from "@/public/honey-preview-special.png"
import HoneyPreview1 from "@/public/honey-preview-1.jpg"
import HoneyPreview2 from "@/public/honey-preview-2.jpg"
import HoneyPreview4 from "@/public/honey-preview-4.jpg"
import SpacePlus from "@/public/space-plus.png"
// definePageMeta({
//   redirect: 'home',
//   notAsMenu: true,
// })
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
                    aut optio quibusdam!" />
            </div>
        </div>
    </div>
    <div class="flex justify-center">
        <img :src="SpacePlus" alt="space-plus">
    </div>
    <div class="flex justify-center items-center ">
        <div class="w-80% flex items-center gap-16">
            <div class="flex-1">
                <SharedInforImage note="Fast & Easy" title="Get Your Favourite Resort Bookings">
                    <template #custom>
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
                                <div class="text-gray-500 text-base font-bold font-['Poppins'] leading-tight">Choose
                                    Destination</div>
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
                                <div class="text-gray-500 text-base font-bold font-['Poppins'] leading-tight">Choose
                                    Destination</div>
                                <div class="text-gray-500 text-base font-normal font-['Poppins'] leading-tight">Lorem
                                    ipsum dolor sit amet, consectetur <br />adipiscing elit. Urna, tortor tempus. </div>
                            </div>
                        </div>
                    </template>
                </SharedInforImage>
            </div>
            <div class="flex-1">2</div>
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

/* .honey-img img {
    object-fit: cover;
    object-position: 58% 50%;
    width: 100%;
    height: 100%;
    clip-path: path("M 0 690 L 0 690 A 4 5 0 0 1 473 330 L 690 690 Z");
    image-rendering: pixelated;
} */
</style>