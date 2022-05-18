<script>
    import Nav from "../components/nav.svelte";
    import ReturnHome from "../components/returnHome.svelte";
</script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/lucaburgio/iconoir@master/css/iconoir.css">

<style>
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
</style> 

<ReturnHome />
<slot></slot> 
<Nav />