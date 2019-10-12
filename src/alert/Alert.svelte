<script>
  export let title="success alert"
  export let effect="light"
  export let type="success"

let open=true;


</script>
{#if open}
   <div role="alert" class="el-alert el-alert--{type} is-{effect}">
  <div class="el-alert__content">
    <span class="el-alert__title">{title}</span>
    <i class="el-alert__closebtn el-icon-close" on:click={()=>open=false} />
  </div>
</div>
{/if}

