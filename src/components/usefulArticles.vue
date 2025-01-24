<template>
    <div class="useful-articles">
        <div class="wrapper">
            <h2 class="useful-articles__title">Полезные статьи</h2>
            <div class="useful-articles__block">
                <a class="useful-articles__block__item" v-for="item in items">
                    <p class="useful-articles__block__item__title" v-text="item.title"></p>
                    <p class="useful-articles__block__item__date" v-text="item.date"></p>
                    <p class="useful-articles__block__item__description" v-text="item.description"></p>
                </a>
            </div>
            <a class="useful-articles__all-articles" href="#">ВСЕ СТАТЬИ</a>
        </div>
    </div>
</template>

<script>
export default {
    name: "usefulArticles",
    data() {
        return {
            items: [
                {
                    id: 1,
                    title: 'Заголовок',
                    date: '12 феврала',
                    description: 'Тут текст на несколько строк Тут текст на несколько строк Тут текст точнона несколько строк Тут текст ',
                },
                {
                    id: 2,
                    title: 'Заголовок',
                    date: '12 феврала',
                    description: 'Тут текст на несколько строк Тут текст на несколько строк Тут текст точнона несколько строк Тут текст ',
                },
                {
                    id: 3,
                    title: 'Заголовок',
                    date: '12 феврала',
                    description: 'Тут текст на несколько строк Тут текст на несколько строк Тут текст точнона несколько строк Тут текст ',
                },
                {
                    id: 4,
                    title: 'Заголовок',
                    date: '12 феврала',
                    description: 'Тут текст на несколько строк Тут текст на несколько строк Тут текст точнона несколько строк Тут текст ',
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.useful-articles {
    margin-top: 170px;

    &__title {
        font-size: 38px;
        line-height: 120%;
        color: #000000;
    }

    &__block {
        margin-top: 90px;
        margin-bottom: 60px;
        display: flex;
        justify-content: space-between;

        &__item {
            display: flex;
            flex-direction: column;
            gap: 10px;
            width: 245px;
            position: relative;

            &__title {
                font-weight: bold;
                font-size: 16px;
                line-height: 21px;
                color: #000000;
            }

            &__date {
                font-weight: 400;
                font-size: 12px;
                line-height: 21px;
                color: #C6C6C6;
            }

            &__description {
                font-weight: 500;
                font-size: 12px;
                line-height: 21px;
                color: #000000;
            }
        }
        
    }
    &__all-articles {
        position: sticky;
        top: calc(100% + 60px);
        left: 100%;
        font-size: 18px;
        font-weight: bold;
        line-height: 120%;
        color: black;
        cursor: pointer;
    }
}
</style>