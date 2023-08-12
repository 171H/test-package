<script setup lang='ts'>
const { count, inc, dec } = useCount()
</script>

<template>
  <div class="my-3 inline-flex">
    <UButton
      :ui="{ rounded: 'rounded-full', color: 'white' }" icon="heroicons:minus-solid" @click="dec()" />
    <div class="m-auto inline-block w-14 font-mono">
      {{ count }}
    </div>
    <UButton
      :ui="{ rounded: 'rounded-full' }" icon="heroicons:plus-solid" @click="dec()" />
  </div>
</template>
