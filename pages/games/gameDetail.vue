<template>
    <div>
        <div>
        <p>{{ gameId }}</p>
            <v-card
                class="mx-auto mt-4"
                max-width="950"
            >
                <v-img
                :src="results.thumbnail"
                height="450px"
                ></v-img>

                <v-card-title>
                {{ results.title }}
                </v-card-title>

                <v-card-subtitle>
                {{ results.description }}
                </v-card-subtitle>
            </v-card>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return {
            gameId: this.$route.params.id,
            results: []
        }
    },
    created() {
        this.loadGameDetail()
         
    }, 
    methods: {
        loadGameDetail() {
            // v-for="games in results" :keys="games.id"
            const config = {
                headers: {
                    "x-rapidapi-key": '2a50aee9e6msh55cf8498c0e6c1ap1c932fjsn9403eb2b255d',
                    "x-rapidapi-host": "free-to-play-games-database.p.rapidapi.com"
                }
            }
            // console.log(this.gameId);
            const url = "https://free-to-play-games-database.p.rapidapi.com/api/game?id=3"
            axios.get(url, config).then((res) => {
                this.results = res.data
            //  console.log(res.data);
            })
        }
    }
}
</script>

<style scoped>
.card-div {
    height: 800px;
    overflow-y: auto;
}
</style>