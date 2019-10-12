<script>
 import {onMount} from "svelte"
  let open=false;
  let element;

  onMount(()=>{
  document.addEventListener("click",()=>{
    if(open){
     return;
    }
    open=false;
  })
  })


</script>



<div class="el-select" style="position: relative;" bind:this={element}>
  <!---->
  <div class="el-input el-input--suffix" on:click={()=>open=!open}>
    <!---->
    <input
      type="text"
      readonly="readonly"
      autocomplete="off"
      placeholder="Select"
      class="el-input__inner" />
    <!---->
    <span class="el-input__suffix">
      <span class="el-input__suffix-inner">
        <i class="el-select__caret el-input__icon el-icon-arrow-up" />
        <!---->
        <!---->
        <!---->
        <!---->
        <!---->
      </span>
      <!---->
    </span>
    <!---->
    <!---->
  </div>
  <div
    class="el-select-dropdown el-popper"
    style="display: none; min-width: 240px;">
    <div class="el-scrollbar" style="">
      <div
        class="el-select-dropdown__wrap el-scrollbar__wrap"
        style="margin-bottom: -17px; margin-right: -17px;">
        <ul class="el-scrollbar__view el-select-dropdown__list">
          <!---->
          <li class="el-select-dropdown__item">
            <span>Option1</span>
          </li>
          <li class="el-select-dropdown__item">
            <span>Option2</span>
          </li>
          <li class="el-select-dropdown__item">
            <span>Option3</span>
          </li>
          <li class="el-select-dropdown__item">
            <span>Option4</span>
          </li>
          <li class="el-select-dropdown__item">
            <span>Option5</span>
          </li>
        </ul>
      </div>
      <div class="el-scrollbar__bar is-horizontal">
        <div class="el-scrollbar__thumb" style="transform: translateX(0%);" />
      </div>
      <div class="el-scrollbar__bar is-vertical">
        <div class="el-scrollbar__thumb" style="transform: translateY(0%);" />
      </div>
    </div>
    <!---->
  </div>
{#if open}
  <div
    class="el-select-dropdown el-popper"
    style="min-width: 240px; transform-origin: center top; z-index: 2098;
    position: absolute;"
    x-placement="bottom-start">
    <div class="el-scrollbar" style="">
      <div
        class="el-select-dropdown__wrap el-scrollbar__wrap"
        style="margin-bottom: -17px; margin-right: -17px;">
        <ul class="el-scrollbar__view el-select-dropdown__list">
          <!---->
          <li class="el-select-dropdown__item hover">
            <span>Option1</span>
          </li>
          <li class="el-select-dropdown__item">
            <span>Option2</span>
          </li>
          <li class="el-select-dropdown__item">
            <span>Option3</span>
          </li>
          <li class="el-select-dropdown__item">
            <span>Option4</span>
          </li>
          <li class="el-select-dropdown__item">
            <span>Option5</span>
          </li>
        </ul>
      </div>
      <div class="el-scrollbar__bar is-horizontal">
        <div class="el-scrollbar__thumb" style="transform: translateX(0%);" />
      </div>
      <div class="el-scrollbar__bar is-vertical">
        <div class="el-scrollbar__thumb" style="transform: translateY(0%);" />
      </div>
    </div>
    <!---->
    <div x-arrow="" class="popper__arrow" style="left: 35px;" />
  </div>

{/if}

</div>
