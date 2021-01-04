<template>
  <div class="parent">
    <h1>Calculator</h1>
    <div class="frame">
      <div class="screen">
        <Screen :value="value" />
        <div class="digits">
          <Button :digit=item v-for="item in digits" :key="item" @update-data="updateData" />
        </div>
        <div class="operators">
          <Button :digit=item v-for="item in operators" :key="item" />
        </div>
      </div>
    </div>
  </div>

</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Screen from "./Screen.vue";
import Button from "./Button.vue";

@Options({
  data: function(){
    return{
      digits: [
        7,8,9,4,5,6,1,2,3,0
      ],
      operators: [
        "/", "X", "-", "+"
      ],
      value: 0,
    }
  },
  props: {
    msg: String
  },
  components: {
    Screen,
    Button
  },
  methods:{
    updateData: function(value: number){
      this.value = value
    }
  }
})
export default class Frame extends Vue {
  msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="sass">

.frame
  width: 320px
  height: 500px
  background-color: brown
  border: 1px solid black

.digits
  width: 75% 
  float: left

.operators
  width: 25%
  float: left
</style>
