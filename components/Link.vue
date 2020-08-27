<template>
    <a :href="href" class="a-link">{{text}}</a>
</template>
<style lang='scss' scoped>
$this: &;

.a-link {
    font-size: 24px;
    text-decoration: none;
    color: $text-color--dark;
    padding: $padding-small;

    &:hover,
    &:focus {
        border-bottom: 1px solid rgba($text-color--dark, 0.3);
        color: rgba($text-color--dark, 0.7);
    }

    &--small {
    font-size: 16px;
    text-decoration: none;
    color: $text-color--dark;
    padding: $padding-small;

    &:hover,
    &:focus {
        border-bottom: 1px solid rgba($text-color--dark, 0.3);
        color: rgba($text-color--dark, 0.7);
    }
    }

    &--dark {
    font-size: 24px;
    text-decoration: none;
    color: $text-color--light;
    padding: $padding-small;
    background-color: $text-color--dark;

    &:hover,
    &:focus {
        border-bottom: 1px solid rgba($text-color--light, 0.3);
        color: rgba($text-color--light, 0.7);
    }
    }

    &--dark-small {
        background-color: $text-color--dark;
         color: $text-color--light;
         font-size: 16px;

    &:hover,
    &:focus {
        border-bottom: 1px solid rgba($text-color--light, 0.3);
        color: rgba($text-color--light, 0.7);
    }
    }
}
</style>

<script>
export default {
    props: {
        text: String,
        href: String
    }
}
</script>