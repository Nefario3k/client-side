<template>
  <div>
    <Nav />
    <div class="container">
      <LargeCardDisplay
        v-for="info in largeCard.slice(0, 1)"
        :key="info.id"
        :cardsSection="info"
      />
      <SmallCardDisplay
        v-for="sCardInfo in smallCardInfo"
        :key="sCardInfo.id"
        :smallCardsSection="sCardInfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js";
export default {
  data() {
    return {
      largeCard: largeCardSections,
      smallCardInfo: smallCardSections,
    };
  },
};
</script>

<style scoped></style>
