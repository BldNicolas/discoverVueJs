<template>
    <nav>
        <span v-for="parent in pages.parents">
            <a :href="parent.path">{{ parent.name }}</a>
            {{ this.separator }}
        </span>
        <span>{{ pages.active.name }}</span>
    </nav>
</template>

<script>
export default {
    props: {
        pages: Object,
        separator: String,
    },
};
</script>

<style>
nav, nav * {
    display: flex;
    gap: 1rem;
    justify-content: end;
    background-color: blue;
    color: white;
}

a {
    text-decoration: none !important;
}
</style>
