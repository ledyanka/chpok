<template>
    <button> {{ msg }}</button>
</template>

<script>
export default {
    name: 'BigCup',
    props: {
        msg: String,
    }
}
</script>
