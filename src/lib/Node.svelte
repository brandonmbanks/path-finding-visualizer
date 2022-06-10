<script>
  export let row;
  export let col;
  export let isStart;
  export let isEnd;
</script>

<div class="node {isStart && "start"} {isEnd && "end"}"></div>

<style>
  .node {
    width: 25px;
    height: 25px;
    border: 1px solid black;
    display: inline-block;
    margin: 0px 3px auto;
  }

  .start {
    background-color: green;
  }

  .end {
    background-color: red;
  }

  .wall {
    background-color: grey;
  }
</style>
