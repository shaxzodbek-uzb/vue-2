<template>
  <li @click="$emit('selected')" :class="{selected: active == id}">{{ name }}</li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: ""
    },
    id: {
      type: Number,
      default: 0
    },
    active: {
      type: Number,
      default: 0
    }
  }
};
</script>