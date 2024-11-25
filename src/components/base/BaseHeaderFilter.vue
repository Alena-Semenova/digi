<template>
    <div class="header-filter" :class="{ 'header-filter_center': !needCleaned }">
        <div class="header-filter__title"> {{ title }} </div>
        <div v-if="needCleaned" class="header-filter__clean" @click="clean"> Очистить </div>
    </div>
</template>

<script>
export default {
    name: "BaseHeaderFilter",
    props: {
        filterId: {
            type: String,
            default: "filter",
            required: true,
        },
        title: {
            type: String,
            default: ""
        },
        needCleaned: {
            type: Boolean,
            default: false
        }
    },

    methods: {
        clean() {
            this.$emit("clean", this.filterId);
        }
    }
}
</script>

<style lang="scss" scoped>
.header-filter {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    height: 20px;
    padding: 0 10px;
    margin-bottom: 16px;

    &_center {
        justify-content: center;
    }

    &__title {
        font-size: 16px;
        font-weight: 700;
        line-height: 20px;
        cursor: default;
    }

    &__clean {
        font-size: 12px;
        font-weight: 400;
        line-height: 12px;
        text-align: right;
        color: var(--color-font-seconds);
        text-decoration: underline;
        cursor: pointer;
    }
}
</style>