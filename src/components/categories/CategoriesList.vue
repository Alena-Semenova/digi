<template>
    <div class="categories-list">

        <CategoryRow />

        <ul class="categories-list__items">
            <li class="category">
                <CategoryRow />
            </li>

            <li class="category">
                <CategoryRow />
            </li>

            <li class="category">
                <CategoryRow />
            </li>
        </ul>
    </div>
</template>

<script>
import CategoryRow from './CategoryRow.vue';

export default {
    name: 'CategoriesList',
    components: {
        CategoryRow,
    }
}
</script>

<style lang="scss" scoped>
.categories-list {
    cursor: default;

    &__title {
        position: relative;
        font-size: 14px;
        font-weight: 400;
        color: var(--color-font-main);
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 30px;
        padding: 0 8px;
        border-radius: 5px;

        &:hover {
            background-color: var(--color-font-bg);
        }
    }

    &__count {
        font-size: 12px;
        font-weight: 400;
        color: var(--color-font-seconds)
    }

    &__items {
        padding: 0;
        margin: 0;
        padding-left: 32px;
    }

    .category {
        list-style-type: none;
    }
}
</style>