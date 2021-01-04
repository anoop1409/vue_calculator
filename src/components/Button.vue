<template>
  <button class="number-button">
    {{digit}}
  </button>

</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    digit: Number
  }
})
export default class Button extends Vue {
  msg!: string;
}
</script>

<style scoped lang="sass">
.number-button
  width: 80px
  height: 50px
  font-size: 30px
  float: left
</style>
