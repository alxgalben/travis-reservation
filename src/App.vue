<template>
  <div id="app">

    <!-- MAIN CARD -->


    <div class="card main w-25 p-3">
      <div class="card-body">
        <h5 class="card-title">Personal Data</h5>
        <div class="form-container">
          <form>

            <div class="row">
              <div class="col">
                <label for="firstName">First Name</label>
                <input type="text" class="form-control" id="firstName" placeholder="Enter your first name"
                  v-model="formData.firstName" :class="{ 'is-invalid': !validateFirstName() }">
                <div class="invalid-feedback">Please enter a valid first name.</div>
              </div>
              <div class="col">
                <label for="lastName">Last Name</label>
                <input type="text" class="form-control" id="lastName" placeholder="Enter your last name"
                  v-model="formData.lastName" :class="{ 'is-invalid': !validateLastName() }">
                <div class="invalid-feedback">Please enter a valid last name.</div>
              </div>
            </div>

            <div class="row">
              <div class="col">
                <label for="exampleInputEmail1">Email address</label>
                <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp"
                  placeholder="Enter your email" v-model="formData.email" :class="{ 'is-invalid': !validateEmail() }">
                <div class="invalid-feedback">Please enter a valid email address.</div>
              </div>
              <div class="col">
                <label for="inputState">Country</label>
                <select class="form-control" id="inputState">
                  <option selected>Choose...</option>
                </select>
              </div>
            </div>

            <div class="row">
              <div class="col">
                <label for="phone">Phone</label>
                <input type="tel" class="form-control" id="phone" placeholder="Enter your phone number"
                  v-model="formData.phone" :class="{ 'is-invalid': !validatePhoneNumber() }">
                <div class="invalid-feedback">Please enter a valid phone number.</div>
              </div>
              <div class="col">
                <label for="dob">Date of Birth</label>
                <input type="date" class="form-control" id="dob">
              </div>
            </div>

            <div class="row">
              <div class="col">
                <label for="flightNumber">Flight Number</label>
                <input type="text" class="form-control" id="flightNumber" placeholder="Enter your flight number">
              </div>
              <div class="col">
                <label for="hearAbout">How did you hear about us?</label>
                <select class="form-control" id="hearAbout">
                  <option value="0"></option>
                  <option value="1">Internet search (Google)</option>
                  <option value="2">Google sponsored ad</option>
                  <option value="3">Social networks</option>
                  <option value="4">Facebook ad</option>
                  <option value="5">By recommendation</option>
                  <option value="6">Airport office</option>
                  <option value="7">Direct access to the site</option>
                  <option value="8">I am a loyal customer</option>
                  <option value="9">Another source</option>
                </select>
              </div>
            </div>

            <div class="form-group">
              <label for="specialRequest">Special Request</label>
              <textarea class="form-control" id="specialRequest" rows="3"
                placeholder="Enter your special request"></textarea>
            </div>

            <div class="alert alert-warning" role="alert">
              Make the full payment now and get a 5% DISCOUNT of the rental rate on the spot! Use the "PAYNOW" coupon to
              get the discount.
            </div>

            <div class="input-group mb-3">
              <input type="text" class="form-control" id="voucher-code-input" placeholder="Do you have a voucher?"
                aria-label="Do you have a voucher?" aria-describedby="basic-addon2">
              <div class="input-group-append">
                <button class="btn btn-outline-warning" id="btn-discount" type="button">Apply discount!</button>
              </div>
            </div>
          </form>

        </div>
      </div>
    </div>


    <!-- END OF MAIN CARD -->


    <!-- SECOND CARD -->


    <div class="card another w-75 p-3">
      <div class="card-body" style="text-align: center;">
        <div class="alert alert-warning" role="alert" style="text-align: center;">
          <h1>THE FINAL PRICE WILL BE:</h1>
        </div>
        <div class="big-text" style="margin-top: 50px;">
          <h1 style="font-size: 40px;"><span class="strikethrough">144 €</span></h1>
          <h1 style="font-size: 100px;">123 €</h1>
        </div>
      </div>
      <div class="row rowcard" style="margin-bottom: 20px;">
        <div class="col-sm-4">
          <div class="card" style="text-align: center;">
            <div class="card-body">
              <h1>
                <p class="card-text">0 €</p>
              </h1>
              <input type="radio" class="btn-check" name="payment-option" id="btn-check-0" autocomplete="off">
              <label class="btn btn-outline-warning" for="btn-check-0" style="margin-top: 15px;">I WILL PAY
                LATER!</label><br>
            </div>
          </div>
        </div>
        <div class="col-sm-4">
          <div class="card" style="text-align: center;">
            <div class="card-body">
              <h1>
                <p class="card-text">50 €</p>
              </h1>
              <input type="radio" class="btn-check" name="payment-option" id="btn-check-50" autocomplete="off">
              <label class="btn btn-outline-warning" for="btn-check-50" style="margin-top: 15px;">I PAY PART
                NOW!</label><br>
            </div>
          </div>
        </div>
        <div class="col-sm-4">
          <div class="card" style="text-align: center;">
            <div class="card-body">
              <h1>
                <p class="card-text">123 €</p>
              </h1>
              <input type="radio" class="btn-check" name="payment-option" id="btn-check-123" autocomplete="off">
              <label class="btn btn-outline-warning" for="btn-check-123" style="margin-top: 15px;">I PAY FULL
                NOW!</label><br>
            </div>
          </div>
        </div>
      </div>

      <div class="form-check form-check">
        <input class="form-check-input" type="checkbox" id="inlineCheckbox1" value="option1">
        <label class="form-check-label" for="inlineCheckbox1">
          I agree with <a href="https://rentacar.travis.ro/en/car-rental-terms-and-conditions" target="_blank"> booking
            terms and conditions </a> and <a href="https://rentacar.travis.ro/en/privacy-policy" target="_blank"> privacy
            policy </a>
        </label>
      </div>
      <div class="form-check form-check">
        <input class="form-check-input" type="checkbox" id="inlineCheckbox2" value="option2">
        <label class="form-check-label" for="inlineCheckbox2">
          I want to create an account on rentacar.travis.ro
        </label>
      </div>
      <div class="form-check form-check">
        <input class="form-check-input" type="checkbox" id="inlineCheckbox3" value="option3">
        <label class="form-check-label" for="inlineCheckbox3">
          I want to be the first to find out about special offers and benefits offered by Travis Rent a Car
        </label>
      </div>

      <button type="submit" class="btn btn-warning" style="font-weight: bold; margin-bottom: 20px;">COMPLETE YOU
        BOOKING</button>
    </div>


    <!-- END OF SECOND CARD -->


  </div>
