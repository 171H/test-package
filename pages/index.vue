<script setup lang="ts">
const online = useOnline()
</script>

<template>
  <div>
    <Logos class="mb-6" />
    <Suspense>
      <ClientOnly>
        <PageView v-if="online" />
        <div class="text-gray-400 opacity-80" v-else>
          You're offline
        </div>
      </ClientOnly>
      <template #fallback>
        <div class="italic opacity-80">
          <span class="animate-pulse">Loading...</span>
        </div>
      </template>
    </Suspense>
    <InputEntry />
  </div>
</template>
