<template>
  <div>
    <Nav />
    <div class="container">
      <hero/>
      <large-card-display
        v-for="card in largeCardInfo"
        :key="card.id"
        :cardsSection="card"
      />
      <small-card-display
        v-for="card in smallCardInfo"
        :key="card.id"
        :cardsSection="card"
      />
    </div>
  </div>
</template>

<script>
import {largeCardSections, smallCardSections} from "../assets/data.js"
import Hero from "../components/Hero";
import LargeCardDisplay from "../components/LargeCardDisplay";
import SmallCardDisplay from "../components/SmallCardDisplay";

export default {
  components: {SmallCardDisplay, LargeCardDisplay, Hero},
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardInfo: smallCardSections
    }
  },
}
</script>
