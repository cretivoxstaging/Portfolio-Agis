<template>
    <div>
        <Navbar />
        <slot />
    </div>
</template>

<script>
import Navbar from '~/components/navbar.vue';


export default {
    components: {
        Navbar
    }
}
</script>

<style lang="scss" scoped></style>