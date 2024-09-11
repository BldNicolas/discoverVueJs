<template>
   <div>
    <h1>Mes Personnages</h1>
    <ListCharacters :characters="characters" :limit="limit"></ListCharacters>
    <input type="number" name="limit" v-model="limit">
   </div>
</template>

<script>
import ListCharacters from './components/characters/ListCharacters.vue';

export default {
  components: {
    ListCharacters
  },
  data() {
    return {
      characters: [
        {
          id: 1,
          pseudo: "Tharok",
          hp: 150,
          atk: 25,
          type: "warrior"
        },
        {
          id: 2,
          pseudo: "Eldra",
          hp: 100,
          atk: 40,
          type: "wizard"
        },
        {
          id: 3,
          pseudo: "Baldric",
          hp: 130,
          atk: 20,
          type: "warrior"
        },
        {
          id: 4,
          pseudo: "Lunara",
          hp: 90,
          atk: 35,
          type: "archer"
        },
        {
          id: 5,
          pseudo: "Morgath",
          hp: 110,
          atk: 30,
          type: "necromancer"
        }
      ],
      limit: 99999
    }
  }
}
</script>