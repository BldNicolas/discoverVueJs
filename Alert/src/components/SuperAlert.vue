<template>
    <div class="alert" :class="`alert-${type}`">
        <slot></slot>
        <i>X</i>
    </div>
</template>

<script>
    export default {
        props: {
            type: String
        }
    }
</script>

<style scoped>
    .alert {
        background-color: #ddd;
        padding: 1rem;
        border-radius: 0.375rem;
    }

    .alert-danger {
        background-color: orange;
    }

    .alert-error {
        background-color: red;
    }

    .alert-success {
        background-color: green;
    }
</style>