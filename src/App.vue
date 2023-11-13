<template>
  <div id="app">
    <div class="form-container">
    <form>
  <div class="form-group">
    <label for="surname">Surname</label>
    <input type="text" class="form-control" id="surname" placeholder="Enter your surname">
  </div>
  <div class="form-group">
    <label for="firstName">First Name</label>
    <input type="text" class="form-control" id="firstName" placeholder="Enter your first name">
  </div>
  <div class="form-group">
    <label for="exampleInputEmail1">Email address</label>
    <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp" placeholder="Enter email">
    <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
  </div>
  <div class="form-group">
    <label for="phone">Phone</label>
    <input type="tel" class="form-control" id="phone" placeholder="Enter your phone number">
  </div>
  <div class="form-row">
    <div class="form-group col-md-6">
      <label for="flightNumber">Flight Number</label>
    <input type="text" class="form-control" id="flightNumber" placeholder="Enter your flight number">
    </div>
    <div class="form-group col-md-4">
      <label for="inputState">Country</label>
      <select  class="form-control" id="inputState">
        <option selected>Choose...</option>
      </select>
    </div>
  </div>
  <div class="form-group">
    <label for="birthDate">Birth Date</label>
    <button type="button" class="btn btn-primary" data-toggle="modal" data-target="#datePickerModal">
      Select Birth Date
    </button>
    <!-- Modal for date picker -->
    <div class="modal" id="datePickerModal">
      <!-- Your date picker content here -->
    </div>
  </div>
  <div class="form-group">
    <label for="flightNumber">Flight Number</label>
    <input type="text" class="form-control" id="flightNumber" placeholder="Enter your flight number">
  </div>
  <div class="form-group">
    <label for="hearAbout">How did you hear about us?</label>
    <select class="form-control" id="hearAbout">
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <!-- Add other options -->
    </select>
  </div>
  <div class="form-group">
    <label for="specialRequest">Special Request</label>
    <textarea class="form-control" id="specialRequest" rows="3" placeholder="Enter your special request"></textarea>
  </div>
  <button type="submit" class="btn btn-primary">Submit</button>
</form>

  </div>
</div>
</template>

<script>


export default {
  components: {

  },
  data() {
    return {
      todos: [
        {
          _id: "1",
          title: 'Walk the dog',
          description: 'Go to forrest near the zoo'
        },
        {
          _id: "2",
          title: 'Buy a new PC',
          description: 'preferably a macbook pro M3'
        },
        {
          _id: "3",
          title: 'Go to the gym',
          description: 'Do the Friday program'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
// $color-red: red; -> variable

#app {
  display: flex;
      justify-content: start;
      align-items: center;
      height: 100vh;
      margin: 0;
}

.form-container {
      width: 30%;
      margin: 0 auto;
    }
 

</style>
