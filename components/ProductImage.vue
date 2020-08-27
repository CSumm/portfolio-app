<template>
    <img class="a-product-image" :src="imgUrl"/>
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
        imgUrl: String
    }
}
</script>