<template>
  <div id="app">
    <i-container class="contain">
      <i-row>
        <i-column class="border-right" sm="6">
          <h1>Markdown</h1>
          <textarea
            v-model="value"
            class="form-control"
            id="exampleFormControlTextarea1"
            rows="13"
            placeholder="Enter Some Markdown here..."
          ></textarea>
        </i-column>
        <i-column sm="6" class="preview">
          <h1 id="pre">Preview</h1>
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
        color: "#151515",
        fontsize: "1rem",
        width: "auto",
        height: "483px",
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
#body {
  background-color: #151515;
}
.contain {
  margin-top: 40px;
}
.border-right {
  border-color: #bcc4ca !important;
  height: 600px;
}
.form-control {
  font-size: 1.5rem;
}
.preview {
  color: #151515;
  font-size: 30px;
}

#pre {
  color: #9e9e9e;
}
h1 {
  color: #9e9e9e;
}
</style>