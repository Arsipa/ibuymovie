<template>
    <header>
        <div class="container">
            <router-link to="/" class="logo"
                ><img src="@/assets/logo.svg" alt="IBUYMOVIE"
            /></router-link>
            <nav>
                <router-link to="/">Главная</router-link>
                <router-link to="/">Мувимейкинг</router-link>
                <router-link to="/">Арена</router-link>
                <router-link to="/">Маркет</router-link>
                <Dropdown
                    title="Помощь"
                    :dropdown="[
                        { text: 'Правила', to: '/' },
                        { text: 'Вопросы и ответы', to: '/' },
                        { text: 'Команда проекта', to: '/' },
                        { text: 'Авторское право', to: '/' },
                        { text: 'Контакты', to: '/' },
                    ]"></Dropdown>
            </nav>
            <div class="header__right">
                <button class="green-btn">Авторизоваться</button>
            </div>
        </div>
    </header>
</template>

<script>
import Dropdown from "@/components/Dropdown.vue";

export default {
    name: "Header",
    components: {
        Dropdown,
    },
};
</script>

<style scoped>
header {
    background: #181818;
    padding: 22px 0;
    font-family: "FS Elliot Pro", sans-serif;
    color: white;
}

.logo {
    display: flex;
}

.container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 95px;
}

nav {
    flex-grow: 1;
    display: flex;
    align-items: center;
    gap: 22px;
}

nav a {
    letter-spacing: 0.35px;
    font-size: 16px;
    color: inherit;
    font-weight: bold;
}

.header__right {
    display: flex;
    align-items: center;
}

.green-btn {
    padding: 11px 22px;
    letter-spacing: 0.13px;
    color: white;
    font-size: 16px;
    box-shadow: 0px 0.6px 2px #00000029;
    border-radius: 6px;
    background: #34a951;
    font-weight: bold;
}
</style>
