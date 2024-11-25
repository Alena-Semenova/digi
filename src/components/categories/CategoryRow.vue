<template class="category">
    <h3 class="category__title"> {{ title }}
        <span class="category__count"> {{ count }}</span>
    </h3>
</template>

<script>
export default {
    name: 'CategoryRow',
    props: {
        title: {
            type: String,
            default: 'Название категории'
        },
        count: {
            type: Number,
            default: 3
        }
    }
}
</script>

<style lang="scss" scoped>
.category {
    &__title {
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
}
</style>