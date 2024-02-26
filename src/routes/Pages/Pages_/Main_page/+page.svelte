<script>
    import SearchBar from "../../../Components/Search_bar.svelte";
    import ItemGrid from "../../../Components/Item_Grid.svelte";
</script>




<div class="content">
    <div class="search_bar_conatiner">
        <SearchBar/>
    </div>

    <div class="Grid_items">

        <div class="Item">
            <ItemGrid Item = {{
                name: "Camara FujiFilm", 
                description: "The Paradigm of Major Notion", 
                price: 42, 
                rating: 2}} />
        </div>
        <div class="Item_3">
            <ItemGrid Item = {{
                name: "Camara FujiFilm", 
                description: "The Paradigm of Major Notion", 
                price: 42, 
                rating: 2}} />
        </div>
        
    </div>
</div>





<style>
    .content{
        display: flex;
        flex-direction: column;
        
    }

    .search_bar_conatiner{
        padding: 40px 0;
        margin-left: 16px;
        width: 100%;
        
    }

    .Grid_items{
        display: grid;
        grid-template-columns: 0.1fr 1fr 0.1fr 1fr 0.1fr;
        grid-template-rows: 1fr;
        gap: 0px 0px;
        grid-auto-flow: row;
        grid-template-areas:
    ". . . . .";
    }

    .Item{
        grid-column-start: 2;
        grid-column-end: 3;
    }

    .Item_3{
        grid-column-start: 4;
        grid-column-end: 5;
    }
    
</style>