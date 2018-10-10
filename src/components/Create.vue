<template>
    <div>
        <div class="createBox">
            <h3>Bot Name*</h3>
            <input type="text" v-model="bot.name">
            <h3>Attack Points*</h3>
            <input type="number" v-model="bot.attack">
            <h3>Health Points*</h3>
            <input type="number" v-model="bot.health">

            <div>
                <button @click="submit">Submit</button>
                <button @click='clear'>Clear</button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
    data: function() {
        return {
            bot: {name: '', attack: '', health: ''}
    };

  },

  methods: {
      clear: function(){
          this.bot = {name: '', attack: '', health: ''}
      },
      submit: function(){
      
          this.Bots = this.bot;
          this.swapList();
      }
  }
};
            
</script>

<style scoped>
.createBox {
  border: 1px solid;
  width: 300px;
  height: auto;
  padding: 10px;
  margin: auto;
  margin-top: 30px;
}
</style>

