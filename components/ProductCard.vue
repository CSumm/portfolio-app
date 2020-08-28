<template>
    <a class="m-product-card" :href="href">
        <ProductImage class="m-product-card__img" :src="src" />
        <ProductName class="m-product-card__name" :text="productName"/>
        <ProductPrice class="m-product-card__price" :text="productPrice"/>
        </a>
</template>

<style lang="scss">
.m-product-card {
    display: inline-block;
    text-align: center;
    padding-bottom: 10px;
     text-decoration: none;

     &__img {
         margin-bottom: 10px;
     }

    &__name,
    &__price
    {
        color: $text-color--dark;
    }

    &__name {
        margin-bottom: 5px;
    }

    &:hover,
    &:focus {
        border-bottom: 1px solid rgba($text-color--dark, 0.3);
    }
}
</style>

<script>
export default {
    props: {
        src: String,
        productName: String,
        productPrice: String,
        href: String
    }
}
</script>