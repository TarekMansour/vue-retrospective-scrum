<template>
  <div>
    <h2>Static template:</h2>
    <TextField>Hello</TextField>
    <TextField type="primary">Hello</TextField>

    <h2>Dynamically inserted:</h2>
    <div ref="container">
      <button @click="onClick">Click to insert</button>
    </div>
  </div>
</template>

<script>
import Vue from "vue";
import TextField from "../components/TextField.vue";

export default {
  name: "Retro",
  components: { TextField },
  methods: {
    onClick() {
      var ComponentClass = Vue.extend(TextField);
      var instance = new ComponentClass({
        propsData: { type: "primary" }
      });
      instance.$slots.default = ["Click me!"];
      instance.$mount(); // pass nothing
      //         console.log(this.$refs)
      this.$refs.container.appendChild(instance.$el);
    }
  }
};
</script>

<style></style>
