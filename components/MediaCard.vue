<template>
<div class="m-media-card" :href="href">
    <div class="m-media-card__img">
        <img  :src="src"/>
    </div>
    <div class="m-media-card__cta">
           <p class="m-media-card__overlay-text">{{text}}</p>
           <Button v-if="!isDark" class="m-media-card__btn a-btn--primary"  :btnText="btnText"/>
           <Button v-if="isDark" class="m-media-card__btn a-btn--secondary"  :btnText="btnText"/>
    </div>
            </div>
</template>

<style lang="scss">

.m-media-card{
    position: relative;
    display: inline-block;
    padding: 0;

    img {
       max-width:100%;
max-height:100%;
    }


    &__img::after{
        content: "";
        position: absolute;
        top: 0;
        left: 0;
       width: 100%;
       height: 99.5%;
       background-color: rgba($text-color--light, 0.5);
    }

&__cta {
        position: absolute;
        display: inline-block;
          color: $text-color--dark;
           top: 20%;
           width: 100%;
           padding: 0 20px 0 20px;
         font-size: 24px;
         text-align: center;
    }

    &__overlay-text {
        margin-bottom: 40px;
    }

    &--dark {
       .m-media-card__overlay-text {
           color: $text-color--light;
       }

       .m-media-card__img::after {
           background-color: rgba($text-color--dark, 0.9);
       }
    }

    &--long {
        .m-media-card__cta {
            top: 25%; 
        }
        
    }
}
</style>

<script>
export default {
    props: {
        href: String,
        src: String,
        text: String,
        btnText: String,
        isDark: Boolean
    }
}
</script>