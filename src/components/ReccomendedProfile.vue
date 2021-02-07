<template>
  <div >
    <header class="header section">
      <div class="header-author">
        <Avatar :size="32" :src="source"></Avatar>
        <div class="author">
          <CustomText tag="b">{{title}}</CustomText>
          <CustomText size="small" class="light-gray">
            Senin İçin Önerilenler
          </CustomText>
        </div>
      </div>
      <a class="follow-button">
        <CustomText size="small" tag="b" class="blue">
          Takip Et
        </CustomText>
      </a>
    </header>
  </div>
</template>

<script>
import Avatar from "@/components/Avatar";
import CustomText from "@/components/CustomText";
export default {
  name: "ReccomendedProfile",
  components: {
    Avatar,
    CustomText,
  },
  props: {
    source: {
      type: String,
      default:
        "https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-19/s150x150/74479455_405159716820785_1883930487483793408_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_ohc=UMAU7Ng9-vEAX8TjjUu&tp=1&oh=683b724fc0e40a97dc0018cafff499c6&oe=603F8884",
    },
    title:{
        type:String,
        default:"Onur AKÇAY"
    }
  },
};
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
    padding-bottom: 6px;
    padding-top: 6px;
  justify-content: space-between;
}
.header .header-author {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.header .header-author .author {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
}
.light-gray {
  color: rgba(var(--f52, 142, 142, 142), 1);
}
.follow-button {
  color: rgba(var(--d69, 0, 149, 246), 1);
}
</style>
