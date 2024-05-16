<template>
  <div class="ourteam-section">
    <div class="ourteam-section__info">
      <h1 class="title">OUR TEAM</h1>
      <p class="descr">
        Empire FBA Prep services provide reliable Amazon FBA packaging and Prep
        services Ontario, California, Toronto, and Canada. Packaging is
        imperative to making a huge first impression with customers.
      </p>
    </div>
    <div class="ourteam-section__people">
      <div class="ourteam-section__people-item">
        <img src="../assets/img/ourteam/Larry.png" />
        <h2 class="name">Larry Stuber</h2>
        <p class="profession">East Coast Account Manager</p>
      </div>
      <div class="ourteam-section__people-item">
        <img src="../assets/img/ourteam/John.png" />
        <h2 class="name-second">John Soos</h2>
        <p class="profession-second">Chief Operating Officer</p>
      </div>
      <div class="ourteam-section__people-item">
        <img src="../assets/img/ourteam/Nima.png" />
        <h2 class="name">Nima Hassanpour</h2>
        <p class="profession">President</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ourTeamComponent",
};
</script>

<style lang="scss" scoped>
.ourteam-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  &__info {
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    .title {
      font-size: 40px;
      font-weight: 700;
      font-family: "Poppins";
      line-height: 60px;
      color: #ffffff;
      margin-top: 85px;
    }
    .descr {
      font-size: 16px;
      font-weight: 500;
      font-family: "Lato";
      line-height: 26px;
      color: #ffffff;
      margin-top: 17px;
      max-width: 725px;
    }
  }
  &__people {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    margin-top: 51px;
    gap: 0 7px;
  }
  &__people-item {
    text-align: center;
    width: 362px;
    height: 354px;
    border-radius: 10px;
    background: #ffffff;
    &:first-child {
      background: none;
    }
    &:last-child {
      background: none;
    }
    img {
      margin-top: 43px;
      pointer-events: none;
    }
    .name {
      font-size: 18px;
      font-weight: 700;
      font-family: "Poppins";
      line-height: 25px;
      color: #ffffff;
      text-transform: uppercase;
    }
    .name-second {
      color: #313131;
      font-size: 18px;
      font-weight: 700;
      font-family: "Poppins";
      line-height: 25px;
      text-transform: uppercase;
      margin-top: 22px;
    }
    .profession {
      font-size: 16px;
      font-weight: 500;
      font-family: "Poppins";
      line-height: 25px;
      color: #ffffff;
      text-transform: uppercase;
    }
    .profession-second {
      font-size: 16px;
      font-weight: 500;
      font-family: "Poppins";
      line-height: 25px;
      color: #ef7b3e;
      text-transform: uppercase;
      margin-top: 7px;
    }
  }
}
</style>