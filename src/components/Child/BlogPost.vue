<template>
  <div class="card">
    <div class="card-body">
      <h5 class="card-title">{{ title }}</h5>
      <p class="card-text">{{ text }}</p>
      <div class="card-footer">
        <button @click="$emit('enlargeText')">Enlarge text</button>
        <button @click="$emit('ensmallText')">EnSmall text</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["title", "text"],
};
</script>

<style>
</style>