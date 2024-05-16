<template>
  <div class="contacts">
    <div class="address">
      <img src="../assets/img/header/address.png" />
      <p class="address__text">
        California: 4010 Valley Blvd Ste 108, Walnut, CA 91789
      </p>
    </div>
    <div class="email">
      <img src="../assets/img/header/email.png" />
      <p class="email__text">info@empireprepservices.com</p>
    </div>
    <div class="phone">
      <img src="../assets/img/header/phone.png" />
      <p class="phone__text">1 (877) 618-0069</p>
    </div>
    <button class="btn">Book Now</button>
  </div>
</template>

<script>
export default {
  name: "headerComponent",
};
</script>

<style lang="scss" scoped>
.contacts {
  display: flex;
  justify-content: flex-end;
}
.address {
  display: flex;
  gap: 8px;
  align-items: center;
  margin-right: 40px;
  cursor: pointer;
  &__text {
    font-weight: 400;
    font-size: 16px;
    line-height: 19.2px;
    color: #313131;
    font-family: "Lato";
  }
}
.email {
  display: flex;
  gap: 8px;
  align-items: center;
  margin-right: 25px;
  cursor: pointer;
  &__text {
    font-weight: 400;
    font-size: 16px;
    line-height: 19.2px;
    color: #313131;
    font-family: "Lato";
  }
}
.phone {
  display: flex;
  align-items: center;
  margin-right: 40px;
  gap: 8px;
  cursor: pointer;
  &__text {
    font-weight: 600;
    font-size: 16px;
    line-height: 19.2px;
    color: #313131;
    font-family: "Lato";
  }
}
img {
  width: 15px;
  height: 15px;
}
.btn {
  cursor: pointer;
  width: 161px;
  height: 45px;
  border-radius: 35px;
  background: #ef7b3e;
  border: none;
  margin-right: 146px;
  margin-top: 4px;
  color: #ffffff;
  font-weight: 600;
  font-size: 16px;
  line-height: 10px;
  font-family: "Poppins";
}
</style>