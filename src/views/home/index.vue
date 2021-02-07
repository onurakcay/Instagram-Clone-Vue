<template>
  <div class="home">
    <div class="timeline">
      <Post profile_img="https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-19/s150x150/101631384_700500324059481_3407705667727785984_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_ohc=JHPW5kfYB_kAX_sZfHv&tp=1&oh=ece33e49c4a3b3b92a2c0ec87a7e4b06&oe=6049745A" title="saykodelipaylasimlarr" source="https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-15/e35/146837605_695421221136260_4793435536311471443_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_cat=1&_nc_ohc=pwUbu9-1lLAAX9G5Lyi&tp=1&oh=7a879c9f02cf8d0a5ba712bfe81c63a7&oe=60476D8D" />
       <Post profile_img="https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-19/s150x150/101189838_898118164039285_9101055177900687360_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_ohc=4cXmuj3X2y0AX_flgAQ&tp=1&oh=2485792af4551be2825729bdea9644c9&oe=604A35ED" title="nicepaylasimlar" source="https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-15/e35/p1080x1080/146235181_409204617043429_7691668934689263151_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_cat=1&_nc_ohc=b5j8FPfVBB4AX-lK41N&tp=1&oh=664e5b92c028b075713e3455caf63282&oe=60487123" />
    </div>
    <div class="sidebar">
     <Sidebar />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import CustomText from "@/components/CustomText";
import Post from "@/components/Post";
import Sidebar from '@/components/Sidebar';

export default {
  name: "Home",
  components: {
    Post,
    Sidebar,
  },
};
</script>
<style scoped>
.home {
  display: grid;
  grid-template-columns: 1fr 295px;
  grid-gap: 30px;
}
.sidebar {
}
@media only screen and (max-width: 768px) {
  .home {
    display: block;
    max-width: 685px;
    margin-left: auto;
    margin-right: auto;
  }
  .sidebar {
    display: none;
  }
}
</style>
