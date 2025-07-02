<template>
  <div>
    <div class="body">
      <fund-wallet-modal @close="hideDialog" v-if="dialogIsVisible" :selected-item="selectedItem" />

      <form style="display: none"  @submit.prevent="showDialog" id="InteracFundingCard" class="dashboard-body-wrapper align-center">

        <h4 class="header">Follow the instructions below to fund your wallet</h4>

        <hr/>

        <div class="margin-top margin-medium">

          <div class="interac-funding-steps">
            <div class="margin-bottom margin-small">
              <div class="text-block-60">STEP 1</div>
            </div>

            <div >
              <a class="">
                <br/>
                <div class="setup-title-wrapper">
                  <img src="@/assets/bank.svg" loading="lazy" alt="">
                  <div class="setup-title">
                    <div class="text-block-51">
                      Enter Amount Below
                      <!--                    <strong>payment@rubieswire.com</strong>-->
                    </div>
                  </div>
                </div>
              </a>
            </div>

          </div>

          <div class="input-form-2">
            <input type="number" class="input-form-3" placeholder="Amount" required name="Amount" v-model="btcBalance"/>
          </div>

          <div class="interac-funding-steps">
            <div class="margin-bottom margin-small">
              <div class="text-block-60">STEP 2</div>
            </div>

            <div >
              <a >
                <br/>
                <div class="setup-title-wrapper">
                  <img src="@/assets/bank.svg" loading="lazy" alt="">
                  <div class="setup-title">
                    <div class="text-block-51">
                      Select Deposit Method Below
                      <!--                    <strong>payment@rubieswire.com</strong>-->
                    </div>
                  </div>
                </div>
              </a>
            </div>

          </div>

          <div class="input-form-2">
            <select
                required
                class="input-form-3"
                v-model="depositMethod"
                aria-required="required"
                data-name="Field"
                @change="getList"
            >
              <option selected disabled value="">Deposit Method List</option>
              <!--              <option :value="null" disabled>Select Digital Currency</option>-->
              <option value="Bitcoin">Bitcoin</option>
              <option value="Ethereum">Ethereum</option>
              <option value="Dogecoin">Dogecoin</option>
              <option value="Litecoin">Litecoin</option>
              <option value="Xrp">Xrp</option>
              <option value="ERC20">USDT ( ERC20 NETWORK )</option>
              <option value="TRC20">USDT ( TRC20 NETWORK )</option>
              <option value="BankTransfer">Bank Transfer</option>
            </select>
          </div>


          <p
              v-if="this.depositMethod === 'Bitcoin' ||
          this.depositMethod === 'Ethereum' ||
          this.depositMethod === 'BankTransfer'||
          this.depositMethod === 'BankTransfer'||

           this.depositMethod === 'Dogecoin' ||
          this.depositMethod === 'Litecoin'||
          this.depositMethod === 'Xrp'||

          this.depositMethod === 'ERC20' ||
          this.depositMethod === 'TRC20'"
             class="text-3">Transfer desired amount to the details displayed below and have your balance funded</p>


          <div>
            <div v-if="this.depositMethod === 'Bitcoin' ">
              <p class="text-4">Wallet Name : {{depositMethod}}</p>
              <p class="text-5">Wallet Address : {{this.bitcoinAddress}}</p>
              <p @click="copyText" class="button"
                      style="background-color: #5d78ff;
                        width: 100px;height: 30px;font-size: 11px;
                      border: 1px solid #5d78ff;float: right;">
                Copy</p>
            </div>

            <div v-if="this.depositMethod === 'Ethereum' ">
              <p class="text-4">Wallet Name : {{depositMethod}}</p>
              <p class="text-5">Wallet Address : {{this.ethereumAddress}}</p>
              <p @click="copyText2" class="button"
                 style="background-color: #5d78ff;
                        width: 100px;height: 30px;font-size: 11px;
                      border: 1px solid #5d78ff;float: right;">
                Copy</p>
            </div>

            <div v-if="this.depositMethod === 'ERC20' ">
              <p class="text-4">Wallet Name : USDT ( ERC20 NETWORK )</p>
              <p class="text-5">Wallet Address : {{this.ERC20}}</p>
              <p @click="copyText3" class="button"
                 style="background-color: #5d78ff;
                        width: 100px;height: 30px;font-size: 11px;
                      border: 1px solid #5d78ff;float: right;">
                Copy</p>
            </div>

            <div v-if="this.depositMethod === 'TRC20' ">
              <p class="text-4">Wallet Name : USDT ( TRC20 NETWORK )</p>
              <p class="text-5">Wallet Address : {{this.TRC20}}</p>
              <p @click="copyText4" class="button"
                 style="background-color: #5d78ff;
                        width: 100px;height: 30px;font-size: 11px;
                      border: 1px solid #5d78ff;float: right;">
                Copy</p>
            </div>

            <div v-if="this.depositMethod === 'Dogecoin' ">
              <p class="text-4">Wallet Name : {{this.depositMethod}}</p>
              <p class="text-5">Wallet Address : {{this.dogecoinAddress}}</p>
              <p @click="copyText5" class="button"
                 style="background-color: #5d78ff;
                        width: 100px;height: 30px;font-size: 11px;
                      border: 1px solid #5d78ff;float: right;">
                Copy</p>
            </div>

            <div v-if="this.depositMethod === 'Litecoin' ">
              <p class="text-4">Wallet Name : {{this.depositMethod}}</p>
              <p class="text-5">Wallet Address : {{this.litecoinAddress}}</p>
              <p @click="copyText6" class="button"
                 style="background-color: #5d78ff;
                        width: 100px;height: 30px;font-size: 11px;
                      border: 1px solid #5d78ff;float: right;">
                Copy</p>
            </div>

            <div v-if="this.depositMethod === 'Xrp' ">
              <p class="text-4">Wallet Name : {{this.depositMethod}}</p>
              <p class="text-5">Wallet Address : {{this.xrpAddress}}</p>
              <p @click="copyText7" class="button"
                 style="background-color: #5d78ff;
                        width: 100px;height: 30px;font-size: 11px;
                      border: 1px solid #5d78ff;float: right;">
                Copy</p>
            </div>

            <div v-if="this.depositMethod === 'BankTransfer' ">
              <p class="text-4">Bank Name : {{this.bankName}}</p>
              <p class="text-5">Bank Address : {{this.accountNumber}}</p>
              <p class="text-5">Bank Routing Number : {{this.routingNumber}}</p>

              <p class="text-3">Contact support to proceed with this Deposit Method
                <span class="note-span">
              <a style="color: rgba(219,101,123,0.6);" href="mailto:support@marketmoverstrade.com" class="para-last">support@marketmoverstrade.com</a>
            </span>
              </p>
            </div>

            <div v-if="this.depositMethod === 'Bitcoin' " class="qr-code">
              <vue-qrcode :value="bitcoinAddress"></vue-qrcode>
            </div>

            <div v-if="this.depositMethod === 'Ethereum'" class="qr-code">
              <vue-qrcode :value="ethereumAddress"></vue-qrcode>
            </div>

            <div v-if="this.depositMethod === 'Dogecoin'" class="qr-code">
              <vue-qrcode :value="dogecoinAddress"></vue-qrcode>
            </div>

            <div v-if="this.depositMethod === 'Litecoin'" class="qr-code">
              <vue-qrcode :value="litecoinAddress"></vue-qrcode>
            </div>

            <div v-if="this.depositMethod === 'Xrp'" class="qr-code">
              <vue-qrcode :value="xrpAddress"></vue-qrcode>
            </div>


            <div v-if="this.depositMethod === 'TRC20' " class="qr-code">
              <vue-qrcode :value="TRC20"></vue-qrcode>
            </div>

            <div v-if="this.depositMethod === 'ERC20'" class="qr-code">
              <vue-qrcode :value="ERC20"></vue-qrcode>
            </div>
          </div>


          <p
              v-if="this.depositMethod === 'Bitcoin' ||
          this.depositMethod === 'Ethereum' ||
          this.depositMethod === 'BankTransfer'||
          this.depositMethod === 'BankTransfer'||
          this.depositMethod === 'Dogecoin' ||
          this.depositMethod === 'Litecoin'||
          this.depositMethod === 'Xrp'||
          this.depositMethod === 'ERC20' ||
          this.depositMethod === 'TRC20'"
              class="text-3">Note: After making your deposit,kindly send a screenshot/proof of deposit to
            <span class="note-span">
              <a style="color: rgba(219,101,123,0.6);" href="mailto:support@marketmoverstrade.com" class="para-last">support@marketmoverstrade.com</a>
            </span> for documentation and to boost the funding process
          </p>



          <div class="interac-funding-steps">
            <div class="margin-bottom margin-small">
              <div class="text-block-60">STEP 3</div>
            </div>

            <div >
              <a class="">
                <br/>
                <div class="setup-title-wrapper">
                  <img src="@/assets/bank.svg" loading="lazy" alt="">
                  <div class="setup-title">
                    <div class="text-block-51">
                      Additional Comment
                      <!--                    <strong>payment@rubieswire.com</strong>-->
                    </div>
                  </div>
                </div>
              </a>
            </div>

          </div>

          <div class="input-form-2">
            <input type="text" class="input-form-3" placeholder="Enter Additional Comment" required name="Amount" v-model="model.additionalComment"/>
          </div>


          <div class="interac-funding-steps">
            <div class="margin-bottom margin-small">
              <div class="text-block-60">STEP 4</div>
            </div>

            <div>
              <a>
                <br/>
                <div class="setup-title-wrapper"><img src="@/assets/bank.svg" loading="lazy" alt="">
                  <div class="setup-title">
                    <div class="text-block-51">
                      Click Proceed to Process transactions
                      <!--                    <strong>payment@rubieswire.com</strong>-->
                    </div>
                  </div>
                </div>
              </a>
            </div>

          </div>

        </div>

        <div class="margin-top margin-medium">
          <div class="payment-email-wrapper">
