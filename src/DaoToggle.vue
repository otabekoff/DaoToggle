<template>
  <div class="checkbox-slider">
    hell
    <input type="checkbox" v-model="checked" @change="onChange" id="checkbox">
    <label for="checkbox" class="slider"></label>
    <label for="checkbox">
      <slot></slot>
    </label>
  </div>
</template>

<script>
export default {
  name: 'DToggle',
  props: {
    defaultChecked: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      checked: this.defaultChecked
    }
  },
  methods: {
    onChange() {
      this.$emit('input', this.checked)
    }
  }
}
</script>

<style lang="scss">
.checkbox-slider {
  display: flex;
  align-items: center;
  .slider {
    position: relative;
    margin-right: 10px;
    width: 50px;
    height: 30px;
    background: #ddd;
    transition: 0.4s;
    border-radius: 15px;
    cursor: pointer;
  }
  .slider::before {
    position: absolute;
    content: '';
    height: 20px;
    width: 20px;
    left: 5px;
    top: 5px;
    background: #fff;
    transition: 0.4s;
    border-radius: 50%;
    box-shadow: 0, 0, 1 rgba(0, 0, 0, 0.15);
  }
  input {
    display: none;
  }
  input:checked + .slider {
    background: blue;
  }
  input:checked + .slider:before {
    transform: translateX(20px);
  }
}
</style>
