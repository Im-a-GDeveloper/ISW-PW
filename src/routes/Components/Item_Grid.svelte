<script>
    /**
     * @typedef {Object} Item
     * @property {String} name
     * @property {String} description
     * @property {Number} price
     * @property {Number} rating 
     */


    export let Item = {
        name: "",
        description: "",
        price: 0,
        rating: 0
    }
</script>



<div class="Item_container">
    <div class="img_container">
        <img src="" alt="">
    </div>

    <div class="item_description">
        <p>{Item.name}</p>
        <p class="description">{Item.description}</p>
        <p class="price">{Item.price} $</p>
    </div>
</div>


<style>
    .Item_container{
        width: 100%;
        height: 274px;
        border-radius: 10px;
        
    }

    .item_description{
        margin-top: 10px;
        
    }

    .item_description > *{
        margin-bottom: 4px;
    }

    .img_container{
        background-image: url("/img/pexels-math-90946.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        height: 206px;
        border-radius: 10px 10px 0 0;
    }
    /* .Item_container img{
        width: 100%;
        height: 200px;
        
    } */


    .description{
        color: #A9A9A9;
    }
    .price{
        color: #00B865;
    }

    
</style>