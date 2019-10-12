<script>
  export let on = "on";
  export let off = "off";
  export let checked=false;
  export let disabled=false;

  function onClick() {
    if(disabled){
      return;
    }
   checked=!checked
  }

  $:classes=`
   el-switch
   ${checked&&'is-checked'}
   ${disabled&&'is-disabled'}
  `
</script>

<div role="switch" class={classes}>
  <input type=checkbox name="" true-value="true" class="el-switch__input" bind:checked={checked} {disabled}/>
  <span class="el-switch__label el-switch__label--left {!checked&&'is-active'}" on:click={onClick}>
    <!---->
    {#if !checked}
      <span>{off}</span>
    {/if}

  </span>
  <span class="el-switch__core" style="width: 40px;" on:click={onClick}/>
  <span class="el-switch__label el-switch__label--right {checked&&'is-active'}" on:click={onClick}>
    <!---->


        {#if checked}
 <span aria-hidden="true">{on}</span>
    {/if}
  </span>
</div>


