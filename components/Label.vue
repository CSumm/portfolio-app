<template>
    <label class="a-label">{{text}}</label>
</template>

<style lang="scss">
.a-label {
    font-size: size(16);
    font-weight: 700;
    font-family: 'Maven Pro', sans-serif;
    color: $text-color--dark;

    &--small {
        font-size: 14px;
        font-weight: 500;
    }
}
</style>

<script>
export default {
    props: {
        text: String
    }
}
</script>