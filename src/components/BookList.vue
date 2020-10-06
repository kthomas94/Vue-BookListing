<template>
  <div>
    <h1>{{ title }}</h1>
    <ul>
      <li v-for="book in books" :book="book"><book-item></book-item></li>
    </ul>
  </div>
</template>

<script>
import BookItem from "./BookItem";

export default {
  name: "BookList",
  components: {
    BookItem,
  },
  data() {
    return {
      title: "All Books",
      books: [
        { title: "Self-Reliance", author: "Ralph Waldo Emerson" },
        { title: "American Gods", author: "Meil Gailman" },
        { title: "Amusing Ourselves to Death", author: "Neil Postman" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}
</style>