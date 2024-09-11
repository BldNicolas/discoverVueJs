<template>
    <MyBreadCrumb
        :pages="{
            parents: [
                {
                    name: 'Accueil',
                    path: '/',
                },
                {
                    name: 'Formations',
                    path: '/formations',
                },
                {
                    name: 'Étudiant',
                    path: '/formations/etudient',
                },
            ],
            active: {
                name: 'HTML',
            },
        }"
        separator=">"
    />
</template>

<script>
import MyBreadCrumb from "./components/MyBreadCrumb.vue";

export default {
    components: {
        MyBreadCrumb,
    },
};
</script>
