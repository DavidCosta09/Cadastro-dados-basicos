<template>
  <div id="app">

    <Header/>
    <!--Criação da div pai para formatar todo o espaço do formulário-->

    <div class="formulario">
      <!--criação de dicv para texto principal -->
      <div class="cabecalho">
        
        <button class="pesquisar" click="">Pesquisar</button>
      </div>

      <!--Criação dos campos para preenchimento do formulário -->

      <div class="codigo">
        <label class="interno">Código Interno</label>
        <Input label="Código Externo" styles="max-width: 434px"/>
      </div>

      <div class="codigo">
        <Input label="Nome Fantasia" styles="max-width: 400px" />
        <Input label="Razão Social" styles="max-width: 400px"/>

        <div class="pfpj">
          <label class="indic">Indic. PJ/PF</label>
          <div class="radios">
            <div class="radio">
              <input type="radio" class="pj" nome="pj" value="" />
              <label class="pj-pf">PJ</label>
            </div>

            <div class="radio">
              <input type="radio" class="pj" nome="pf" value="" />
              <label class="pj-pf">PF</label>
            </div>
          </div>
        </div>
      </div>

      <div class="codigo">
        <Input label="CNPJ/CPF" styles="max-width: 320px"/>

        <Input label="Insc. Est" styles="max-width: 320px"/>

        <Select styles="max-width: 77px" label="UF"/>

        <Input label="CULT" styles="max-width: 400px"/>
      </div>

      <div class="codigo">
        <Input label="Tempo Permanencia" styles="max-width: 400px"/>
        <Input label="Insc. Municipal" styles="max-width: 400px"/>
        <InputData />
      </div>

      <div class="codigo">
        <div class="radios">
          <div class="radio one">
            <input type="radio" class="pj" nome="nao-contribuinte"  value="" />
            <label class="pj-pf">Não Contribuinte</label>
          </div>
          
          <div class="radio one">
              <input type="radio" class="pj" nome="isento" value="" />
              <label class="pj-pf">Isento de CNPJ Nr. Doc Estrangeiro</label>
          </div>
          
        </div>

        <Input label="" styles="max-width: 340px"/>

        <div class="radio two">
          <input type="radio" class="pj" nome="especial" value="" />
          <label class="pj-pf">Cliente Especial</label>
        </div>
      </div>

      <div class="codigo">
        <label class="cnae">CNAE</label>
        <Input label="" styles="max-width: 200px"/>

        <Input label="Tempo Permanencia" styles="max-width: 580px"/>

        <Select styles="max-width: 294px" label="Atividade Economica"/>
      </div>
    </div>
  </div>
</template>

<script>
import InputData from './components/InputData.vue'
import Input from './components/Input.vue'
import Select from './components/Select.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    InputData,
    Input,
    Select,
    Header
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: #2c3e50;
  margin: 0;
  padding: 0;
  width: 100%;
}

.formulario {
  width: 100%;
  background: #ffffff;
  margin: 0 auto;
  margin-top: 60px;
  max-width: 1170px;
  border-radius: 4px;
  box-shadow: 2px 2px 2px #00000020;
  padding: 30px 20px;
 }

.cabecalho {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  margin-bottom: 20px;
}

.pesquisar {
  width: 108px;
  height: 36px;
  font-size: 12px;
  background-color: #1e90ff;
  border-radius: 100px;
  color: #ffff;
  border: 0;
  cursor: pointer;
}

.codigo {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 20px;
}

.interno {
  font-size: 16px;
  color: #ababab;
  font-weight: 400px;
}

.pfpj {
  width: 300px;
  height: 56px;
  font-size: 16px;
  color: #26283b;
  display: flex;
  flex-direction: column;
  padding-top: 11px;
}

.indic {
  font-size: 16px;
  font-weight: 500;
  margin-bottom: 5px;
  color: #26283b;
}

.radios {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}

.radio{
  width: auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.one{
  margin-right: 30px;
}

.two{
  width: 300px;
  justify-content: initial;
}

.pj {
  margin-bottom: 5px;
  width: 18px;
  height: 18px;
  margin-right: 10px;
}

.pj-pf {
  font-size: 16px;
  font-weight: 400;
  color:#26283b
}

.cnae{
  font-size: 16px;
  font-weight: 400;
  color: #26283b
}
</style>
