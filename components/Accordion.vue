<template>
    <div class="m-accordion" ref="accordion">
        <span class="m-accordion__title" @click="trigger">
            {{accordionTitle}}
               <div class="m-accordion__drop-icon "> 
                             <font-awesome-icon v-if="!isOpen" class="fa-1x" :key="new Date().getTime()" :icon="['fas', 'plus']"/>
                              <font-awesome-icon v-if="isOpen" class="fa-1x" :key="new Date().getTime()" :icon="['fas', 'minus']"/>
        </div>
            </span>
         
        <div v-show="isOpen" class="m-accordion__content">
            <RadioButtonGroup
            :idOne="idOne"
            :idTwo="idTwo"
            :idThree="idThree"
            :textOne="textOne"
            :textTwo="textTwo"
            :textThree="textThree"
            :name="name" 
            class="m-accordion__choices" />
        </div>
        </div>
</template>

<style lang="scss">
.m-accordion {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;

    &__title{
        display: flex;
        justify-content: space-between;
        border-bottom: 2px solid rgba($text-color--dark,0.3);
        width: 100%;
        cursor: pointer;
    }

    &__drop-icon {
        padding-bottom: 10px;
     
    }

    &__content {
        top: 40%;
        left: 0;
        width: 100%;
        padding: 20px;
    }
}


</style>

<script>
export default {
    props: {
        accordionTitle: String,
        idOne: String,
        idTwo: String,
        idThree: String,
        textOne: String,
        textTwo: String,
        textThree: String,
        name: String,
    },
data: function(){
    return {
        isOpen: false
    }
},
methods: {
    trigger: function(){
    this.isOpen = !this.isOpen;
    }
}
}
</script>