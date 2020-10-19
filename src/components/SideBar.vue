<template>
  <div class="sidebar-container">
    <div class="bottom-logo-box">
      <v-img src="../assets/mzuri.svg"></v-img>
    </div>
  </div>
</template>

<script>
export default {
  name: "SideBar"
};
</script>
<style lang="scss" scoped>
.sidebar-container {
  .bottom-logo-box {
    background: #ffffff;
    display: flex;
    align-items: center;
    width: 100%;
    padding: 2px 3.4rem;
    margin-bottom: 0;
    align-self: end;
  }
}
</style>
