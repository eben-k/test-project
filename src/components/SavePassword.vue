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
      <p class="bottom-text">
        For security purposes, you can only change your password once a day
      </p>
    </v-form>
  </div>
</template>
<script>
export default {
  name: "SavePassword",
  data: () => ({
    valid: true
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
    .bottom-text {
      align-self: center;
      margin-top: 5rem;
      font-family: "Lato";
      font-style: normal;
      font-weight: normal;
      font-size: 14px;
      line-height: 17px;
      text-align: center;
      color: #333333;
    }
  }
}
</style>
