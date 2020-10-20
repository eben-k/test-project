<template>
  <div class="form-container">
    <div class="form-header">
      <p class="header-text">Change Password</p>
      <v-icon>mdi-close</v-icon>
    </div>
    <v-form ref="form" lazy-validation>
      <v-text-field
        required
        placeholder="Old Password"
        outlined
        color="#0979a2"
        light
      ></v-text-field>

      <v-text-field
        required
        placeholder="New Password"
        outlined
        color="#0979a2"
        light
      ></v-text-field>

      <v-text-field
        required
        placeholder="Confirm Password"
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
          <SavePassword />
        </v-overlay>
      </div>
    </v-form>
  </div>
</template>
<script>
import SavePassword from "@/components/SavePassword.vue";

export default {
  name: "ChangePassword",
  components: { SavePassword },
  data: () => ({
    valid: true,
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
