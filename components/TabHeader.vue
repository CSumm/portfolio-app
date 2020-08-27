<template>
    <h5 class="tab-header">{{text}}</h5>
</template>

<style lang="scss">

.tab-header {
    display: inline-block;
    cursor: pointer;

    &:focus,
    &:active {
        border-bottom: 2px solid $text-color--dark;
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