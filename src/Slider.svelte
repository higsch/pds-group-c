<script>
  const { min, max, correctValue } = $props();

  let value = $state(0);
  let hasSelected = $state(false);
</script>

<div class="container">
  <div class="input-container">
    <input
      type="range"
      min={min}
      max={max}
      step="100" 
      bind:value={value}
      onchange={() => hasSelected = true}
    />
    <span
      class:is-correct-and-selected={value == correctValue && hasSelected}
      class:is-not-correct-and-selected={value != correctValue && hasSelected}
    >
      {value}
    </span>
  </div>

  {#if hasSelected}
  <div class="input-container">
    <input
      type="range"
      min={min}
      max={max}
      value={correctValue}
      disabled
    />
    <span
      class="correct-value"
    >
      {correctValue}
    </span>
  </div>
  {/if}
</div>

<style>
  .container {
    display: flex;
    flex-direction: column;
    margin-bottom: 20px;
    align-items: center; /* Zentriert die Regler horizontal */
    width: 100%;
  }

  .input-container {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 50%; /* Regler sind jetzt nur halb so breit wie der Bildschirm */
    max-width: 400px; /* Optionale Begrenzung der maximalen Breite */
  }

  input[type="range"] {
    width: 100%; /* Füllt die Breite des Containers aus */
  }

  .is-correct-and-selected {
    color: green;
  }

  .is-not-correct-and-selected {
    color: red;
  }

  .correct-value {
    color: green;
  }
</style>
