<template>
  <button :class="type"><slot /></button>
</template>

<script>
export default {
  name: "TextField",
  props: ["type"]
};
</script>

<style></style>
