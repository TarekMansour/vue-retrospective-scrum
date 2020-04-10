<template>
  <!-- <button :class="type"><slot /></button> -->
  <div class="col col-11">
    <input
      :class="type"
      class="form-control "
      placeholder="what's up?"
      aria-label="what's up?"
      aria-describedby="basic-addon2"
    />
  </div>
</template>

<script>
export default {
  name: "TextField",
  props: ["type"]
};
</script>

<style></style>
