<script>
  import { Icon } from "svelte-icons-pack";
  import { FaSolidHeart, FaSolidCircleUser } from "svelte-icons-pack/fa";

  import { likeCount } from "../store";
</script>

<div class="header">
  <div class="header__content container">
    <div class="header__content_logo">
      <h1>Pugstagram</h1>
    </div>
    <div class="header__content_nav">
      <ul>
        <li class="header__content_like_count">
          <Icon src={FaSolidHeart} />
          <span>{$likeCount === 0 ? "" : $likeCount}</span>
        </li>
        <li>
          <Icon src={FaSolidCircleUser} />
        </li>
      </ul>
    </div>
  </div>
</div>

<style>
  .header {
    background-color: white;
    position: fixed;
    width: 100%;
    border-bottom: 1px solid rgba(38, 38, 38, 0.4);
  }
  .header__content {
    grid-template-columns: minmax(auto, 936px);
    display: grid;
    justify-content: center;
    background-color: white;
  }
  .header__content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.5em;
  }
  .header ul {
    list-style: none;
  }
  .header li {
    display: inline-block;
    margin: 0 0 0 1em;
  }

  .header li.header__content_like_count {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    gap: 3px;
  }

  h1 {
    padding: 0;
    margin: 0;
    font-size: 28px;
    color: black;
    font-family: "Pacifico", cursive;
    cursor: pointer;
    position: relative;
    background: #fff;
    mix-blend-mode: multiply;
    display: inline-block;
  }

  h1:before {
    content: "";
    display: block;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle at top left, #f09433, #bc1888);
    mix-blend-mode: screen;
    position: absolute;
    top: 0;
    left: 0;
  }
</style>
