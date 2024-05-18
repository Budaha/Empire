<template>
  <div class="contacts">
    <div class="address" v-for="(contact, index) in contacts" :key="index">
      <img class="address__img" :src="contact.img" />
      <p class="address__text">{{ contact.description }}</p>
    </div>
    <button class="btn">Book Now</button>
  </div>
</template>

<script>
import { ref } from "vue";
import address from "../assets/img/header/address.png";
import email from "../assets/img/header/email.png";
import phone from "../assets/img/header/phone.png";
export default {
  name: "headerComponent",
  setup() {
    const contacts = ref([
      {
        id: 1,
        img: address,
        description: "California: 4010 Valley Blvd Ste 108, Walnut, CA 91789",
      },
      {
        id: 2,
        img: email,
        description: "info@empireprepservices.com",
      },
      {
        id: 3,
        img: phone,
        description: "1 (877) 618-0069",
      },
    ]);
    return {
      contacts,
    };
  },
};
</script>

<style lang="scss" scoped>
.contacts {
  display: flex;
  justify-content: flex-end;
}
.address {
  display: flex;
  gap: 9px;
  align-items: center;
  margin-right: 25px;
  cursor: pointer;
  &:first-child {
    margin-right: 39px;
  }
  &__text {
    font-weight: 400;
    font-size: 16px;
    line-height: 19.2px;
    color: #313131;
    font-family: "Lato";
    //   &:last-child {
    //   font-weight: 600;
    // }
  }
  &__img {
    width: 15px;
    height: 15px;
  }
}
.btn {
  cursor: pointer;
  width: 161px;
  height: 45px;
  border-radius: 35px;
  background: #ef7b3e;
  border: none;
  margin-left: 15px;
  margin-right: 146px;
  margin-top: 4px;
  color: #ffffff;
  font-weight: 600;
  font-size: 16px;
  line-height: 10px;
  font-family: "Poppins";
}
</style>