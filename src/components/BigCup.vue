<template>
 <form onsubmit="return false">
     <v-text-field label="Regular" v-model="text_xxx"></v-text-field>

    <v-btn @click='method_xxx'>hjkghjg</v-btn>
</form>
</template>

<script>
export default {
    name: 'BigCup',
    props: {
        msg: String,
    },
    data: () => ({
        text_xxx: '',
    }),

    methods: {
        method_xxx() {
            console.log('sitename', this.text_xxx)
            // this.$emit()
        },
    },
}    
</script>
