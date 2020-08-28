<template>
    <div class="m-breadcrumbs">
        <Link class="a-link--small" :href="firstHref" :text="firstLink"/>
        <span>/</span>
        <Link class="a-link--small" :href="secondHref" :text="secondLink"/>
         <span>/</span>
         <Link class="a-link--small" :href="thirdHref" :text="thirdLink"/>
        </div>
</template>

<script>
export default {
    props:{
        firstLink: String,
        firstHref: String,
        secondLink: String,
        secondHref: String,
        thirdLink: String,
        thirdHref: String,
    }
}
</script>