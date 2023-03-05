<script>
import {
  BCard,
  BAvatar,
  BRow,
  BCol
} from 'bootstrap-vue'

import Teammitglied from './Teammitglied.vue'

export default {
  components: {
    BCard,
    BAvatar,
    BRow,
    BCol,
    Teammitglied
  },
  name: 'Footer',
  data() {
    return {}
  }
}
</script>

<template>
  <div id="team">
    <BCard title="Unser Team">
      <BRow>
        <BCol lg="3">
          <Teammitglied 
            mitgliedname="Manuel Mitarbeiter"
            stelle="Geschäftsführer" 
          />
        </BCol>
        <BCol lg="3">
          <Teammitglied 
            mitgliedname="Bernd Mitarbeiter"
            stelle="Head of Sales" 
          />
        </BCol>
        <BCol lg="3">
          <Teammitglied 
            mitgliedname="Gregor Mitarbeiter"
            stelle="CIO" 
          />
        </BCol>
        <BCol lg="3">
          <Teammitglied 
            mitgliedname="Herbert Mitarbeiter"
            stelle="Softwareentwickler" 
          />
        </BCol>
      </BRow>
    </BCard>
  </div>
</template>

<style></style>
