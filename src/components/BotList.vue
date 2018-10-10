<template>
    <div>
        <div class="botList">
            <div class="botCard">
                <h3>{{this.listBot.name}}</h3>
                <h3>{{this.listBot.attack}}</h3>
                <h3>{{this.listBot.health}}</h3>

                <div>
                    <button>Select</button>
                    <button @click="retire">Retire</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {

    data: function(){
        return{

        }
    },

    methods: {
        retire: function(){
            this.listbot[0].remove()
        }
    },

   props: ['listBot']
};
</script>

<style scoped>

.topCollec{
    height: 150px;
    border: 1px solid;
}

.botCard{
    
    border: 1px solid;
    width: 150px;
    height: 200px;
    margin: auto;
}



</style>


