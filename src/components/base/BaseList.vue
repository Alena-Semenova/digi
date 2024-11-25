<template>
    <ul class="base-list">
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>
        <li class="base-list__item">
            <input type="checkbox" class="base-list__checkbox">
            <span class="base-list__title">Атрибут</span>
            <span class="base-list__count">3</span>
        </li>

    </ul>
</template>

<script>
export default {
    name: 'BaseList',
}
</script>

<style lang="scss" scoped>
.base-list {
    width: 100%;
    height: 180px;
    list-style-type: none;
    padding-left: 0;
    display: flex;
    flex-direction: column;
    gap: 12px;
    overflow: auto;
    scrollbar-width: thin;

    &__item {
        position: relative;
        display: flex;
        align-items: center;
    }

    &__checkbox {
        margin-right: 12px;
    }

    &__count {
        position: absolute;
        right: 13px;
        color: var(--color-font-seconds);
        font-size: 12px;
        font-weight: 400;
        line-height: 14px;
    }
}
</style>