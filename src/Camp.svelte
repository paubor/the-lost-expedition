<script>
import ExplorerCard from './cards/ExplorerCard.svelte';
export const time = 'morning';
export const food = 3;
export const ammunition = 2
export const health = {
  navigation: 3,
  jungle: 3,
  camping: 3
}
</script>
<div class="flex">
  <ExplorerCard name="candido" expertise="navigation" health={health.navigation}/>
  <ExplorerCard name="yimes" expertise="jungle" health={health.jungle}/>
  <ExplorerCard name="bessie" expertise="camping" health={health.camping}/>
  <div class="inventory">
    <div>Time: {time.toUpperCase()}</div>
    <div>Food: {food}</div>
    <div>Ammunition: {ammunition}</div>
  </div>
</div>
