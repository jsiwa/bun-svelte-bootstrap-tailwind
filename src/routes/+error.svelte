<script>
  import { page } from '$app/stores';
</script>

<svelte:head>
  <title>{$page.status} - 页面未找到</title>
</svelte:head>

<main class="grid min-h-full place-items-center bg-white px-6 py-24 sm:py-32 lg:px-8">
  <div class="text-center">
    {#if $page.status === 404}
    <h1 class="mt-4 text-3xl font-bold tracking-tight text-gray-900 sm:text-5xl">404</h1>
      <p class="text-base font-semibold text-indigo-600">页面未找到</p>
      <p class="mt-6 text-base leading-7 text-gray-600">对不起，我们找不到你请求的页面。</p>
      <div class="mt-10 flex items-center justify-center gap-x-6">
        <a href="/" class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">返回首页</a>
        <a href="#" class="text-sm font-semibold text-gray-900">联系客服 <span aria-hidden="true">&rarr;</span></a>
      </div>
    {:else}
    <h1 class="mt-4 text-3xl font-bold tracking-tight text-gray-900 sm:text-5xl">{$page.status}</h1>
      <p class="text-base font-semibold text-indigo-600">{$page.error?.message}</p>
    {/if}
  </div>
</main>