<template>
    <div class="customer-reviews">
        <div class="wrapper">
            <h2 class="customer-reviews__title">Отзывы клиентов</h2>
            <div class="customer-reviews__slider">
                <swiper :navigation="true" :modules="modules" :slides-per-view="slidesPerView" :spaceBetween="47"
                    class="customer-reviews__slider__swiper">
                    <swiper-slide v-for="item in items"> <img :src="item.img" :alt="item.alt"> </swiper-slide>
                    <a class="customer-reviews__slider__button" href="#">ПОКАЗАЬТЬ ВСЕ</a>
                </swiper>
            </div>
        </div>
    </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import { Navigation } from 'swiper/modules';
import 'swiper/swiper-bundle.css';
import Review from '../assets/img/CustomerReviews/review.jpg';

export default {
    name: "customerReviews",
    components: {
        Swiper,
        SwiperSlide
    },
    data() {
        return {
            items: [
                {
                    id: 1,
                    alt: 'Отзыв от клиента',
                    img: Review,
                },
                {
                    id: 2,
                    alt: 'Отзыв от клиента',
                    img: Review,
                },
                {
                    id: 3,
                    alt: 'Отзыв от клиента',
                    img: Review,
                },
                {
                    id: 4,
                    alt: 'Отзыв от клиента',
                    img: Review,
                },
                {
                    id: 5,
                    alt: 'Отзыв от клиента',
                    img: Review,
                },
                {
                    id: 6,
                    alt: 'Отзыв от клиента',
                    img: Review,
                },
            ]
        }
    },
    setup() {
        return {
            modules: [Navigation],
            slidesPerView: 3,

        };
    },
}
</script>

<style lang="scss">
.customer-reviews {
    background-color: #3e3e3d;

    .wrapper {
        background-image: url(../assets/img/customerReviews/man.svg);
        background-repeat: no-repeat;
        background-position: right -40px;
        background-size: contain;
    }

    &__title {
        color: #fff;
        text-align: center;
        font-weight: bold;
        font-size: 36px;
        line-height: 120%;
        margin: 0 auto;
        padding-top: 125px;
        position: relative;
        right: 276px;
    }

    &__slider {
        position: relative;
        right: 276px;

        &__swiper {
            width: 50%;
            height: 242px;
            position: relative;
            margin-top: 106px;
            padding-bottom: 167px;
        }

        &__button {
            position: absolute;
            right: 0;
            bottom: 80px;
            color: #fff;
            font-size: 18px;
            line-height: 120%;
            font-weight: bold;
            cursor: pointer;
            pointer-events: all;
        }
    }

}
</style>

<style lang="scss">
.swiper {
    &-slide {
        text-align: center;
        font-size: 18px;
        background: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 242px;

        img {
            display: block;
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }

    &-navigation {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 10px;
        margin-top: 20px;
    }

    &-button {
        &-prev,
        &-next {
            position: absolute;
            width: 34px;
            height: 34px;
            margin-top: 80px;
            z-index: 999;
            background: #fff;
            border: 1px;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: visible;
            cursor: pointer;
            color: #000;

            &:hover {
                background-color: #fff;
                color: #DC911B;
                border: 1px solid #DC911B;
                transition: all 0.3s ease-in-out;
            }

            &::after {
                font-size: 20px;
                font-weight: bold;
            }
        }

        &-prev {
            left: 44%;
            background-color: #C4C4C4;
            opacity: 1;
            border: 1px solid #C4C4C4;

            &.swiper-button-disabled {
                opacity: 1;
                pointer-events: all;
                border: 1px solid #C4C4C4;

                &:hover {
                    background-color: #fff;
                    color: #DC911B;
                    border: 1px solid #DC911B;
                    transition: all 0.3s ease-in-out;
                }
            }
        }

        &-next {
            right: 44%;
            background-color: #DC911B;
            border: 1px solid #DC911B;

            &.swiper-button-disabled {
                opacity: 1;
                pointer-events: all;

                &:hover {
                    background-color: #fff;
                    color: #DC911B;
                    border: 1px solid #DC911B;
                    transition: all 0.3s ease-in-out;
                }
            }
        }
    }
}
</style>