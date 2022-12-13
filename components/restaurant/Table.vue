<script setup lang="ts">

import restaurants from "@/data.json"
const restaurantsOrganized = {
    // Prend les restaurants de l'index 0 jusqu'à 25
    first: [...restaurants].splice(0,25),
    // Prend les restaurants de l'index 25 jusqu'au 25 derniers
    second: [...restaurants].splice(25,25)
}

</script>


<template>
    <div class="table">
        <h1 class="font-bold text-2xl">TOP 50: THE RANKING</h1>
        <div class="table-container">
            <div class="table-col">
                <RestaurantRow :isHeader= true />
                <RestaurantRow v-for="(restaurant, index) in restaurantsOrganized.first" 
                :key="restaurant.id"
                :name="restaurant.name"
                :rank="restaurant.rank"
                :index="index"/>
            </div>
            <div class="table-col">
                <RestaurantRow :isHeader= true />
                <RestaurantRow v-for="(restaurant, index) in restaurantsOrganized.second" 
                :key="restaurant.id"
                :name="restaurant.name"
                :rank="restaurant.rank"
                :index="index"/>
            </div>
        </div>
    </div>
</template>
 

<style scoped>

    .table {
        display: initial;
    }
    .table h1 {
        margin-bottom: 2rem;
        margin-left: 5rem;
    }

    .table-container {
        display: flex;
        justify-content: space-between;
    }

    .table-col {
        width: 48%;
        margin-left: 5rem;
    }

</style>