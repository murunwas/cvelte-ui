<script>
  export let type = "primary";
  export let round = false;
  export let plain = false;
  export let circle = false;
  export let disabled = false;
  export let block=false;
  export let icon = "";

$: classes= `
 el-button
  el-button--${type}
 ${round&& 'is-round'}
 ${plain&& 'is-plain'}
 ${circle&& 'is-circle'}
 ${disabled&& 'is-disabled'}
 `
</script>

<style>
  .block{
    width:100%;
  }
</style>

<button
   {disabled}
   class:block
  class={classes}
  on:click>
  {#if icon && !circle}
    <i class="el-icon-{icon}" />
  {/if}
  {#if !circle}
      <slot />
  {/if}

    {#if circle}
     <i class="el-icon-{icon||"search"}" />
    {/if}

</button>
