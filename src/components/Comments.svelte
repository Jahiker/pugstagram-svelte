<div class="comments">
  <div class="comments__content">
    <div class="comments__users">
      <h3>Jahiker</h3>
      <span>Hola Elmo</span>
    </div>
    <div class="comments__form">
      <form>
        <input
          type="text"
          class="comments__input"
          placeholder="Agregar comentario"
          id="comments__input"
        />
        <button type="submit">Post</button>
      </form>
    </div>
  </div>
</div>

<style>
  .comments h3 {
    font-size: 14px;
    color: black;
    font-weight: bold;
    margin: 0;
    padding: 0;
  }
  .comments span {
    font-size: 14px;
    margin: 0 0 0 0.5em;
    font-weight: normal;
    color: rgba(black, 0.9);
  }
  .comments__form {
    padding: 1em 1em 1em 1em;
    border-top: 1px solid rgba(219, 219, 219, 0.8);
  }
  .comments__form form {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .comments__content {
    padding: 0 1em 0.5em 1em;
  }
  .comments__users {
    margin: 0 0 0.5em 0;
    display: flex;
  }

  input {
    border: solid 1px #e9e9e9;
    border-radius: 5px;
    color: #696969;
    border: 1px solid transparent;
    font-size: 12px;
    outline: none;
    width: 100%;
    display: flex;
  }
  button {
    border: none;
    color: #3897f0;
    font-size: 12px;
    outline: none;
    cursor: pointer;
  }
  label {
    display: none;
  }
</style>