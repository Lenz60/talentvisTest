<template>
  <div>
    <div class="flex flex-col">
      <div class="flex flex-col justify-center items-center">
        <!--* Title for the web  -->
        <div class="flex flex-row">
          <h1 class="text-[50px] font-medium text-primary pt-2">Green</h1>
          <h1 class="text-[50px] font-medium text-neutral-content pt-2 pl-2">
            Aquatic Shop
          </h1>
        </div>
        <h3 class="p-2 text-md font-sans text-secondary">
          Get your aquatic plants for your aquascape
        </h3>
      </div>
      <div class="m-5 rounded-md bg-base-200 flex flex-col">
        <!--* Row1 of the product  -->
        <div class="flex flex-row">
          <div
            class="w-[300px] rounded-md hover:bg-primary-content hover:-translate-y-1 flex flex-col justify-center items-center p-2 m-2"
          >
            <h1 class="font-semibold text-neutral-content p-2">
              Rotala Ramosior Florida
            </h1>
            <img
              class="w-[250px] h-[250px] rounded-md"
              src="https://cdn.shopify.com/s/files/1/0230/7266/9773/files/2hrAquaristDSCF0491_1024x1024.jpg"
              alt=""
            />
            <h3 class="font-semibold p-1 text-primary">$25</h3>
            <CartButton></CartButton>
          </div>
          <div
            class="w-[300px] flex flex-col justify-center items-center p-2 m-2 hover:bg-primary-content hover:-translate-y-1 rounded-md"
          >
            <h1 class="font-semibold p-2 text-neutral-content">
              Rotala Macrandra "Butterfly"
            </h1>
            <img
              class="w-[250px] h-[250px] rounded-md"
              src="https://www.uscape.de/media/image/65/c1/ae/rotala-macrandra-mini-butterfly-aquarienpflanze.jpg"
              alt=""
            />
            <h3 class="font-semibold p-1 text-primary">$20</h3>
            <CartButton></CartButton>
          </div>
          <div
            class="w-[300px] flex flex-col justify-center items-center p-2 m-2 hover:bg-primary-content hover:-translate-y-1 rounded-md"
          >
            <h1 class="font-semibold p-2 text-neutral-content">
              Rotala Blood Red SG
            </h1>
            <img
              class="w-[250px] h-[250px] rounded-md"
              src="https://himadriaquatics.b-cdn.net/wp-content/uploads/2022/09/118574.jpg"
              alt=""
            />
            <h3 class="font-semibold p-1 text-primary">$10</h3>
            <CartButton></CartButton>
          </div>
          <div
            class="w-[300px] flex flex-col justify-center items-center p-2 m-2 hover:bg-primary-content hover:-translate-y-1 rounded-md"
          >
            <h1 class="font-semibold p-2 text-neutral-content">
              Rotala Rotundifolia Red
            </h1>
            <img
              class="w-[250px] h-[250px] bg-clip-border rounded-md"
              src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRbeiqQWYuZ6vfXDsf2RMUW9ytxEM-0uos3vQQx_XLPu4Pet5w2R5igtlfFlfXBWlWPk_k&usqp=CAU"
              alt=""
            />
            <h3 class="font-semibold p-1 text-primary">$10</h3>
            <CartButton></CartButton>
          </div>
        </div>
        <!--* Row 2 of the product-->
        <div class="flex flex-row">
          <div
            class="w-[300px] flex flex-col justify-center items-center p-2 m-2 hover:bg-primary-content hover:-translate-y-1 rounded-md"
          >
            <h1 class="font-semibold p-2 text-neutral-content">
              Hygrophila sp Chai
            </h1>
            <img
              class="w-[250px] h-[250px] rounded-md"
              src="https://media.karousell.com/media/photos/products/2021/12/7/hygrophilia_sp_chai_1638849919_d85e7c82_progressive.jpg"
              alt=""
            />
            <h3 class="font-semibold p-1 text-primary">$700</h3>
            <CartButton></CartButton>
          </div>
          <div
            class="w-[300px] flex flex-col justify-center items-center p-2 m-2 hover:bg-primary-content hover:-translate-y-1 rounded-md"
          >
            <h1 class="font-semibold p-2 text-neutral-content">
              Ludwigia Glandulosa
            </h1>
            <img
              class="w-[250px] h-[250px] rounded-md"
              src="https://down-id.img.susercontent.com/file/f698528700e4bf4168bba49d05dc7c20"
              alt=""
            />
            <h3 class="font-semibold p-1 text-primary">$20</h3>
            <CartButton></CartButton>
          </div>
          <div
            class="w-[300px] flex flex-col justify-center items-center p-2 m-2 hover:bg-primary-content hover:-translate-y-1 rounded-md"
          >
            <h1 class="font-semibold p-2 text-neutral-content">
              Persicaria Maculosa (sao Paolo)
            </h1>
            <img
              class="w-[250px] h-[250px] rounded-md"
              src="https://www.aquariumgallery.com.au/cdn/shop/files/fa931cdb44d698cf44ad0ccb3e89.jpg"
              alt=""
            />
            <h3 class="font-semibold p-1 text-primary">$60</h3>
            <CartButton></CartButton>
          </div>
          <div
            class="w-[300px] flex flex-col justify-center items-center p-2 m-2 hover:bg-primary-content hover:-translate-y-1 rounded-md"
          >
            <h1 class="font-semibold p-2 text-neutral-content">
              Alternanthera Reineckii Rosanervig
            </h1>
            <img
              class="w-[250px] h-[250px] rounded-md"
              src="https://i.ebayimg.com/images/g/UAYAAOSwz1hjm~T0/s-l1600.jpg"
              alt=""
            />
            <h3 class="font-semibold p-1 text-primary">$50</h3>
            <CartButton></CartButton>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CartButton from "../components/Button.vue";
export default {
  components: {
    CartButton,
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped></style>
