<template>
    <div class="anime-row">
        <h3>{{ headerTitle }}</h3>
        <div class="row">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    props: ['headerTitle'],
}
</script>

<style scoped>

    .anime-row {
        display: flex;
        flex-direction: column;
        margin: 1.1rem 0;
    }

    .anime-row h3 {
        color: #ddd;
        font-size: 16px;
        font-weight: 500;
    }

    .row {
        margin: 1rem -.7rem;
    }
</style>