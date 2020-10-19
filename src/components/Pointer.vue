<template>
  <div class="pointer-container">
    <div class="pointer">
      <p class="pointer-text">Settings</p>
    </div>
    <div class="border-pointer">
      <p class="pointer-text">User and Business Profiles</p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.pointer-container {
  display: flex;
  margin-left: -1.5rem;
  margin-right: auto;
  border: 1px solid #eeeeee;

  .pointer {
    width: 16rem;
    position: relative;
    background: #ffffff;
    padding-top: 7px;
    z-index: 1000;

    ::before {
      content: "";
      position: absolute;
      right: -2rem;
      bottom: 0;
      width: 0;
      height: 0;
      border-left: 2rem solid #ffffff;
      border-top: 2rem solid transparent;
      border-bottom: 2rem solid transparent;
    }
  }
  .pointer-text {
    font-family: "Lato";
    font-style: normal;
    font-weight: normal;
    font-size: 1.6rem;
    line-height: 2rem;
    text-align: center;
    letter-spacing: -0.05px;

    color: #7c7c7c;

    opacity: 0.6;
  }

  .border-pointer {
    background: #eeeeee;
    border-radius: 0px 10px 10px 0px;
    width: 26.9rem;
    position: relative;
    padding-left: 3rem;
    padding-top: 7px;
    display: flex;
    align-items: center;

    ::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: 0;
      width: 0;
      height: 0;
      border-left: 2rem solid white;
      border-top: 2rem solid transparent;
      border-bottom: 2rem solid transparent;
    }
  }
}
</style>
