<script>
  import Profile from "./Profile.svelte";
  import Stories from "./Stories.svelte";
  import Footer from "./Footer.svelte";
</script>

<div class="sidebar">
  <div class="sidebar__container">
    <Profile />
    <Stories />
    <Footer />
  </div>
</div>

<style>
  .sidebar {
    position: relative;
    padding: 4.5em 0 0 0;
  }
  .sidebar__container {
    position: fixed;
  }
</style>
