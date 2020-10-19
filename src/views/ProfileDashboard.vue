<template>
  <div class="dashboard">
    <div class="topbar">
      <TopBar />
    </div>
    <div class="sidebar">
      <SideBar />
    </div>
    <div class="main-content">
      <MainContent />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import TopBar from "@/components/TopBar.vue";
import SideBar from "@/components/SideBar.vue";
import MainContent from "@/components/MainContent.vue";

export default {
  name: "Profile",
  components: { TopBar, SideBar, MainContent }
};
</script>

<style lang="scss" scoped>
.dashboard {
  display: grid;
  grid-template-columns: 13.1rem 1fr;
  grid-template-rows: 6rem 1fr;

  .sidebar {
    grid-column: 1/2;
    background: linear-gradient(180deg, #0ca2d9 22.4%, #0077a3 83.85%);
    box-shadow: 0px 0px 0px rgba(63, 63, 68, 0.05),
      0px 1px 3px rgba(63, 63, 68, 0.15);
    display: flex;
    flex-direction: column;
    min-height: 70rem;
    justify-content: flex-end;
  }

  .topbar {
    grid-row: 1/-1;
    grid-column: 1/-1;
    background: #ffffff;
    box-shadow: 0px 0px 1px rgba(0, 0, 0, 0.12);
    display: flex;
    align-items: center;
  }

  .main-content {
    grid-column: 2/-1;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 0 1.5rem;
  }
}
</style>
