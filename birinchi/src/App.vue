<template>
  <div id="app">
    <UserList />
    <hr />
    <UserList />
    <hr />
    <UserList />
    <hr />
    <UserList />
    <hr />
    <UserList />
    <hr />
    <UserList />
  </div>
</template>

<script>
import UserList from "./components/Users.vue";

export default {
  name: "App",
  components: { UserList }
};
</script>

