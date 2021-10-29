<template>
  <div>{{ full_name }}</div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      required: true
    },
    surename: {
      type: String,
      default: ""
    }
  },
  computed: {
    full_name() {
      return `Mr ${this.surename} ${this.name}`;
    }
  }
};
</script>