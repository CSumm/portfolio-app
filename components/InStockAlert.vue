<template>
<div>
    <p v-if="isInStock >= 1" class="a-alert--instock">Currently in Stock</p>
    <p v-else class="a-alert--instock">Out of stock</p>
</div>
</template>

<style lang="scss">
.a-alert--instock {
color: rgba($text-color--dark, 0.4);
font-size: 14px;
}
</style>


<script>
export default {
    props: {
        isInStock: Number
    }
}
</script>