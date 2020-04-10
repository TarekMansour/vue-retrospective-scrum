<template>
  <div>
    <h2>Retrospective</h2>
    <div ref="container">
      <div class="input-group">
        <TextField />
        <div class="input-group-append">
          <button class="btn btn-danger" type="button" @click="onClick">
            <b-icon icon="plus-circle" aria-hidden="true"></b-icon>
          </button>
        </div>
      </div>
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
        propsData: { type: "text" }
      });
      instance.$slots.default = ["Click me!"];
      instance.$mount();
      this.$refs.container.appendChild(instance.$el);
    }
  }
};
</script>

<style></style>
