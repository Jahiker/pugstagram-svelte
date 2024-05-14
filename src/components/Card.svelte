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
        <figure>
          <img
            src="https://c.files.bbci.co.uk/14EC6/production/_124820758_pug1.jpg"
            alt="Pug"
            width="50"
            height="auto"
            loading="lazy"
          />
        </figure>
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

<style>
  .card {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    background-color: white;
    margin: 0 0 2em 0;
  }
  .card__header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1em;
  }
  .card__user {
    display: flex;
    align-items: center;
    justify-content: flex-end;
  }
  .card__user figure {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    overflow: hidden;
  }

  .card__user img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: center;
  }
  .card__user h2 {
    margin: 0;
    padding: 0;
    font-size: 14px;
    font-weight: 600;
    margin: 0 0 0 1em;
    color: black;
  }
  .card__user h2 span {
    display: block;
    font-size: 12px;
    font-weight: normal;
    color: rgba(38, 38, 38, 0.7);
  }
  .card__photo {
    padding: 0;
    margin: 0;
  }
  .card__photo img {
    width: 100%;
    height: auto;
  }
  .card__photo figure {
    margin: 0;
    padding: 0;
    cursor: pointer;
  }
  .card__settings svg {
    cursor: pointer;
  }
  .card__icons {
    padding: 1em;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .card__icons svg {
    margin: 0 1em 0 0;
    cursor: pointer;
    font-size: 20px;
  }
  .card__icons svg:last-child {
    margin: 0;
  }
  .card__description {
    padding: 0 1em 1em 1em;
  }
  .card__description h3 {
    font-size: 14px;
    font-weight: bold;
    color: black;
  }
  .card__description span {
    font-size: 14px;
  }
  .active-like {
    color: #bc1888;
    animation: bounce linear 0.8s;
    animation-iteration-count: 1;
    transform-origin: 20% 20%;
  }
  .active-bookmark {
    color: #f09433;
  }

  @keyframes bounce {
    0% {
      transform: translate(0px, 0px);
    }
    15% {
      transform: translate(0px, -25px);
    }
    30% {
      transform: translate(0px, 0px);
    }
    45% {
      transform: translate(0px, -15px);
    }
    60% {
      transform: translate(0px, 0px);
    }
    75% {
      transform: translate(0px, -5px);
    }
    100% {
      transform: translate(0px, 0px);
    }
  }
</style>
