<template>
    <div class="size-filter">
        <BaseHeaderFilter :title="'Размер'" :filter-id="'size-filter'"/>
        <BaseList></BaseList>
    </div>
</template>


<script>
import BaseHeaderFilter from '../base/BaseHeaderFilter.vue';
import BaseList from '../base/BaseList.vue';

export default {
    name: 'SizeFilter',
    components: {
        BaseHeaderFilter,
        BaseList,
    },
    data() {
        return {

        }
    }
}
</script>

<style lang='scss' scoped>
.brand-filter {
    display: flex;
    flex-direction: column;
    align-items: center;
    border-radius: 4px;

    &__search {
        width: 100%;
        border: 1px solid #D5D5D5;
        border-radius: 4px;
        display: flex;
        align-items: center;

        &-icon {
            margin-left: 13px;
        }

        &-input {
            width: 80%;
            height: 36px;
            padding: 10px 12px;
            border: none;
            outline: none;
            border-radius: 4px;
        }
    }

}
</style>