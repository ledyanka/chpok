<template>
  <v-card>
    <v-tabs v-model="tab" >
      <v-tab v-for="item in items" :key="item.tab">{{ item.tab }}</v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item v-for="item in items" :key="item.tab">
        <v-card flat>
          <v-card-text>{{ item.content }}</v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
export default {
  name: "TabsSamplePage",
  props: { items: Array },
  data() {
    return {
      tab: null,
    }
  },  
}
</script>