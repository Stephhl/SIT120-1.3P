<template>
  <form class="formContact" @submit.prevent="submitForm">
    <div class="form-group">
      <h1 class="ContactHeader">Contact</h1>
    </div>
    <div class="form-group">
      <label for="firstName">First Name:</label>
      <input
        type="text"
        id="firstName"
        placeholder="E.g. John"
        v-model="formData.firstName"
        required
      />
    </div>
    <div class="form-group">
      <label for="lastName">Last Name:</label>
      <input
        type="text"
        id="lastName"
        placeholder="E.g. Dutch"
        v-model="formData.lastName"
        required
      />
    </div>
    <div class="form-group">
      <label for="email">Email:</label>
      <input
        type="email"
        id="email"
        placeholder="E.g. JohnDutch@email.com"
        v-model="formData.email"
        required
      />
    </div>
    <label for="message">Message:</label>
    <div class="form-group">
      <textarea
        id="message"
        v-model="formData.message"
        placeholder="E.g. Hi there! ...."
        rows="6"
      ></textarea>
    </div>
    <div class="form-group">
      <label>
        <input type="checkbox" v-model="formData.isCopy" /> Would you like a
        copy sent to your email?
      </label>
    </div>
    <div class="form-group" v-if="formData.isCopy">
      <p>You will be sent a copy.</p>
    </div>
    <div class="form-group">
      <button type="submit" class="SubmitButton">Submit</button>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        firstName: "",
        lastName: "",
        email: "",
        isCopy: false,
      },
    };
  },
  methods: {
    submitForm() {
      alert("Will get back to you!");
    },
  },
};
</script>

<style scoped>
.formContact {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  border: 2px solid green;
  padding: 20px;
  background-color: rgb(202, 202, 198);
  margin: 20px auto;
  max-width: 400px;
  flex-direction: column;
}

label {
  font-weight: bold;
  font-size: 20px;
  color: black;
}

.form-group {
  margin-top: 5px;
  background-color: rgb(202, 202, 198);
}

.ContactHeader {
  font-weight: bold;
  text-decoration: underline;
  text-align: center;
  margin-bottom: 5px;
  color: black;
}

.SubmitButton {
  background-color: rgb(28, 204, 28);
  color: white;
  border: none;
  border-radius: 10%;
  width: 100px;
  height: 30px;
  font-size: 20px;
  cursor: pointer;
  transition: background-color 0.15s ease-in-out;
}

.SubmitButton:hover {
  background-color: rgb(230, 20, 20);
}
</style>
