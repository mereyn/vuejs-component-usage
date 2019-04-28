<template>
  <div>
    <div class="title">
      <slot name="title"></slot>
      <span style="color: #ccc">
        <slot name="subtitle">Contact Us</slot>
      </span>
    </div>
    <hr>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
h2 {
  color: red;
}

.title {
  font-style: italic;
}
</style>