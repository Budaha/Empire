<template>
  <div class="home-section">
    <img class="firstImg" src="../assets/img/home/firsHomeImg.png" />
    <div class="home-section__block">
      <div class="home-section__info">
        <h1 class="home-section__title">
          Empire <span>FBA</span> Prep Services In USA
        </h1>
        <p class="home-section__text">
          USA & Canada specializes in providing world class prep solutions for
          your Amazon FBA business.
        </p>
        <button class="home-section__btn">Contact Us</button>
      </div>
      <div class="home-section__picture">
        <img
          class="home-section__picture"
          src="../assets/img/home/secondHomeImg.png"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "homeComponent",
};
</script>

<style lang="scss" scoped>
.home-section {
  position: relative;
  .firstImg {
    position: absolute;
    margin-left: -240px;
    pointer-events: none;
    @media(max-width: 1440px) {
      display: none;
    }
  }
  &__block {
    display: flex;
    @media(max-width: 768px) {
      flex-direction: column;
    }
  }
  &__info {
    max-width: 600px;
    margin-left: 145px;
    @media(max-width: 1440px) {
      margin-left: 100px;
      @media(max-width: 1200px) {
        margin-left: 0;
      }
    }
  }
  &__title {
    padding-top: 174px;
    font-size: 80px;
    font-weight: 800;
    font-family: "Poppins";
    line-height: 77px;
    text-transform: uppercase;
    color: #ffffff;
    @media(max-width: 1200px) {
      font-size: 60px;
      line-height: 65px;
    }
    @media(max-width: 1024px) {
      font-size: 40px;
      line-height: 45px;
    }
    @media(max-width: 768px) {
      padding-top: 100px;
    }
    span {
      text-decoration: underline;
      text-underline-offset: 7px;
      text-decoration-thickness: 4px;
    }
  }
  &__text {
    max-width: 560px;
    margin-top: 7px;
    font-size: 16px;
    font-weight: 500;
    line-height: 24px;
    font-family: "Poppins";
    color: #ffffff;
  }
  &__btn {
    margin-top: 26px;
    margin-left: 2px;
    width: 161px;
    height: 45px;
    border-radius: 35px;
    border: none;
    background: #ffffff;
    cursor: pointer;
    color: #ef7b3e;
    font-size: 16px;
    font-weight: 600;
    font-family: "Poppins";
    line-height: 24px;
  }
  button:hover {
    background: #515151;
  }
  &__picture {
    @media(max-width: 1200px) {
      padding-top: 45px;
    }
    @media(max-width: 768px) {
      display: flex;
      justify-content: center;
    }
    img {
      position: absolute;
      padding-left: 130px;
      margin-top: -7px;
      user-select: none;
      pointer-events: none;
      @media(max-width: 1440px) {
        position:static;
        padding-left: 50px;
      }
      @media(max-width: 1200px) {
        max-width: 500px;
      }
      @media(max-width: 1024px) {
        max-width: 400px;
      }
      @media(max-width: 768px) {
        max-width: 350px;
      }
    }
  }
}
</style>