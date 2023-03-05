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
    name: "Header",
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
  <div id="header">
    <BNavbar
      toggleable="lg" 
      variant="success"
      sticky
    > 
      <BNavbarBrand 
        href="#"
        class="ms-4">
        <img 
          src="./assets/recycled-bag.png"  
          height="35"
        />
      </BNavbarBrand>
      <BNavbarToggle target="nav-collapse"></BNavbarToggle>
      <BCollapse            
        id="nav-collapse" 
        is-nav
      >
        <BNavbarNav>
          <BNavItem href="#header"
          >
            <BIcon icon="house-door-fill"/>
            Startseite
          </BNavItem>
          <BNavItem href="#tabelle">
            <BIcon icon="table"/>
            Tabelle
          </BNavItem>
        </BNavbarNav>
      </BCollapse>
    </BNavbar>
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
    background-color: rgb(0,0,0); /* Fallback color */
    background-color: rgba(0,0,0, 0.4); /* Black w/opacity/see-through */
    color: white;
    border: 1px solid #f1f1f1c9;
    border-radius: 5px;
    padding: 20px;
    text-align: center;
  }
</style>
