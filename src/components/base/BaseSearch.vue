<template>
    <div class="base-search">
        <div class="base-search__container">
            <div class="base-search__icon">
                <SearchIcon></SearchIcon>
            </div>
            <input class="base-search__input" placeholder="Поиск по 100 000 товаров" v-model="value">
            <div v-if="value" class="base-search__actions">
                <CrossInCircleIcon :class="'base-search__clear'" @click.native="clearInput" />
                <button class="base-search__button" @click="search"> Найти </button>
            </div>
        </div>
    </div>
</template>

<script>
import CrossInCircleIcon from '../icons/CrossInCircleIcon.vue';
import { SearchIcon } from '../icons/index';

export default {
    name: 'BaseSearch',
    props: {},
    components: {
        CrossInCircleIcon,
        SearchIcon,
    },
    data() {
        return {
            value: '',
            isFocused: false,
        }
    },

    methods: {
        clearInput() {
            this.value = '';
        },

        search() {
            this.$emit('search', this.value);
        }
    }
}
</script>


<style lang="scss" scoped>
.base-search {
    width: 100%;
    height: 48px;
    border-radius: 10px;
    border: 1px solid var(--color-font-main);

    &:hover {
        border-color: var(--color-blue);
        transition: all 0.1s ease-in-out;
    }

    &__container {
        width: 100%;
        height: 100%;
        padding: 11px 16px;
        display: flex;
        align-items: center;
    }

    &__icon {
        width: 24px;
        height: 24px;
        margin-right: 8px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    &__input {
        border: none;
        outline: none;
        flex: 1;
    }

    &__button {
        display: flex;
        align-items: center;
        width: fit-content;
        height: 38px;
        padding: 12px 16px;
        border-radius: 8px;
        border: none;
        outline: none;
        background-color: var(--color-blue);
        color: var(--color-white);
        font-weight: 700;
        cursor: pointer;
    }

    &__actions {
        display: flex;
        align-items: center;
        gap: 8px;
    }

    &__clear {
        cursor: pointer;
    }
}
</style>