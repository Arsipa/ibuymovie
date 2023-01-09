<template>
    <section class="news">
        <Article
            v-for="article in news"
            :article="article"
            ></Article>
        <Pagination :list="news"></Pagination>
    </section>
</template>
<script>
import Article from "@/components/News/Article.vue";
import Pagination from "@/components/Pagination.vue";

import axios from "axios";

export default {
    name: "News",
    components: {
        Article,
        Pagination,
    },
    data() {
        return {
            news: null,
        };
    },
    mounted() {
        // get News
        axios
            .get("https://jsonplaceholder.typicode.com/posts")
            .then((response) => (this.news = response.data));
    },
};
</script>
<style scoped>
.news {
    padding-top: 80px;
}
</style>
