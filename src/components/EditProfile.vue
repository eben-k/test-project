<template>
  <div class="form-container">
    <div class="form-header">
      <p class="header-text">Edit Profile Details</p>
      <v-icon>mdi-close</v-icon>
    </div>
    <v-form ref="form" lazy-validation>
      <v-text-field
        label="First Name"
        required
        placeholder="Fariq"
        outlined
        color="#0979a2"
        light
      ></v-text-field>

      <v-text-field
        label="Last Name"
        required
        placeholder="Abdulahi Umar"
        outlined
        color="#0979a2"
        light
      ></v-text-field>

      <v-text-field
        label="E-mail"
        required
        placeholder="fariq.umar@gmail.com"
        outlined
        color="#0979a2"
        light
      ></v-text-field>

      <v-text-field
        label="Phone Number"
        required
        placeholder="08012345678"
        outlined
        color="#0979a2"
        light
      ></v-text-field>
      <div class="form-button">
        <v-btn color="#0CA2D9" large @click="overlay = !overlay">
          Save
        </v-btn>
        <v-overlay :value="overlay" :z-index="zIndex" opacity="0.6">
          <v-icon @click="overlay = !overlay" class="abs-close"
            >mdi-close</v-icon
          >
          <SaveProfile />
        </v-overlay>
      </div>
    </v-form>
  </div>
</template>
<script>
import SaveProfile from "@/components/SaveProfile.vue";
export default {
  name: "EditProfile",
  components: { SaveProfile },
  data: () => ({
    valid: true,
    firstName: "",
    firstNameRules: [
      v => !!v || "First Name is required",
      v => (v && v.length >= 3) || "First Name must be at least 3 characters"
    ],
    lastname: "",
    lastNameRules: [
      v => !!v || "Last Name is required",
      v => (v && v.length >= 3) || "Last Name must be at least 3 characters"
    ],
    email: "",
    emailRules: [
      v => !!v || "E-mail is required",
      v => /.+@.+\..+/.test(v) || "E-mail must be valid"
    ],
    overlay: false,
    zIndex: 10005
  }),

  methods: {
    resetValidation() {
      this.$refs.form.resetValidation();
    }
  }
};
</script>
<style lang="scss" scoped>
.form-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  border-radius: 4px;
  width: auto;
  min-width: 60rem;

  .form-header {
    display: flex;
    background: linear-gradient(180deg, #0ca2d9 9.38%, #0082c8 100%);
    box-shadow: 0px 2px 2px rgba(50, 50, 71, 0.06),
      0px 2px 4px rgba(50, 50, 71, 0.06);
    width: 100%;
    padding: 1.1rem 1.3rem;
    align-items: center;
    justify-content: space-between;

    .header-text {
      font-family: "Lato";
      font-style: normal;
      font-weight: 500;
      font-size: 1.6rem;
      line-height: 1.9rem;

      color: #ffffff;
    }

    .v-icon.v-icon {
      align-self: flex-start;
    }
  }
  .v-form {
    width: 100%;
    padding: 2rem 1.3rem;
    background: #fafafa;
    display: flex;
    flex-direction: column;

    .theme--dark.v-input {
      color: #333333;
      font-family: "Lato";
      font-style: normal;
      font-weight: normal;
      font-size: 14px;
      line-height: 17px;
    }

    .form-button {
      margin-top: 5rem;
      align-self: center;
      .v-btn {
        text-transform: capitalize;
        padding: 7px 5.6rem;
        font-family: "Lato";
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 19px;
        text-align: center;
      }
      .abs-close {
        position: absolute;
        left: 915px;
        top: 20px;
        z-index: 5000000;
      }
    }
  }
}
</style>
