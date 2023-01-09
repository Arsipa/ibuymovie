<template>
    <div class="item">
        <router-link to="/" class="item__link"></router-link>
        <img src="@/assets/img/aside.png" alt="" class="item__img" />
        <div class="item__info">
            <header>
                <span class="item__date">25 ОКТЯБРЯ - 14:27</span>
                <span class="item__turnir">/ (TITLE name turnir)</span>
            </header>
            <footer>
                <span class="item__person">Mengrelii</span>
                VS
                <span class="item__person">JAIZER</span>
            </footer>
        </div>
    </div>
</template>
<script>
export default {
    name: "AsideItem",
};
</script>
<style scoped>
.item {
    background: #fbfbfb;
    box-shadow: 0px 2px 8px #00000029;
    border-radius: 6px;
    overflow: hidden;
    display: flex;
    align-items: stretch;
    position: relative;
}
.item .item__img {
    width: 38px;
    object-fit: cover;
}
.item .item__info {
    padding: 8px 12px 12px 12px;
    flex-grow: 1;
}
.item .item__date {
    text-transform: uppercase;
    opacity: 0.82;
    color: #181818;
    letter-spacing: 0.34px;
    font-size: 8px;
    line-height: 9px;
    font-weight: bold;
}
.item .item__turnir {
    color: #181818;
    letter-spacing: 0.34px;
    font-size: 8px;
    line-height: 9px;
    font-weight: bold;
    opacity: 0.54;
}
.item .item__link {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}
.item header {
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    gap: 5px;
}
.item .item__person {
    font-weight: bold;
    font-size: 12px;
    letter-spacing: 0.5px;
    color: #181818;
}
.item footer {
    letter-spacing: 0.34px;
    color: #181818;
    font-size: 8px;
    display: flex;
    align-items: center;
    gap: 12px;
}
</style>
