<template>
    <span class="spoiler">
        <span v-show="showSpoil">
            <slot />
        </span>
        <span v-show="!showSpoil" @click="showSpoil = true">
            Attention spoil
        </span>
    </span>
</template>

<script>
export default {
    data() {
        return {
            showSpoil: false,
        };
    },
    methods: {
        showSpoilFct() {
            this.showSpoil = true;
        },
    },
};
</script>

<style>
.spoiler {
    cursor: pointer;
    background-color: red;
    color: white;
    width: fit-content;
}
</style>
