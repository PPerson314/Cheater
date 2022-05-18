<script>
    import Nav from "../components/nav.svelte";
    import ReturnHome from "../components/returnHome.svelte";
</script>

<ReturnHome />
<slot></slot> 
<Nav />

<style>
@tailwind base;
@tailwind components;
@tailwind utilities;
</style> 