<script>
  import Avatar from "../assets/avatar.jpg";
</script>

<div class="profile">
  <div class="profile__content">
    <div class="profile__content_avatar">
      <img
        src={Avatar}
        alt="Avatar User"
        width="100"
        height="100"
        loading="lazy"
      />
    </div>
    <div class="profile__content_info">
      <h2>@jahiker</h2>
      <span>Jahiker Rojas</span>
    </div>
  </div>
</div>

<style>
  .profile__content {
    display: flex;
    align-items: center;
  }
  .profile__content_avatar img {
    width: 42px;
    height: 42px;
    border-radius: 50%;
  }
  .profile__content_info {
    margin: 0 0 0 0.5em;
  }
  .profile__content_info h2 {
    font-size: 14px;
    color: black;
    margin: 0;
    padding: 0;
  }
  .profile__content_info span {
    font-size: 12px;
    font-weight: normal;
  }
</style>
