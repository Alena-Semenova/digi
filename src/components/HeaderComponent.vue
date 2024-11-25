<template>
    <header class="header">

        <div class="header__back-icon">
            <ArrowLeftIcon></ArrowLeftIcon>
        </div>
        <div class="header__section header-main">
            <div class="header-main__logo-container">
                <div class="header-main__logo-img">
                    <ImgSlugIcon></ImgSlugIcon>
                </div>
                <div class="header-main__logo-title">
                    Логотип
                </div>
            </div>
            <div class="header-main__catalog">Каталог</div>


        </div>

        <div class="header__section header__search">
            <BaseSearch></BaseSearch>
        </div>

        <div class="header__section header__info">
            <div>Информация о компании</div>
            <div>Контакты</div>
            <div>Полезные ссылки</div>
        </div>
    </header>
</template>

<script>
// icons
import { ImgSlugIcon } from "@/components/icons/index";

//components 
import BaseSearch from "@/components/base/BaseSearch";
import ArrowLeftIcon from "./icons/ArrowLeftIcon.vue";

export default {
    name: 'HeaderComponent',
    components: {
        ImgSlugIcon,
        BaseSearch,
        ArrowLeftIcon,
    },
    data() {
        return {}
    }
}
</script>

<style lang="scss" scoped>
.header {
    width: 100%;
    height: 72px;
    background-color: var(--color-white);
    padding: 12px 128px;
    display: flex;
    gap: 24px;
    margin-bottom: 24px;

    &__back-icon {
        display: none;
    }

    .header-main {
        width: 257px;


        &__logo-container {
            width: 145px;
            padding: 12px 24px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        &__logo-img {
            width: 18px;
            height: 18px;
            color: var(--color-blue);
        }

        &__catalog {
            width: 104px;
            height: 48px;
            border: 1px solid var(--color-blue);
            padding: 15px 24px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            font-weight: 500;
        }
    }

    &__section {
        display: flex;
        align-items: center;
        justify-content: space-between
    }

    &__search {
        width: 479px;
    }

    &__info {
        width: 400px;

        div {
            cursor: pointer;
        }
    }
}


@media screen and (max-width: 500px) {
    .header {
        height: 52px;
        padding: 0px 16px;
        display: flex;
        align-items: center;

        &__back-icon {
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
        }

        .header-main {
            display: none;
        }

        &__section {
            display: flex;
            align-items: center;
            justify-content: space-between
        }

        &__search {
            *::v-deep {
                .base-search__input {
                    max-width: 133px;
                }
            }
        }

        &__info {
            display: none;
        }
    }
}
</style>