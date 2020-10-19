<template>
  <div class="container">
    <div class="pointer-info-container">
      <Pointer />
      <v-icon color="#333333">mdi-alert-circle-outline</v-icon>
    </div>
    <div class="central-logo-container">
      <v-img src="../assets/bc.svg"></v-img>
      <div class="central-logo-textbox">
        <h4 class="logo-text">Boldseams Couture</h4>
      </div>
    </div>
    <div class="personal-info-container">
      <div class="profile-header-box">
        <p class="header-text">My Profile</p>
        <div class="action-container">
          <p class="action-text">Change Password</p>
          <p class="action-text">Edit</p>
        </div>
      </div>
      <div class="info-flexbox">
        <div class="info-container">
          <p class="title-text">Name</p>
          <p class="info-text">Fariq</p>
        </div>
        <div class="info-container">
          <p class="title-text">Email</p>
          <p class="info-text">fariq.umar@gmail.com</p>
        </div>
      </div>
      <div class="info-container">
        <p class="title-text">Phone Number</p>
        <p class="info-text">08012345678</p>
      </div>
    </div>
    <div class="personal-info-container">
      <div class="profile-header-box">
        <p class="header-text">Businesses</p>
        <div class="action-container">
          <p class="plain-text">
            <v-icon color="#0CA2D9" class="ma-4">mdi-plus-circle</v-icon>
            Add Business
          </p>
        </div>
      </div>
      <div class="info-flexbox">
        <div class="business-box" v-for="(item, index) in items" :key="index">
          <p class="plain-text">{{ item.businessName }}</p>
          <p class="title-text">{{ item.businessId }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Pointer from "@/components/Pointer.vue";
export default {
  name: "MainContent",
  components: { Pointer },
  data: () => {
    return {
      items: [
        {
          businessName: "Boldseams Stitches",
          businessId: "RC-906374"
        },
        {
          businessName: "East-West Farmers",
          businessId: "BN-905374"
        },
        {
          businessName: "Mizzle Pharmaceuticals",
          businessId: "RC-907864"
        },
        {
          businessName: "Wigan Automobile",
          businessId: "BN-524374"
        }
      ]
    };
  }
};
</script>
<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;

  .pointer-info-container {
    display: flex;
    width: 100%;
    align-items: flex-start;
  }

  .central-logo-container {
    display: flex;
    flex-direction: column;
    align-self: center;
    align-items: center;
    margin-top: 3rem;

    .central-logo-textbox {
      margin-top: 1.9rem;

      .logo-text {
        font-family: "Lato";
        font-style: normal;
        font-weight: 600;
        font-size: 2rem;
        line-height: 2.4rem;
        text-align: center;

        color: #0979a2;
      }
    }
  }

  .personal-info-container {
    background: #ffffff;
    border: 1px solid rgba(124, 124, 124, 0.2);
    box-sizing: border-box;
    border-radius: 4px;
    margin-top: 3rem;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 2rem 5rem;
    width: 100%;

    .profile-header-box {
      display: flex;
      align-items: center;
      width: 100%;

      .header-text {
        margin-right: auto;
        font-family: "Lato";
        font-style: normal;
        font-weight: bold;
        font-size: 1.4rem;
        line-height: 1.7rem;
        text-align: center;
        color: #7c7c7c;
      }

      .action-container {
        display: flex;
        align-items: center;
        cursor: pointer;

        .action-text {
          font-family: "Lato";
          font-style: normal;
          font-weight: normal;
          font-size: 1.4rem;
          line-height: 1.7rem;
          text-decoration-line: underline;
          color: #0ca2d9;
          &:not(:last-child) {
            margin-right: 2rem;
          }
        }
      }
    }

    .info-container {
      display: flex;
      flex-direction: column;
      border-bottom: 1px solid #eaeaea;
      align-items: flex-start;
      width: auto;
      min-width: 40rem;

      &:not(:last-child) {
        margin-right: 4.7rem;
      }

      .info-text {
        font-family: "Lato";
        font-style: normal;
        font-weight: normal;
        font-size: 1.4rem;
        line-height: 1.7rem;
        color: #333333;
      }
    }

    .title-text {
      font-family: "Lato";
      font-style: normal;
      font-weight: normal;
      font-size: 1.4rem;
      line-height: 1.7rem;
      color: #7c7c7c;
    }

    .info-flexbox {
      display: flex;
      width: 100%;
      flex-wrap: wrap;

      &:not(:last-child) {
        margin-bottom: 1.3rem;
      }
    }

    .plain-text {
      font-family: "Lato";
      font-style: normal;
      font-weight: normal;
      font-size: 1.4rem;
      line-height: 1.7rem;
      color: #0ca2d9;
    }

    .business-box {
      display: flex;
      flex-direction: column;
      border: 0.5px solid rgba(124, 124, 124, 0.4);
      box-sizing: border-box;
      border-radius: 4px;
      padding: 6px 1.6rem;
      align-items: flex-start;
      width: auto;
      min-width: 40rem;
      margin-bottom: 3rem;

      &:not(:last-child) {
        margin-right: 4.7rem;
      }
    }

    .flex-column {
      display: flex;
      flex-direction: column;
    }
  }
}
</style>
