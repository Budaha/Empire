<template>
  <div class="stages-section">
    <div class="stages-section__block">
      <h1 class="stages-section__title">GET STARTED FOR AS LOW AS $0.50</h1>
      <p class="stages-section__descr">
        How it works: Complete our service request form and provide all the
        required details.
      </p>
      <p class="stages-section__text">
        Once you are ready, send your products and custom packaging directly
        from your manufacturer or wholesaler to one of our three prep centers.
        Create an abbreviated shipping plan and grant Empire FBA Prep Services
        limited secure access via the Assistant Account on Amazon.
      </p>
      <button class="btn">SEND A SHIPMENT FORM</button>
    </div>
    <div class="stages-section__item">
      <div class="el">
        <img src="../assets/img/stages/firstStages.png" />
        <h2 class="title">CREATE AN ABBREVITED SHIPPING PLAN</h2>
        <p class="descr">
          Create a new shipping plan in Seller Central. List the products you
          are sending along with quantities and then you are done!
        </p>
      </div>
      <img class="arrow arrow--1" src="../assets/img/stages/fourStages.png" />
      <div class="el">
        <img src="../assets/img/stages/secondStages.png" />
        <h2 class="title">SEND US YOUR INSTRUCTION</h2>
        <p class="descr">
          Complete our service request form with detailed instructions or
          anything special you’d like for us to do.
        </p>
      </div>
      <img class="arrow arrow--2" src="../assets/img/stages/fiveStages.png" />
      <div class="el">
        <img src="../assets/img/stages/threeStages.png" />
        <h2 class="title">WE’LL TAKE IT FROM THERE</h2>
        <p class="descr">
          Using your input our experts will carefully prepare your shipment
          start to finish with impeccable care and attention to detail.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "stagesComponent",
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
      &--1 {
        left: 217px;
        top: 11px;
      }
      &--2 {
        right: 210px;
        top: 50px;
      }
    }
  }
}
</style>