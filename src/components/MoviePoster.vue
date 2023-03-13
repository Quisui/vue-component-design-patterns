<script>
export default {
  props: {
    image: {
      type: String,
      default:
        "https://www.google.com/images/branding/googlelogo/1x/googlelogo_light_color_272x92dp.png",
      validator: (proprValue) => {
        const hasImagesDirectory = proprValue.indexOf("/images/") > -1;
        const isPNG = proprValue.endsWith(".png");
        const isJPEG =
          proprValue.endsWith(".jpeg") || proprValue.endsWith(".jpg");
        const hasValidExtension = isPNG || isJPEG;
        return hasImagesDirectory && hasValidExtension;
      },
    },
    title: {
      type: String,
      required: true,
    },
    length: {
      type: [Number, String],
      default: 90,
    },
    watched: {
      type: Boolean,
      default: false,
    },
  },
};
</script>
<template>
  <section>
    <img :src="image" />
    <h1>{{ title }}</h1>
    <p>{{ length }}</p>
    <span v-if="watched">Yes sr.</span>
  </section>
</template>
