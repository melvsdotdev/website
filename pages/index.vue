<script lang="ts" setup>
  const techStacks = ref([
    { image: 'vue.png', altText: 'Vue.js' },
    { image: 'nuxt.png', altText: 'Nuxt JS' },
    { image: 'figma.png', altText: 'Figma' },
    { image: 'nodejs.png', altText: 'Node JS' },
    { image: 'strapi.png', altText: 'Strapi' },
    { image: 'git.png', altText: 'Git' }
  ])
</script>

<template>
  <div class="flex flex-nowrap items-center h-full">
    <div class="flex-none w-[560px]">
      <h1 class="text-[32px] leading-[35px]">
        <span class="font-bold">Hey, I’m <span class="text-primary">Melvs</span></span> — I transform ideas into intuitive, engaging web experiences
      </h1>
      <p class="mt-5 mb-7">
        With over 4 years of experience in translating UI wireframes and integrating REST APIs
      </p>
      <div class="flex">
        <AppButton href="mailto:melvinmoratoborja@gmail.com">
          <img src="~/assets/images/plane.svg" alt="" class="mr-2" />
          Send a message
        </AppButton>
        <AppButton href="/Resume.pdf" download="Melvin_Borja_Resume.pdf" text>
          <img src="~/assets/images/download.svg" alt="" class="mr-2" />
          Resume
        </AppButton>
      </div>
      <p class="mt-12 text-sm">
        Mostly used tech stacks
        <div class="flex mt-5">
          <img
            v-for="(stack, index) in techStacks"
            :key="index"
            :src="`/${stack.image}`"
            :alt="stack.altText"
            class="mx-2"
            style="height: 28px;"
          />
        </div>
      </p>
    </div>
    <div class="flex-auto">
      <img src="~/assets/images/illustration.svg" alt="" class="w-[120%]">
    </div>
  </div>
</template>
