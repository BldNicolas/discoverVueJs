<template>
    <div class="character-list">
        <CardCharacters
            v-for="character in limitCharacter"
            :key="character.id"
            :character="character"
        ></CardCharacters>
    </div>
</template>

<script>
import CardCharacters from "@/components/characters/CardCharacters.vue";

export default {
    components: {
        CardCharacters,
    },
    props: {
        characters: Array,
        limit: Number,
    },
    computed: {
        limitCharacter() {
            return this.characters.slice(0, this.limit)
        }
    }
};
</script>

<style scoped>
.character-list {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
}
</style>
