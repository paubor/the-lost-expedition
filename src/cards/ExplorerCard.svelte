<script>
  import IconWrapper from '../IconWrapper.svelte'

  export let name = "NAME"
  export let expertise = 'jungle'
  export let health = 12

  
  function toActionString(){
    switch(expertise){
      case 'jungle': return 'addJungle'
      case 'navigation': return 'addNavigation'
      case 'camping': return 'addCamping'
    }
  };
</script>
<style>
.name {
    position: absolute;
    bottom: 10px;
    font: 14px Arial, sans-serif;
    width: inherit;
    text-transform: uppercase;
    border-radius: 4px;
    padding: auto 50px;
}
</style>
<div class="card">
  <div>
    <IconWrapper actionString={toActionString()}/>
  </div>
  <div>
    <div class="name">{name}</div>
  </div>
  {health}
</div>