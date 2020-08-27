<template>
    <div class="m-search-bar">
        <TextInput class="m-search-bar__input" placeholder="Search"/>
            <a class="m-search-bar__submit" type="button" href="">
                 <font-awesome-icon class="fa-1x search-glass" :icon="['fas', 'search']"/>
            </a>
    </div>
</template>

<style lang="scss">

.m-search-bar {

&__submit {
    position: relative;
    right: 40px;
    padding: 3px 10px;
    color: rgba($text-color--dark, 0.4);
}
}


</style>