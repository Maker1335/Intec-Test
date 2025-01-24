<template>
    <div class="mainBlock">
        <div class="wrapper">
            <Header />
            <div class="mainBlock__container">
                <h1 class="mainBlock__container__title">ОХРАНА ТРУДА <br> ПОЖАРНАЯ БЕЗОПАСНОСТЬ <br> ОБУЧЕНИЕ СОТРУДНИКОВ</h1>
                <p></p>
            </div>
        </div>
    </div>
</template>

<script>
import Header from './header.vue';
export default {
    name: 'mainBlock',
    components: {
        Header
    }
}
</script>

<style lang="scss" scoped>
.mainBlock {
    background: url(../assets/img/mainBlock/firefighters.jpg);
    background-size: cover;
    background-position: center;
    height: 687px;

    .wrapper {
        width: 100%;
        height: calc(100% - 96px);
    }

    &__container {
        display: flex;
        align-items: center;
        height: 100%;

        &__title {
            color: #2D2D2D;
            font-weight: bold;
            font-size: 32px;
            line-height: 150%;
        }

        &__img {}
    }
}
</style>