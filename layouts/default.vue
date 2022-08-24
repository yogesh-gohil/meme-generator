<script>
export default {
  created() {
    console.log('layout created')
  },
}
</script>

<template>
  <div class="flex flex-col bg-gray-100">
    <SiteHeader />
    <main>
      <slot />
    </main>
    <SiteFooter class="flex flex-end" />
  </div>
</template>
