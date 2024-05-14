<main class="main">
  <div class="main__container container">
    <slot />
  </div>
</main>

<style>
  .main {
    display: grid;
    grid-template-columns: minmax(auto, 936px);
    justify-content: center;
    background-color: #fafafa;
  }
  .main__container {
    display: grid;
    grid-template-columns: 3fr 1fr;
    grid-gap: 2em;
    padding: 2em 0;
  }

  @media screen and (max-width: 768px) {
    .main__container {
      grid-template-columns: 1fr;
    }
  }
</style>
