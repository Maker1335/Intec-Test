<template>
    <div class="projects">
        <div class="wrapper">
            <h2 class="projects__title">ПРОЕКТЫ</h2>
            <div class="projects__block">
                <div class="projects__block__item" v-for="item in items">
                    <img class="projects__block__item__img" :src="item.img" :alt="item.alt">
                    <p class="projects__block__item__name" v-text="item.name"></p>
                    <p class="projects__block__item__description" v-text="item.description"></p>
                    <a class="projects__block__item__link" :href="item.link"></a>
                    <p class="projects__block__item__date" v-text="item.date"></p>
                </div>
                <a class="projects__block__button" href="#">ВСЕ ПРОЕКТЫ</a>
            </div>
        </div>
    </div>
</template>

<script>
import Project1 from '../assets/img/projects/project1.svg'
import Project2 from '../assets/img/projects/progect2.jpg'

export default {
    name: "Projects",
    data() {
        return {
            items: [
                {
                    id: 1,
                    img: Project1,
                    alt: 'Проект 1',
                    name: 'НАЗВАНИЕ ПРОЕКТА 1',
                    description: `Очень много текста примерно на три строчки, ибо больше никто читать не будет.`,
                    link: '',
                    date: '12/2020'
                },
                {
                    id: 2,
                    img: Project2,
                    name: 'НАЗВАНИЕ ПРОЕКТА 2',
                    alt: 'Проект 2',
                    description: `Очень много текста примерно на три строчки, ибо больше никто читать не будет.`,
                    link: '',
                    date: '12/2020'
                }
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
.projects {
    padding-bottom: 90px;
    &__title {
        font-size: 36px;
        font-weight: bold;
        line-height: 120%;
        color: #000;
        margin-top: 75px;
    }

    &__block {
        margin-top: 50px;
        display: flex;
        flex-direction: column;
        gap: 100px;

        &__item {
            position: relative;
            display: grid;
            grid-template-areas:
                ".  img ."
                "name img description"
                "date img link";
            grid-template-columns: 150px 556px 300px;
            grid-template-rows: 140px 130px 42px;
            gap: 0 50px;

            &__img {
                grid-area: img;
                width: 556px;
                height: 312px;
                object-fit: cover;
            }

            &__name {
                grid-area: name;
                width: max-content;
                font-weight: bold;
                font-size: 36px;
                line-height: 120%;
                color: #000;
            }

            &__description {
                grid-area: description;
                font-weight: 400;
                font-size: 16px;
                line-height: 150%;
                color: #000;
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

            &__date {
                grid-area: date;
                font-weight: bold;
                font-size: 13px;
                line-height: 120%;
                color: #000;
            }
        }
        &__button {
            position: sticky;
            left: 100%;
            font-weight: bold;
            font-size: 18px;
            line-height: 120%;
            color: black;
            cursor: pointer;
            box-sizing: border-box;
            width: fit-content;
    
            &::after {
                content: '';
                position: absolute;
                top: 45%;
                left: calc(100% + 10px);
                width: 10px;
                height: 10px;
                border-top: 2px solid #DC911B;
                border-left: 2px solid #DC911B;
                transform: translate(-50%, -50%) rotate(137deg);
            }
        }
    }

    
}
</style>