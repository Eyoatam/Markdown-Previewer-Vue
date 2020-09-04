<template>
  <div id="app">
    <i-container class="container">
      <i-row>
        <i-column class="border-right" sm="6">
          <h1>Markdown</h1>
          <textarea
            v-model="value"
            class="form-control"
            id="exampleFormControlTextarea1"
            rows="4"
            placeholder="Enter Some Markdown here..."
          ></textarea>
        </i-column>
        <i-column sm="6">
          <h1>Preview</h1>
          <!-- <textarea
            readonly
            v-model="value"
            class="form-control"
            id="exampleFormControlTextarea1"
            rows="4"
            placeholder="Enter Some Markdown here..."
          >
          </textarea> -->
          <vue-markdown :style="styleObj" :source="value"></vue-markdown>
        </i-column>
      </i-row>
    </i-container>
  </div>
</template>

<script>
import VueMarkdown from "vue-markdown";
export default {
  name: "App",
  data() {
    return {
      value: "",
      styleObj: {
        fontsize: "1rem",
        width: "auto",
        height: "500px",
        backgroundColor: "#e9ecef",
        padding: "20px",
        borderRadius: "5px",
      },
    };
  },
  components: {
    VueMarkdown,
  },
};
</script>

<style>
.container {
  margin-top: 40px;
}
.border-right {
  border-color: #000 !important;
  height: 600px;
}
.form-control {
  font-size: 1.3rem;
}
</style>
