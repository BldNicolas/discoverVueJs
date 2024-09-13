<template>
    <h1>Money Converter</h1>
    <div class="input-wrapper">
        <div class="currency-card">
            <label for="euro">Euro :</label>
            <input
                type="number"
                v-model="euro"
                @input="convertToFrancs(euro)"
            />
        </div>
        <div class="currency-card">
            <label for="francs">Francs :</label>
            <input
                type="number"
                v-model="francs"
                @input="convertToEuro(francs)"
            />
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            euro: 0,
            francs: 0,
			convertionRateEuroToFrancs: 6.55957
        };
    },
    methods: {
        convertToFrancs(euro) {
            this.francs = euro * this.convertionRateEuroToFrancs;
        },
        convertToEuro(francs) {
            this.euro = francs / this.convertionRateEuroToFrancs;
        },
    },
};
</script>

<style scoped>
.input-wrapper {
    display: flex;
    gap: 1rem;
    flex-direction: column;
}

.currency-card {
	display: flex;
	gap: 1rem;
	background-color: #ddd;
	border-radius: 1rem;
	padding: 1rem;
	min-width: 1rem;
}
</style>
