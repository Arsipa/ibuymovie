<template>
    <aside class="aside">
        <div class="aside__block">
            <p class="aside__title">ПРЕДСТОЯЩИЕ МАТЧИ</p>
            <div class="aside__list">
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
            </div>
        </div>
        <div class="aside__block">
            <p class="aside__title">ИСТОРИЯ МАТЧЕЙ</p>
            <div class="aside__list">
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
                <AsideItem></AsideItem>
            </div>
        </div>
        <router-link to="/" class="see-all-mathes"
            >СМОТРЕТЬ ВСЕ МАТЧИ</router-link
        >
        <div class="sponsor-advertisement">
            <a href="#">
                <img src="@/assets/img/advertisement.png" alt="">
            </a>
        </div>
    </aside>
</template>
<script>
import AsideItem from "@/components/Aside/AsideItem.vue";

export default {
    name: "Aside",
    components: {
        AsideItem,
    },
};
</script>
<style scoped>
.sponsor-advertisement{
    display: block !important;
    margin-top: 60px;
    position: sticky;
    top: 10px;
}
.see-all-mathes {
    background: #34a951;
    box-shadow: 0px 0.6px 2px #00000029;
    border-radius: 6px;
    font-weight: bold;
    font-size: 16px;
    letter-spacing: 0.13px;
    color: #ffffff;
    text-transform: uppercase;
    padding: 12px;
    text-align: center;
}
.aside {
    background: white;
    min-width: 400px;
    max-width: 400px;
    padding: 80px 16px 100px 16px;
    display: flex;
    flex-direction: column;
    align-items: stretch;
    gap: 25px;
    font-family: "FS Elliot Pro", sans-serif;
}
.aside .aside__block {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 30px;
}
.aside .aside__title {
    font-weight: bold;
    font-size: 24px;
    letter-spacing: 1.01px;
    margin-left: -16px;
    color: #181818;
    text-transform: uppercase;
    border-left: 2px solid #34a951;
    padding-left: 14px;
}
.aside .aside__list {
    display: flex;
    align-items: stretch;
    flex-direction: column;
    gap: 6px;
    width: 100%;
}
</style>
