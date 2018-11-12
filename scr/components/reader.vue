<template>

  <div>
    <p>{{ flower }}</p>
  </div>
  
</template>

<script>

  module.exports = {
    methods: {
      readTextFromFile(file) {
        file.readFile('/data/issue-1.txt', function(text) {
          var textByLine = text.split('\n');
        })
      }
    },
    data() {
     return {
       flower: textByLine[1];
     }
    }
  }
</script>

<style scoped>

p {
  font-family: "Futura";
  font-size: 16px;
}

</style>
