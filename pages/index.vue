<template>
   <div>
     <Nav/>
      <div>
      <Hero />
      <LargeCardDisplay
        v-for="cardInfo in largeCardInfo"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      />
      <SmallCardDisplay 
        v-for="cardInfo in smallCardSections"
        :key="cardInfo.id"
        :cardsSection="cardInfo"
      /> 
    </div>
   </div>
</template>

<script>
import Hero from '../components/Hero.vue'
import LargeCardDisplay from '../components/LargeCardDisplay.vue'
import { largeCardSections , smallCardSections } from '@/assets/data.js'
import Nav from '../components/Nav.vue'

export default {
  components: { LargeCardDisplay, Hero, Nav },
  data(){
    return {
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections
    }
  }
}
</script>

<style>

</style>
