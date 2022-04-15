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
  render() {
    return (
      <div>
        <div>八皇后jsx</div>
        <div class="grid">
          {grids.map((row, r_index) => (
            <div class="row" key={r_index}>
              {row.map((cell) => (
                <div class="cell" key={cell.key}>
                  q
                </div>
              ))}
            </div>
          ))}
        </div>
      </div>
    );
  },
};
</script>

<style lang="scss" scoped></style>
