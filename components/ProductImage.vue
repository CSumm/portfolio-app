<template>
    <img class="a-product-image" :src="src"/>
</template>

<style lang="scss" scoped>
.a-product-image {
    &--thumbnail {
        max-width: 103px;
        max-height: 105px;
    }
}
</style>

<script>
export default {
    props: {
        src: String
    }
}
</script>