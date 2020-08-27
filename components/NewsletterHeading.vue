<template>
<div>
    <h5 class="a-newsletter-heading">{{text}}</h5>
</div>
</template>

<style lang="scss" scoped>

.a-newsletter-heading {
    font-weight: 400;
}

</style>

<script>
export default {
    props: {
        text: String
    }
}
</script>