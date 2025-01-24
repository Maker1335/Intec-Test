<template>
    <div class="footer">
        <div class="wrapper">
            <div class="footer__content">
                <div class="footer__links" v-for="item in items">
                    <a v-text="item.text" class="footer__links__main-link" href="#"></a>
                    <ul class="footer__links__sub-links">
                        <li class="footer__links__sub-link" v-for="item in item.items">
                            <a href="#" v-text="item.link" class="footer__links__sub-link-item"></a>
                        </li>
                    </ul>
                </div>
                <div class="footer__info">
                    <div class="footer__info__search">
                        <input class="footer__info__search__input" type="text" placeholder="Поиск" name="search">
                        <img src="../assets/img/footer/search.svg" alt="search-icon"
                            class="footer__info__search__search-icon">
                    </div>
                    <div class="footer__info__feedback">
                        <a class="footer__info__feedback__email" href="#"><img src="../assets/img/footer/email.svg"
                                alt=""> hello@stkrost.ru</a>
                        <a class="footer__info__feedback__phone" href="#"><img src="../assets/img/footer/phone.svg"
                                alt=""> +7 (351) 700-07-71</a>
                        <p class="footer__info__feedback__maps"><img src="../assets/img/footer/maps.svg" alt=""> г.
                            Челябинск</p>
                        <button class="footer__info__feedback__call">Обратный звонок</button>
                    </div>
                </div>
            </div>
            <div class="footer__bottom">
                <p class="footer__bottom__text">© 2020 Universe, Все права защищены</p>
                <a class="footer__bottom__logo" href="#"><img src="../assets/img/footer/intec-logo.svg" alt="intec-logo"></a>
                <div class="footer__bottom__empty-space">
                    <p></p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Footer",
    data() {
        return {
            items: [
                {
                    text: 'О нас',
                    items: [
                        {
                            link: 'Новости'
                        },
                        {
                            link: 'Статьи'
                        },
                        {
                            link: 'Сертификаты'
                        },
                        {
                            link: 'Объекты'
                        },
                        {
                            link: 'Склад'
                        },
                    ]
                },
                {
                    text: 'Каталог',
                    items: [
                        {
                            link: 'Прайсы'
                        },
                        {
                            link: 'Акции'
                        },
                    ],
                },
                {
                    text: 'Контакты',
                },
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
.footer {
    margin-top: 86px;
    background-color: #3E3E3D;
    padding-top: 30px;

    &__content {
        display: flex;
        justify-content: space-between;
        gap: 150px;
        padding-bottom: 55px;
    }

    &__links {
        display: flex;
        flex-direction: column;
        gap: 15px;

        &__main-link {
            font-size: 16px;
            font-weight: bold;
            color: white;
            text-decoration: none;
            line-height: 16px;

            &:hover {
                color: #DC911B;
                text-decoration: underline;
                transition: all .5s ease;
            }
        }

        &__sub-links {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        &__sub-link {
            &-item {
                font-size: 14px;
                color: #777E89;

                &:hover {
                    color: #DC911B;
                    transition: all .5s ease;
                }
            }
        }
    }

    &__info {
        display: flex;
        flex-direction: column;
        gap: 20px;
        width: 420px;

        &__search {
            width: 100%;
            height: 40px;
            position: relative;

            &__input {
                width: 100%;
                height: 40px;
                padding: 12px 18px;
                font-size: 13px;
                border: 1px solid white;
                border-radius: 3px;
                background: none;
                line-height: 19px;
                position: absolute;
                color: white;
                box-sizing: border-box;
            }

            &__search-icon {
                position: absolute;
                top: 50%;
                right: 15px;
                transform: translateY(-50%);
                cursor: pointer;
            }

            &:focus {
                outline: none;
                border: 1px solid white;
            }
        }

        &__feedback {
            display: flex;
            flex-wrap: wrap;
            gap: 22px;

            &__email,
            &__phone,
            &__maps,
            &__call {
                font-size: 14px;
                color: white;
                text-decoration: none;
                width: calc(50% - 11px);
                display: flex;
                gap: 10px;

                img {
                    width: 16px;
                    max-height: 18px;
                }

                &:hover {
                    color: #DC911B;
                    text-decoration: underline;
                    transition: all .5s ease;
                }
            }

            &__phone {
                font-size: 16px;
            }

            &__call {
                padding: 12px 22px;
                background-color: #FD9913;
                border: 1px solid #FD9913;
                color: white;
                font-size: 14px;
                font-weight: bold;
                border: none;
                border-radius: 5px;
                cursor: pointer;
                width: max-content;

                &:hover {
                    background-color: white;
                    color: black;
                    text-decoration: none;
                    transition: all .5s ease;
                }
            }
        }
    }
    &__bottom {
        display: flex;
        justify-content: space-between;
        flex: content;
        margin-top: 20px;
        padding-bottom:55px;
        padding-top: 55px;
        border-top: 1px solid #777E89;
        flex: none;
        &__text {
            font-size: 13px;
            line-height: 19px;
            color: white;
            flex: 1;
        }
        &__logo {
            flex: 0;
        }
        &__empty-space {
            flex: 1;
        }
    }
}
</style>