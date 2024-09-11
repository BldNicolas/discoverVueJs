<template>
    <div class="character-card">
        <header class="character-card-header">
            <img
                :src="`http://picsum.photos/800/400?random=${character.id}`"
                :alt="`Avatar - ${character.pseudo}`"
            />
        </header>
        <div class="character-card-content">
            <h3>
                {{ getEmojiFromType(character.type) }}
                {{ character.pseudo }}
            </h3>
            <ul>
                <li>PV : {{ character.hp }}</li>
                <li>ATK : {{ character.atk }}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        character: Object,
        limit: Number,
    },
    methods: {
        getEmojiFromType(type) {
            const typeToEmoji = {
                warrior: "⚔️",
                archer: "🏹",
                wizard: "🧙‍♂️",
            };
            return typeToEmoji[type];
        },
    },
};
</script>

<style scoped>
.character-card {
    box-shadow: 2px 2px 1rem rgba(0, 0, 0, 0.1);
    border-radius: 1rem;
}

.character-card-header img {
    width: 100%;
    border-top-left-radius: 0.5rem;
    border-top-right-radius: 0.5rem;
}
</style>
