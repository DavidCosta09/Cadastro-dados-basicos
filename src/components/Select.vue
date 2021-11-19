<template>
  <div class="select" :style="styles">
    <label class="label-select">{{label}}</label>
    <select class="sigla">
      <option></option>
      <option class="UF">AC</option>
    </select>
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

<style scoped>
    .select {
    height: 56px;
    width: 90%;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: flex-end;
    
  }

  .label-select{
    position: absolute;
    font-size: 12px;
    background-color: #FFFFFF;
    top: 0;
    left: 10px;
    padding: 0 3px;
    color: #ABABAB;
  }

  .sigla{
    width: 100%;
    height: 49px;
    padding: 0 10px;
    border: 1px solid  #ABABAB;
    border-radius: 4px
  }

  
</style>