<!--            <div class="payment-email">-->
<!--&lt;!&ndash;              <div  class="text-block-62"></div>&ndash;&gt;-->
<!--              <div style="font-size: 15px;"  class="text-block-61">Selected Method :-->
<!--                <span style="padding-left: 10px;">{{depositMethod}}</span>-->
<!--              </div>-->
<!--              &lt;!&ndash;          <div class="text-block-62">Selected Currency would be displayed here</div>&ndash;&gt;-->
<!--            </div>-->
            <div class="copy-button">
<!--              <p  class="button">Proceed</p>-->
              <base-button
                  style="
                    border: 0.5px solid #5d78ff;
                    background-color: #5d78ff;"
                  class="button"
                  :loading="loading || loading2"
              >Proceed</base-button>
            </div>
          </div>
        </div>

        <p class="text-block-51" style="padding-top: 10px; color: #6c757d;" >
          Note: Deposits will be credited to your Market Movers Trade Account after 2 network confirmations.
        </p>

      </form>

      <div v-if="this.transactionScreen === 'screen1'"  id="InteracFundingCard" class="dashboard-body-wrapper align-center" >

        <h4 class="header">Select Deposit Method below</h4>

        <div class="section-container">
          <div class="section-container-1">
            <div class="section-container-inner-1">
              <img width="40" height="40" src="https://img.icons8.com/color/48/ethereum.png" alt="ethereum"/>
              <p class="section-container-text-1">ETH (Ether)</p>
            </div>
            <div @click="selectTransaction2" class="section-container-inner-2">
              <i class='bx bx-chevron-right'/>
            </div>
          </div>
          <div class="section-container-2">
            <div class="section-container-inner-1">
              <label class="switch">
                <input v-model="ethereumChecked" type="checkbox">
                <span class="slider"></span>
              </label>
              <p class="section-container-text-2">Ethereum Network</p>
            </div>
          </div>
        </div>

        <div class="section-container">
          <div class="section-container-1">
            <div class="section-container-inner-1">
              <img width="40" height="40" src="@/assets/tether-usdt-logo.svg" alt="tether--v1"/>
              <p class="section-container-text-1">USDT (Tether)</p>
            </div>
            <div @click="selectTransaction6" class="section-container-inner-2">
              <i class='bx bx-chevron-right'/>
            </div>
          </div>
          <div class="section-container-2">
            <div class="section-container-inner-1">
              <label class="switch">
                <input v-model="erc20Checked" type="checkbox">
                <span class="slider"></span>
              </label>
              <p class="section-container-text-2">ERC20 Network</p>
            </div>
          </div>
        </div>

        <div class="section-container">
          <div class="section-container-1">
            <div class="section-container-inner-1">
              <img width="40" height="40" src="@/assets/tether-usdt-logo.svg" alt="tether--v1"/>
              <p class="section-container-text-1">USDT (Tether)</p>
            </div>
            <div @click="selectTransaction7" class="section-container-inner-2">
              <i class='bx bx-chevron-right'/>
            </div>
          </div>
          <div class="section-container-2">
            <div class="section-container-inner-1">
              <label class="switch">
                <input v-model="trc20Checked" type="checkbox">
                <span class="slider"></span>
              </label>
              <p class="section-container-text-2">TRC20 Network</p>
            </div>
          </div>
        </div>

        <div class="section-container">
          <div class="section-container-1">
            <div class="section-container-inner-1">
              <img width="40" height="40" src="@/assets/dogecoin-doge-logo.svg" alt="tether--v1"/>
              <p class="section-container-text-1">Dogecoin</p>
            </div>
            <div @click="selectTransaction3" class="section-container-inner-2">
              <i class='bx bx-chevron-right'/>
            </div>
          </div>
          <div class="section-container-2">
            <div class="section-container-inner-1">
              <label class="switch">
                <input v-model="dogecoinChecked" type="checkbox">
                <span class="slider"></span>
              </label>
              <p class="section-container-text-2">Dogecoin Network</p>
            </div>
          </div>
        </div>

        <div class="section-container">
          <div class="section-container-1">
            <div class="section-container-inner-1">
              <img width="40" height="40" src="@/assets/litecoin-ltc-logo.svg" alt="tether--v1"/>
              <p class="section-container-text-1">Litecoin</p>
            </div>
            <div @click="selectTransaction4" class="section-container-inner-2">
              <i class='bx bx-chevron-right'/>
            </div>
          </div>
          <div class="section-container-2">
            <div class="section-container-inner-1">
              <label class="switch">
                <input v-model="litecoinChecked" type="checkbox">
                <span class="slider"></span>
              </label>
              <p class="section-container-text-2">Litecoin Network</p>
            </div>
          </div>
        </div>

        <div class="section-container">
          <div class="section-container-1">
            <div class="section-container-inner-1">
              <img width="40" height="40" src="@/assets/xrp-xrp-logo.svg" alt="tether--v1"/>
              <p class="section-container-text-1">Xrp</p>
            </div>
            <div @click="selectTransaction5" class="section-container-inner-2">
              <i class='bx bx-chevron-right'/>
            </div>
          </div>
          <div class="section-container-2">
            <div class="section-container-inner-1">
              <label class="switch">
                <input v-model="xrpChecked" type="checkbox">
                <span class="slider"></span>
              </label>
              <p class="section-container-text-2">XRP Ledger Network</p>
            </div>
          </div>
        </div>

        <div class="section-container">
          <div class="section-container-1">
            <div class="section-container-inner-1">
              <img width="40" height="40" src="@/assets/bitcoin-btc-logo.svg" alt="bitcoin"/>
              <p class="section-container-text-1">BTC (Bitcoin)</p>
            </div>
            <div @click="selectTransaction" class="section-container-inner-2">
              <i class='bx bx-chevron-right'/>
            </div>
          </div>
          <div class="section-container-2">
            <div class="section-container-inner-1">
              <label class="switch">
                <input v-model="lightningChecked"  type="checkbox">
                <span class="slider"></span>
              </label>
              <p class="section-container-text-2">Lightning Network</p>
            </div>
          </div>
        </div>

        <p class="text-block-51" style="padding-top: 10px; color: #6c757d;" >
          Note : Deposits will be credited to your Market Movers Trade Account after 2 network confirmations.
        </p>

      </div>

      <form @submit.prevent="handleShowDialog" v-if="this.transactionScreen === 'screen2'" id="InteracFundingCard" class="dashboard-body-wrapper align-center" >

