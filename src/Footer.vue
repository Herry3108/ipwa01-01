<script>
import {
    BNavbar,
    BNavbarNav,
    BNavItem
} from 'bootstrap-vue'

export default {
   components: {
    BNavbar,
    BNavbarNav,
    BNavItem
   },
    name: 'Footer',
    data() {
      return {
        currentYear: new Date().getFullYear()
      }
    }
}
</script>

<template>
  <div 
    id="footer" 
    class="bg-success mx-auto"
  >
    <BNavbar>
      <BNavbarNav class="mx-auto">
        <BNavItem href="#header">
          Datenschutz
        </BNavItem>
        <BNavItem href="#header">
          Impressum
        </BNavItem>
      </BNavbarNav>
    </BNavbar>
    <span>
      <small>
        Copyright © {{ currentYear }}. All Rights Reserved
      </small>
    </span>
  </div>
</template>

<style>
  small {
    color: rgba(0, 0, 0, 0.55);
  }
</style>
