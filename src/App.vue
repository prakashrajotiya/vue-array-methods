<template>
  <div id="app">
    <h4>Array Methods Practice</h4>
    <button @click="atPractice()">Array At</button>
    <button @click="concatePractice()">Array concate</button>
    <button @click="copywithinPractice()">Copy With In</button>
    <button @click="entriesPractice()">Entries</button>
    <button @click="everyPractice()">Every</button>
    <button @click="filterPractice()">filter</button>
    <button @click="findPractice()">Find</button>
    <button @click="findIndexPractice()">Find Index</button>
    <button @click="indexOfPractice()">IndexOf</button>
    <button @click="mapPractice()">map</button>
    <button @click="reducePractice()">reduce</button>
    <button @click="slicePractice()">slice</button>
    <button @click="sortPractice()">Sort</button>
    <button @click="splicePractice()">splice</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      test: 'test',
      myarray: [
        10,
        0,
        1,
        2,
        3,
        4,
        5,
        '6',
        'hello',
        'prakash',
        'kumar',
        'suthar',
        'arnay',
      ],
      myarray1: [6, 7, 8, 9, 10, 'end'],
      myarray2: [6, 7, 8, 9, 10],
      obj: [
        { name: 'Bob', age: '32', occupation: 'developer' },
        { name: 'Bill', age: '17', occupation: 'delinquent' },
        { name: 'Brad', age: '40', occupation: 'yes' },
      ],
    };
  },
  methods: {
    atPractice() {
      console.log(this.myarray.at(0));
    },
    concatePractice() {
      console.log(this.myarray.concat(this.myarray1));
    },
    copywithinPractice() {
      console.log(this.myarray.copyWithin(0, 8, 9));
    },
    entriesPractice() {
      for (let i of this.myarray.entries()) {
        console.log(i);
      }
    },
    everyPractice() {
      console.log(
        this.myarray1.every((item) => {
          return item > 0;
        })
      );
    },
    filterPractice() {
      console.log(
        // this.myarray.filter((item) => {
        //   return parseInt(item) == item;
        // })
        this.myarray.filter(Number)
        // this.myarray.filter(Number.isInteger)
        // this.myarray.filter(Number.isFinite)
      );
    },
    findPractice() {
      console.log(
        this.myarray.find((item) => {
          return item > 5;
        })
      );
    },
    findIndexPractice() {
      console.log(
        this.myarray.findIndex((item) => {
          return item == 5;
        })
      );
    },
    indexOfPractice() {
      console.log(this.myarray.indexOf('prakash'));
    },
    mapPractice() {
      console.log(
        this.myarray.map((item) => {
          return item * 4;
        })
      );
    },
    reducePractice() {
      console.log(
        this.myarray2.reduce((total, currVal) => {
          console.log('total', total, 'current', currVal);
          console.log('plus', total + currVal);
          return total + currVal;
        })
      );
    },
    slicePractice() {
      console.log(this.myarray2.slice(2, 3));
    },
    sortPractice() {
      // console.log(this.myarray.sort());
      console.log(
        this.myarray1.sort(function (a, b) {
          return a - b;
        })
      );
    },
    splicePractice() {
      console.log(this.myarray);
      console.log(this.myarray.splice(0, 0));
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
