<script>
import { userMeldungen } from '../js/konstanten.js'

import {
  BNavbar,
  BNavbarToggle,
  BCollapse,
  BNavbarNav,
  BNavItem,
  BNavbarBrand,
  BJumbotron,
  BRow,
  BCol,
  BButton,
  BIcon
} from 'bootstrap-vue'

export default {
  components: {
    BNavbar,
    BNavbarToggle,
    BCollapse,
    BNavbarNav,
    BNavItem,
    BNavbarBrand,
    BJumbotron,
    BRow,
    BCol,
    BButton,
    BIcon
  },
  name: "HeaderContent",
  data() {
    return {
      userMeldungen: userMeldungen
    };
  },
  methods: {
    gebeUserMeldungShopAus: function () {
      document.getElementById("user-meldungen").innerText = this.userMeldungen.shopMeldung;
      document.getElementById("user-meldungen").style.color = "red";
    }
  }
}
</script>

<template>
  <div id="header-content">
    <BRow>
      <BCol 
        lg="8" 
        offset-lg="2" 
        sm="12" 
        offset-sm="0"
      >
        <BJumbotron 
          class="ps-5 pt-5 pe-5 text-white hintergrund-bild custom-jumbotron" 
          header="Umwelthelden GmbH"
          lead="Fairtrade Stofftaschen -  Bei uns steht der Mensch an erster Stelle!" bg-variant="light"
          border-variant="muted"
        >
          <div class="vordergrund mb-4">
            <p class="text-left mt-4 mb-4">
              Willkommen! Wir freuen uns sehr, dass Sie des Weg auf unsere Webseite gefunden haben. Unser Unternehmen
              spezialisiert sich auf die Fairtrade-Produktion
              Stofftaschen für den Einzelhandel.
            </p>
            <BButton 
              variant="primary" 
              href="#tabelle" 
              id="emission-button"
            >
              CO²-Emission
            </BButton>
            <BButton 
              variant="success" 
              href="#" 
              @click="gebeUserMeldungShopAus"
            >
              Taschen bestellen
            </BButton>
          </div>
        </BJumbotron>
      </BCol>
    </BRow>
    <small id="user-meldungen"></small>
  </div>
</template>

<style>
@media (max-width: 992px) {
  #emission-button {
    margin-bottom: 5px;
  }
}

.hintergrund-bild {
  background-image: url("./assets/cloth-bag.jpg");
  background-position: center;
  background-repeat: no-repeat;
}

.custom-jumbotron {
  border: none !important;
}

.vordergrund {
  background-color: rgb(0, 0, 0);
  background-color: rgba(0, 0, 0, 0.4);
  color: white;
  border: 1px solid #f1f1f1c9;
  border-radius: 5px;
  padding: 20px;
  text-align: center;
}
</style>
