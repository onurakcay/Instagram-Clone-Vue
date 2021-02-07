<template>
  <div class="app">
    <MasterHeader />

    <main class="main">
      <Container>
      <router-view />
      </Container>
    </main>
  </div>
</template>
<script>
import MasterHeader from "@/components/Header";
import Container from './components/Container.vue';
export default {
  name: "App",
  components: { MasterHeader,Container },
};
</script>

    Container<style>
.main{
  padding-top: 100px;
}

</style>
