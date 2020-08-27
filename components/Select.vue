<template>
  <div
    class="a-custom-select"
    :tabindex="tabindex"
    @blur="open = false"
  >
    <div
      class="a-custom-select__selected"
      :class="{open: open}"
      @click="open = !open"
    >
      {{ selected }}
      <font-awesome-icon v-if="!open" class="fa-1x a-custom-select__arrow-down" :icon="['fas', 'angle-down']"/>
      <font-awesome-icon v-if="open" class="fa-1x a-custom-select__arrow-up" :icon="['fas', 'angle-up']"/>
    </div>
    <div
      class="a-custom-select__items"
      :class="{selectHide: !open}"
    >
      <div
        class="a-custom-select__item"
        v-for="(option, i) of options"
        :key="i"
        @click="selected=option; open=false; $emit('input', option)"
      >
        {{ option }}
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>


.a-custom-select {
  position: relative;
  width: 100%;
  text-align: left;
  outline: none;
  height: 47px;
  line-height: 47px;

  &__arrow-down {
    position: absolute;
    top: 15px;
    right: 20px;
  }

  &__arrow-up {
    position: absolute;
    top: 15px;
    right: 20px;
  }

  &__selected {
      background-color: $text-color--light;
  border-radius: 6px;
  border: 1px solid #858586;
  color: $text-color--dark;
  padding-left: 8px;
  cursor: pointer;
  user-select: none;  
  }

  &__selected-open {
border: 1px solid rgba($text-color--dark, 0.4);
  border-radius: 6px 6px 0px 0px;
} 
  
  &__selected::after {
position: absolute;
  content: "";
  top: 22px;
  right: 10px;
  width: 0;
  height: 0;
  border: 4px solid transparent;
  border-color: #fff transparent transparent transparent;
  }

  &__items {
      color: $text-color--dark;
  border-radius: 0px 0px 6px 6px;
  overflow: hidden;
  border-right: 1px solid rgba($text-color--dark, 0.4);
  border-left: 1px solid rgba($text-color--dark, 0.4);
  border-bottom: 1px solid rgba($text-color--dark, 0.4);
  position: absolute;
  background-color: $text-color--light;
  left: 0;
  right: 0; 
  }

  &__item {
      color: $text-color--dark;
  padding-left: 8px;
  cursor: pointer;
  user-select: none;
}

&__item:hover{
    background-color: rgba($text-color--dark, 0.1);
}
  }

.selectHide {
  display: none;
}
</style>

<script>
export default {
  props:{
    options:{
      type: Array,
      required: true
    },
    tabindex:{
      type: Number,
      required: false,
      default: 0
    }
  },
  data() {
    return {
      selected: this.options.length > 0 ? this.options[0] : null,
      open: false
    };
  },
  mounted(){
    this.$emit('input', this.selected);
  }
};
</script>
