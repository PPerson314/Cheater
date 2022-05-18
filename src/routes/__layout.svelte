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
<div class="w-auto h-auto bg-slate-200 flex flex-col justify-between">
    <ReturnHome />
    <slot></slot> 
    <Nav />
</div>
