<template>
  <div class="stages-section">
    <div
      class="stages-section__block"
      v-for="(block, index) in blocks"
      :key="index"
    >
      <h1 class="stages-section__title">{{ block.title }}</h1>
      <p class="stages-section__descr">{{ block.description }}</p>
      <p class="stages-section__text">{{ block.text }}</p>
      <button class="btn">SEND A SHIPMENT FORM</button>
    </div>
    <div class="stages-section__item">
      <div class="el" v-for="(item, index) in items" :key="index">
        <img :src="item.img" />
        <h2 class="title">{{ item.title }}</h2>
        <p class="descr">
          {{ item.description }}
        </p>
        <img
          v-if="index === 0"
          :class="`arrow arrow--${index + 1}`"
          src="../assets/img/stages/fourStages.png"
        />
        <img
          v-if="index === 1"
          :class="`arrow arrow--${index + 1}`"
          src="../assets/img/stages/fiveStages.png"
        />
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import firstStages from "../assets/img/stages/firstStages.png";
import secondStages from "../assets/img/stages/secondStages.png";
import threeStages from "../assets/img/stages/threeStages.png";
export default {
  name: "stagesComponent",
  setup() {
    const blocks = ref([
      {
        id: 1,
        title: "GET STARTED FOR AS LOW AS $0.50",
        description:
          "How it works: Complete our service request form and provide all the required details.",
        text: "Once you are ready, send your products and custom packaging directly from your manufacturer or wholesaler to one of our three prep centers. Create an abbreviated shipping plan and grant Empire FBA Prep Services limited secure access via the Assistant Account on Amazon.",
      },
    ]);
    const items = ref([
      {
        id: 1,
        title: "CREATE AN ABBREVITED SHIPPING PLAN",
        description:
          "Create a new shipping plan in Seller Central. List the products you are sending along with quantities and then you are done!",
        img: firstStages,
      },
      {
        id: 2,
        title: "SEND US YOUR INSTRUCTION",
        description:
          "Complete our service request form with detailed instructions or anything special you’d like for us to do.",
        img: secondStages,
      },
      {
        id: 3,
        title: "WE’LL TAKE IT FROM THERE",
        description:
          "Using your input our experts will carefully prepare your shipment start to finish with impeccable care and attention to detail.",
        img: threeStages,
      },
    ]);
    return {
      items,
      blocks,
    };
  },
};
</script>

<style lang="scss" scoped>
.stages-section {
  &__block {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 168px;
  }
  &__title {
    text-transform: uppercase;
    font-size: 40px;
    font-weight: 700;
    font-family: "Poppins";
    line-height: 53px;
    text-align: center;
    color: #313131;
  }
  &__descr {
    font-weight: 600;
    font-size: 18px;
    line-height: 25px;
    text-align: center;
    font-family: "Poppins";
    color: #2e2e2e;
    margin-top: 14px;
  }
  &__text {
    max-width: 1000px;
    margin-top: 13px;
    font-weight: 400;
    font-size: 16px;
    line-height: 23px;
    font-family: "Lato";
    text-align: center;
    color: #2e2e2e;
  }
  .btn {
    width: 247px;
    height: 45px;
    border-radius: 35px;
    border: none;
    font-weight: 600;
    font-size: 16px;
    line-height: 24px;
    background: #ef7b3e;
    color: #ffffff;
    margin-top: 28px;
    cursor: pointer;
  }
  &__item {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 0 119px;
    margin-top: 67px;
    max-width: 1100px;
    margin-left: auto;
    margin-right: auto;
    position: relative;
    .el {
      text-align: center;
      z-index: 1;
      max-width: 250px;
      padding-left: 20px;
      &:first-child {
        max-width: 230px;
        padding-left: 40px;
      }
      img {
        pointer-events: none;
      }
      .title {
        font-size: 18px;
        font-weight: 700;
        line-height: 25px;
        color: #000000;
        font-family: "Poppins";
        margin-top: 28px;
      }
      .descr {
        font-size: 16px;
        font-weight: 400;
        line-height: 22px;
        color: #515151;
        font-family: "Lato";
        margin-top: 8px;
      }
    }
    .arrow {
      max-width: 294px;
      height: 39px;
      text-align: center;
      z-index: 2;
      position: absolute;
      pointer-events: none;
      display: none;
      &--1 {
        display: flex;
        left: 217px;
        top: 11px;
      }
      &--2 {
        display: flex;
        right: 210px;
        top: 50px;
      }
    }
  }
}
</style>