<template>
  <div class="parent">
    <h1>Calculator</h1>
    <div class="frame">
      <div class="screen">
        <Screen />
      </div>
    </div>
  </div>

</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Screen from "./Screen.vue";

@Options({
  props: {
    msg: String
  },
  components: {
    Screen
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
  border: 1px solid black
</style>
