<template>
  <div>
    <div class="backdrop"></div>
    <dialog open>
      <div class="alpha">

        <div class="first-part">
          <img src="@/assets/fund-wallet-icon.svg" alt="fund-wallet-icon"/>
          <i class='bx bx-x' @click="close"></i>
        </div>

        <div class="second-part">
          <p class="text-1">Withdrawal</p>
          <p class="text-2">Your Request Has Been Sent For Processing!!</p>
          <p class="text-3">Kindly Note:For Faster Response you can contact support at
            <span>
              <a href="mailto:support@marketmoverstrade.com" class="para-last">support@marketmoverstrade.com</a>
            </span>
          </p>
        </div>


        <br/>
        <button @click="close">cancel</button>

      </div>

    </dialog>
  </div>
</template>

<script>
import Swal from "sweetalert2";

export default {
  name: "WithdrawalModal",
  emits: ['close'],
  methods:{
    async close() {
      await this.$emit('close')
      await Swal.fire({
        icon: 'success',
        title: 'Pending',
        text: 'Withdrawal Request Pending',
      });
    },
  },
}
</script>
<style scoped >

.backdrop {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  z-index: 10;
  background-color: rgba(0, 0, 0, 0.7);
}


dialog {
  position: fixed;
  top: 18vh;
  width: 32rem;
  height: 20rem;
  left: calc(50% - 9rem);
  margin: 0;
  background-color: transparent;
  z-index: 100;
  border: none;
  animation: modal 0.3s ease-out forwards;
}

.alpha{
  position: relative;
  display: block;
  overflow: hidden;
  width: 400px;
  height: 360px;
  /*height: auto;*/
  padding: 24px;
  border-radius: 5px;
  background-color: #0f171c;
  box-shadow: 0 0 34px 0 rgba(3, 28, 67, 0.13);
  border: 0.5px solid #3C4A57FF;
}

.first-part{
  display: flex;
  justify-content: space-between;
}

.bx-x{
  font-size: 25px;
  padding-top: 2px;
  color: #ffffff;
}

.text-1{
  font-weight: 600;
  font-size: 18px;
  line-height: 28px;
  color: #ffffff;
  padding-top: 2.5%;
  padding-bottom: 1%;
}

.text-2{
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #ffffff;
  padding-top: 1%;
  padding-bottom: 2%;
}

.text-3{
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #ffffff;
  padding-top: 1.5%;
  padding-bottom: 2%;
}

.text-4, .text-5, .text-6{
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #667085;
  padding-top: 1.5%;
  padding-bottom: 1.5%;
}

button{
  padding: 8px 55px;
  color: white;
  background-color: #0f171c;
  border: 0.5px solid #3C4A57FF;
  border-radius: 5px;
  font-size: 13px;
  text-decoration: none;
  /*display: block;*/
  /*margin-left: auto;*/
  /*margin-right: auto;*/
}
button:hover{
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  color: #0f171c;
  background-color: #ffffff;
  border: 0.5px solid #3C4A57FF;
  -webkit-transition: all 0.35s ease;
  transition: all 0.35s ease;
}

.para-last{
  color: rgba(219,101,123,0.6);
}
@keyframes modal {
  from {
    opacity: 0;
    transform: translateY(-50px) scale(0.9);
  }

  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}
@media (max-width: 500px) {
  dialog {
    top: 14vh;
    width: 27rem;
    height: 20rem;
    left: calc(50% - 10.5rem);
    right: 30px;
  }
  h3{
    font-size: 20px;
  }
  p{
    font-size: unset;
  }
  .alpha{
    width: 340px;
    height: 340px;
  }
}
</style>