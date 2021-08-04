<template>
  <div>
    <hr />

    <div class="column">
      <section class="section" id="results">
        <div class="box alert alert-secondary">
          <ul>
            <!-- loop through all the `form` properties and show their values -->
            <li v-for="(key, value) in form" v-bind:key="key.id">
              <strong>{{ value }}:</strong> {{ key }}
            </li>
          </ul>
        </div>
      </section>
    </div>
    <form style="text-align: left" v-on:submit.prevent="formSubmit">
      <!-- Binding Text Field -->
      <div class="form-group">
        <label for="name">Name</label>
        <input
          type="text"
          class="form-control"
          id="name"
          placeholder="Your name"
          v-model="form.name"
        />
      </div>
      <!-- Binding Email Field -->
      <div class="form-group">
        <label for="email">Email address</label>
        <input
          type="email"
          class="form-control"
          id="email"
          placeholder="name@example.com"
          v-model="form.email"
        />
      </div>
      <!-- Binding Radio Buttons -->
      <div class="form-group">
        <label for="formControlRange">Gender</label><br />
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="radio"
            name="gender"
            id="gender-male"
            value="male"
            v-model="form.gender"
          />
          <label class="form-check-label" for="gender">Male</label>
        </div>
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="radio"
            name="gender"
            id="gender-female"
            value="female"
            v-model="form.gender"
          />
          <label class="form-check-label" for="gender">Female</label>
        </div>
      </div>
      <!-- Binding Select Box -->
      <div class="form-group">
        <label for="refer">From where did you hear about us?</label>
        <select
          name="refer"
          class="form-control"
          id="refre"
          v-model="form.refer"
        >
          <option value="website">Website</option>
          <option value="newspaper">Newspaper</option>
          <option value="friend">Friend</option>
          <option value="online-ad">Online Ad</option>
          <option value="other">Other</option>
        </select>
      </div>
      <!-- Binding Multi Select Box -->
      <div class="form-group">
        <label for="exampleFormControlSelect2">You are a : </label>
        <select
          multiple
          class="form-control height-in-group"
          id="exampleFormControlSelect2"
          v-model="form.profession"
        >
          <option value="developer">Developer</option>
          <option value="designer">Graphic Designer</option>
          <option value="manager">Manager</option>
          <option value="ceo">Company Head / CEO</option>
          <option value="other">Other</option>
        </select>
      </div>
      <!-- Binding Multiple Check Boxes -->
      <div class="form-group">
        <label for="formControlRange"
          >Which of our service are you interested in?</label
        ><br />
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="checkbox"
            id="inlineCheckbox1"
            value="online"
            v-model="form.interested"
          />
          <label class="form-check-label" for="inlineCheckbox1"
            >Online Tests</label
          >
        </div>
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="checkbox"
            id="inlineCheckbox2"
            value="paper"
            v-model="form.interested"
          />
          <label class="form-check-label" for="inlineCheckbox2"
            >Paper Based Tests</label
          >
        </div>
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="checkbox"
            id="inlineCheckbox3"
            value="customized"
            v-model="form.interested"
          />
          <label class="form-check-label" for="inlineCheckbox3"
            >Customized Tests</label
          >
        </div>
      </div>
      <!-- Binding TextArea -->
      <div class="form-group">
        <label for="message">Your message</label>
        <textarea
          name="message"
          class="form-control"
          id="message"
          rows="3"
          v-model="form.message"
        ></textarea>
      </div>
      <!-- Binding Range Input -->
      <div class="form-group selector-color">
        <label for="satisfaction"
          >How satisfied are you with our service?</label
        >
        <input
          type="range"
          name="satisfaction"
          class="form-control-range"
          id="formControlRange"
          min="0"
          max="10"
          v-model="form.satisfaction"
        />
      </div>
      <!-- Binding Single Checbox -->
      <div class="form-group">
        <div class="form-check form-check-inline">
          <input
            class="form-check-input"
            type="checkbox"
            id="terms"
            value="yes"
            v-model="form.terms"
          />
          <label class="form-check-label" for="inlineCheckbox3"
            >Agree to Terms & Conditions</label
          >
        </div>
      </div>

      <div class="form-group">
        <button class="btn btn-primary">Submit</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "InputBinding",
  data() {
    return {
      form: {
        name: "",
        email: "",
        gender: "",
        refer: "",
        profession: [],
        interested: [],
        message: "",
        satisfaction: "",
        terms: false,
      },
    };
  },
  methods: {
    formSubmit: function (event) {
      console.log(this.form.name);
      console.log(this.form.email);
      console.log(this.form.gender);
      console.log(this.form.refer);
      console.log(this.form.profession);
      console.log(this.form.interested);
      console.log(this.form.message);
      console.log(this.form.satisfaction);
      console.log(this.form.terms);
      event.target.reset();
    },
  },
};
</script>

<style scoped>
form {
  background-color: cadetblue;
  padding: 15px;
}
.height-in-group {
  height: 120px !important;
}
input[type="range"],
input[type="range"]::-webkit-slider-runnable-track,
input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
}

input[type="range"]:focus {
  outline: none;
}

input[type="range"]::-webkit-slider-thumb {
  margin-top: -9px;
}

input[type="range"]:focus::-webkit-slider-runnable-track {
  outline: none;
}
</style>