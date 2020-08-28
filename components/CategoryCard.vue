<template>
    <a class="m-category-card" :href="href">
        <div class="m-category-card__img">
        <img :src="src"/>
        </div>
        <p class="m-category-card__text">{{text}}</p>
        </a>
</template>

<style lang="scss">

.m-category-card {
text-decoration: none;
 color: $text-color--dark;
display: inline-block;

 &__img {
     position: relative;
      
 }

 img {
    width: 100%;
    height: 100%;
 }

 &__img::after{
        content: "";
        position: absolute;
        top: 0;
        left: 0;
       width: 100%;

       /* height of 99.5 seems to cover the exact amount
       and 100 seems to overlap the div
       */
       height: 99.5%;

       background-color: rgba($text-color--dark, 0.5);
       opacity: 0;
       transition: opacity ease-in 0.2s;
    }

&__text {
    margin-top: 13px;
    font-size: 24px;
}

&:hover,
    &:focus {

        .m-category-card__img::after {
            opacity: 1;
        }

        .m-category-card__text {
            color: rgba($text-color--dark, 0.5);
        }
    }

    &--center {
        text-align: center;
    }

    &--right {
        text-align: right;
    }
}

</style>

<script>
export default {
    props: {
        text: String,
        src: String,
        href: String
    }
}
</script>