<script setup>
const props = defineProps({
  tel: {
    type: String,
    default: () => '700 000 000'
  },
  nazwa_sklepu: {
    type: String,
    default: () => 'Sklep Michał Stahlke'
  },
});
</script>

<template>
    <div class="info">
        <span>Tel: {{ tel }}</span>
        <span> {{ nazwa_sklepu }}</span>
    </div>
</template>

<style scoped lang="scss">
.info {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    height: 50px;
    background-color: black;
    color: white;
    justify-content: center;
    align-items: center;
    font-size: 20px;

    @media (max-width: 465px) {
        height: 100px;
    }

    span {
        margin: 0 10px 0 10px;
    }
}
</style>