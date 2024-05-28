<script setup lang="ts">
import EuropeTour from "@/public/europe-tour.png"
import BgStyle from "@/public/bg-style.png"

</script>

<template>
    <div class="flex justify-center items-center h-800px">
        <div class="w-80% flex items-center justify-between relative flex-wrap">
            <div>
                <SharedInforImage note="Promotion" title="We Provide You Best Europe Sightseeing Tours" :isShowButton="true"
                    des="Et labore harum non nobis ipsum eum molestias mollitia et corporis praesentium a laudantium internos. Non quis eius quo eligendi corrupti et fugiat nulla qui soluta recusandae in maxime quasi aut ducimus illum aut optio quibusdam!" />

            </div>
            <div class="bg-style flex items-center justify-center">
                <!-- <img class="w-[578.16px] h-[852.87px] origin-top-left rotate-[90.60deg] opacity-20" :src="BgStyle" /> -->
                <div class="w-[612px] h-[612px] rounded-full flex justify-center items-center bg-border">
                    <img :src="EuropeTour" class="w-90% min-w-549px" />
                </div>
            </div>

        </div>
    </div>
</template>
<style scoped>
.bg-border {
    background-image: url(@/public/ellipse.png);
    background-color: transparent;
}

.bg-style {
    background-image: url(@/public/bg-style.png);
    background-color: transparent;
    width: 700px;
    flex-shrink: 0;
}
</style>
