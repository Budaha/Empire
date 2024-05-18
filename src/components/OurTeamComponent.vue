<template>
  <div class="ourteam-section">
    <div
      class="ourteam-section__info"
      v-for="(info, index) in infos"
      :key="index"
    >
      <h1 class="title">{{ info.title }}</h1>
      <p class="descr">{{ info.description }}</p>
    </div>
    <div class="ourteam-section__people">
      <div
        class="ourteam-section__people-item"
        v-for="(people, index) in peoples"
        :key="index"
      >
        <img :src="people.img" />
        <h2 class="name">{{ people.name }}</h2>
        <p class="profession">{{ people.profession }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
import Larry from "../assets/img/ourteam/Larry.png";
import John from "../assets/img/ourteam/John.png";
import Nima from "../assets/img/ourteam/Nima.png";
export default {
  name: "ourTeamComponent",
  setup() {
    const infos = ref([
      {
        id: 1,
        title: "OUR TEAM",
        description:
          "Empire FBA Prep services provide reliable Amazon FBA packaging and Prep services Ontario, California, Toronto, and Canada. Packaging is imperative to making a huge first impression with customers.",
      },
    ]);
    const peoples = ref([
      {
        id: 1,
        img: Larry,
        name: "Larry Stuber",
        profession: "East Coast Account Manager",
      },
      {
        id: 2,
        img: John,
        name: "John Soos",
        profession: "Chief Operating Officer",
      },
      {
        id: 3,
        img: Nima,
        name: "Nima Hassanpour",
        profession: "President",
      },
    ]);
    return {
      infos,
      peoples,
    };
  },
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