<template>
    <p class="a-product-price">{{text}}</p>
</template>

<style lang="scss">
.a-product-price {
    font-size: 28px;
}
</style>

<script>
export default {
    props: {
        text: String
    }
}
</script>