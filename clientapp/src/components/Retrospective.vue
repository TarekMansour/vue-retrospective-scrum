<template>
  <div>
    <h1>Retrospective</h1>

    <div>
      <div class="row  mt-10">
        <label class="col col-4">MAD</label>
        <label class="col col-4">SAD</label>
        <label class="col col-4">GLAD</label>
      </div>
      <div class="row row-margin-05">
        <div class="input-group col col-4">
          <TextField class="col col-11" />
          <div class="input-group-append col col-1">
            <button class="btn btn-danger" type="button" @click="onMadClick">
              <b-icon icon="plus-circle" aria-hidden="true"></b-icon>
            </button>
          </div>
        </div>
        <div class="input-group col col-4">
          <TextField class="col col-11" />
          <div class="input-group-append col col-1">
            <button class="btn btn-warning" type="button" @click="onSadClick">
              <b-icon icon="plus-circle" aria-hidden="true"></b-icon>
            </button>
          </div>
        </div>
        <div class="input-group col col-4">
          <TextField class="col col-11" />
          <div class="input-group-append col col-1">
            <button class="btn btn-success" type="button" @click="onGladClick">
              <b-icon icon="plus-circle" aria-hidden="true"></b-icon>
            </button>
          </div>
        </div>
      </div>
      <div class="row ">
        <div ref="container1" class="col"></div>
        <div ref="container2" class="col"></div>
        <div ref="container3" class="col"></div>
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
    onMadClick() {
      var ComponentClass = Vue.extend(TextField);
      var instance = new ComponentClass({
        propsData: { type: "text" }
      });
      //instance.$slots.default = ["Click me!"];
      instance.$mount();
      this.$refs.container1.appendChild(instance.$el);
    },
    onSadClick() {
      var ComponentClass = Vue.extend(TextField);
      var instance = new ComponentClass({
        propsData: { type: "text" }
      });
      instance.$mount();
      this.$refs.container2.appendChild(instance.$el);
    },
    onGladClick() {
      var ComponentClass = Vue.extend(TextField);
      var instance = new ComponentClass({
        propsData: { type: "text" }
      });
      instance.$mount();
      this.$refs.container3.appendChild(instance.$el);
    }
  }
};
</script>

<style></style>
