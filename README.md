# **Install**

```bash
npm i @murunwas/cvelte-ui
```
or
```bash
yarn add @murunwas/cvelte-ui
```

This package has no dependencies.

# **Usage**

```html
<script>
  import { ButtonGroup, Button,Input,Icon,Switch,Select,Tag,Alert } from "./";

let disabled =true;
  function onSubmit(params) {
    console.log("clicked");
    disabled=!disabled;
  }
</script>

<!-- <Button on:click={onSubmit} circle icon="search">Submit</Button> -->
<ButtonGroup>
  <Button  bind:disabled={disabled}>Submit</Button>
  <Button  type="danger" icon="search">Danget</Button>
  <Button  type="success">Add</Button>
</ButtonGroup>

<Button on:click={onSubmit} type="success" circle icon="delete">Block</Button>

<Input bind:disabled={disabled} pass/>

<Icon/>

<Switch bind:checked={disabled}  bind:disabled={disabled}/>
<br/>
<Select/>
<br/>
<Tag effect="light"/>
<br/>
<Alert effect="dark"/>
```