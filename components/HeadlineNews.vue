<template>
  <div class="mt-6 flex">
    <div class="sidebar-news">
      <ul role="list" class="p-2 divide-y divide-slate-200 w-[300px] border border-gray-200">
        <!-- Remove top/bottom padding when first/last child -->
        <SmallNewsItem href="https://google.com"/>
        <SmallNewsItem/>
        <SmallNewsItem/>
        <Square300Add/>
      </ul>
    </div>
    <HeadingHighlightNews />

    <div class="sidebar-news p-2 border border-gray-200">
      <h1 class="text-center text-lg mb-3">Opinion</h1>
      <UDivider/>
      <ul role="list" class=" p-2 w-[300px] divide-y divide-slate-200 ">
        <SmallNewsItem css_class="rounded-full h-[70px] w-[70px]" href="https://google.com"/>
        <SmallNewsItem css_class="rounded-full h-[70px] w-[70px]" href="https://google.com"/>
      </ul>
      <Square300Add/>
    </div>


  </div>
</template>
<script setup lang="ts">
import SmallNewsItem from "~/components/Utils/SmallNewsItem.vue";
import HeadingHighlightNews from "~/components/Utils/HeadingHighlightNews.vue";
import Square300Add from "~/components/Advertisement/Square300Add.vue";
</script>