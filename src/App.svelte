<script>
  import Header from "./components/Header.svelte";
  import Timeline from "./components/Timeline.svelte";
  import Sidebar from "./components/Sidebar.svelte";
  import Main from "./components/Main.svelte";
</script>

<Header />
<Main>
  <Timeline />
  <Sidebar />
</Main>

<style>
  :global(body) {
    background-color: #676778;
    color: #ffffff;
  }
</style>
