<template>
    <div class="flex mt-3">
      <div class="sidebar w-[300px] p-1 border h-[500px]">

      </div>
      <div class="news-items px-3 flex flex-wrap gap-4 justify-between w-[908px]">
        <CartNews/>
        <CartNews/>
        <CartNews/>
        <CartNews/>
        <CartNews/>
<!--        <AdvertisementSquare300Add/>-->
        <CartNews/>
        <CartNews/>
        <CartNews/>
        <CartNews/>
      </div>
    </div>
</template>
<script setup lang="ts">
import CartNews from "~/components/Utils/CartNews.vue";
</script>