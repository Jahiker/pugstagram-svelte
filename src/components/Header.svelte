<script>
  import { Icon } from "svelte-icons-pack";
  import { FaSolidHeart, FaSolidCircleUser } from "svelte-icons-pack/fa";
</script>

<div class="header">
  <div class="header__content container">
    <div class="header__content_logo">
      <h1>Pugstagram</h1>
    </div>
    <div class="header__content_nav">
      <ul>
        <li>
          <Icon src={FaSolidHeart} />
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
    width: 100%;
  }

  .header__content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .header__content_nav > ul {
    list-style: none;
    display: flex;
    justify-content: end;
    align-items: center;
    gap: 10px;
  }
</style>
