<template>
  <form @submit.prevent="onPostClick">
    <div class="wrapper">
      <div class="headline">
        <router-link to="/">
          <img src="@/assets/logo.png" alt="logo" class="company-logo">
        </router-link>
        <h2>Password Reset</h2>
        <p>Enter New Password for {{ForgotPasswordFormData.email}}</p>
      </div>
      <div class="form">
        <div class="signup">

          <div class="has-addons">
            <input v-if="showPassword2"  required="required" type="text"  class="input-form-1 password" v-model="newPassword"   placeholder="Enter New Password"   />
            <input v-else type="password" required="required"  class="input-form-1 password" v-model="newPassword"   placeholder="Enter New Password"   >
            <div class="space" @click="toggleShow2">
              <i class="fas" :class="{ 'fa-eye-slash': showPassword2, 'fa-eye': !showPassword2 }" ></i>
            </div>
          </div>

          <div class="has-addons">
            <input v-if="showPassword2"  required="required" type="text"  class="input-form-1 password" v-model="confirmPassword"   placeholder="Confirm New Password"   />
            <input v-else type="password" required="required"  class="input-form-1 password" v-model="confirmPassword"   placeholder="Confirm New Password"   >
            <div class="space" @click="toggleShow2">
              <i class="fas" :class="{ 'fa-eye-slash': showPassword2, 'fa-eye': !showPassword2 }" ></i>
            </div>
          </div>

          <p v-if="error" class="error">{{ error }}</p>


          <button class="btn btn-white btn-animated"
          >Proceed</button
          >
        </div>
      </div>
    </div>
  </form>
</template>

<script>

import {mapState} from "vuex";
import StoreUtils from "@/utility/StoreUtils";

export default {
  name: 'NewPasswordForm',
  data() {
    return {
      showPassword2: false,
      newPassword: "",
      confirmPassword: "",
      error: "",
    };
  },
  computed:{
    ...mapState({
      loading: state => state.auth.loading,
      auth: state => state.auth
    }),
    ForgotPasswordFormData() {
      return StoreUtils.rootGetters(StoreUtils.getters.auth.getForgotPasswordFormData)
    },

  },
  methods: {
    async onPostClick() {
      this.error = "";
      if (!this.newPassword || !this.confirmPassword) {
        this.error = "Both passwords are required.";
        return;
      }
      if (this.newPassword !== this.confirmPassword) {
        this.error = "Passwords do not match.";
        return;
      }
      await StoreUtils.dispatch(StoreUtils.actions.auth.resetPassword, {
        userId : "46",
        newPassword: this.newPassword
      })
      await this.$router.push("/login");
    },
    toggleShow2() {
      this.showPassword2 = !this.showPassword2;
    },
  },
}
</script>

<style scoped>
form {
  margin: 0 auto;
  max-width: 40rem;

  margin-top: 5%;
}

.company-logo{
  width: 32%;
  margin-bottom: 1.5%;
}

:root {
  --primary-color: #3525d3;
  --white-color: #fff;
  --black-color: #3c4a57;
  --light-gray: #e4e8ee;
}

.wrapper {
  position: relative;
  align-items: center;
  justify-content: center;
}


.wrapper {
  width: 100%;
  margin: auto;
}

.wrapper::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  min-height: 100vh;
  z-index: -1;
}

.wrapper .headline {
  text-align: center;
  padding-bottom: 20px;
}


.wrapper .headline h2 {
  font-weight: 400;
  font-size: 20px;
  padding-top: 1.5%;
  /*margin-top: 10%;*/
  color: #0f171c;
  padding-bottom: 5px;
  font-family: 'BR-Firma-Bold', sans-serif;
}

p{
  color: #0f171c;
}

.wrapper .form {
  max-width: 350px;
  width: 100%;
  margin: auto;
}


.wrapper .form-group input {
  display: block;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: -0.1px;
  padding: 12px 16px;
  height: 48px;
  border-radius: 8px;
  color: var(--black-color);
  border: 1px solid #e4e8ee;
  box-shadow: none;
  width: 100%;
}

.wrapper .form-group input:focus {
  outline: none;
  border: 1px solid #24405A;
}

.wrapper .form-group input::placeholder {
  color: var(--black-color);
  font-weight: 400;
  font-size: 14px;
}

.btn,
.btn-white,
.btn-animated {
  width: 100%;
  margin: 15px 0 30px;
  line-height: 22px;
  padding: 12px 155px;
  border: none;
  text-align: center;
  border-radius: 5px;
}

.btn:link,
.btn:visited {
  text-decoration: none;
  padding: 10px 40px;
  border-radius: 100px;
  transition: all 0.2s;
  position: relative;
}

.btn-white {
  background: #000021;
  border: 1px solid #000021;
  color: white;
  font-size: 15px;
}


.has-addons{
  display: flex;
  flex-direction: row-reverse;
  justify-content: center;
  align-items: center;
  align-content: center;
}
button{
  background-color: transparent;
}
.fas{
  font-size: 13px;
  margin-top: 10%;
}
.space{
  padding-top: 13px;
  padding-bottom: 13px;
  padding-right: 10px;
  border: 1px solid #d0d5dd;
  border-left-style: none;
  border-radius: 0 8px 8px 0;
  font-size: 1rem;
  background-color: #FFFFFF;
}
.input-form-1{
  order: 1;
  width: 100%;
  padding: 13px 20px;
  margin: 8px 0;
  display: inline-block;
  box-sizing: border-box;
}
input {
  box-sizing: border-box;
  border: 1px solid #D0D5DD;
  border-radius: 8px;
  -webkit-transition: 0.3s;
  padding-top: 12px;
  padding-bottom: 12px;
  transition: 0.3s;
  outline: none;
  color: var(--black-color);
  letter-spacing: 0.5px;
}
input:focus {
  border: 1px solid #24405A;
}
input::placeholder {
  color: var(--black-color);
}
.input-form-1.password {
  border-right-style: none;
  border-radius: 8px 0 0 8px;
}


@media (max-width: 1030px) {
  .wrapper::before {
    left: -25%;
    min-height: 60vh;
    height: 500px;
  }
}
@media (max-width: 767px) {
  .wrapper {
    max-width: 550px;
  }
  .wrapper .headline h1 {
    font-size: 22px;
    line-height: 25px;
  }
}
@media (max-width: 990px) {
  .wrapper .headline h1  {
    font-size: 32px;
  }
  .wrapper .headline h2  {
    font-size: 28px;
  }
}
@media (max-width: 500px) {
  .wrapper {
    padding: 10px 25px 0;
  }
  form {
    max-width: 40rem;
    border-radius: 12px;
  }
  .wrapper .headline h1  {
    font-size: 25px;
  }
  .wrapper .headline h2  {
    font-size: 23px;
  }
  .company-logo{
    width: 50%;
    margin-top: unset;
  }
}

</style>


