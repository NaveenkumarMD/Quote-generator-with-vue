<template>
  <div id="container" style="text-align: center">
    <div id="quote">{{ quote }}</div>
    <br />
    <button v-on:click="getdata">Next</button>
  </div>
</template>
<script>
export default {
  name: "Quote",
  data() {
    return {
      quote: "Hello",
      quotes: [],
    };
  },
  beforeMount() {
    this.quote = "Loading....";
    this.get();
  },
  methods: {
    async get() {
      const apiUrl = "https://type.fit/api/quotes";
      try {
        const res = await fetch(apiUrl);
        var apiquotes = await res.json();
        this.quotes = apiquotes;
        this.getdata();
      } catch (error) {
        alert(error);
      }
    },
    getdata() {
      var num = Math.floor(Math.random() * 1500);
      if (num > 1) {
        this.quote = this.quotes[num].text;
      }
    },
  },
};
</script>
<style  scoped>
#container {
  display: flex;
  flex-direction:column;
  align-items: center;
  justify-content: center;
  height: 75vh;
  max-width: 90vw;
  margin:10px auto
}
#quote {
  
  margin: 20px;
  padding: 20px;
  border-radius: 3px;
  font-size: 70px;
}
button {
  background-color: rgb(1, 167, 42);
  color: White;
  padding: 10px 30px 10px 30px;
  border: 0px;
  border-radius: 2px;
}
</style>