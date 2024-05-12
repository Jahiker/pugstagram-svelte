<script>
  import { Icon } from "svelte-icons-pack";
  import {
    FaSolidEllipsis,
    FaSolidHeart,
    FaSolidPaperPlane,
    FaSolidBookmark,
  } from "svelte-icons-pack/fa";
  import Comments from "./Comments.svelte";
</script>

<div class="card">
  <div class="card__container">
    <div class="card__header">
      <div class="card__user">
        <img
          src="https://c.files.bbci.co.uk/14EC6/production/_124820758_pug1.jpg"
          alt="Pug"
          width="50"
          height="auto"
          loading="lazy"
        />
        <h2>
          Elmo.pug
          <span>Bogotá, Colombia</span>
        </h2>
      </div>
      <div class="card__settings">
        <Icon src={FaSolidEllipsis} />
      </div>
    </div>

    <div class="card__photo">
      <figure>
        <img
          src="https://c.files.bbci.co.uk/14EC6/production/_124820758_pug1.jpg"
          alt="Pug"
          width="500"
          height="auto"
          loading="lazy"
        />
      </figure>
    </div>

    <div class="card__icons">
      <div class="card__icons_firts">
        <Icon src={FaSolidHeart} />
        <Icon src={FaSolidPaperPlane} />
      </div>
      <div class="card__icons_second">
        <Icon src={FaSolidBookmark} />
      </div>
    </div>

    <div class="card__description">
      <h3>elmo.pug</h3>
      <span>Hola!!!</span>
    </div>
    
    <Comments />
  </div>
</div>
