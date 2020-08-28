<template>
    <a class="a-btn" href="">{{btnText}}</a>
</template>


<style lang="scss" scoped>
  .a-btn {
    padding: $padding-medium $padding-xl;
    text-decoration: none;
    background-color: rgb(209, 209, 209);
    color: #000;

    &--primary {
    background-color: $button-primary--background;
    color: $text-color--light;

     &:hover,
    &:focus,
    &:active {
        background-color: $button-tertiary--background;
    } 
    }

    &--secondary {
    background-color: $button-secondary--background;
    color: $text-color--dark;

    &:hover,
    &:focus,
    &:active
    {
        background-color: transparent;
        border: 1px solid $text-color--light;
        color: $text-color--light;
    }
    }

    &--tertiary {
            background-color: $button-secondary--background;
    color: $text-color--dark;
    border: 1px solid $text-color--dark;

      &:hover,
    &:focus,
    &:active {
        background-color: $button-primary--background;
        color: $text-color--light;
    }
    }
  }
</style>

<script>
export default {
    props: {
        btnText: String,
    }
}
</script>