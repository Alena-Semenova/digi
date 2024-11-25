<template>
    <button class="base-button">
        {{ text }}
    </button>
</template>

<script>
export default {
    name: 'BaseButton',
    props: {
        text: {
            type: String,
            deault: 'Текст кнопки'
        }
    }
}
</script>

<style lang="scss" scoped>
.base-button {
    background-color: var(--color-white);
    border: 1px solid var(--color-brand);
    border-radius: 4px;
    font-size: 14px;
    font-weight: 700;
    height: 38px;
    width: fit-content;
    color: var(--color-brand);
    padding: 12px 16px;
    display: flex;
    align-items: center;
    cursor: pointer;

    &:hover {
        background-color: var(--color-brand);
        color: var(--color-white);
        transition: all 0.4s ease-in-out;
    }
}
</style>