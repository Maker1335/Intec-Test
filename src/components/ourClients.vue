<template>
    <div class="our-clients">
        <div class="wrapper">
            <div class="our-clients__content">
                <h3 class="our-clients__content__title">НАШИ КЛИЕНТЫ</h3>
                <div class="our-clients__content__block">
                    <img class="our-clients__content__block__img" :src="item.img" :alt="item.alt" v-for="item in items">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import ducharme from '../assets/img/ourClients/ducharme.svg'
import ducharme1 from '../assets/img/ourClients/ducharme1.svg'
import mattias from '../assets/img/ourClients/mattias.svg'
import mattias1 from '../assets/img/ourClients/mattias1.svg'
import poff from '../assets/img/ourClients/poff.svg'
import vega from '../assets/img/ourClients/vega.svg'
import volans from '../assets/img/ourClients/volans.svg'
import volans1 from '../assets/img/ourClients/volans1.svg'

export default {
    name: "ourClients",
    data() {
        return {
            items: [
                {
                    img: vega,
                    alt: 'вега'
                },
                {
                    img: ducharme,
                    alt: 'ducharme'
                },
                {
                    img: volans,
                    alt: 'volans'
                },
                {
                    img: mattias,
                    alt: 'mattias'
                },
                {
                    img: volans1,
                    alt: 'volans1'
                },
                {
                    img: mattias1,
                    alt: 'mattias1'
                },
                {
                    img: poff,
                    alt: 'poff'
                },
                {
                    img: ducharme1,
                    alt: 'ducharme1'
                },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
.our-clients {
    margin-top: 60px;

    &__content {
        &__title {
            margin-left: 220px;
            font-weight: bold;
            font-size: 36px;
            line-height: 120%;
            color: #000000;
            width: max-content;
        }

        &__block {
            display: flex;
            flex-wrap: wrap;
            margin-top: 60px;
            justify-content: space-between;

            &__img {
                width: 220px;
                padding: 60px 39px;
                border: 1px solid #F2F2F2;
            }
        }
    }
}
</style>