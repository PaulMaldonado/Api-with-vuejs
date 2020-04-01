<template>
    <div>
         <div class="jumbotron jumbotron-fluid">
            <div class="container">
                <h1 class="display-4">Ricky & Morthy</h1>
                <p class="lead">Ricky and Morthy personajes</p>

                <button class="btn btn-primary" @click="printResults">Consultar datos</button>
            </div>
        </div>

        <div class="container">
            <div class="row mt-4">
                <div class="col-md-4 col-sm-12 col-lg-4 col-xl-4" v-for="character in characters" :key="character.id">
                    <div class="card mt-3">
                        <img v-bind:src="character.image" v-bind:alt="character" class="card-img-top">
                        <div class="card-body">
                            <h5 class="card-title">{{ character.name }}</h5>
                            <p class="card-text">{{ character.gender }}</p>
                            <h6 class="card-text">{{ character.status}}</h6>

                            <button class="btn btn-danger ustify-content-around">Eliminar</button>
                            <button class="btn btn-success">Ver más</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    data() {
        return {
            url: 'https://rickandmortyapi.com/api/character',
            characters: [],
        }
    },

    methods: {
        printResults() {
            axios.get(this.url)
                .then(response => {
                    this.characters = response.data.results
                    console.log(response.data.results)
                })

                .catch(error => {
                    console.log(error);
                });
        }
    }
}
</script>

<style scoped>
    
</style>