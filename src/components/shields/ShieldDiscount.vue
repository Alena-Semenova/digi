<template>
    <div class="shield-discount">
        {{ discount }} %
    </div>
</template>

<script>
export default {
    name: 'ShieldDiscount',
    props: {
        discount: {
            type: Number,
        }
    }
}
</script>

<style>
.shield-discount {
    width: fit-content;
    height: 26px;
    padding: 6px 10px;
    background-color: var(--color-brand);
    color: var(--color-white);
    border-radius: 4px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: default;
}
</style>