<!--        <h4 class="header">Please send to address : </h4>-->
        <p @click="back" class="back">Back</p>

        <div class="interac-funding-steps">
<!--          <div class="margin-bottom margin-small">-->
<!--            <div class="text-block-60">STEP 1</div>-->
<!--          </div>-->

          <div >
            <a class="">
              <br/>
              <div class="setup-title-wrapper">
                <img src="@/assets/bank.svg" loading="lazy" alt="">
                <div class="setup-title">
                  <div class="text-block-51">
                    Enter Amount Below
                  </div>
                </div>
              </div>
            </a>
          </div>

        </div>

        <div class="input-form-2">
          <input type="number" class="input-form-3" placeholder="Amount" required name="Amount" v-model="btcBalance"/>
        </div>

        <div class="interac-funding-steps">
<!--          <div class="margin-bottom margin-small">-->
<!--            <div class="text-block-60">STEP 2</div>-->
<!--          </div>-->

          <div >
            <a class="">
              <br/>
              <div class="setup-title-wrapper">
                <img src="@/assets/bank.svg" loading="lazy" alt="">
                <div class="setup-title">
                  <div class="text-block-51">
                    Please send to address
                  </div>
                </div>
              </div>
            </a>
          </div>

        </div>


        <div class="transaction-container">
          <div class="transaction-container-header">
            <p>{{transactionNetwork}} Network only</p>
          </div>
          <div class="transaction-container-body">
            <div class="transaction-container-body-1">
              <p v-if="this.depositMethod === 'Bitcoin'" >{{this.bitcoinAddress}}</p>
              <p v-if="this.depositMethod === 'Ethereum'" >{{this.ethereumAddress}}</p>

              <p v-if="this.depositMethod === 'ERC20'" >{{this.ERC20}}</p>
              <p v-if="this.depositMethod === 'TRC20'" >{{this.TRC20}}</p>

              <p v-if="this.depositMethod === 'Dogecoin'" >{{this.dogecoinAddress}}</p>
              <p v-if="this.depositMethod === 'Litecoin'" >{{this.litecoinAddress}}</p>

              <p v-if="this.depositMethod === 'Xrp'" >{{this.xrpAddress }}</p>
            </div>
            <div class="transaction-container-body-2">
              <i v-if="this.depositMethod === 'Bitcoin'" @click="copyText" class='bx bx-copy'></i>

              <i v-if="this.depositMethod === 'Ethereum'" @click="copyText2" class='bx bx-copy'></i>

              <i v-if="this.depositMethod === 'ERC20'" @click="copyText3" class='bx bx-copy'></i>

              <i v-if="this.depositMethod === 'TRC20'" @click="copyText4" class='bx bx-copy'></i>

              <i v-if="this.depositMethod === 'Dogecoin'" @click="copyText5" class='bx bx-copy'></i>

              <i  v-if="this.depositMethod === 'Litecoin'" @click="copyText6" class='bx bx-copy'></i>

              <i  v-if="this.depositMethod === 'Xrp'" @click="copyText7" class='bx bx-copy'></i>
            </div>
          </div>
        </div>

        <p class="text-block-51" style="padding-top: 10px; color: #6c757d;" >
          Only send {{depositMethod}} on {{transactionNetwork}} network.
        </p>

        <div class="interac-funding-steps">
          <div class="margin-bottom margin-small">
            <div class="text-block-60">or scan the QR code :</div>
          </div>
        </div>


        <div v-if="this.depositMethod === 'Bitcoin' " class="qr-code">
          <vue-qrcode class="qr-code" :value="bitcoinAddress"></vue-qrcode>
        </div>

        <div v-if="this.depositMethod === 'Ethereum'" class="qr-code">
          <vue-qrcode class="qr-code" :value="ethereumAddress"></vue-qrcode>
        </div>

        <div v-if="this.depositMethod === 'Dogecoin'" class="qr-code">
          <vue-qrcode class="qr-code" :value="dogecoinAddress"></vue-qrcode>
        </div>

        <div v-if="this.depositMethod === 'Litecoin'" class="qr-code">
          <vue-qrcode class="qr-code" :value="litecoinAddress"></vue-qrcode>
        </div>

        <div v-if="this.depositMethod === 'Xrp'" class="qr-code">
          <vue-qrcode class="qr-code" :value="xrpAddress"></vue-qrcode>
        </div>

        <div v-if="this.depositMethod === 'TRC20' " class="qr-code">
          <vue-qrcode class="qr-code" :value="TRC20"></vue-qrcode>
        </div>

        <div v-if="this.depositMethod === 'ERC20'" class="qr-code">
          <vue-qrcode class="qr-code" :value="ERC20"></vue-qrcode>
        </div>

        <p
            v-if="this.depositMethod === 'Bitcoin' ||
          this.depositMethod === 'Ethereum' ||
          this.depositMethod === 'BankTransfer'||
          this.depositMethod === 'BankTransfer'||
          this.depositMethod === 'Dogecoin' ||
          this.depositMethod === 'Litecoin'||
          this.depositMethod === 'Xrp'||
          this.depositMethod === 'ERC20' ||
          this.depositMethod === 'TRC20'"
            class="text-3">Note: After making your deposit,kindly send a screenshot/proof of deposit to
          <span class="note-span">
              <a style="color: rgba(219,101,123,0.6);" href="mailto:support@marketmoverstrade.com" class="para-last">support@marketmoverstrade.com</a>
            </span> for documentation and to boost the funding process
        </p>


