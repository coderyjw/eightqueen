<template>
  <div>
    <h1 class="title">八皇后</h1>
    <div class="grid">
      <div class="row" v-for="(row, rIndex) in grids" :key="rIndex">
        <div
          class="cell"
          v-for="(cell, cIndex) in row"
          :key="cell.key"
          @click.stop="select(rIndex, cIndex)"
        >
          <div v-if="cell.ok">Q</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
const grids = new Array(8).fill(1).map((_, r) => {
  return new Array(8).fill(1).map((_, c) => {
    return {
      key: `key-${r * 8 + c}`,
      ok: false,
    };
  });
});
export default {
  data() {
    return {
      grids,
    };
  },
  methods: {
    select(rIndex, cIndex) {
      console.log(rIndex, cIndex);
      this.grids[rIndex][cIndex].ok = true;
    },
  },
};
</script>

<style scoped>
.grid {
  width: 400px;
  margin: 0 auto;
}
.cell {
  width: 50px;
  height: 50px;
  line-height: 50px;
  text-align: center;
  background-color: #999;
  float: left;
}

.cell:nth-child(2n) {
  background-color: #efefef;
}

.row {
  height: 50px;
  width: 400px;
  display: flow-root;
}

.row:nth-child(2n) .cell:nth-child(2n) {
  background-color: #999;
}
.row:nth-child(2n) .cell:nth-child(2n - 1) {
  background-color: #efefef;
}
</style>
