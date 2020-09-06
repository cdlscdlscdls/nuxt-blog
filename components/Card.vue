<template>
  <v-card
    class="mx-auto"
    max-width="344"
    outlined
  >
    <nuxt-link
      :to="{ name: 'blog-slug', params: {
        sys: id
      }}"
      class="wrapper"
    >
    <v-list-item three-line>
      <v-list-item-content>
        <div class="overline mb-4">{{ title }}</div>
        <v-list-item-title class="headline mb-1">{{ id }}</v-list-item-title>
        <v-list-item-subtitle>{{ date }}</v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-avatar
        tile
        size="80"
        color="grey"
      ></v-list-item-avatar>
    </v-list-item>

    <v-card-actions>
      <v-btn text>Button</v-btn>
      <v-btn text>Button</v-btn>
    </v-card-actions>
  </nuxt-link>
  </v-card>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
      default: ''
    },
    id: {
      type: String,
      default: ''
    },
    date: {
      type: String,
      default: ''
    }
  }
}
</script>
