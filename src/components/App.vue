<template>
  <div id="app">
    <app-user></app-user>
  </div>
</template>

<script>
  import User from './User.vue';
  import UserInventory from "./UserInventory.vue";

  export default {
    components: {
            appUser: User,
            appUserInventory: UserInventory
        }
  }
</script>

<!-- CSS libraries -->
<style src="normalize.css/normalize.css"></style>

<!-- Global CSS -->
<style>
</style>
