<template>
  <div>
    <h1>Calculator</h1>
    <div class="frame">

    </div>
  </div>

</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({
  props: {
    msg: String
  }
})
export default class Frame extends Vue {
  msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">
.frame
  width: 500px
  height: 600px
  background-color: brown
</style>
