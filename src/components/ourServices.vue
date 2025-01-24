<template>
    <div class="our-services">
        <div class="wrapper">
            <div class="our-services__content">
                <h2 class="our-services__content__title">НАШИ УСЛУГИ</h2>
                <div class="our-services__content__item" v-for="item in items" >
                    <img class="our-services__content__item__img" :src="item.img" alt="" v-if="item.id % 2 != 0">
                    <div class="our-services__content__item__description">
                        <p class="our-services__content__item__description__title">{{ item.title }}</p>
                        <p class="our-services__content__item__description__text">{{ item.text }}</p>
                        <a href="#" class="our-services__content__item__description__button">Показать больше</a>
                    </div>
                    <img class="our-services__content__item__img" :src="item.img" alt="" v-if="item.id % 2 == 0">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import industrialSafety from '../assets/img/ourServices/industrial-safety.svg'
import laborProtection from '../assets/img/ourServices/labor-protection.svg'
import trainingWorkers from '../assets/img/ourServices/training-workers.svg'
import trainingPersonsWithDisabilities from '../assets/img/ourServices/training-persons-with-disabilities.svg'

export default {
    name: "ourServices",
    data() {
        return {
            items: [
                {
                    id: 1,
                    img: industrialSafety,
                    title: 'ПРОМЫШЛЕННАЯ БЕЗОПАСНОСТЬ',
                    text: `Создаем и интегрируем актуальные системы безопасности, осуществляем 
                        полное сопровождение предприятий. Все услуги: от аудита до проектов 
                        «под ключ» и разработки документации на все виды объектов.`
                },
                {
                    id: 2,
                    img: laborProtection,
                    title: 'ОХРАНА ТРУДА',
                    text: `Создаем и интегрируем актуальные системы безопасности, осуществляем полное сопровождение
                        предприятий. Все услуги: от аудита до проектов «под ключ» и разработки документации на все виды
                        объектов.`
                },
                {
                    id: 3,
                    img: trainingWorkers,
                    title: 'ОБУЧЕНИЕ РАБОЧИХ',
                    text: `Создаем и интегрируем актуальные системы безопасности, осуществляем полное сопровождение
                        предприятий. Все услуги: от аудита до проектов «под ключ» и разработки документации на все виды
                        объектов.`
                },
                {
                    id: 4,
                    img: trainingPersonsWithDisabilities,
                    title: 'ОБУЧЕНИЕ ЛИЦ С ОГРАНИЧЕННЫМИ ВОЗМОЖНОСТЯМИ ЗДОРОВЬЯ',
                    text: `Создаем и интегрируем актуальные системы безопасности, осуществляем полное сопровождение
                        предприятий. Все услуги: от аудита до проектов «под ключ» и разработки документации на все виды
                        объектов.`
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
.our-services {
    background-image: url(../assets/img/ourServices/servicesline.svg);
    background-repeat: no-repeat;
    background-position: 0 273px;
    padding: 60px 0 205px 0;

    &__content {
        display: flex;
        gap: 100px;
        flex-direction: column;

        &__title {
            font-weight: bold;
            font-size: 36px;
            line-height: 120%;
            color: #000;
            margin: 0 auto;
        }

        &__item {
            display: flex;
            gap: 100px;
            align-items: center;
            justify-content: space-between;

            &__img {
                width: auto;
                height: auto;
            }

            &__description {
                display: flex;
                flex-direction: column;
                gap: 34px;
                width: 48%;
                position: relative;
                align-items: flex-end;

                &__title {
                    font-weight: bold;
                    font-size: 24px;
                    line-height: 120%;
                    color: #000;
                    width: 100%;
                    display: flex;
                    align-items: flex-start;
                }

                &__text {
                    font-weight: 400;
                    font-size: 16px;
                    line-height: 150%;
                    color: #000;
                }

                &__button {
                    line-height: 120%;
                    font-size: 14px;
                    font-weight: 400;
                    margin-top: 20px;
                    width: 166px;
                    height: 40px;
                    border: 1px solid #DC911B;
                    border-radius: 5px;
                    color: #000;
                    background: none;
                    cursor: pointer;
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    &:hover {
                        background-color: #DC911B;
                        color: #fff;
                        transition: all 0.5s ease;
                    }
                }
            }
        }
    }
}
</style>