</template>

<script>


export default {
  data() {
    return {
      formData: {
        firstName: '',
        lastName: '',
        email: '',
        phone: '',
      }
    };
  },
  methods: {
    validateFirstName() {
      const regex = /^[A-Za-z\s]{2,}$/;
      return regex.test(this.formData.firstName);
    },
    validateLastName() {
      const regex = /^[A-Za-z\s]{2,}$/;
      return regex.test(this.formData.lastName);
    },
    validateEmail() {
      const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      return regex.test(this.formData.email);
    },
    validatePhoneNumber() {
      const regex = /^\d{10}$/;
      return regex.test(this.formData.phone);
    },
  },
  mounted() {
    const input = document.querySelector("#phone");
    window.intlTelInput(input, {
      utilsScript: "https://cdn.jsdelivr.net/npm/intl-tel-input@18.2.1/build/js/utils.js",
    });

    // const country = document.querySelector(".countrypicker");
    // country.countrypicker();
  }
}

</script>

<style lang="scss" scoped>
#app {
  display: flex;
  justify-content: start;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.main {
  margin-left: 50px;
  min-width: 550px;
  height: 85vh;
  overflow-y: auto;
}

.card-title {
  font-size: 40px;
  margin-bottom: 20px;
}

.form-group {
  margin: 10px 0;
}

.btn-warning {
  margin-top: 10px;
}

.row {
  margin-top: 5px;
}

label {
  margin-bottom: 3px;
}

.alert {
  margin: 20px 0;
}

.another {
  margin: 0 50px;
  height: 85vh;
  min-width: none;
  overflow-y: auto;
}

.strikethrough {
  position: relative;
}

.strikethrough:before {
  position: absolute;
  content: "";
  left: 0;
  top: 50%;
  right: 0;
  border-top: 3px solid;
  border-color: inherit;

  -webkit-transform: rotate(-20deg);
  -moz-transform: rotate(-20deg);
  -ms-transform: rotate(-20deg);
  -o-transform: rotate(-20deg);
  transform: rotate(-20deg);
}

#btn-discount {
  border-radius: 0 5px 5px 0;
}</style>
