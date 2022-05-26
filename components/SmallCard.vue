<template>
  <NuxtLink :to="`/products/${card.id}`" class="card-container">
    <img
      :src="require(`@/assets/images/${card.image || fe1.jpg}`)"
      alt=""
      class="image"
    />
  </NuxtLink>
</template>

<script>
export default {
  props: ["card"],
};
</script>

<style scoped>
.card-container {
  width: 24%;
  height: 12.5rem;
  border-radius: 0.5rem;
  overflow: hidden;
  cursor: pointer;
  margin: 10px 10px 0.5rem 0;
}
.image {
  height: 100%;
  width: 100%;
}
</style>
