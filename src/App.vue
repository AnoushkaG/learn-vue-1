<template>
  Hello, {{ name }}
  <div v-text="company"></div>
  <div v-html="designation"></div>
  <div v-html="hack"></div>
  <div v-bind:id="headingId">Heading</div>
  <button v-bind:disabled="isDisabled">Press Me</button>
  <h2 class="underline">Underline text</h2>

  <!-- to apply dynamic classes -->
</template>

<script>
export default {
  name: "App",
  components: {
    // HelloWorld
  },
  data() {
    return {
      name: "Anoushka",
      company: "Infosys",
      designation: "<b>Developer</b>",
      hack: `<a href="#" onclick="alert('You have been hacked')">Win a prize</a>`,
      headingId: "heading",
      isDisabled: true,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#heading {
  color: #8626c3;
  font-size: large;
}
.underline {
  text-decoration: underline;
}
</style>
