<template>
    <div class="sidebar-container">
        <CategoriesList />
        <PriceFilter />
        <BrandFilter />
        <SizeFilter />
    </div>
</template>

<script>
import PriceFilter from "@/components/filters/PriceFilter.vue";
import BrandFilter from "./filters/BrandFilter.vue";
import SizeFilter from "./filters/SizeFilter.vue";
import CategoriesList from "./categories/CategoriesList.vue";

export default {
    name: "SidebarComponent",
    components: {
        PriceFilter,
        BrandFilter,
        SizeFilter,
        CategoriesList,
    },
}
</script>

<style lang="scss" scoped>
.sidebar-container {
    width: 280px;
    height: 100%;
    background-color: var(--color-white);
    display: flex;
    flex-direction: column;
    gap: 28px;
}

@media screen and (max-width: 500px) {
    .sidebar-container {
        display: none;
    }
}
</style>