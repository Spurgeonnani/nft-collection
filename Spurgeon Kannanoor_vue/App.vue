<template>
  <MyHeader appName="NFT Collection" />
  <NftsList :nfts="nfts" />
  <MyFooter />
</template>

<script>
import MyHeader from "./components/MyHeader.vue";
import NftsList from "./components/NftsList.vue";
import MyFooter from "./components/MyFooter.vue";

export default {
  name: "App",
  components: {
    MyHeader,
    NftsList,
    MyFooter,
  },
  data() {
    return {
      nfts: [],
    };
  },
  methods: {
    async fetchNfts() {
      const res = await fetch("https://nfts-collection.onrender.com/api");
      const data = await res.json();
      console.log(data);
      return data.nfts;
    },
  },
  async created() {
    this.nfts = await this.fetchNfts();
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: sans-serif;
}

#app {
  background-color: rgb(60, 64, 67);
}
</style>
