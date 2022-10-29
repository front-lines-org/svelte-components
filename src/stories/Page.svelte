<script>
    import ArticlePreview from '../components/ArticlePreview.svelte';
    import InsetBorder from '../components/InsetBorder.svelte';
    import './page.css';
</script>

<div class="grid overflow-hidden md grid-cols-3 auto-rows-auto md:grid-cols-12">
    <div class="col-start-1 col-span-9">
        <div class="grid overflow-hidden lg grid-cols-3 md:grid-cols-12 auto-rows-auto ">
            <div class="col-span-3 order-2 md:order-1">
                <div>
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
                </div>
            </div>
            <div class="box col-span-9 order-1 md:order-2 ">
                <div>
                    <InsetBorder>
                        <ArticlePreview
                            title="Test title"
                            author="Ruben"
                            img="https://test.front-lines.org/images/ukraine(63)-ejs-1280.webp"
                            showExcerpt
                            description="test description"
                            size="lg"
                        />
                    </InsetBorder>
                    {#each Array(3) as _, i}
                        <InsetBorder>
                            <ArticlePreview
                                title="Test title"
                                author="Ruben"
                                img="https://test.front-lines.org/images/ukraine(63)-ejs-1280.webp"
                                showExcerpt
                                description="test description"
                                size="md"
                            />
                        </InsetBorder>
                    {/each}
                </div>
            </div>
        </div>
    </div>

    <div class="col-span-3">
        <div>
            {#each Array(6) as _, i}
                <InsetBorder>
                    <ArticlePreview
                        title="Test title"
                        author="Ruben"
                        img="https://test.front-lines.org/images/ukraine(63)-ejs-1280.webp"
                        showExcerpt
                        description="test description"
                        publishDate={'2022-02-14'}
                        size="xs"
                    />
                </InsetBorder>
            {/each}
        </div>
    </div>
</div>
