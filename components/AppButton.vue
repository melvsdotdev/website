<script lang="ts" setup>
  const props = defineProps({
    color: { type: String, default: 'bg-primary' },
    text: { type: Boolean, default: false }
  })
  const buttonClass = ref('')

  if (props.text) {
    buttonClass.value = 'text-primary font-medium px-10 py-6 ma-1 rounded-full'
  } else {
    buttonClass.value = 'bg-primary text-white font-medium px-10 py-6 ma-1 rounded-full'
  }
</script>

<template>
  <a :class="buttonClass">
    <div class="flex">
      <slot />
    </div>
  </a>
</template>

<style scoped>
a {
  font-size: 21px;
}
</style>
