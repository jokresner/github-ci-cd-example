<script>
  let count = 0;
  let step = 1;

  const increment = () => {
    count += step;
  };

  const decrement = () => {
    count -= step;
  };
</script>

<style>
  main {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 2em;
  }

  h1 {
    color: #4caf50;
  }

  button {
    background-color: #4caf50;
    color: white;
    border: none;
    padding: 0.5em 1em;
    margin: 0.5em;
    cursor: pointer;
    font-size: 1em;
  }

  button:hover {
    background-color: #45a049;
  }

  input {
    width: 50px;
    text-align: center;
  }
</style>

<main>
  <h1>Simple Counter</h1>
  <p>Count: <strong>{count}</strong></p>

  <div>
    <button on:click={decrement}>-</button>
    <button on:click={increment}>+</button>
  </div>

  <div>
    <label for="step">Step:</label>
    <input id="step" type="number" bind:value={step} min="1" />
  </div>
</main>