<!--        <div v-if="this.showButton === true" class="scanning">-->
<!--          <span class="loader"></span>-->
<!--          <p>Scanning blockchain network</p>-->
<!--        </div>-->

        <base-button
            style="border: 0.5px solid #5d78ff; background-color: #5d78ff;"
            class="button"
            :loading="loading || loading2"
        >
          Proceed
        </base-button>



        <p class="text-block-51" style="padding-top: 10px; color: #6c757d;" >
          Note : Deposits will be credited to your Market Movers Trade Account after 2 network confirmations.
        </p>

      </form>


    </div>
  </div>
</template>

<script>
import FundWalletModal from "@/components/BaseComponents/modal/FundWalletModal.vue";
import router from "@/router";
import BaseButton from "@/components/BaseComponents/buttons/BaseButton.vue";
import DepositRequest from "@/model/request/DepositRequest";
import {mapState} from "vuex";
import StoreUtils from "@/utility/StoreUtils";
import VueQrcode from '@xkeshi/vue-qrcode';
import Swal from "sweetalert2";


export default {
  name: "DashBoardFundWallet",
  components: {
    BaseButton,
    FundWalletModal,
    VueQrcode // Register the component
  },
  computed:{
    readPaymentWalletById() {
      return StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)
    },
    ...mapState({
      loading: state => state.deposit.loading,
      loading2: state => state.paymentWallet.loading,
      auth: state => state.auth,
    }),
  },
  data() {
    return {
      showButton: false, // Initially false
      model: new DepositRequest().createDeposit,
      dialogIsVisible: false,
      btcBalance: "",
      depositMethod: "",
      selectedItem: null,
      options: [
        { id: 1, label: "STANDARD", value1: "STANDARD", value2: "10%" },
        { id: 2, label: "PREMIUM", value1: "PREMIUM", value2: "30%" },
        { id: 3, label: "DELUXE", value1: "DELUXE", value2: "50%" },
      ],
      userId: "",
      userInfo: "",
      randomString: "",
      accountNumber: '',
      bankName: '',
      bitcoinAddress: '',
      ethereumAddress: '',
      routingNumber: '',
      ERC20: '',
      TRC20: '',
      litecoinAddress: '',
      dogecoinAddress: '',
      xrpAddress: '',

      transactionScreen: 'screen1',
      transactionNetwork: '',
      lightningChecked: false,
      ethereumChecked: false,
      erc20Checked: false,
      dogecoinChecked: false,
      litecoinChecked: false,
      xrpChecked: false,
      trc20Checked: false,
    };
  },
  methods: {

    async back() {
      this.transactionScreen = 'screen1'
      await router.push('/over-view');
    },

    selectTransaction() {
      if (!this.lightningChecked) {
        Swal.fire({
          icon: 'warning',
          title: 'Network Required',
          text: 'Please enable Lightning Network before proceeding.',
        });
        return;
      }

      this.depositMethod = 'Bitcoin';
      this.transactionScreen = 'screen2';
      this.transactionNetwork = 'Lightning';
      this.getList();
    },


    selectTransaction2() {
      if (!this.ethereumChecked) {
        Swal.fire({
          icon: 'warning',
          title: 'Network Required',
          text: 'Please enable Ethereum Network before proceeding.',
        });
        return;
      }

      this.depositMethod = 'Ethereum';
      this.transactionScreen = 'screen2';
      this.transactionNetwork = 'Ethereum';
      this.getList();
    },


    selectTransaction3() {
      if (!this.dogecoinChecked) {
        Swal.fire({
          icon: 'warning',
          title: 'Network Required',
          text: 'Please enable Dogecoin Network before proceeding.',
        });
        return;
      }

      this.depositMethod = 'Dogecoin';
      this.transactionScreen = 'screen2';
      this.transactionNetwork = 'Dogecoin';
      this.getList();
    },


    selectTransaction4() {
      if (!this.litecoinChecked) {
        Swal.fire({
          icon: 'warning',
          title: 'Network Required',
          text: 'Please enable Litecoin Network before proceeding.',
        });
        return;
      }

      this.depositMethod = 'Litecoin';
      this.transactionScreen = 'screen2';
      this.transactionNetwork = 'Litecoin';
      this.getList();
    },


    selectTransaction5() {
      if (!this.xrpChecked) {
        Swal.fire({
          icon: 'warning',
          title: 'Network Required',
          text: 'Please enable XRP Ledger Network before proceeding.',
        });
        return;
      }

      this.depositMethod = 'XRP';
      this.transactionScreen = 'screen2';
      this.transactionNetwork = 'XRP Ledger';
      this.getList();
    },


    selectTransaction6() {
      if (!this.erc20Checked) {
        Swal.fire({
          icon: 'warning',
          title: 'Network Required',
          text: 'Please enable ERC20 Network before proceeding.',
        });
        return;
      }

      this.depositMethod = 'USDT';
      this.transactionScreen = 'screen2';
      this.transactionNetwork = 'ERC20';
      this.getList();
    },


    selectTransaction7() {
      if (!this.trc20Checked) {
        Swal.fire({
          icon: 'warning',
          title: 'Network Required',
          text: 'Please enable TRC20 Network before proceeding.',
        });
        return;
      }

      this.depositMethod = 'USDT';
      this.transactionScreen = 'screen2';
      this.transactionNetwork = 'TRC20';
      this.getList();
    },


    async copyText() {
      await this.$copyText(this.bitcoinAddress)
      await Swal.fire({
        icon: 'success',
        title: 'success',
        text: 'Wallet Address Copied Successfully',
      });
    },

    async copyText2() {
      await this.$copyText(this.ethereumAddress)
      await Swal.fire({
        icon: 'success',
        title: 'success',
        text: 'Wallet Address Copied Successfully',
      });
    },

    async copyText3() {
      await this.$copyText(this.ERC20)
      await Swal.fire({
        icon: 'success',
        title: 'success',
        text: 'Wallet Address Copied Successfully',
      });
    },

    async copyText4() {
      await this.$copyText(this.TRC20)
      await Swal.fire({
        icon: 'success',
        title: 'success',
        text: 'Wallet Address Copied Successfully',
      });
    },

    async copyText5() {
      await this.$copyText(this.dogecoinAddress)
      await Swal.fire({
        icon: 'success',
        title: 'success',
        text: 'Wallet Address Copied Successfully',
      });
    },

    async copyText6() {
      await this.$copyText(this.litecoinAddress)
      await Swal.fire({
        icon: 'success',
        title: 'success',
        text: 'Wallet Address Copied Successfully',
      });
    },

    async copyText7() {
      await this.$copyText(this.xrpAddress)
      await Swal.fire({
        icon: 'success',
        title: 'success',
        text: 'Wallet Address Copied Successfully',
      });
    },

    async hideDialog() {
      this.dialogIsVisible = false;
      await router.push('/over-view')
    },

    handleShowDialog() {
      if (!this.btcBalance || this.btcBalance <= 0) {
        Swal.fire({
          icon: 'warning',
          title: 'Invalid Amount',
          text: 'Please enter a valid amount before proceeding.',
        });
        return;
      }

      this.showDialog();
    },

    async showDialog() {
      await StoreUtils.dispatch(StoreUtils.actions.deposit.depositCreate, {
        userId: this.userId,
        amount: this.btcBalance,
        transactionMethod: this.depositMethod,
        transactionType: "deposit",
        transactionReference: this.randomString,
        depositStatus: "pending",
        additionalComment: "deposit"
      });

      await Swal.fire({
        icon: 'success',
        title: 'Pending',
        text: 'Deposit Request Pending',
      });

      await router.push('/over-view');
    },


    // async showDialog() {
    //   await StoreUtils.dispatch(StoreUtils.actions.deposit.depositCreate, {
    //     userId : this.userId,
    //     amount : this.btcBalance,
    //     transactionMethod : this.depositMethod,
    //     transactionType : "deposit",
    //     transactionReference : this.randomString,
    //     depositStatus: "pending",
    //     additionalComment : "deposit"
    //   })
    //   // await StoreUtils.dispatch(StoreUtils.actions.paymentWallet.readPaymentWalletById, {
    //   //   walletId: 1,
    //   // })
    //   // StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)
    //   // this.selectedItem = this.depositMethod;
    //   // this.dialogIsVisible = true;
    //   await Swal.fire({
    //     icon: 'success',
    //     title: 'Pending',
    //     text: 'Deposit Request Pending',
    //   });
    //   await router.push('/over-view')
    // },

    generateRandomString() {
      const characters = '0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz';
      let result = '';
      for (let i = 0; i < 10; i++) {
        const randomIndex = Math.floor(Math.random() * characters.length);
        result += characters.charAt(randomIndex);
      }
      this.randomString = result;
    },

    populateForm() {
      this.bitcoinAddress = this.readPaymentWalletById.paymentWallet.bitcoinAddress;
      this.ethereumAddress = this.readPaymentWalletById.paymentWallet.ethereumAddress;
      this.bankName = this.readPaymentWalletById.paymentWallet.bankName;
      this.accountNumber = this.readPaymentWalletById.paymentWallet.accountNumber;
      this.routingNumber = this.readPaymentWalletById.paymentWallet.routingNumber;

      this.litecoinAddress = this.readPaymentWalletById.paymentWallet.LitecoinAddress;
      this.dogecoinAddress = this.readPaymentWalletById.paymentWallet.DogecoinAddress;
      this.xrpAddress = this.readPaymentWalletById.paymentWallet.XRPAddress;
      this.ERC20 = this.readPaymentWalletById.paymentWallet.UsdtERC20Address;
      this.TRC20 = this.readPaymentWalletById.paymentWallet.UsdtTRC20Address;
    },

    async getList() {
      await StoreUtils.dispatch(StoreUtils.actions.paymentWallet.readPaymentWalletById, {
        walletId: 1,
      });

      await StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)
      await this.populateForm();
    }



  },

  beforeMount() {
    this.generateRandomString()
    this.populateForm()

    StoreUtils.dispatch(StoreUtils.actions.paymentWallet.readPaymentWalletById, {
      walletId: 1,
    })
    StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)

    this.userId = localStorage.getItem('userId')


    // Retrieve the object from local storage
    const storedObject = localStorage.getItem('userInfo');

    if (storedObject) {
      this.userInfo = JSON.parse(storedObject);
    }
  },

  created() {
    this.generateRandomString()
    this.populateForm()
    this.getList()

    StoreUtils.dispatch(StoreUtils.actions.paymentWallet.readPaymentWalletById, {
      walletId: 1,
    })
    StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)

    this.userId = localStorage.getItem('userId')


    // Retrieve the object from local storage
    const storedObject = localStorage.getItem('userInfo');

    if (storedObject) {
      this.userInfo = JSON.parse(storedObject);
    }
  },

  mounted() {
    this.generateRandomString()
    this.populateForm()
    this.getList()

    // Show button after 20 seconds (20000ms)
    setTimeout(() => {
      this.showButton = true;
      console.log("Button is now visible"); // optional debug
    }, 20000);

    StoreUtils.dispatch(StoreUtils.actions.paymentWallet.readPaymentWalletById, {
      walletId: 1,
    })
    StoreUtils.rootGetters(StoreUtils.getters.paymentWallet.getReadPaymentWalletById)

    this.userId = localStorage.getItem('userId')

    // Retrieve the object from local storage
    const storedObject = localStorage.getItem('userInfo');

    if (storedObject) {
      this.userInfo = JSON.parse(storedObject);
    }
  }
}
</script>

