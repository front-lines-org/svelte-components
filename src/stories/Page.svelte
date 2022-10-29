<script>
    import ArticlePreview from '../components/ArticlePreview.svelte';
    import InsetBorder from '../components/InsetBorder.svelte';
    import './page.css';
</script>

<article>
    {#each Array(3) as _, i}
        <InsetBorder>
            <ArticlePreview
                title="Test title"
                author="Ruben"
                img="https://test.front-lines.org/images/ukraine(63)-ejs-1280.webp"
                showExcerpt
                description="test description"
                size="sm"
            />
        </InsetBorder>
    {/each}
</article>
