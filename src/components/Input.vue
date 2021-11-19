<template>
  <div class="input" :style="styles">
    <label class="texto">{{label}}</label>
    <input class="input-texto"/>
  </div>
</template>

<script>
export default {
  props: {
    label: String,
    styles: String
  }
}
</script>

<style  scoped>

  .input {
    height: 56px;
    width: 90%;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    
  }

  .texto{
    position: absolute;
    font-size: 12px;
    background-color: #FFFFFF;
    top: 0;
    left: 10px;
    padding: 0 3px;
    color: #ABABAB
  }

  .input-texto{
    width: 100%;
    height: 45px;
    padding: 0 10px;
    border: 1px solid  #ABABAB;
    border-radius: 4px
  }


</style>