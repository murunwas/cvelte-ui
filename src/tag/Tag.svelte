<script>
  export let  effect="plain"

  $:classes=`
  el-tag el-tag--${effect}
  `
</script>


<span class={classes}>Tag 1</span>