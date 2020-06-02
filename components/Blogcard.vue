<template>
  <v-card class="mx-auto">
    <v-list-item three-line>
      <v-list-item-content>
        <v-list-item-title class="headline mb-1" v-text="title" />
        <v-card-text v-text="text" />
      </v-list-item-content>
    </v-list-item>
  </v-card>
</template>

<script>
export default {
  name: "BlogPost"
  props: ['title', 'text']
}
</script>
