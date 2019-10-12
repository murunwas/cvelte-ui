<script>
  export let value;
  export let disabled = false;
  export let pass=false;


  $:classes=`
     el-input
      ${disabled&&"is-disabled"}
  `
</script>

{#if pass}
   <div class="el-input--suffix">
  <input
    type="password"
    autocomplete="off"
    placeholder="Please input password"
    class="el-input__inner"
    bind:value
    {disabled}
    />
  <span class="el-input__suffix">
    <span class="el-input__suffix-inner">
    </span>
  </span>
</div>
{:else}
  <div class={classes}>
  <input
    type="text"
    autocomplete="off"
    placeholder="Please input"
    class="el-input__inner"
    bind:value
    {disabled} />
</div>
{/if}




