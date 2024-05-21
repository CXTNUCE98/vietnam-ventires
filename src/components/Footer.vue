<script setup lang="ts">

import Travel from "@/public/travel.png"

</script>

<template>
    <div class="footer-bg flex justify-center items-center">
        <div class="w-65% flex justify-between">
            <div>
                <img :src="Travel" class="h-64px" alt="travel_logo">
                <p class="text-#757095 max-w-213px pt-2">Travel helps companies manage payments easily.</p>

                <div>
                    <div class="carbon:logo-linkedin"></div>
                </div>
            </div>
            <div>2</div>
            <div>3</div>
            <div>4</div>
        </div>
    </div>
</template>
<style scoped>
.footer-bg{
    background-image: url(../public/footer.png);
    height: 484px;
    width: auto;
}
</style>