<template>
    <div class="container">
      <h3 class="header"> {{smallCardsSection.title}}</h3>
      <div class="cards-container">
          <SmallCard
          v-for="smallCard in smallCardsSection.cards" :key="smallCard.id" :card="smallCard"
          />
      </div>
  </div>
</template>

<script>
    export default {
        props: ['smallCardsSection']
        
    }
</script>

<style scoped>
.container {
    margin-top: 2rem;
}
    .header {
        font-weight: 700;
        font-size: 1.5rem;
        margin-bottom: 2rem;
    }

    .cards-container {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
    }
</style>