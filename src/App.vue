<template>
  <div id="app">
  </div>
</template>

<script>

export default {
  name: 'app',
  components: {
  },
  mounted: function() {
    const testArray = ['test', 'test1', 'test3']
    console.log(testArray.__proto__)
    
    this.testConcat()
    this.testCopyWithin()
    this.testEnteries()
    this.testEvery()
    this.testFill()
    this.testFilter()
    this.testFind()
    this.testFindIndex()
  },
  methods: {
    testConcat() {
      // arr.concat - połącz nie nadpisując
      const testArray = ['test', 'test1', 'test3']
      console.log(testArray.concat(['test4']))
    },
    testCopyWithin() {
      // arr.copyWithin - kopiuj wewnątrz i zamień nadpisując
      const testArray = ['test', 'test1', 'test3']
      console.log(testArray.copyWithin(0, 2, 3))
    },
    testEnteries() {
      // arr.entries - zwraca iterator zawierający [index, wartosc]
      const testArray = ['test', 'test1', 'test3']
      const iterator = testArray.entries()
      console.log(iterator.next().value)
    },
    testEvery() {
      // arr.entries - przyjmuje metodę która sprawdza czy każdy element przechodzi test
      const testArray = ['test', 'test1', 'test3']
      const isTest = (element, index, array) => {
          return element === 'test'
      }
      console.log(testArray.every(isTest))
    },
    testFill() {
      // arr.fill(val, indexS, indexE) - wypełnia tablice podaną wartością od indexS do indexE
      const testArray = ['test', 'test1', 'test3']
      console.log(testArray.fill(0, 1, 3))
    },
    testFilter() {
      const testArray = ['test', 'test', 'test3']
      const isTest = (element, index, array) => {
        return element === 'test'
      } 
      // arr.filter()
      console.log(testArray.filter(isTest))

    },
    testFind() {
      const testArray = ['test', 'test', 'test3']
      const isTest = (element, index, array) => {
        return element === 'test'
      } 
      // arr.filter()
      console.log(testArray.find(isTest))
    },
    testFindIndex() {
      const testArray = ['test', 'test', 'test3']
      const isTest = (element, index, array) => {
        return element === 'test3'
      } 
      // arr.filter()
      console.log(testArray.findIndex(isTest))
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
