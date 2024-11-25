<template>
    <div class="price-filter">
        <BaseHeaderFilter :title="'Цена'" :filter-id="'price-filter'" />

        <div class="price-filter__inputs">
            <div class="price-filter__input">
                <span>от</span>
                <input :value="minPriceResult">
            </div>
            <div class="divider"></div>
            <div class="price-filter__input">
                <span>до</span>
                <input :value="maxPriceResult">
            </div>
        </div>
    </div>
</template>

<script>
import BaseHeaderFilter from '../base/BaseHeaderFilter.vue';

export default {
    name: 'PriceFilter',
    components: {
        BaseHeaderFilter,
    },
    props: {
        minPrice: {
            type: Number,
            default: 5500
        },
        maxPrice: {
            type: Number,
            default: 5500
        }
    },
    computed: {
        minPriceResult() {
            return this.minPrice + ' ₽';
        },
        maxPriceResult() {
            return this.maxPrice + ' ₽';
        }
    }
}
</script>

<style lang="scss" scoped>
.price-filter {
    width: 100%;

    &__title {
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 16px;
        font-weight: 700;
        margin-bottom: 16px;
    }

    &__inputs {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    &__input {
        border: 1px solid #D5D5D5;
        color: #D5D5D5;
        border-radius: 4px;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 119px;
        gap: 6px;
        padding: 0px 8px;
        height: 36px;

        input {
            width: 100%;
            border: none;
            outline: none;
        }
    }

    .divider {
        width: 10px;
        height: 1px;
        background-color: #D5D5D5;
        margin: 10px 0;

    }
}
</style>