<template>
  <div class="topbar-container">
    <div class="logo-box">
      <div class="logo">
        <h5 class="logo-text">BC</h5>
      </div>
      <div class="logo-namebox">
        <h5 class="logo-name">Boldseams Couture</h5>
      </div>
    </div>
    <div class="profile-detail-box">
      <div class="notification-container">
        <v-badge
          color="#F72F09"
          content="5"
          overlap
          offset-y="15"
          offset-x="20"
        >
          <v-icon large color="#000000">
            mdi-bell-outline
          </v-icon>
        </v-badge>
      </div>
      <div class="username-box">
        <p class="username-text">Seun James</p>
        <p class="logout-text">
          Log out
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TopBar"
};
</script>

<style lang="scss" scoped>
.topbar-container {
  padding: 1rem 1.6rem;
  display: flex;
  width: 100%;
  background: #ffffff;
  box-shadow: 0px 0px 1px rgba(0, 0, 0, 0.12);
  align-items: center;
  justify-content: center;

  .logo-box {
    display: flex;
    margin-right: auto;
    font-family: "Roboto";
    font-style: normal;
    font-weight: bold;
    color: #333333;

    .logo {
      background: #ffffff;
      border: 0.4px solid #c7c7c7;
      border-radius: 1rem;
      padding: 1rem 7px;
      margin-right: 8px;

      .logo-text {
        font-size: 2rem;
        line-height: 100%;
        text-align: center;
      }
    }
    .logo-namebox {
      display: flex;
      align-items: center;

      .logo-name {
        font-size: 1.6rem;
        line-height: 120%;
      }
    }
  }

  .profile-detail-box {
    display: flex;
    font-family: "Lato";

    .notification-container {
      margin-right: 3.6rem;
      cursor: pointer;
    }

    .username-box {
      display: flex;
      flex-direction: column;
      align-content: flex-end;
      cursor: pointer;

      .username-text {
        font-style: normal;
        font-weight: normal;
        font-size: 1.2rem;
        line-height: 1.4rem;
        text-align: right;

        color: #343434;
      }

      .logout-text {
        text-align: right;
        color: #1665d8;
        text-decoration: underline;
        margin-top: -1.4rem;
      }
    }
  }
}
</style>
