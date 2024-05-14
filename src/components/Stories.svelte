<script>
  import Avatar from "../assets/avatar.jpg";
</script>

<div class="stories">
  <div class="stories__container">
    <div class="stories__head">
      <h3>Historias</h3>
      <span>Ver todas</span>
    </div>
    <div class="stories__items">
      <div class="stories__item">
        <div class="stories__item_box">
          <img
            src={Avatar}
            alt="Avatar User"
            width="40"
            height="40"
            loading="lazy"
          />
        </div>
        <h2>
          jahiker
          <span>10 horas antes</span>
        </h2>
      </div>
    </div>
  </div>
</div>

<style>
  .stories {
    border: 1px solid rgba(219, 219, 219, 1);
    border-radius: 4px;
    margin: 1em 0;
    padding: 0.5em 1em;
    background-color: white;
  }
  .stories__item img {
    width: 32px;
    height: 32px;
    border-radius: 50%;
  }
  .stories__item {
    display: flex;
    align-items: center;
    margin: 0 0 0.5em 0;
  }
  .stories__item h2 {
    font-size: 14px;
    color: black;
    margin: 0 0 0 0.5em;
  }
  .stories__item h2 span {
    display: block;
    font-size: 9px;
    text-transform: uppercase;
    color: gray;
  }
  .stories__head {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.5em 0 0 0;
  }
  .stories__head h3 {
    font-size: 12px;
    font-weight: 600;
  }
  .stories__head span {
    font-size: 12px;
    font-weight: normal;
    color: black;
  }
  .stories__items {
    margin: 0.5em 0 0.5em 0;
  }
  .stories__item_box {
    width: 32px;
    height: 32px;
    border: double 2px transparent;
    border-radius: 100%;
    background-image: linear-gradient(#fff, #fff),
      radial-gradient(circle at top left, #f09433, #bc1888);
    background-origin: border-box;
    background-clip: content-box, border-box;
  }
</style>
