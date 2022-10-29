<script>
    import Nav from './components/nav.svelte';
    import Button from './components/Button.svelte';
    let menuItems = [
        {link: '#', name: 'Docs'},
        {link: '#', name: 'Home'},
        {link: '#', name: 'Blog'}
    ];
</script>

<Nav {menuItems} />
<Button text="Something" />

<style global lang="postcss">
    @tailwind base;
    @tailwind components;
    @tailwind utilities;
</style>
