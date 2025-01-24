<template>
    <div class="header">
        <div class="wrapper">
            <a class="header__logo" href="#">
                <img src="../assets/logo.svg" alt="">
            </a>
            <div class="header__links">
                <ul>
                    <li><a href="">О нас </a></li>
                    <li><a href="">Услуги </a></li>
                    <li><a href="">Новости </a></li>
                    <li><a href="">Акции </a></li>
                    <li><a href="">Документы </a></li>
                    <li><a href="">Отзывы </a></li>
                    <li><a href="">Контакты </a></li>
                </ul>
            </div>
            <div class="header__contacts">
                <div class="header__contacts__phone">
                    <img src="../assets/img/header/phone.svg" alt="">
                    <button>+7 (351) 777-80-70</button>
                </div>
                <div class="header__contacts__order">
                    <button>Заказать звонок</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header'
}

</script>

<style lang="scss" scoped>
.header {
    padding-top: 17px;
    box-sizing: border-box;
    

    .wrapper{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    &__logo {
        img {
            width: 192px;
            height: 75px;
        }
    }

    &__links {
        ul {
            display: flex;
            list-style: none;
            gap: 42px;

            li {
                a {
                    color: #2D2D2D;
                    font-weight: bold;
                    font-size: 14px;
                    line-height: 21px;
                }
            }
        }
    }

    &__contacts {
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        &__phone,
        &__order {
            button {
                color: #2D2D2D;
                font-weight: bold;
                font-size: 16px;
                background: none;
                border: none;
                cursor: pointer;
            }
        }
        &__phone {
            display: flex;
            align-items: center;

            img {
                margin-right: 10px;
            }

            button {
                line-height: 24px;
            }
        }

        &__order {
            button {
                line-height: 19px;
                text-decoration: underline dotted #2D2D2D; 
                text-underline-offset: 3px; 
                cursor: pointer;
            }
        }
    }
}
</style>