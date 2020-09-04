<template>
<div class="a-radio-btn">
   <label>
       <input :id="id" type="radio" :name="name" ref="radioBtn" :value="value"/>
       <span @keyup.enter="checkedRadio" role="radio" tabindex="0" aria-checked="false" class="a-radio-btn__design"/>
       <label :for="id" class="a-radio-btn__label">{{text}}</label>
   </label>
   </div>
</template>

<style lang="scss" scoped>

[type="radio"]{
    opacity: 0;
}

.a-radio-btn {
   font-family: 'Maven Pro', sans-serif;
   margin-bottom: 25px;

&__label {
    position: relative;
    padding-left: 30px;
    line-height: 1.3;
    cursor: pointer;
    font-weight: 700;
    display: inline-block;

    &:hover {
        color: rgba($text-color--dark, 0.8);
    }
}

&__design {
    position: absolute;
    left: 20px;
    width: 20px;
    height: 20px;
    border: 2px solid rgba($text-color--dark,0.7);
    border-radius: 50px;
    cursor: pointer;
}

&__design:focus {
    background-color: rgba( $text-color--dark, 0.1);
    border-radius: 50px;
}

   [type="radio"]:checked + &__design::after {
         content: "";
         position: absolute;
         left: 2px;
         top: 2px;
    width: 13px;
    height: 13px;
    border: 1px solid $text-color--dark;
    border-radius: 50px;
    cursor: pointer;
         background-color: $text-color--dark;
         animation: fadeIn ease-out 0.3s;
     }
}

@keyframes fadeIn {
    from {
    opacity: 0;
    }
    to {
        opacity: 1;
    }
}
</style>

<script>
export default {
    props: {
        id: String,
        text: String,
        name: String,
        value: String
    },
    methods: {
        checkedRadio: function(event) {
           if(event.key == "Enter"){
                this.$refs.radioBtn.checked = true;
           }
    }
        }
    }

</script>