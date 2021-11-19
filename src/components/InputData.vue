<template>
  <div class="data">
    <label class="data-label">Data Nascimento</label>
    <input type="date" class="data-input"/>
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default defineComponent({
  setup() {
    
  },
})
</script>

<style scoped>

  .data {
    height: 56px;
    width: 90%;
    max-width: 280px;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: flex-end;  
  }

  .data-label{
    position: absolute;
    font-size: 12px;
    background-color: #FFFFFF;
    top: 0;
    left: 10px;
    padding: 0 3px;
    color: #ABABAB
  }

  .data-input{
    width: 100%;
    height: 45px;
    padding: 0 10px;
    border: 1px solid  #ABABAB;
    border-radius: 4px
  }

  .data-input[type=date]{
    color:#ABABAB;
  }

</style>
