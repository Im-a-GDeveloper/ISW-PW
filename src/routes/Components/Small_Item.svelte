<script>

    /**@type {string}*/
    export let name;
    /**@type {string}*/
    export let description;

    /**@type {number}*/
    export let price;


</script>



<div class="item_container">
    <div class="item">

        <div class="item_description">
            <p>{name}</p>
            <p>{description}</p>
            <p>{price}</p>
        </div>


    </div>
</div>


<style>
    .item_container{
        width: 90%;
        background-color: #1E212A;
        height: 140px;
        border-radius: 10px;
        color: white;
    }
</style>