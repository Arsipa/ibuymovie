<template>
    <div class="cookie" v-if="!this.isHidden">
        <p>
            Сайт использует cookie-файлы. Продолжив просмотр сайта, Вы таким
            образом подтверждаете свое согласие на использование этих файлов.
        </p>
        <button @click="this.acceptCookie()">Принять</button>
    </div>
</template>

<script>
export default {
    name: "Cookie",
    data() {
        return {
            isHidden: false,
        };
    },
    methods: {
        getCookie(name) {
            const parts = `; ${document.cookie}`.split(`; ${name}=`);
            if (parts.length === 2) return parts.pop().split(";").shift();
        },
        acceptCookie() {
            document.cookie = "accept=true; path=/; max-age=604800"; //7day
            this.isHidden = true;
        },
    },
    mounted() {
        this.getCookie("accept")
            ? (this.isHidden = true)
            : (this.isHidden = false);
    },
};
</script>

<style scoped>
.cookie {
    z-index: 10;
    font-family: 'FS Elliot Pro', sans-serif;
    position: fixed;
    left: 50%;
    bottom: 16px;
    transform: translateX(-50%);
    background: #232323;
    padding: 26px;
    border-radius: 6px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 48px;
}
p {
    font-weight: bold;
    font-size: 16px;
    line-height: 19px;
    letter-spacing: 0.67px;
    color: white;
    max-width: 530px;
}
button {
    background: #34a951;
    padding: 8px 16px;
    color: #fcfcfc;
    text-transform: uppercase;
    font-size: 20px;
    box-shadow: 0.5px 2px 6px #00000029;
    border-radius: 6px 0 6px 0;
}
</style>
