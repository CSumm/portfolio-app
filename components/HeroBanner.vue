<template>
<div class="m-hero-banner">
    <img class="m-hero-banner__img" src="https://via.placeholder.com/728x150"/>
    <SectionTitle class="m-hero-banner__overlay" text="Lorem ipsum"/>
    </div>
</template>

<style lang="scss">
.m-hero-banner {
position: relative;

    &__img {
     width: 100%;   
    }

    &__overlay {
        font-size: 24px;
        position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
    }

    &--light {
       .m-hero-banner__overlay {
           color: $text-color--light;
       }
    }

 @media (min-width: 576px) { 
     &__overlay {
         font-size:36px;
     }
  }

 @media (min-width: 992px) { 
     &__overlay {
         font-size: 60px;
     }
  }
}


</style>