<template>
    <div>
        <SectionHero />
        <Journey />
    </div>
</template>

<script>
import Journey from '~/components/journey.vue';
import SectionHero from '../components/section-hero.vue'
export default {
    components: {
        SectionHero,
        Journey
    },
    data() {
        return {
        }
    }

}
</script>

<style scoped></style>