<script>
  import Slider from './Slider.svelte';

  let value1 = $state(0);
  let value2 = $state(0);
  let value3 = $state(0);
  let value4 = $state(0);
  let value5 = $state(0);
  let value6 = $state(0);

  let hasSelected1 = $state(false);
  let hasSelected2 = $state(false);
  let hasSelected3 = $state(false);
  let hasSelected4 = $state(false);
  let hasSelected5 = $state(false);
  let hasSelected6 = $state(false);

  // Hier kannst du Unterüberschriften für jeden Regler festlegen
  let subtitle1 = "Ulm";
  let subtitle2 = "Konstanz";
  let subtitle3 = "Lüneburg";
  let subtitle4 = "Fuldabrück";
  let subtitle5 = "Hamburg";
  let subtitle6 = "München";
</script>

<!-- Überschrift und Unterüberschrift -->
<div class="header">
  <h2>Durchschnittliche Mietpreise in Deutschen Städten</h2>
  <h4>Schätzen Sie den monatlichen Preis und stellen Sie die Regler ein!</h4>
</div>

<!-- Abstand zwischen Überschrift und Reglern -->
<div class="spacer"></div>

<div class="slider-container">
  <!-- Erster Regler mit Unterüberschrift -->
  <div class="slider-item">
    <h5>{subtitle1}</h5>
    <Slider
      min="0"
      max="2000"
      correctValue="1100"
    />
  </div>

  <!-- Zweiter Regler mit Unterüberschrift -->
  <div class="slider-item">
    <h5>{subtitle2}</h5>
    <Slider
      min="0"
      max="2000"
      correctValue="1300"
    />
  </div>

  <!-- Dritter Regler mit Unterüberschrift -->
  <div class="slider-item">
    <h5>{subtitle3}</h5>
    <Slider
      min="0"
      max="2000"
      correctValue="1000"
    />
  </div>

  <!-- Vierter Regler mit Unterüberschrift -->
  <div class="slider-item">
    <h5>{subtitle4}</h5>
    <Slider
      min="0"
      max="2000"
      correctValue="800"
    />
  </div>

  <!-- Fünfter Regler mit Unterüberschrift -->
  <div class="slider-item">
    <h5>{subtitle5}</h5>
    <Slider
      min="0"
      max="2000"
      correctValue="1300"
    />
  </div>

  <!-- Sechster Regler mit Unterüberschrift -->
  <div class="slider-item">
    <h5>{subtitle6}</h5>
    <Slider
      min="0"
      max="2000"
      correctValue="1800"
    />
  </div>
</div>

<style>
  /* Setzt die Schriftart auf Georgia für das gesamte Dokument */
  * {
    font-family: "Georgia", serif;
  }

  /* Styling für Überschrift und Unterüberschrift */
  .header {
    text-align: center;
    margin-bottom: 20px;
  }

  .header h2 {
    font-size: 1.8em;
    margin: 0 0 10px;
  }

  .header h4 {
    font-size: 1.2em;
    margin: 0 0 30px;
    color: #666;
  }

  .spacer {
    height: 30px; /* Abstand zwischen der Überschrift und den Reglern */
  }

  .slider-container {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  /* Styling für die einzelnen Regler mit ihren Unterüberschriften */
  .slider-item {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  h5 {
    font-size: 1.1em;
    margin-bottom: 8px;
    color: #444;
  }
</style>
