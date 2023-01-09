<script>
import Header from "@/components/Header";
import Footer from "@/components/Footer";
import Cookie from "@/components/Cookie";
import Auth from "@/components/Auth";

export default {
    name: "App",
    components: {
        Header,
        Footer,
        Cookie,
        Auth,
    },
};
</script>

<template>
    <Header></Header>
    <router-view />
    <Footer></Footer>
    <Auth v-if="true"></Auth>
    <Cookie></Cookie>
</template>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: inherit;
}
body {
    overflow-x: hidden;
    background: #FBFBFB;
}
ul {
    list-style: none;
}
.container {
    width: 1440px;
    margin: 0 auto;
}
a {
    text-decoration: none;
}
button {
    cursor: pointer;
    border: none;
}
::-webkit-scrollbar {
    width: 8px;
    background: none;
}

::-webkit-scrollbar-thumb {
    background: rgba(52, 169, 81, 0.7);
    border-radius: 100px;
}
::-webkit-scrollbar-thumb:hover {
    background: rgb(52, 169, 81);
}
.aside-page .aside-page__inner{
    display: flex;
    align-items: stretch;
    gap: 40px;
    justify-content: space-between;
}
</style>
