<template>
  <div class="book">
    <slot name="title" :bookTitle="bookTitle"></slot>
  </div>
</template>

<script>
export default {
  data() {
    return {
      bookTitle: "Child Provindg data",
    };
  },
};
</script>

<style lang="scss" scoped>
</style>