<template>
    <input type="text" :placeholder="placeholder" class="a-input-box"/>
</template>

<style lang="scss" scoped>
.a-input-box {
    font-family: 'Maven Pro', sans-serif;
    font-weight: 800;
    color: rgba($text-color--dark, 0.7);
    border: 1px solid rgba($text-color--dark, 0.4);
    padding: 5px 0 5px $padding-small;
    width: 347px;
}
</style>

<script>
export default {
    props: {
        placeholder: String
    }
}
</script>