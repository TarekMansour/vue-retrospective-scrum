<template>
  <!-- <button :class="type"><slot /></button> -->
  <div class="col col-4">
    <input
      :class="type"
      class="form-control "
      placeholder="Recipient's username"
      aria-label="Recipient's username"
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
