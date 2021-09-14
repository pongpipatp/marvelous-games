<template>
    <div>
        <div class="d-flex flex-wrap">
            <v-card
                v-for="games in results"
                :key="games.id"
                class="ma-2 mt-8"
                max-width="344"
                :to="{path: '/games/gameDetail/' + games.id}"
                @click="handleGameClicked(games)"
                
                
            >
                <v-img
                :src="games.thumbnail"
                height="200px"
                ></v-img>

                <v-card-title>
                {{ games.title }}
                </v-card-title>

                <v-card-subtitle>
                {{ games.short_description }}
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
             alignments: [
        'start',
        'center',
        'end',
      ],
            results: [],
            id: 0
        }
    },
    created() {
        this.loadGameList()
         
    }, 
    methods: {
        loadGameList() {
            // v-for="games in results" :keys="games.id"
            const config = {
                headers: {
                    "x-rapidapi-key": '2a50aee9e6msh55cf8498c0e6c1ap1c932fjsn9403eb2b255d',
                    "x-rapidapi-host": "free-to-play-games-database.p.rapidapi.com"
                }
            }
            const url = "https://free-to-play-games-database.p.rapidapi.com/api/games"
            axios.get(url, config).then((res) => {
                this.results = res.data
                // console.log(res.data);
            })
        },
        handleGameClicked(games) {
            // console.log("Games", games.id);
            this.id = games.id

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