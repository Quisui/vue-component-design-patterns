<!-- eslint-disable vue/multi-word-component-names -->
<script>
export default {
  data() {
    return {
      bookTitle: "Providing parent data",
    };
  },
};
</script>

<template>
  <Book>
    <template v-slot:title="{ bookTitle }">
      {{ bookTitle }}
    </template>
  </Book>
</template>

<style lang="scss" scoped></style>
