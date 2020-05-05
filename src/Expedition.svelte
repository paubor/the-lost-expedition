<script>
    import ExpeditionCard from "./cards/ExpeditionCard.svelte";
    export let playerPosition;
    const pathSize = 9;
</script>
<style>

</style>
<div class="flex">
    {#each [...Array(pathSize).keys()] as position}
        <ExpeditionCard {position} player={playerPosition===position}/>
    {/each}
</div>