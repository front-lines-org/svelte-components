<script>
    export let title;
    export let description;
    export let author;
    export let url;
    export let img;
    export let publishDate;
    export let showExcerpt;

    export let size = 'md';
</script>

<a href={url} class="hover:underline">
    <div class="flex flex-wrap justify-evenly">
        {#if size !== 'xs'}
            <div class={`image-${size}`}>
                <img src={img && img.startsWith('http') ? img : `/images/${img}`} alt="" />
            </div>
        {/if}
        <div class="item w-32 h-44 flex-grow p-4">
            {#if size !== 'xs'}
                <p style="color: #f9a1bc;" class="font-black">Ukraine</p>
            {/if}
            <h1 class="text-gray-900 font-bold py-2 text-lg ">{title}</h1>
            {#if description && showExcerpt && size != 'xs'}
                <p class="font-normal text-gray-400">{description}</p>
            {/if}
            {#if publishDate}
                <p class="font-normal text-gray-400">{new Date(publishDate).toLocaleString()}</p>
            {/if}
            {#if author && size != 'xs'}
                <p class="font-bold py-1 text-gray-600 text-sm">By {author}</p>
            {/if}
        </div>
    </div>
</a>

<style>
    .image-sm {
        @apply w-44 my-auto;
    }
    .image-md {
        @apply w-full my-auto;
    }
</style>
