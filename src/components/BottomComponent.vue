<template>
  <div class="bottom-section">
    <div class="bottom-section__item">
      <p class="left">Terms & Conditions</p>
    </div>
    <div class="bottom-section__item">
      <p class="right">
        Copyright Notice: © 2022 | All Rights Reserved. Empire Prep Services
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "bottomComponent",
};
</script>

<style lang="scss" scoped>
.bottom-section {
  display: flex;
  justify-content: space-between;
  padding-top: 14px;
  @media (max-width: 768px) {
    flex-direction: column;
    align-items: center;
  }
  &__item {
    .left {
      padding-left: 147px;
      @media (max-width: 1024px) {
        padding-left: 15px;
      }
    }
    .right {
      padding-right: 152px;
      @media (max-width: 1024px) {
        padding-right: 15px;
      }
      @media (max-width: 768px) {
        padding-top: 10px;
      }
    }
    p {
      font-family: "Lato";
      font-size: 14px;
      font-weight: 700;
      line-height: 16.8px;
      color: #ffffff;
      pointer-events: none;
      user-select: none;
    }
  }
}
</style>