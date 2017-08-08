<template>
  <div class="hello">
  
    <md-toolbar>
      <md-button class="md-icon-button">
        <md-icon>menu</md-icon>
      </md-button>
  
      <h3 class="md-title" style="flex: 1">{{ msg }}</h3>
  
      <md-button class="md-icon-button">
        <md-icon>star</md-icon>
      </md-button>
    </md-toolbar>
  
    
  
    <form novalidate @submit.stop.prevent="submit" id="form">
      <md-input-container>
        <label>Initial value</label>
        <md-input v-model="initialValue"></md-input>
      </md-input-container>
  
      <md-input-container>
        <label>Autocomplete (with fetch)</label>
        <md-input v-model="autocompleteValue" :fetch="fetchFunction"></md-input>
      </md-input-container>
  
      <md-input-container>
        <label>With label</label>
        <md-input placeholder="My nice placeholder"></md-input>
      </md-input-container>
  
      <md-input-container md-inline>
        <label>Inline field</label>
        <md-input></md-input>
      </md-input-container>
  
      <md-input-container>
        <label>Number</label>
        <md-input type="number"></md-input>
      </md-input-container>
  
      <md-input-container>
        <label>Textarea</label>
        <md-textarea></md-textarea>
      </md-input-container>
  
      <md-input-container>
        <label>Disabled</label>
        <md-input disabled></md-input>
      </md-input-container>
  
      <md-input-container md-clearable>
        <label>Clearable</label>
        <md-input v-model="initialValue"></md-input>
      </md-input-container>
    </form>
  
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      msg: 'vuejs material boilerplate'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

#form{
  margin-left: 200px;
   margin-right: 200px;
}
</style>
