<template>
    <div class="brand-filter">
        <BaseHeaderFilter :title="'Бренд'" :filter-id="'brand-filter'" :need-cleaned="true" />
        <div class="brand-filter__search">
            <SearchIcon2 class="brand-filter__search-icon" />
            <input v-model="value" class="brand-filter__search-input" type="text" placeholder="Поиск" >
            <CrossInCircleIcon v-if="value" class="brand-filter__clean-icon" @click.native="clean" />
        </div>
        <BaseList></BaseList>
    </div>
</template>

<script>
import SearchIcon2 from '../icons/SearchIcon2.vue';
import BaseHeaderFilter from '../base/BaseHeaderFilter.vue';
import BaseList from '../base/BaseList.vue';
import CrossInCircleIcon from '../icons/CrossInCircleIcon.vue';

export default {
    name: 'BrandFilter',
    components: {
        SearchIcon2,
        BaseHeaderFilter,
        BaseList,
        CrossInCircleIcon,
    },
    data() {
        return {
            value: '',
        }
    },

    methods: {
        clean() {
            this.value = '';
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

    &__clean-icon {
        cursor: pointer;
    }
}
</style>