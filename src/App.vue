<script>
import Header from "@/components/Header";
import Footer from "@/components/Footer";

export default {
    name: "App",
    components: {
        Header,
        Footer,
    },
};
</script>

<template>
  <Header></Header>
  <router-view/>
  <Footer></Footer>
</template>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: inherit;
}
ul{
  list-style: none;
}
.container{
  width: 1440px;
  margin: 0 auto;
}
a{
  text-decoration: none;
}
button{
  cursor: pointer;
  border: none;
}
</style>
