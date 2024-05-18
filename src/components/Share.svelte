<script>
  import { Icon } from "svelte-icons-pack";
  import { FaSolidCircleXmark, FaBrandsFacebook } from "svelte-icons-pack/fa";
</script>

<div class="share">
  <div class="share__head">
    <h2>Compartir</h2>
    <span on:click>
      <Icon src={FaSolidCircleXmark} />
    </span>
  </div>
  <div class="share__content">
    <a
      href="http://www.facebook.com/sharer/sharer.php?&u=https://pugstagram.com"
    >
      <Icon src={FaBrandsFacebook} />
      Compartir en Facebook
    </a>
  </div>
</div>

<style>
  .share {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    background-color: white;
    margin: 0 0 2em 0;
    width: 300px;
    height: 80px;
    position: absolute;
    top: 300px;
    left: 30%;
    z-index: 9;
    padding: 1em;
  }
  .share__head {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .share__head h2 {
    font-size: 16px;
  }
  .share__head svg {
    cursor: pointer;
  }
  .share__content a {
    display: flex;
    align-items: center;
    text-decoration: none;
    color: black;
    font-size: 14px;
    margin: 2em 0 0 0;
  }
  .share__content svg {
    color: #3b5998;
    margin: 0 0.5em 0 0;
    font-size: 20px;
  }
</style>
