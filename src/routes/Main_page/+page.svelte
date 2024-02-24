<script>
    import TabBar from "../Components/Tab_Bar.svelte";
    import SmallItem from "../Components/Small_Item.svelte";

    const items = [
        {name: "Pizza", description: "lorem ipsum", price: 125},
        {name: "Helado", description: "lorem ipsum", price: 125},
        {name: "Refresco", description: "lorem ipsum", price: 125},
        {name: "Pan", description: "lorem ipsum", price: 125},
    ]
</script>


<div class="main">

    {#each items as item}
        <li>
            <SmallItem 
            name={item.name} 
            description={item.description} 
            price={item.price}/> 
        </li>
    {/each}
    
    <div class="tab_var">
        <TabBar/>
    </div>
    
</div>




<style>
    .main{
        display: flex;
        flex-direction: column;
        justify-items: center;
    }

    .tab_var{
        position: absolute;
        bottom: 0;
        width: 100%;
    }   

    li{
        margin-bottom: 20px;
    }
</style>


