<template>
  <div class="home">
    <h2 class="home__category-title">Название категории</h2>

    <SidebarComponent />

    <div class="cards-list">
      <ProductCardItem v-for="(item, index) in productItems" :product-item="item" :key="index"
        class="cards-list__card" />
    </div>

  </div>
</template>

<script>
import SidebarComponent from '@/components/SidebarComponent.vue';
import ProductCardItem from '@/components/ProductCardItem.vue';


export default {
  name: 'MainPageView',
  components: {
    SidebarComponent,
    ProductCardItem,
  },
  data() {
    return {
      productItems: [
        {
          id: 1,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: true,
        },
        {
          id: 2,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: true,
        },
        {
          id: 3,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: false,
        },
        {
          id: 4,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: true,
        },
        {
          id: 5,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: true,
        },
        {
          id: 6,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: true,
        },
        {
          id: 7,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: true,
        },
        {
          id: 8,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: true,
        },
        {
          id: 9,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: true,
        },
        {
          id: 10,
          brand: "Бренд",
          new_price: 5999,
          old_price: 5999,
          description: "Полное название товара в несколько строк для вида с обрывом в конце...",
          image: "",
          in_stock: true,
        }
      ],
    }
  }
}
</script>


<style lang="scss" scoped>
.home {
  width: calc(100% - 200px);
  height: calc(100% - 96px);
  margin: 0 auto;
  padding-bottom: 36px;
  display: flex;
  justify-content: space-between;

  .cards-list {
    height: 100%;
    width: calc(100% - 316px);
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(3, 1fr);
    grid-column-gap: 24px;
    grid-row-gap: 24px;

  }

  &__category-title {
    display: none;
  }
}


@media screen and (max-width: 500px) {
  .home {
    width: calc(100% - 32px);
    display: flex;
    flex-direction: column;

    .cards-list {
      height: 100%;
      width: 100%;
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      grid-template-rows: repeat(3, 1fr);
      grid-column-gap: 24px;
      grid-row-gap: 24px;
    }

    &__category-title {
      display: block;
      font-size: 22px;
      font-weight: 400;
      line-height: 28px;
      margin-bottom: 12px;

    }
  }
}
</style>
