<template>
    <p class="a-product-name" >{{text}}</p>
</template>

<style lang="scss">
.a-product-name {
    font-size: 22px;
    font-weight: 700;
    font-family: 'Maven Pro', sans-serif;
}
</style>

<script>
export default {
    props: {
        text: String
    }
}
</script>