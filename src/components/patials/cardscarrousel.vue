<script>
export default {
  data() {
    return {
      
      slides: [
        {
          imgSrc: "img/04-768x768.jpg",
          discount: "-44%",
          vote: "4",
          productName: "Sony DualShock 4 V2",
          fullPrice: "£ 180.00",
          discountedPrice: "£ 100.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/09-768x768.jpg",
          vote: "0",
          productName: "Avermedia LIVE Micro AEGIS",
          discountedPrice: "£ 83.00 - £ 90.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/03-768x768.jpg",
          discount: "-10%",
          vote: "3",
          productName: "Gaming Mouse Pad Black-Red",
          fullPrice: "£ 20.00",
          discountedPrice: "£ 18.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/11-768x768.jpg",
          vote: "2",
          productName: "Sony DualShock 4 V1",
          fullPrice: "£ 50.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/02-768x768.jpg",
          vote: "5",
          productName: "Microsoft Xbox One Stereo Headset",
          fullPrice: "£ 70.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/05-768x768.jpg",
          discount: "-10%",
          vote: "3",
          productName: "Oculus Rift",
          fullPrice: "£ 400.00",
          discountedPrice: "£ 360.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/06-768x768.jpg",
          discount: "-30%",
          vote: "3",
          productName: "Sony Z1R",
          fullPrice: "£ 2300.00",
          discountedPrice: "£ 16100.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/07-768x768.jpg",
          vote: "3",
          productName: "Etichette Adesive per PS4 controller",
          fullPrice: "£ 10.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/08-768x768.jpg",
          vote: "3",
          productName: "Etichette Adesive per PS4 controller",
          fullPrice: "£ 10.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/10-768x768.jpg",
          vote: "2",
          productName: "Controller Generico SNES",
          fullPrice: "£ 20.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/12-768x768.jpg",
          discount: "-50%",
          vote: "3",
          productName: "Sony MDR-1ABT",
          fullPrice: "£ 2600.00",
          discountedPrice: "£ 1300.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },
        {
          imgSrc: "img/13-768x768.jpg",
          vote: "3",
          productName: "Etichette Adesive per Xbox One controller",
          fullPrice: "£ 10.00",
          activeButtons: [],
          buttons: [
            { icon: "fa-bag-shopping", index: 0 },
            { icon: "fa-heart", index: 1 },
            { icon: "fa-maximize", index: 2 },
            { icon: "fa-eye", index: 3 },
          ],
        },

      ],
    };
  },
  methods: {
    setActiveButton(index, slide) {
      if (slide.activeButtons.includes(index)) {
        slide.activeButtons = slide.activeButtons.filter((i) => i !== index);
      } else {
        slide.activeButtons.push(index);
      }
    },
  },
};
</script>

<template>
  <div class="container">
    <swiper :slidesPerView="4" class="mySwiper">
      <swiper-slide v-for="(slide, index) in slides" :key="index">
        <div class="card">
          <img :src="slide.imgSrc" alt="" />
          <div v-if="slide.discount" class="paralelogramo">
            <p>{{ slide.discount }}</p>
          </div>
          <div class="info">
            <div class="stars">
              <i v-for="n in 5" :key="n" :class="['fa-solid fa-star', slide.vote >= n ? 'filled' : 'empty']"></i>
            </div>
            <p>{{ slide.productName }}</p>
            <div class="price">
              <p class="fullprice">{{ slide.fullPrice }}</p>
              <p class="discount">{{ slide.discountedPrice }}</p>
            </div>
            <div class="options">
              <button
                v-for="button in slide.buttons"
                :key="button.index"
                type="button"
                class="custom-button"
                :class="{ 'btn-color': slide.activeButtons.includes(button.index) }"
                @click="setActiveButton(button.index, slide)"
              >
                <i class="fa-solid" :class="button.icon"></i>
              </button>
            </div>
          </div>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<style lang="scss" scoped>
@import '../../scss/partials/vars';
swiper {
  width: 100%;
  height: 100%;
  display: flex;
  gap: 15px;
  overflow:auto;

  swiper-slide {
    text-align: center;
    font-size: 18px;
    display: flex;
    justify-content: center;
    align-items: center;
    width: calc(100% / 4 - 10px);
  }
}

.container {
  margin: 50px auto;

  .card {
    background-color: #22162e;
    position: relative;
    margin-bottom: 40px;
    img {
      width: 100;
    }
    .paralelogramo {
      position: absolute;
      margin: 5%;
      width: 50px;
      height: 30px;
      background-color: $yellow-color;
      transform: skew(-14deg);
      margin-bottom: 20px;

      p {
        position: absolute;
        transform: skew(14deg);
        color: black;
        font-size: 15px;
        font-weight: bold;
        width: 100%;
        text-align: center;
        top: 50%;
        transform: translateY(-50%);
      }
    }

    .info {
      text-align: start;
      color: white;
      background-color: darken($purple-color, 2%);
      height: 120px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      .stars{
        padding-left: 15px;
        padding-top: 5px;
      }
      .fa-star {
        color: grey;
        font-size: 11px;
      }

      .filled {
        color: $yellow-color;
      }

      .empty {
        color: grey;
      }

      .price {
        display: flex;

        .discount {
          color: $yellow-color;
        }
      }

      p {
        height: 30px;
        padding-left: 15px;
        margin: 0;
      }


      .options {
        display: none;

        .custom-button {
          border-radius: 0;
          border: 1px solid black;
          background: none;
          color: white;
          width: calc(100% / 4);
          height: 30px;
        }

        .btn-color {
          color: $yellow-color;
        }
      }
    }

    &:hover .options {
      display: block;
    }

    &:hover .price {
      display: none;
    }
  }
}
</style>