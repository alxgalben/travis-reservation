<template>
  <div id="app">
    <div class="card w-25 p-3">
      <div class="card-body">
        <h5 class="card-title">Personal Data</h5>
        <div class="form-container">
          <form>

            <div class="row">
              <div class="col">
                <label for="firstName">First Name</label>
                <input type="text" class="form-control" id="firstName" placeholder="Enter your first name">
              </div>
              <div class="col">
                <label for="surname">Last Name</label>
                <input type="text" class="form-control" id="surname" placeholder="Enter your last name">
              </div>
            </div>

            <div class="row">
              <div class="col">
                <label for="exampleInputEmail1">Email address</label>
                <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp"
                  placeholder="Enter your email">
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
                <input type="tel" class="form-control" id="phone" placeholder="Enter your phone number">
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
                  <!-- Add other options -->
                </select>
              </div>
            </div>

            <div class="form-group">
              <label for="specialRequest">Special Request</label>
              <textarea class="form-control" id="specialRequest" rows="3"
                placeholder="Enter your special request"></textarea>
            </div>

            <button type="submit" class="btn btn-warning">Submit</button>
          </form>

        </div>
      </div>
    </div>
  </div>
</template>

<script>


export default {
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

.card {
  margin-left: 50px;
  min-width: 550px;

  &-title {
    font-size: 40px;
    margin-bottom: 20px;
  }
}

.form-group {
  margin: 10px 0;
}

.btn-warning {
  margin-top: 10px;
}

.row {
  margin-top: 20px;
}

label {
  margin-bottom: 3px;
}
</style>
