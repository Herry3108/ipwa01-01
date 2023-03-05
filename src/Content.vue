<script>
import {
  BContainer,
  BTable,
  BFormGroup,
  BInputGroup,
  BFormInput,
} from 'bootstrap-vue'
import Team from './Team.vue'

import { tablefields } from '../js/tablefields.js'
import { tableitems } from '../js/tableitems.js'

export default {
    components: {
      BContainer,
      BTable,
      BFormGroup,
      BInputGroup,
      BFormInput,
      Team
    },
    name: "Content",
    data() {
      return {
        filter: "",
        tablefields: tablefields,
        tableitems: tableitems
      };
    },
    methods: {
      filterTable: function(row, filter) {
        return row.land.toLowerCase().includes(filter.toLowerCase());
      }
    }
}
</script>

<template>
  <div id="content">
    <BContainer>
      <BFormGroup class="d-flex justify-content-end">
        <BInputGroup size="sm">
          <BFormInput
            id="filter-input"
            v-model="filter"
            type="search"
            placeholder="Land suchen"
          ></BFormInput>
        </BInputGroup>
      </BFormGroup>
      <BTable
        striped
        bordered
        hover
        class="mb-4"
        head-variant="light"
        label-sort-asc=""
        label-sort-desc=""
        id="tabelle" 
        :items="tableitems"
        :filter="filter"
        :filter-function="filterTable"
        :fields="tablefields">
      </BTable>

      <Team />
      
    </BContainer>
  </div>
</template>

<style>  
  #content {
    margin-bottom: 4em;
  }
</style>

