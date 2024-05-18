<script>
  import { onMount } from "svelte";

  import Header from "./components/Header.svelte";
  import Timeline from "./components/Timeline.svelte";
  import Sidebar from "./components/Sidebar.svelte";
  import Main from "./components/Main.svelte";

  let data = {};
  const API = "https://kittygram-api.vercel.app/";

  onMount(async () => {
    const response = await fetch(API);
    data = await response.json();
  });
</script>

<Header />
<Main>
  <Timeline posts={data.posts} />
  <Sidebar />
</Main>
