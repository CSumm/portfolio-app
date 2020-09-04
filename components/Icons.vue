<template>
<div>
    <font-awesome-icon class="fa-2x" :icon="['fas', 'user-circle']"/>
    <font-awesome-icon class="fa-2x" :icon="['fas', 'shopping-bag']"/>
    <font-awesome-icon class="fa-2x" :icon="['fas', 'bars']"/>
    <font-awesome-icon class="fa-2x" :icon="['fas', 'arrow-right']"/>
    <font-awesome-icon class="fa-2x" :icon="['fas', 'angle-up']"/>
    <font-awesome-icon class="fa-2x" :icon="['fas', 'angle-down']"/>
    <font-awesome-icon class="fa-2x" :icon="['fas', 'caret-left']"/>
    <font-awesome-icon class="fa-2x disabled" :icon="['fas', 'caret-left']"/>
    <font-awesome-icon class="fa-2x" :icon="['fas', 'caret-right']"/>
        <font-awesome-icon class="fa-2x disabled" :icon="['fas', 'caret-right']"/>
    <font-awesome-icon class="fa-2x search-glass" :icon="['fas', 'search']"/>
    <font-awesome-icon class="fa-2x search-glass" :icon="['fas', 'plus']"/>
    <font-awesome-icon class="fa-2x" :icon="['fas', 'sort-amount-down-alt']"/>
     <font-awesome-icon class="fa-2x yellow-star" :icon="['fas', 'star-half']"/>
      <font-awesome-icon class="fa-2x yellow-star" :icon="['fas', 'star']"/>
    </div>
</template>

<style lang="scss" scoped>

.yellow-star {
    color: #f2e94e;
}

.disabled {
    color: rgba(#efefd0, 0.9);
}

.search-glass {
color: rgba(#808080,0.4)
}
</style>