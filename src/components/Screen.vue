<template>
  <div class="screen">
    1234567890
  </div>

</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    msg: String
  }
})
export default class Screen extends Vue {
  msg!: string;
}
</script>

<style scoped lang="sass">
.screen
  width: 100%
  height: 60px
  border-bottom: 1px solid black
  background-color: white
  font-size: 50px
  text-align: right
</style>
