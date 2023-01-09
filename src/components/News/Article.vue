<template>
    <article class="article" 
        :class="{ 'articleOpen': isTextOpen }"
        @click="isTextOpen = !isTextOpen"
    >
        <div class="article__info">
            <!-- <p class="article__type">НОВОСТИ</p> -->
            <p class="article__type">{{ article.id }}</p>
            <p class="article__title">{{article.title}}</p>
            <p class="article__text">
                {{ article.body }}
            </p>
            <p class="article__date">25 Октября 2022 в 20:32</p>
        </div>
        <img src="@/assets/img/article.png" alt="" class="article__img" />
    </article>
</template>

<script>
export default {
    name: "Article",
    props: {
        article: Object,
    },
    data() {
        return {
            isTextOpen: false,
        };
    },
};
</script>

<style scoped>

.article {
    display: flex;
    align-items: stretch;
    justify-content: space-between;
    font-family: "FS Elliot Pro", sans-serif;
    margin-bottom: 30px;
    gap: 80px;
}

.article .article__info {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}
.article .article__type {
    font-weight: 900;
    font-size: 14px;
    letter-spacing: 0.59px;
    color: #232323;
    text-transform: uppercase;
    opacity: 0.36;
    margin-bottom: 20px;
}

.article .article__title {
    font-weight: 900;
    font-size: 24px;
    margin-bottom: 8px;
    letter-spacing: 1.01px;
    color: #232323;
}

.article .article__text {
    font-size: 18px;
    flex-grow: 1;
    line-height: 22px;
    letter-spacing: 0.22px;
    margin-bottom: 30px;
    color: #a1a1a1;
    cursor: pointer;

    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 6;
    line-clamp: 6;
}


.article .article__date {
    font-weight: 900;
    font-size: 14px;
    letter-spacing: 0.17px;
    color: #a1a1a1;
    opacity: 0.82;
}

.article .article__img {
    box-shadow: 0px 2px 8px #00000029;
    border-radius: 0px 38px;
    height: 10%;
    object-fit: cover;
    transition: 0.5s;
    max-width: 35%;
}

.article.articleOpen{
    gap: 10px;
}
.article.articleOpen .article__text {
    -webkit-box-orient: unset;
}
.article.articleOpen .article__img{
    max-width: 10%;
    position: sticky;
    top: 5px;
}
</style>
