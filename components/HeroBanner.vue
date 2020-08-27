<template>
<div class="m-hero-banner">
    <img class="m-hero-banner__img" src="https://via.placeholder.com/728x150"/>
    <SectionTitle class="m-hero-banner__overlay" text="Lorem ipsum"/>
    </div>
</template>

<style lang="scss">
.m-hero-banner {
    &__img {
     width: 100%;   
    }

    &__overlay {
        position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, 0);
    }
}


</style>