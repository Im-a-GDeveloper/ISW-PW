<script>
    import TabBar from "../../Components/Tab_bar.svelte";
</script>


<div class="main">
    
    
    <slot/>
    
    <div class="tab_bar">
        <TabBar/>
    </div>
    
    
</div>



<style>
    .tab_bar{
        position: absolute;
        bottom: 0;
        width: 100%;
        
    }
</style>


