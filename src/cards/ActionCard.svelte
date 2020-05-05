
<script>
import IconWrapper from '../IconWrapper.svelte';
export let data = {
        "name": "deserted outpost",
        "value": 46,
        "events": [
            "addPath"
        ],
        "choices": [
            [
                "addAmmunition",
                "removeAmmunition"
            ],
            [
                "removeHealth",
                "removeCamping"
            ]
        ]
    };
let mode = "picking"; //Not possible to click on icons: only with "resolving"
</script>

<style>
.value {
    border-radius: 50%;
    width: 18px;
    height: 18px;
    padding: 5px;
    background-color: olive;
    text-align:center;
    font: 16px Arial, sans-serif;
    position: absolute;
    bottom: 25px;
    left: 5px;
}

.name {
    position: absolute;
    bottom: 10px;
    font: 14px Arial, sans-serif;
    width: inherit;
    text-transform: uppercase;
    border-radius: 4px;
    padding: auto 50px;
}
.actions {
    border-radius: 4px;
    margin-bottom: 5px
}
.events {
    border: 2px dashed peru;
}
.choice {
    border: 2px dashed red;
}

.option {
    border: 2px dashed royalblue;
}

</style>

<div class="card">
        <div class="events flex actions">
            {#each data.events || [] as actionString}
                <IconWrapper {actionString}/>
            {/each}
        </div>
        {#each data.choices || [] as choice}
            <div class="choice flex actions">
                {#each choice as actionString}
                    <IconWrapper {actionString}/>
                {/each}
            </div>
        {/each}
        {#each data.options || [] as option}
            <div class="option flex actions">
                {#each option as actionString}
                    <IconWrapper {actionString}/>
                {/each}
            </div>
        {/each}
    <div id="actionIdentifier" class="flex">
        <div class="name">{data.name}</div>
        <div class="value">{data.value}</div>
    </div>
</div>