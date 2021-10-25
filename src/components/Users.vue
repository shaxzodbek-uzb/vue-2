<template>
  <ul>
    <UserItem
      v-for="(item, index) in names"
      :key="index"
      :name="item"
      @selected="selected(index)"
      :id="index"
      :active="active"
    />
  </ul>
</template>

<script>
import UserItem from "./UserItem";

export default {
  components: { UserItem },
  data() {
    return {
      active: null,
      names: [
        "Shaxzodbek",
        "Baxriddin",
        "Azizbek",
        "Shaxzodbek",
        "Baxriddin",
        "Azizbek",
        "Shaxzodbek",
        "Baxriddin",
        "Azizbek",
        "Shaxzodbek",
        "Baxriddin",
        "Azizbek",
        "Shaxzodbek",
        "Baxriddin",
        "Azizbek",
        "Shaxzodbek",
        "Baxriddin",
        "Azizbek",
        "Nodirbek"
      ]
    };
  },
  methods: {
    selected(index) {
      this.active = index;
    }
  }
};
</script>

<style>
.selected {
  font-weight: bold;
  color: blue;
}
</style>