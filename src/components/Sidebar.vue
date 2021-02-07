<template>
  <div>
    <div class="profile">
      <header class="header section">
        <div class="header-author">
          <Avatar :size="50"></Avatar>
          <div class="author">
            <CustomText tag="b">onurakcay.tr</CustomText>
            <CustomText size="normal" class="light-gray">Onur Akçay</CustomText>
          </div>
        </div>
      </header>
    </div>
    <div class="reccomendation">
      <div class="text">
        <CustomText size="normal" tag="b" class="light-gray">
          Senin İçin Öneriler
        </CustomText>
        <a href="#"><CustomText size="small">Tümünü Gör</CustomText></a>
      </div>
    </div>
    <div class="recommendedProfile">
        <ReccomendedProfile title="demira626" source="https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-19/s150x150/121039626_810989026324221_4018608705021580781_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_ohc=PPLKj339rCQAX8FOuBa&tp=1&oh=63b0cb74d8541ee9b53c085f9e9c8327&oe=604A1578"/>
        <ReccomendedProfile title="kilinctasarim" source="https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-19/s150x150/70520490_2093438130761922_5664277366172549120_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_ohc=UqTPF1v-gAkAX_9J03G&tp=1&oh=91b494bb993dfd2e83260ca2aed619d9&oe=6048988E"/>
        <ReccomendedProfile title="seyremofficial" source="https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-19/s150x150/106368816_387018615601714_687387702395229097_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_ohc=WYCUP_9z5_IAX8Mdnfk&tp=1&oh=793c415278497241c0c1db1d548b8c21&oe=60487D87"/>
        <ReccomendedProfile title="okkes.kilinc" source="https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-19/s150x150/13696529_311462709186884_1829140535_a.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_ohc=RW1Sb6qHwvgAX9jwTyy&tp=1&oh=481c1fab580906dc0f3748863f77074b&oe=604AE682"/>
        <ReccomendedProfile title="zduranel" source="https://instagram.fist13-1.fna.fbcdn.net/v/t51.2885-19/s150x150/122516800_1022731718243672_9019488690128687574_n.jpg?_nc_ht=instagram.fist13-1.fna.fbcdn.net&_nc_ohc=VAKhrlbO7GQAX9wsuGt&tp=1&oh=5c6669f4a616bcdfb1634ce7fd31d47b&oe=6049A809"/>
    </div>
  </div>
</template>

<script>
import Avatar from "@/components/Avatar";
import CustomText from "@/components/CustomText";
import ReccomendedProfile from "@/components/ReccomendedProfile";
export default {
  name: "Sidebar",
  components: { Avatar, CustomText,ReccomendedProfile },
};
</script>

<style scoped>
.reccomendedProfile {
  padding-bottom: 8px;
  padding-top: 8px;
}
.reccomendation {
  padding-bottom: 4px;
  padding-top: 4px;
}
.text {
  display: flex;
  justify-content: space-between;
}
.profile {
  height: auto;
  margin-bottom: 10px;
  margin-top: 18px;
}
.header {
  display: flex;
  align-items: center;
  height: 60px;
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
</style>
