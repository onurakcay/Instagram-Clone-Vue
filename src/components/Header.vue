<template>
  <header class="header">
    <Container class="header-inner">
      <router-link to="/" class="logo"><img src="https://assets.stickpng.com/images/580b57fcd9996e24bc43c521.png" width="30px" alt=""></router-link>
      <form class="search">
        <input type="search" name="" id="" placeholder="Ara" />
      </form>
      <nav class="navigation">
        <router-link to="/">
          <IconHomeFill v-if="$route.name === 'Home'"></IconHomeFill>
          <IconHome v-else></IconHome>
        </router-link>
        <router-link to="/direct">
          <IconDirectFill v-if="$route.name === 'Direct'"></IconDirectFill>
          <IconDirect v-else></IconDirect>
        </router-link>
        <router-link to="/explore">
          <IconExploreFill v-if="$route.name === 'Explore'"></IconExploreFill>
          <IconExplore v-else></IconExplore>
        </router-link>
        <router-link to="/profile">
          <Avatar :size="20"></Avatar>
        </router-link>
      </nav>
    </Container>
  </header>
</template>

<script>
import IconHome from "@/icons/home.svg";
import IconHomeFill from "@/icons/home-fill.svg";

import IconDirect from "@/icons/direct.svg";
import IconDirectFill from "@/icons/direct-fill.svg";

import IconExplore from "@/icons/explore.svg";
import IconExploreFill from "@/icons/explore-fill.svg";

import Container from "@/components/Container";
import Avatar from "@/components/Avatar";
export default {
  name: "MainHeader",
  components: {
    IconHome,
    IconHomeFill,
    IconDirect,
    IconDirectFill,
    IconExplore,
    IconExploreFill,
    Container,
    Avatar,
  },
};
</script>
<style scoped>
.header {
  border-bottom: 1px solid rgb(var(--b6a));
  height: var(--header-height);
  display: flex;
  align-items: center;
  background-color: white;
}
.header-inner {
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  align-items: center;
}
.logo {
  font-size: 1.6rem;
  font-weight: bold;
  display: contents;
}
.search {
  text-align: center;
}
.search input {
  width: 215px;
  height: 28px;
  border: 1px solid rgb(var(--b6a));
  border-radius: 3px;
  background-color: rgb(var(--b3f));
  text-align: center;
  padding: 7px;
}
.navigation {
  position: static;
  display: flex;
  align-items: center;
  justify-content: flex-end;
}
@media only screen and (max-width: 600px) {
  .navigation {
    z-index: 90;
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: white;
    border-top: 1px solid rgb(var(--b6a));
    padding: 20px 0px;
    justify-content: space-around;
  }
  .search {
    display: none;
  }
  .header {
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    z-index: 90;
  }
  .header-inner {
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
  }
}
.navigation a {
  margin-left: 20px;
}
</style>
