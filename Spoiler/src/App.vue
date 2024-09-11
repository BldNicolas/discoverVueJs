<template>
    <h1>Coucou</h1>
    <div>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam,
        expedita temporibus nesciunt possimus ducimus quia sequi molestiae,
        autem labore,
        <SpoilerAlert>Coucou je suis une mega spoil</SpoilerAlert>
        culpa explicabo? Aspernatur at laudantium cupiditate libero distinctio,
        nihil rem aliquam!
    </div>
</template>

<script>
import SpoilerAlert from "./components/SpoilerAlert.vue";

export default {
    components: {
        SpoilerAlert,
    },
};
</script>
