<template>

  <div>
    <div class='header'>
      <button @click='swapCreate'>Create</button>
      <h1>Battle Bots</h1>
      <button @click='swapList'>Collection</button>
    </div>
  
    <div class="middle">

      <create v-if="showform" :someValue='swapList' @update='submit'>

      </create>

      <bot-list v-else v-for="(botList, i) in bots" :key='i' :listBot='botList' class="botList">

      </bot-list>

    </div>

  </div>
  
</template>

<script>
import Create from './components/Create';
import BotList from './components/BotList';

export default {
   data: function(){
        return{
            bots: [{name: 'RoboCop', attack: 500, health: 400}, {name: 'Johnny Five', attack: 600, health: 500}],
            showform: true,
        }
    },

  methods: {
    
    swapCreate: function(){
      this.showform = true;
    },
    swapList: function(){
      this.showform = false;
    },
    
  },

  components: {
    Create: Create,
    BotList: BotList
  },
}
</script>

<style scoped>

.header{
  display: flex;
  justify-content: space-around;
  height: 25px;
}

.middle{
  border: 1px solid;
  height: 500px;
  
  margin-top: 50px;
  margin-bottom: 10px;
  

}

.lower{
  border: 1px solid;
  height: 500px;
}

.botList{
    display: flex;
    align-items: flex-start;
    flex-wrap: wrap;
}

</style>


