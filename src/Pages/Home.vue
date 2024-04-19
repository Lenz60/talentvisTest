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
          <!--* Loop the plants array and limit the display from 1st item to 4th item  -->
          <div v-for="plant in Plants.slice(0, 4)">
            <div
              class="w-[300px] rounded-md hover:bg-primary-content hover:-translate-y-1 flex flex-col justify-center items-center p-2 m-2"
            >
              <h1 class="font-semibold text-neutral-content p-2">
                {{ plant.name }}
              </h1>
              <img
                class="w-[250px] h-[250px] rounded-md"
                :src="plant.images"
                alt=""
              />
              <h3 class="font-semibold p-1 text-primary">{{ plant.price }}</h3>
              <!--* Check the state of the button  -->
              <!--* if loadingButton is true, then display loading button with disabled button  -->
              <!--* if loadingButton is false, then display add to cart button  -->
              <div v-if="loadingButton">
                <button
                  class="btn btn-primary rounded-lg"
                  :disabled="loadingButton"
                >
                  <span class="loading loading-spinner"></span>
                  loading..
                </button>
              </div>
              <div v-else>
                <button
                  class="btn btn-primary rounded-lg"
                  @click="addCart(plant.name, plant.price)"
                >
                  Add to cart
                </button>
              </div>
            </div>
          </div>
        </div>
        <!--* Row 2 of the product-->
        <div class="flex flex-row">
          <!--* Loop the plants array and limit the display from 4th item to 8th item  -->
          <div v-for="plant in Plants.slice(4, 8)">
            <div
              class="w-[300px] rounded-md hover:bg-primary-content hover:-translate-y-1 flex flex-col justify-center items-center p-2 m-2"
            >
              <h1 class="font-semibold text-neutral-content p-2">
                {{ plant.name }}
              </h1>
              <img
                class="w-[250px] h-[250px] rounded-md"
                :src="plant.images"
                alt=""
              />
              <h3 class="font-semibold p-1 text-primary">{{ plant.price }}</h3>
              <div v-if="loadingButton">
                <button
                  class="btn btn-primary rounded-lg"
                  :disabled="loadingButton"
                >
                  <span class="loading loading-spinner"></span>
                  loading..
                </button>
              </div>
              <div v-else>
                <button
                  class="btn btn-primary rounded-lg"
                  @click="addCart(plant.name, plant.price)"
                >
                  Add to cart
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CartButton from "../components/Button.vue";
import { ref } from "vue";
export default {
  components: {
    CartButton,
  },
  setup() {
    const loadingButton = ref(false);
    const Plants = [
      {
        name: "Rotala Ramosior Florida",
        images:
          "https://cdn.shopify.com/s/files/1/0230/7266/9773/files/2hrAquaristDSCF0491_1024x1024.jpg",
        price: "$30",
      },
      {
        name: "Rotala Macrandra 'Butterfly'",
        images:
          "https://www.uscape.de/media/image/65/c1/ae/rotala-macrandra-mini-butterfly-aquarienpflanze.jpg",
        price: "$35",
      },
      {
        name: "Rotala Blood Red SG",
        images:
          "https://himadriaquatics.b-cdn.net/wp-content/uploads/2022/09/118574.jpg",
        price: "$50",
      },
      {
        name: "Rotala Rotundifolia Red",
        images:
          "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRbeiqQWYuZ6vfXDsf2RMUW9ytxEM-0uos3vQQx_XLPu4Pet5w2R5igtlfFlfXBWlWPk_k&usqp=CAU",
        price: "$15",
      },
      {
        name: "Hygrophila sp Chai",
        images:
          "https://media.karousell.com/media/photos/products/2021/12/7/hygrophilia_sp_chai_1638849919_d85e7c82_progressive.jpg",
        price: "$100",
      },
      {
        name: "Ludwigia Glandulosa",
        images:
          "https://down-id.img.susercontent.com/file/f698528700e4bf4168bba49d05dc7c20",
        price: "$10",
      },
      {
        name: "Persicaria Maculosa (Sao Paolo)",
        images:
          "https://www.aquariumgallery.com.au/cdn/shop/files/fa931cdb44d698cf44ad0ccb3e89.jpg",
        price: "$40",
      },
      {
        name: "Alternanthera Reineckii Rosanervig",
        images: "https://i.ebayimg.com/images/g/UAYAAOSwz1hjm~T0/s-l1600.jpg",
        price: "$20",
      },
    ];

    return { Plants, loadingButton };
  },
  methods: {
    addCart(name, price) {
      //Change the state of the button to loading
      this.loadingButton = !this.loadingButton;
      // Delay 3 seconds to be able to see the loading indicator in the button cart
      const delayInMilliseconds = 3000; //3 second

      setTimeout(() => {
        const answer = window.confirm(
          "Are you sure want to add " + name + " to the cart?"
        );
        if (answer) {
          this.loadingButton = !this.loadingButton;
          // console.log("yes");
          alert(name + " added to cart");
        } else {
          // console.log("no");
          this.loadingButton = !this.loadingButton;
        }
        //After the answer is satisfied, change back the state of button to default
      }, delayInMilliseconds);
    },
  },
};
</script>

<style lang="scss" scoped></style>
