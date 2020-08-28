<template>
<a class="m-carousel-item" :href="href">
    <div class="m-carousel-item__img">
        <img  :src="src"/>
    </div>
           <p class="m-carousel-item__overlay-text">{{text}}</p>
            </a>
</template>

<style lang="scss">

.m-carousel-item{
    position: relative;
    display: inline-block;

    &__img::after{
        content: "";
        position: absolute;
        top: 0;
        left: 0;
       width: 100%;
       height: 100%;
       background-color: rgba($text-color--light, 0.5);
    }

&__overlay-text {
    display: inline-block;
        font-size: 24px;
        position: absolute;
          top: 20%;
          left: 10%;
          color: $text-color--dark;
    }

    &--light {
       .m-carousel-item__overlay-text {
           color: $text-color--light;
       }

       .m-carousel-item__img::after {
           background-color: rgba($text-color--dark, 0.5);
       }
    }
}
</style>

<script>
export default {
    props: {
        href: String,
        src: String,
        text: String
    }
}
</script>