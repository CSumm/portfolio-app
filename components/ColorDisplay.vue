<template>
    <div>
        <div class="color-swatch color-swatch--dark">#1e212b</div>
        Raisin Black
        <br/>
        <br/>
         <div class="color-swatch color-swatch--light">#fff</div>
         White
         <br/>
         <br/>
          <div class="color-swatch color-swatch--tertiary">#1E212B</div>
          Gray
    </div>
</template>

<style lang="scss" scoped>
.color-swatch {
    width: 10vw;
    height: 10vw;

    &--light {
        background-color: $text-color--light;
        color: $text-color--dark;
        border: 1px solid black;
    }

    &--dark {
        background-color: $text-color--dark;
        color: $text-color--light;
    }

    &--tertiary {
        background-color: $button-tertiary--background;
        color: $text-color--light;
    }
}
</style>