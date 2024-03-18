<script setup lang="ts">
const route = useRoute()

const links = [
    [
      {
        label: 'Profile',
      },
      {
        label: 'Installation',
        to: '/getting-started/installation'
      },
      {
        label: 'Horizontal Navigation',
        to: `${route.path.startsWith('/dev') ? '/dev' : ''}/components/horizontal-navigation`
      },
      {
        label: 'Command Palette',
        to: '/components/command-palette'
      }
    ],
    [
      {
        label: 'Login',
      },
      {
        label: 'Signup',
      },
    ]
  ];


const isOpen = ref(false)
</script>

<template>
  <UHorizontalNavigation :links="links" class="border-b border-gray-200 dark:border-gray-800 max-md:hidden" >
    <template #default="{ link }">
      <span class="group-hover:text-primary relative">{{ link.label }}</span>
    </template>
  </UHorizontalNavigation>
  <div class="md:hidden">
    <div class="flex justify-between pt-2 pb-2">
      <UButton @click="isOpen = true" icon="i-heroicons-bars-3" variant="soft" square size="sm"/>
      <div>
        <UButton variant="link" class="text-gray-500 me-2" >Login</UButton>
        <UButton variant="link" class="text-gray-500" >Signup</UButton>
      </div>
    </div>
    <UDivider class="" size="2xs"/>
  </div>
  <USlideover class="w-[200px]" :transition="false" v-model="isOpen" side="left">
    <UButton @click="isOpen = false"  variant="ghost" icon="i-heroicons-x-mark-20-solid" color="red" class="absolute right-[10px] top-[10px]"/>
    <div class="mt-10 flex flex-col overflow-scroll">
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Category</UButton>
    </div>
  </USlideover>
</template>