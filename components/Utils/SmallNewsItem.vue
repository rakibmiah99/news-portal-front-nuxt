<template>
    <ULink :to="href" class="flex py-4 first:pt-0 last:pb-0">
      <li class="flex py-4 first:pt-0 last:pb-0">
        <NuxtImg :class="css_class ?? 'rounded-sm me-2'" :height="height ?? 80" :width="width ?? 100"  :src="src ?? 'https://en.breakingnewsbd.net/admin/public/images/2024-03-18/1710748135internatioal.jpg'"/>
        <div class="ml-2 overflow-hidden">
          <p class="text-sm font-medium mb-1 text-slate-900 text-left line-clamp-2">{{title ?? 'Netanyahu snaps back against growing US criticism after being accused of losing his way on Gaza'}}</p>
          <p class="text-sm text-slate-500 truncate text-left">{{ time ?? '7 hour ago'}}</p>
        </div>
      </li>
    </ULink>
</template>

<script setup>
  defineProps([
      'height',
      'weight',
      'src',
      'title',
      'time',
      'href',
      'css_class'
  ])
</script>