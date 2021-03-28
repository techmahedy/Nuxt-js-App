<template>
    <div class="container">
        <Nav/>
        <LargeCardDisplay
            v-for="cardInfo in largeCardInfo.slice(0,1)"
            :key="cardInfo.id"
            :cardsSection="cardInfo"
        />
        <SmallCardDisplay 
            v-for="cardInfo in smallCardSections"
            :key="cardInfo.id"
            :cardsSection="cardInfo"
        /> 
    </div>
</template>

<script>
import { largeCardSections, smallCardSections } from "@/assets/data.js"
import Nav from '../../components/Nav.vue'
    export default {
    components: { Nav },
        data(){
            return {
                largeCardInfo: largeCardSections,
                smallCardSections: smallCardSections
            }
        }
    }
</script>

<style scoped>
</style>