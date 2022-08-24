<script setup>
definePageMeta({
  layout: "default",
});
const { pending, data } = useLazyFetch("https://api.imgflip.com/get_memes");
</script>

<template>
  <section class="my-12 px-12 lg:px-44">
    <div class="columns-1 md:columns-2 lg:columns-3 -mx-4">
      <div v-for="(meme, i) in data.data.memes" :key="i">

      <NuxtLink :to="`/meme/${meme.id}`">
        <img
          class="p-4"
          :src="meme.url"
        />
      </NuxtLink>
      </div>
    </div>
  </section>
</template>