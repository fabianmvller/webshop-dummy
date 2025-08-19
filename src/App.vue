<template>
  <h1>Angebot</h1>
  <div class="centered-text">
    <p>Füllen Sie bitte das Formular aus. Wir melden uns schnellstmöglich mit Ihrem individuellen Angebot.</p>
  </div>

  <div class="card" role="region" aria-labelledby="form-title">
    <form action="#" method="post" novalidate>
      <div class="form-grid">

        <div class="field col-12 angebot-feld">
          <label for="angebot_fuer">Angebot für</label>
          <input
            id="angebot_fuer"
            name="angebot_fuer"
            type="text"
            :value="'EVA-aha'"
            readonly
          />
        </div>

        <div class="field col-3">
          <label for="anrede">Anrede</label>
          <select id="anrede" name="anrede" autocomplete="honorific-prefix">
            <option value="">– bitte wählen –</option>
            <option>Frau</option>
            <option>Herr</option>
            <option>Divers</option>
          </select>
        </div>

        <div class="field col-4">
          <label for="vorname">Vorname<span class="req" aria-hidden="true">*</span></label>
          <input id="vorname" name="vorname" type="text" required autocomplete="given-name" />
        </div>

        <div class="field col-5">
          <label for="nachname">Nachname<span class="req" aria-hidden="true">*</span></label>
          <input id="nachname" name="nachname" type="text" required autocomplete="family-name" />
        </div>

        <div class="field col-6">
          <label for="funktion">Funktion</label>
          <input id="funktion" name="funktion" type="text" autocomplete="organization-title" />
        </div>

        <div class="field col-6">
          <label for="institution">Institution</label>
          <input id="institution" name="institution" type="text" autocomplete="organization" />
        </div>

        <div class="field col-12">
          <label for="firma">Institut/Schule/Firma</label>
          <input id="firma" name="firma" type="text" autocomplete="organization" />
        </div>

        <div class="field col-6">
          <label for="telefon">Tel.-Nr.</label>
          <input id="telefon" name="telefon" type="tel" inputmode="tel"
                 placeholder="+49 731 123456"
                 autocomplete="tel" />
        </div>

        <div class="field col-6">
          <label for="email">E-Mail<span class="req" aria-hidden="true">*</span></label>
          <input id="email" name="email" type="email" required autocomplete="email" />
        </div>

        <div class="field col-8">
          <label for="strasse">Straße / Hausnr.<span class="req" aria-hidden="true">*</span></label>
          <input id="strasse" name="strasse" type="text" required autocomplete="address-line1" />
        </div>

        <div class="field col-4">
          <label for="plz">Postleitzahl<span class="req" aria-hidden="true">*</span></label>
          <input id="plz" name="plz" type="text" required
                 inputmode="numeric" pattern="^\d{5}$"
                 autocomplete="postal-code" />
        </div>

        <div class="field col-12">
          <label for="ort">Ort<span class="req" aria-hidden="true">*</span></label>
          <input id="ort" name="ort" type="text" required autocomplete="address-level2" />
        </div>

        <!-- Neue Checkboxen -->
        <div class="field col-12 checkbox-field">
          <label>
            <input type="checkbox" name="datenschutz" required />
            Ich willige ein, dass meine personenbezogenen Daten zur Erstellung eines Kundenkontos und zur Erstellung des Angebots verarbeitet werden. Weitere Informationen können der Datenschutzerklärung entnommen werden.
          </label>
        </div>

        <div class="field col-12 checkbox-field">
          <label>
            <input type="checkbox" name="newsletter" />
            Ja, ich möchte den monatlichen Newsletter abonnieren.
          </label>
        </div>

      </div>

      <p class="hint">Felder mit <span class="req">*</span> sind erforderlich.</p>

      <div class="actions">
        <button type="reset" class="btn btn-secondary">Zurücksetzen</button>
        <button type="submit" class="btn btn-primary">Absenden</button>
      </div>
    </form>
  </div>
</template>

<style scoped>

h1, h2, h3 {
  text-align: center;
  color: #F25A29;
}
.centered-text {
  text-align: center;
  margin-bottom: 1em;
}
.angebot-info {
  text-align: center;
  font-size: 1.2rem;
  margin-bottom: 1em;
}
.card {
  max-width: 880px;
  margin: 0 auto;
  border-radius: 12px;
  box-shadow: 0 6px 18px rgba(0,0,0,.06);
  padding: 1.25rem 1.25rem 1.5rem;
}
.field.angebot-feld {
  margin-bottom: 2rem;
}
p.hint {
  margin: 0 0 1rem;
  font-size: .95rem;
}
form {
  display: grid;
  gap: 1rem;
}
.form-grid {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(12, 1fr);
}
.col-3{ grid-column: span 3; }
.col-4{ grid-column: span 4; }
.col-5{ grid-column: span 5; }
.col-6{ grid-column: span 6; }
.col-8{ grid-column: span 8; }
.col-12{ grid-column: span 12; }
.field label {
  display: inline-block;
  margin-bottom: .4rem;
}
.req {
  margin-left: .25rem;
}
input, select {
  width: 100%;
  box-sizing: border-box;
  border: 1px solid #ccc;
  border-radius: 10px;
  padding: .65rem .8rem;
  font-size: 1rem;
  background: #fdfdfd;
}
input:focus, select:focus {
  outline: none;
  background: #fff;
  box-shadow: 0 0 0 3px color-mix(in oklab, transparent);
}
.checkbox-field {
  font-size: 0.95rem;
  line-height: 1.4;
}
.checkbox-field input {
  width: auto;
  margin-right: 0.5rem;
  accent-color: #F25A29;
}
.actions {
  display: flex;
  gap: .75rem;
  justify-content: flex-end;
  margin-top: .5rem;
}
.btn {
  appearance: none;
  border: 0;
  border-radius: 10px;
  cursor: pointer;
  padding: .7rem 1.1rem;
  font-size: 1rem;
  font-weight: 600;
}
.btn-primary {
  background:#F25A29;
  color: white;
}
.btn-primary:hover {
  filter: brightness(0.98);
}
.btn-secondary {
  background: #ececf3;
  color: #333;
}
@media (max-width: 760px){
  .form-grid{ grid-template-columns: 1fr; }
  .col-3, .col-4, .col-5, .col-6, .col-8, .col-12{ grid-column: 1 / -1; }
  .actions{ justify-content: stretch; }
  .actions .btn{ width: 100%; }
}
</style>
