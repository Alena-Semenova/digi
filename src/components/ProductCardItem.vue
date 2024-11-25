<template>
    <div class="product-card-item">
        <div class="product-card-item__photo" :class="{ 'photo--empty': !productItem.image }">
            <img v-if="productItem.image" :src="productItem.image" alt="Product Image">
            <ProductNoPhotoIcon v-else />
            <ShieldBestseller :class="'product-card-item__bestseller'" />
            <ShieldDiscount :class="'product-card-item__discount'" :discount="25"></ShieldDiscount>
        </div>

        <div class="product-card-item__info">
            <div class="product-card-item__brand">{{ productItem.brand }}</div>
            <div class="product-card-item__description"> {{ productItem.description }} </div>
        </div>

        <div class="product-card-item__price price-block">
            <div class="price-block__first">{{ productItem.new_price }} ₽</div>
            <div class="price-block__second">{{ productItem.old_price }} ₽</div>
        </div>

        <div v-if="productItem.in_stock" class="product-card-item__buy">
            <BaseButton :text="'Купить'" />
        </div>

        <div v-if="!productItem.in_stock" class="product-card-item__not-available">
            <div class="not-available">Сообщить о поступлении</div>
        </div>
    </div>
</template>

<script>
import BaseButton from './base/BaseButton.vue';
import ProductNoPhotoIcon from './icons/ProductNoPhotoIcon.vue';
import ShieldBestseller from './shields/ShieldBestseller.vue';
import ShieldDiscount from './shields/ShieldDiscount.vue';

export default {
    name: "ProductCardItem",
    props: {
        productItem: {
            type: Object,
            default: () => ({
                id: 1,
                brand: "Бренд",
                new_price: 5999,
                old_price: 5999,
                description: "Полное название товара в несколько строк для вида с обрывом в конце...",
                image: "",
                in_stock: true,
            })
        }
    },
    components: {
        ProductNoPhotoIcon,
        ShieldDiscount,
        ShieldBestseller,
        BaseButton,
    },
}

</script>

<style lang="scss" scoped>
.product-card-item {
    position: relative;
    display: flex;
    flex-direction: column;
    gap: 16px;
    cursor: default;

    &__photo {
        position: relative;
        width: 100%;
        height: 200px;
        background-color: #F8F8FA;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    &__discount {
        position: absolute;
        bottom: 12px;
        left: 12px;
    }

    &__bestseller {
        position: absolute;
        top: 12px;
        left: 12px;
    }

    &__info {
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 8px;
        font-size: 14px;
        font-weight: 400;
        line-height: 16px;
    }

    &__brand {
        width: 100%;
        font-size: 14px;
        font-weight: 400;
        line-height: 16px;
        color: var(--color-font-seconds);
    }

    &__description {
        color: var(--color-font-main);
        cursor: pointer;

        &:hover {
            color: var(--color-font-hover);
        }
    }

    &__price {
        width: 100%;

        &.price-block {
            display: flex;
            gap: 8px;
        }

        .price-block {

            &__first {
                font-size: 16px;
                font-weight: 700;
                line-height: 14px;
                color: var(--color-font-main);
            }

            &__second {
                font-size: 12px;
                font-weight: 400;
                line-height: 14px;
                color: var(--color-font-seconds);
                text-decoration: line-through;
            }
        }
    }

    .not-available {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 38px;
        padding: 12px 16px;
        border-radius: 4px;
        border: 1px solid var(--color-font-seconds);
        color: var(--color-font-seconds);
        background-color: var(--color-white);
        font-size: 14px;
        font-weight: 700;
        line-height: 14px;
        cursor: pointer;
    }
}
</style>