<script lang="ts" setup>
import HoneyMainImg from "@/public/honey-preview-3.jpg"
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
        <div class="w-70% flex flex-col items-center gap-16px">
            <div class="flex-1 relative">
                <div class="honey-img">
                    <img :src="HoneyMainImg" alt="honey-preview" >
                </div>
            </div>
            <div class="flex-1">
                <div>Honeymoon Specials</div>
                <div>Our Romantic Tropical Destinations</div>
                <p>Et labore harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos. Non
                    quis eius quo eligendi corrupti et fugiat nulla qui soluta recusandae in maxime quasi aut ducimus illum
                    aut optio quibusdam!</p>
                <el-button>View packages</el-button>
            </div>
        </div>
    </div>
</template>

<style scoped>
.honey-img {
    height: 690px; 
    width: 476px;
    overflow: hidden;
    /* background: url(../public/honey-preview) lightgray -917.865px -556.092px / 384.05% 192.048% no-repeat; */


    /* clip-path: polygon(50% 0%, 90% 20%, 100% 48%, 100% 100%, 0 100%, 0 47%, 10% 20%); */
  }

  .honey-img img {
    object-fit: cover;
    object-position: center;
    width: 100%;
    height: 100%;
  }
</style>