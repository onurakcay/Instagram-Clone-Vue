<template>
  <div class="home">
    <CustomText tag="h1" class="a1">Profile</CustomText>
    <CustomText tag="p" class="a1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum doloribus cumque laboriosam corporis sint sapiente veritatis placeat repellendus similique. Itaque at tenetur doloribus voluptatum. Accusamus placeat nostrum sequi distinctio molestiae!</CustomText>
     <div id="nav">
      <router-link to="/profile">Post</router-link> |
      <router-link to="/profile/igtv">IGTV</router-link> |
      <router-link to="/profile/save">Save</router-link> |
      <router-link to="/profile/tag">Tag</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
// @ is an alias to /src
import CustomText from "@/components/CustomText";

export default {
  name: "Profile",
  components: {
    CustomText,
  },
};
</script>
<style scoped>

</style>
