<template>
  <div>
    <section v-if="!splashImage" id="inventory">
      <h1> {{ userName }} </h1>
      <h2> {{ userSanity }} </h2>
      <h2> {{ userHat }} </h2>
      <h2> {{ userClothing }} </h2>
      <h2> {{ userShoes }} </h2>
      <h2> $ {{ userMoney }} </h2>
    </section>
    <section id="splashImage" v-else>
      <h1 class="text-center splashH1">What's your name?</h1>
        <input class="text-center center" type="text" name="userName" maxlength="10" v-model="userName" v-on:keydown.enter="splashImage = !splashImage">
        <p><h1 class="text-center splashH1 pressEnter">PRESS ENTER TO PLAY</h1></p>
    </section>
  </div>
</template>

<script>
  import UserInventory from './UserInventory.vue';

  export default {
    data: function() {
            return {
              userHat: null,
              userClothing: "Modern Clothing",
              userShoes: "Modern Shoes",
              userMoney: 2000,
              userName: null,
              userSanity: 100,
              splashImage: true,
              };
        },
        methods: {
        },
        components: {
            appUserInventory: UserInventory,
        }
    }

</script>

<!-- CSS libraries -->
<style src="normalize.css/normalize.css"></style>

<!-- Global CSS -->
<style>
  code {
    font-family: Menlo, Monaco, Lucida Console, Liberation Mono, DejaVu Sans Mono, Bitstream Vera Sans Mono, Courier New, monospace, serif;
    font-size: 0.9em;
    white-space: pre-wrap;
    color: #2c3e50;
  }

  code::before, code::after {
    content: '`';
  }
</style>

<!-- Scoped component css -->
<!-- It only affect current component -->
<style scoped>
  #inventory {
    text-align: center;
    right: 0;
    position: fixed;
  }

  #splashImage {
    text-align: center;
  }
</style>
