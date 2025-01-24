<template>
    <div class="feedback">
        <div class="wrapper">
            <div class="feedback__content">
                <h3 class="feedback__content__title">ВОПРОСЫ?</h3>
                <p class="feedback__content__text">Оставьте заявку и мы с Вами свяжемся</p>
                <div class="feedback__content__form">
                    <div class="feedback__content__form__fields">
                        <input class="feedback__content__form__fields__name" type="text" placeholder="Ваше имя">
                        <input class="feedback__content__form__fields__phone" type="text" placeholder="Ваш телефон">
                    </div>
                    <button class="feedback__content__form__button">оставить заявку</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Feedback"
}
</script>

<style lang="scss" scoped>
.feedback {
    background-image: url(../assets/img/feedback/feedback-line.svg);
    background-repeat: no-repeat;
    margin-top: 200px;
    position: relative;
    background-size: cover;

    &::before {
        content: '';
        position: absolute;
        bottom: -20px;
        left:  calc(50% - 358px);
        width: 100px;
        height: 300px;
        background-image: url(../assets/img/feedback/man.svg);
        background-repeat: no-repeat;
        background-position: right;
    }

    &::after {
        content: '';
        position: absolute;
        bottom: -20px;
        right: calc(50% - 329px);
        width: 125px;
        height: 300px;
        background-image: url(../assets/img/feedback/woman.svg);
        background-repeat: no-repeat;
        background-position: left;
    }

    &__content {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin: 0 auto;
        width: 600px;
        //height: 200px;
        background-color: #FFE0B0;

        &__title {
            font-weight: bold;
            font-size: 24px;
            line-height: 120%;
            color: #000000;
            margin-top: 28px;
        }

        &__text {
            font-weight: normal;
            font-size: 14px;
            line-height: 150%;
            color: #000000;
            margin-top: 10px;
        }

        &__form {
            display: flex;
            flex-direction: column;
            position: relative;

            &__fields {
                display: flex;
                margin-top: 24px;
                gap: 54px;

                &__name,
                &__phone {
                    width: 142px;
                    height: 26px;
                    border: 1px solid #DC911B;
                    box-sizing: border-box;
                    padding-left: 10px;
                    font-weight: normal;
                    font-size: 16px;
                    line-height: 150%;
                    color: #000000;
                    background: none;
                    border: none; 
                    outline: none; 
                    transition: border-color 0.3s; 
                    border-bottom: 1px solid #DC911B;

                    &:focus {
                        border-bottom: 1px solid black;

                    }
                }
            }

            &__button {
                position: relative;
                margin: 0 auto;
                top: 20px;
                cursor: pointer;
                width: 160px;
                margin-top: 20px;
                height: 39px;
                background: none;
                border: 1px solid #DC911B;
                border-radius: 5px;
                font-weight: 400;
                font-size: 14px;
                line-height: 120%;
                color: black;

                &:hover {
                    background-color: #DC911B;
                    color: white;
                    transition: all .5s ease;
                }
            }
        }
    }
}
</style>