<script>
    export let image = "";
    export let name = "Pizza";
    export let price = 100;
</script>

<div class="pizza-card">
    <div class="img">
        <img src={image} alt="" />
    </div>
    <div class="name">{name}</div>
    <PizzaSizeSelector/>
    <div class="size">
        <div class="window">
            <span></span>
        </div>
    </div>
    <div class="price">
        від {price}
        <button class="btn orange">Купити</button>
    </div>
</div>
