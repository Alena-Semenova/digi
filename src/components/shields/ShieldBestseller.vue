<template>
    <div class="shield-bestseller">
        {{ text }}
        <FireIcon></FireIcon>
    </div>
</template>

<script>
import FireIcon from '../icons/FireIcon.vue';

export default {
    name: 'ShieldBestseller',
    components: {
        FireIcon,
    },
    data() {
        return {
            text: 'Хит продаж',
        }
    },
}
</script>


<style>
.shield-bestseller {
    width: fit-content;
    height: 32px;
    padding: 8px;
    background-color: var(--color-white);
    border: 1px solid var(--scroll-bar);
    border-radius: 4px;
    gap: 4px;
    color: var(--color-font-main);
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: default;
}
</style>