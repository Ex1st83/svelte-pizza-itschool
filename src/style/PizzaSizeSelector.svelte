<script>
    import { get } from "svelte/store";

    let selectedValue = "1";

    $: windowPosition = getPosition(selectedValue);

    function getPosition() {
        let value = size.findIndex((fn) => {
            if (fn.value == selectedValue) {
                return true;
            }
        });

        return (33.3333 * value).toString() + "%";
    }
</script>

<div class="selector">
    <div class="type" />
    <div class="size">
        <span class="window" style="left: {windowPosition};">
            {#each size as item}
            <label>
                <input
                    type="radio"
                    bind:qroup={selectedValue}
                    name="size"
                    value={item.value}
                />
                {item.name};
            </label>
        </span>
    </div>
</div>