<style scoped>
.company-logo{
  width: 35%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.scanning{
  display: flex;
  justify-content: center;
  align-content: center;
  align-items: center;
  gap: 5px;
  padding-bottom: 1%;
}

.scanning p{
  color: #E3EBF6;
  font-size: 13px;
}

.loader {
  width: 20px;
  height: 20px;
  border: 2px solid #FFF;
  border-bottom-color: #000000;
  border-radius: 50%;
  display: inline-block;
  box-sizing: border-box;
  animation: rotation 1s linear infinite;
}

@keyframes rotation {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

.qr-code{
  width: 200px;
  margin-left: auto;
  margin-right: auto;
  display: block;
}

.back{
  float: right;
  color: #E3EBF6;
  text-decoration: underline;
}

.transaction-container-header{
  background-color: #000000;
  padding-top: 5px;
  padding-bottom: 5px;
}

.transaction-container-header p{
  text-align: center;
  color: #E3EBF6;
  font-size: 15px;
}

.transaction-container-body{
  display: flex;
  width: 100%;
}

.transaction-container-body-1{
  width: 90%;
  border: 1.5px dashed #000000;
  padding: 10px;
  border-right: none;
  border-top: none;
}

.transaction-container-body-1 p{
  word-wrap: break-word;
  word-break: break-word;
  white-space: normal; /* This allows wrapping */
  overflow-wrap: anywhere; /* Ensures breaking mid-word if necessary */
  color: #E3EBF6;
}

.transaction-container-body-2{
  width: 10%;
  border: 1.5px dashed #000000;
  border-top: none;
  display: flex;
  align-items: center;   /* vertical centering */
  justify-content: center; /* horizontal centering */
}

.bx-copy{
  color: #E3EBF6;
  font-size: 18px;
}

.body{
  padding: 32px;
}

.header{
  font-weight: 700;
  font-size: 17px;
  /*line-height: 25px;*/
  color: #ffffff;
  text-align: left;
  margin-bottom: 3%;
}

.section-container{
  border: 0.5px solid rgba(241, 241, 241, 0.7);
  padding: 20px;
  border-radius: 7px;
  margin-bottom: 5%;
}

.section-container-inner-1{
  display: flex;
  align-items: center;
  align-content: center;
  gap: 5px;
}

.section-container-1{
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: space-between;
  padding-bottom: 5px;
  gap: 5px;
}

.switch {
  position: relative;
  display: inline-block;
  width: 50px;
  height: 22px;
}

.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  transition: 0.4s;
  border-radius: 24px;
}

.slider:before {
  position: absolute;
  content: "";
  height: 14px;
  width: 14px;
  left: 4px;
  bottom: 4px;
  background-color: white;
  transition: 0.4s;
  border-radius: 50%;
}

input:checked + .slider {
  background-color: #4caf50;
}

input:checked + .slider:before {
  transform: translateX(26px);
}

.section-container-text-1{
  color: #FFFFFF;
  font-size: 13px;
}

.section-container-text-2{
  color: #FFFFFF;
  font-size: 12px;
}

.bx-chevron-right{
  color: #FFFFFF;
  font-size: 20px;
}


.text-block-60 {
  color: #ffffff;
  font-size: 14px;
  font-weight: 500;
  letter-spacing: 2px;
}

.interac-card {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  width: 100%;
  padding: 16px 24px 16px 16px;
  -webkit-box-pack: justify;
  -webkit-justify-content: space-between;
  -ms-flex-pack: justify;
  justify-content: space-between;
  -webkit-box-align: center;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  border-radius: 8px;
  background-color: #0f171c;
  border: 0.5px solid #3C4A57FF;
  text-decoration: none;
}

.setup-title-wrapper {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  grid-column-gap: 1rem;
  grid-row-gap: 1rem;
}

.text-block-51 {
  color: #FFFFFF;
  font-size: 13px;
}

.w-inline-block {
  max-width: 100%;
  display: inline-block;
}

h3 {margin: 40px 0 0; }
ul {list-style-type: none; padding: 0; }
li {display: inline-block; margin: 0 10px; }

strong{
  text-transform: lowercase;
}
.input-form-2{
  /*margin-top: 7%;*/
  display: block;
  /*justify-content: center;*/
}
.input-form-3{
  order: 1;
  width: 100%;
  padding: 12px 10px;
  /*margin: 8px 0;*/
  display: inline-block;
  box-sizing: border-box;
  background-color: #000000;
}

input{
  box-sizing: border-box;
  background-color: #0f171c;
  border: 0.5px solid #3C4A57FF;
  border-radius: 5px;
  -webkit-transition: 0.3s;
  padding-top: 30px;
  padding-bottom: 30px;
  height: 45px;
  transition: 0.3s;
  outline: none;
  color: #ffffff;
}

input:focus {
  border: 1px solid #3C4A57FF;
}

input::placeholder{
  color: #ffffff;
}

select{
  box-sizing: border-box;
  background-color: #0f171c;
  border: 0.5px solid #3C4A57FF;
  border-radius: 5px;
  -webkit-transition: 0.3s;
  padding-top: 30px;
  padding-bottom: 30px;
  height: 45px;
  transition: 0.3s;
  outline: none;
  color: #ffffff;
}

select:focus {
  border: 1px solid #3C4A57FF;
}

option{
  box-sizing: border-box;
  border: 1px solid #D0D5DD;
  border-radius: 8px;
  -webkit-transition: 0.3s;
  padding-top: 12px;
  padding-bottom: 12px;
  transition: 0.3s;
  outline: none;
  color: #667085;
}

.dashboard-body-wrapper.align-center {
  max-width: 600px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  background-color: #0f171c;
  padding: 30px 40px;
  width: 93%;
}

.interac-funding-steps{
  margin-bottom: 5%;
  margin-top: 5%;
}

.header{
  color: #FFFFFF;
  font-size: 20px;
}

.connected-banks-list{
  margin-top: 1%;
}

.payment-email-wrapper {
  display: -webkit-box;
  display: -webkit-flex;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
  -webkit-justify-content: space-between;
  -ms-flex-pack: justify;
  justify-content: right;
  -webkit-box-align: center;
  -webkit-align-items: center;
  -ms-flex-align: center;
  align-items: center;
  margin-top: 6%;
}

.text-block-61 {
  color: #ffffff;
  font-size: 17px;
}

.text-block-62 {
  color: #ffffff;
  font-weight: 700;
}

.button{
  color: #FFFFFF;
  text-align: center;
  align-items: center;
  align-content: center;
  padding: 8px 14px;
  gap: 8px;
  font-size: 17px;

  height: 42px;
  border: 0.5px solid #5d78ff;
  background-color: #5d78ff;
  border-radius: 6px;
  margin-top: 3%;
}

.button:hover{
  color: #ffffff;
  border: 0.5px solid #5d78ff;
  background-color: #5d78ff;
  border-radius: 6px;
}

hr {
  border-top: 1px solid #ffffff;
  margin-bottom: 20px;
  margin-top: 20px;
}

.text-3{
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  color: #6c757d;
  padding-top: 1.5%;
  padding-bottom: 2%;
}

.text-4{
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #ffffff;
  padding-top: 3%;
  padding-bottom: 1%;
}

.text-5{
  font-weight: 400;
  font-size: 15px;
  line-height: 24px;
  color: #ffffff;
  padding-top: 2%;
  padding-bottom: 2%;
  word-wrap: break-word; /* or overflow-wrap: break-word; */
}



@media (max-width: 700px) {
  .header{
    font-size: 18px;
  }

  .button{
    padding: 5px 14px;
    font-size: 13px;
    height: 36px;
  }

  hr {
    margin-bottom: 15px;
    margin-top: 15px;
  }

  .dashboard-body-wrapper.align-center {
    max-width: unset;
    padding: 30px 20px;
    width: 100%;
  }

}
</style>