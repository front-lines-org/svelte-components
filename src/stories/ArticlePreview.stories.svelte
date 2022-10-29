<script>
    import {Meta, Template, Story} from '@storybook/addon-svelte-csf';
    import ArticlePreview from '../components/ArticlePreview.svelte';
</script>

<!-- More on default export: https://storybook.js.org/docs/react/writing-stories/introduction#default-export -->
<!-- More on argTypes: https://storybook.js.org/docs/svelte/api/argtypes -->
<!--     
    export let title: " a",
    export let description: " a",
    export let author: " a",
    export let url: " a",
    export let img: " a",
    export let showExcerpt: " a",
 -->
<Meta
    title="Example/ArticlePreview"
    component={ArticlePreview}
    argTypes={{
        title: {control: 'text'},
        description: {control: 'text'},
        author: {control: 'text'},
        url: {control: 'text'},
        img: {control: 'text'},
        showExcerpt: {control: 'boolean'},
        publishDate: {control: 'date'},
        size: {
            control: {type: 'select'},
            options: ['xs', 'sm', 'md', 'lg', 'xl']
        }
    }}
/>

<!-- More on component templates: https://storybook.js.org/docs/svelte/writing-stories/introduction#using-args -->
<Template let:args>
    <ArticlePreview {...args} on:click={args.onClick} />
</Template>

<!-- More on args: https://storybook.js.org/docs/svelte/writing-stories/args -->
<Story
    name="Primary"
    args={{
        title: 'Battle of Antonov Airport',
        description:
            'The Battle of Antonov Airport, also known as the Battle of Hostomel Airport, was a military engagement which occurred at the Antonov Airport in Hostomel, Kyiv Oblast, during the Kyiv offensive of the 2022 Russian invasion of Ukraine.',
        author: 'Wikipedia',
        // url: '',
        img: 'https://test.front-lines.org/images/ukraine(63)-ejs-1280.webp',
        showExcerpt: true
    }}
/>

<Story
    name="Secondary"
    args={{
        label: 'Button'
    }}
/>
<Story
    name="Large"
    args={{
        size: 'large',
        label: 'Button'
    }}
/>

<Story
    name="Small"
    args={{
        size: 'small',
        label: 'Button'
    }}
/>
