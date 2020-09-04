<template>
<div class="m-radio-group">
    <RadioButton 
    :id="idOne" 
    :name="name" 
    :value="textOne" 
    :text="textOne"
    class="m-radio-group__button"
    />
    <RadioButton 
    :id="idTwo" 
    :name="name" 
    :value="textTwo" 
    :text="textTwo"
    class="m-radio-group__button"
    />
    <RadioButton 
    :id="idThree" 
    :name="name" 
    :value="textThree" 
    :text="textThree"
    class="m-radio-group__button"
    />
    </div>
</template>

<style lang="scss">

</style>

<script>
export default {
    props: {
        idOne: String,
        idTwo: String,
        idThree: String,
        textOne: String,
        textTwo: String,
        textThree: String,
        name: String,
    }
}
</script>