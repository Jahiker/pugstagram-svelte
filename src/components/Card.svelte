<script>
  import { blur } from "svelte/transition";
  import { Icon } from "svelte-icons-pack";
  import {
    FaSolidEllipsis,
    FaSolidHeart,
    FaSolidPaperPlane,
    FaSolidBookmark,
  } from "svelte-icons-pack/fa";

  import Comments from "./Comments.svelte";
  import Modal from "./Modal.svelte";
  import Share from "./Share.svelte";

  export let username;
  export let location;
  export let avatar;
  export let photo;
  export let postComment;
  export let comments;

  let isModal = false;

  const handleClick = () => {
    isModal = !isModal;
  };
</script>

<div class="card">
  {#if isModal}
    <div transition:blur>
      <Modal>
        <Share on:click={handleClick} />
      </Modal>
    </div>
  {/if}
  <div class="card__container">
    <div class="card__header">
      <div class="card__user">
        <figure>
          <img src={avatar} alt="Pug" width="50" height="auto" loading="lazy" />
        </figure>
        <h2>
          {username}
          <span>{location}</span>
        </h2>
      </div>
      <div class="card__settings">
        <Icon src={FaSolidEllipsis} />
      </div>
    </div>

    <div class="card__photo">
      <figure>
        <img src={photo} alt="Pug" width="500" height="auto" loading="lazy" />
      </figure>
    </div>

    <div class="card__icons">
      <div class="card__icons_firts">
        <span>
          <Icon src={FaSolidHeart} />
        </span>

        <span on:click={handleClick}>
          <Icon src={FaSolidPaperPlane} />
        </span>
      </div>
      <div class="card__icons_second">
        <Icon src={FaSolidBookmark} />
      </div>
    </div>

    <div class="card__description">
      <h3>{username}</h3>
      <span>{postComment}</span>
    </div>

    <Comments {comments} />
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
