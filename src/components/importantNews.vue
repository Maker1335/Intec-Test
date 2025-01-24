<template>
    <div class="important-news">
        <div class="wrapper">
            <div class="important-news__content">
                <h3 class="important-news__content__title">РУБРИКА ВЫЖНЫХ НОВОСТЕЙ</h3>
                <div class="important-news__content__item" v-for="item in items">
                    <p class="important-news__content__item__title" v-text="item.title"></p>
                    <p class="important-news__content__item__date" v-text="item.date"></p>
                    <p class="important-news__content__item__description" v-text="item.description"></p>
                    <a class="important-news__content__item__link" :href="item.link"></a>
                </div>
            </div>
            <a class="important-news__all-news" href="#">ВСЕ НОВОСТИ</a>
        </div>
    </div>
</template>

<script>
export default {
    name: "importantNews",
    data() {
        return {
            items: [
                {
                    id: 1,
                    title: 'ВАЖНАЯ НОВОСТЬ',
                    date: '12/2020',
                    description: 'Очень много текста примерно на три строчки, ибо больше никто читать не будет.',
                    link: '#'
                },
                {
                    id: 2,
                    title: 'ВАЖНАЯ НОВОСТЬ',
                    date: '12/2020',
                    description: 'Очень много текста примерно на три строчки, ибо больше никто читать не будет.',
                    link: '#'
                },
                {
                    id: 3,
                    title: 'ВАЖНАЯ НОВОСТЬ',
                    date: '12/2020',
                    description: 'Очень много текста примерно на три строчки, ибо больше никто читать не будет.',
                    link: '#'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.important-news {
    margin-top: 90px;
    height: 470px;
    position: relative;

    &::before {
        content: '';
        position: absolute;
        top: 0;
        left: 0;
        width: 50%;
        height: 100%;
        background: #EDEEEF;
        background-image: url(../assets/img/importantNews/man.svg);
        background-repeat: no-repeat;
        background-position: center bottom; /* Разместить фон слева по центру */
    }

    .wrapper {
        height: 100%;
    }

    &__content {
        display: flex;
        justify-content: space-between;
        position: relative;
        top: 120px;

        &__title {
            font-weight: bold;
            font-size: 36px;
            line-height: 120%;
            color: #000000;
            width: min-content;
        }

        &__item {
            display: flex;
            flex-direction: column;
            gap: 16px;
            width: 228px;
            position: relative;

            &:last-child {
                &::after {
                    content: '';
                    position: absolute;
                    right: calc(100% + 50px);
                    width: 1px;
                    height: 100%;
                    border-left: 1px solid #B1B1B0;
                }
            }

            &__title {
                font-weight: bold;
                font-size: 18px;
                line-height: 120%;
                color: #000000;
            }

            &__date {
                font-weight: 400;
                font-size: 14px;
                line-height: 120%;
                color: #6F6F6E;
            }

            &__description {
                font-weight: 500;
                font-size: 16px;
                line-height: 150%;
                color: #000000;
            }

            &__link {
                grid-area: link;
                position: relative;
                width: 42px;
                height: 42px;
                cursor: pointer;
                background-color: #DC911B;
                border: 1px solid #DC911B;

                &::after {
                    content: '';
                    position: absolute;
                    top: 50%;
                    left: 45%;
                    width: 10px;
                    height: 10px;
                    border-top: 2px solid black;
                    border-left: 2px solid black;
                    transform: translate(-50%, -50%) rotate(137deg);
                }

                &:hover {
                    background-color: white;

                    &::after {
                        border-top: 2px solid #DC911B;
                        border-left: 2px solid #DC911B;
                    }

                    transition: all 1s ease;
                }
            }
        }
    }
    &__all-news {
        position: sticky;
        top: 100%;
        left: 100%;
        font-size: 18px;
        font-weight: bold;
        line-height: 120%;
        color: black;
        cursor: pointer;
    }
}
</style>