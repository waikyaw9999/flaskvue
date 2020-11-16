<template>
  <v-container fluid>
    <v-row dense>
    <v-col v-for="(book,index) in books" :key="index" cols="12">
      <v-card
      elevation="2"
      class="mx-auto"
      max-width="500"
    >
      <v-img
        src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
        height="200px"
      ></v-img>

      <v-card-title>
        {{book.title}}
      </v-card-title>

      <v-card-subtitle>
        {{book.author}}
      </v-card-subtitle>

      <v-card-actions>
        <v-btn
          color="orange lighten-2"
          text
        >
          Explore
        </v-btn>

        <v-spacer></v-spacer>

        <v-btn
          icon
          @click="show = !show"
        >
          <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
        </v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="show">
          <v-divider></v-divider>
          <v-card-text>
            I'm a thing. But, like most politicians, he promised more than he could deliver.
          </v-card-text>
        </div>
      </v-expand-transition>
    </v-card>
    </v-col>
  </v-row>
  </v-container>
</template>
<script>
import axios from 'axios';

export default {
  data() {
    return {
      books: [],
      show: false,
    };
  },
  methods: {
    getBooks() {
      const path = 'http://localhost:5000/books';
      axios.get(path)
        .then((res) => {
          this.books = res.data.books;
        })
        .catch((error) => {
          // eslint-disable-next-line
          console.error(error);
        });
    },
  },
  created() {
    this.getBooks();
  },
};
</script>
