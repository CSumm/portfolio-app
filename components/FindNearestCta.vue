<template>
    <a class="a-nearest-store-cta" type="button" :href="href">Find Nearest Store
        <span class="a-nearest-store-cta__icon"><font-awesome-icon class="fa-1x" :icon="['fas', 'arrow-right']"/></span>
        </a>
</template>

<style lang="scss">
.a-nearest-store-cta {
    color: $text-color--dark;
    font-weight: 700;

    &__icon {
        padding-left: 20px;
    }
}
</style>


<script>
export default {
    props: {
        href: String
    }
}
</script>