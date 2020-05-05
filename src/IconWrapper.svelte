<script>
import actions from './assets/actions.js';
export let actionString = "addFood";
let data = actions[actionString] || {};

function valueToIconName(subject, verb){
    console.log("called with value", subject)
    switch (subject){
        case "food":
            return "fa-drumstick-bite";
        case "ammunition":
            break;
        case "health":
            break;
        case "path" :
            return "fa-drumstick-bite";
    }
}

</script>
<style>
div {
    width: 25px;
    height: 25px;
    border-radius: 2px;
    border: 1px solid black;
}
div img {
    max-width: 20px;
}
</style>

<div title={actionString}>
    <img src="img/{actionString}.png" alt="{actionString}"/>
</div>