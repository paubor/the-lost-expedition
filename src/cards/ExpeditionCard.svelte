<script>
    export let position = 1;
    export let player = false;
</script>
<style>
.player{
    border-color: green;
}
.player p {
    color: green;
}
</style>
<div class="miniCard" class:player={player}>
    <p>{position}</p>
</div>