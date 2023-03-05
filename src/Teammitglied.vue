<script>
import {
  BAvatar,
} from 'bootstrap-vue'

export default {
  components: {
    BAvatar
  },
  props: {
    mitgliedname: {
      type: String,
      required: true
    },
    stelle: {
      type: String,
      required: true
    }
  },
  name: 'Footer',
  data() {
    return {}
  }
}
</script>

<template>
  <div>
    <BAvatar size="8rem"></BAvatar>
    <br>
    <h3> {{ mitgliedname }}</h3>
    <h5> {{ stelle }} </h5>
  </div>
</template>

<style></style>
