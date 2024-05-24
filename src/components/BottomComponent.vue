<template>
  <div class="bottom-section">
    <div class="bottom-section__grid">
      <p>Terms & Conditions</p>
      <p>
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
  justify-content: center;
  &__grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 0 285px;
    margin-top: 13px;
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