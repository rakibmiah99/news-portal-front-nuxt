<script setup lang="ts">
const route = useRoute()

const links = [
    [
      {
        label: 'Bangladesh',
      },
      {
        label: 'International',
        to: '/getting-started/installation'
      },
      {
        label: 'Sports',
        to: `${route.path.startsWith('/dev') ? '/dev' : ''}/components/horizontal-navigation`
      },
      {
        label: 'Opinion',
        to: '/components/command-palette'
      },
      {
        label: 'Business',
        to: '/components/command-palette'
      },
      {
        label: 'Entertainment',
        to: '/components/command-palette'
      },
      {
        label: 'Latest',
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


const languages = [
  {
    name: "English",
    value: 'en'
  },
  {
    name: "Bangla",
    value: 'bn'
  }
]

var  language = reactive('en')
</script>

<template>

  <div class="flex justify-between items-center pt-4 pb-4">
    <div class="left">
      <div class="actions flex">
        <UButton @click="isOpen = true" icon="i-heroicons-bars-3" variant="ghost" class="me-3 btn-light" square size="sm"/>
        <UButton @click="isOpen = true" icon="i-heroicons-magnifying-glass" variant="ghost" class="btn-light" square size="sm"/>
      </div>
      <div class="today mt-3">
          <p class="font-light">Monday Mar 18, 2024</p>
      </div>
    </div>
    <div class="logo">
        <img height="281" width="300" src="/assets/images/logo.png"/>
    </div>
    <div class="right">
      <USelect v-model="language" class="focus:border-gray-500" :options="languages" option-attribute="name" />
      <UButton variant="ghost"  class="btn-light mt-3">
        <template #leading>
          <UAvatar
              src="https://cdn.iconscout.com/icon/free/png-256/free-facebook-263-721950.png"
              size="3xs"
          />
        </template>
      </UButton>
      <UButton variant="ghost"  class="btn-light mt-3">
        <template #leading>
          <UAvatar
              src="https://cdn-icons-png.freepik.com/256/1384/1384060.png"
              size="3xs"
          />
        </template>
      </UButton>
      <UButton variant="ghost"  class="btn-light mt-3">
        <template #leading>
          <UAvatar
              src="https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/x-social-media-black-icon.png"
              size="3xs"
          />
        </template>
      </UButton>
      <UButton variant="ghost"  class="btn-light mt-3">
        <template #leading>
          <UAvatar
              src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Instagram_icon.png/2048px-Instagram_icon.png"
              size="3xs"
          />
        </template>
      </UButton>
    </div>
  </div>
  <UDivider/>


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
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Bangladesh</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">International</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Sports</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Opinion</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Business</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Youth</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Entertainment</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Lifestyle</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">World</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Latest</UButton>
       <UButton size="xs" variant="ghost" class="border-b text-gray-500 rounded-none border-gray-200 p-3">Commercial</UButton>
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