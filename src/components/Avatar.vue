<template>
  <figure class="avatar">
    <img :src="src" :alt="alt" :width="size" :height="size" />
  </figure>
</template>

<script>
export default {
  name: "Avatar",
  props: {
    src: {
      type: String,
      default:
        "https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-19/s150x150/74479455_405159716820785_1883930487483793408_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_ohc=UMAU7Ng9-vEAX8TjjUu&tp=1&oh=683b724fc0e40a97dc0018cafff499c6&oe=603F8884",
    },
    alt: {
      type: String,
    },
    size: {
      type: Number,
    },
  },
};
</script>

<style>
.avatar {
  padding: 2px;
  background: linear-gradient(
    45deg,
    #405de6,
    #5851db,
    #833ab4,
    #c13584,
    #e1306c,
    #fd1d1d
  );
  border-radius: 999px;
  display: inline-flex;
}
.avatar img {
  border-radius: inherit;
  border: 2px solid white;
}
</style>
