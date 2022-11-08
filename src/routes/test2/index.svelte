<script>
    import { copy } from 'svelte-copy';
  	let a = 50;
  	let b = 100;
    let ab = (a / 100) * b
  	let c = 20;
  	let d = 40;
  	let e = 1;
  	let f = 1.5;
</script>

<h1 class="text-4xl dark:text-white pb-8">Percentage Calculator</h1>

<form>
	<div class="flex">
		<span class="inline-flex items-center px-3 text-sm text-gray-900 bg-gray-200 rounded-l-md border border-r-0 border-gray-300 dark:bg-gray-600 dark:text-gray-400 dark:border-gray-600">
			What is
		</span>
		<input type="number" id="website-admin" class="bg-gray-50 border border-gray-300 text-gray-900 focus:ring-blue-500 focus:border-blue-500 block flex-1 min-w-0 w-full text-sm border-gray-300 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="a" bind:value={a}>
		<span class="inline-flex items-center px-3 text-sm text-gray-900 bg-gray-200 rounded-r-md border border-l-0 border-gray-300 dark:bg-gray-600 dark:text-gray-400 dark:border-gray-600 mr-4 -z-10">
		%
	</span>

			<span class="inline-flex items-center px-3 text-sm text-gray-900 bg-gray-200 rounded-l-md border border-r-0 border-gray-300 dark:bg-gray-600 dark:text-gray-400 dark:border-gray-600">
			of
		</span>
		<input type="number" id="website-admin" class="bg-gray-50 border border-gray-300 text-gray-900 focus:ring-blue-500 focus:border-blue-500 block flex-1 min-w-0 w-full text-sm border-gray-300 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="b" bind:value={b}>
		<span class="inline-flex items-center px-3 text-sm text-gray-900 bg-gray-200 rounded-r-md border border-l-0 border-gray-300 dark:bg-gray-600 dark:text-gray-400 dark:border-gray-600 -z-10">
		?
	</span>
	
	</div>


<label for="website-admin" class="block mb-2 text-sm font-medium text-gray-900 dark:text-gray-300">Result</label>
<div class="flex">
<input disabled type="number" id="website-admin" class="bg-gray-50 border border-gray-300 text-gray-900 focus:ring-blue-500 focus:border-blue-500 block flex-1 min-w-0 w-full text-sm border-gray-300 p-2.5  dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" value={(a / 100) * b}>
<button type="button" class="text-white bg-gray-800 hover:bg-gray-900 focus:outline-none focus:ring-4 focus:ring-gray-300 font-medium rounded-r-md border border-l-0 text-sm px-5 py-2.5 dark:bg-gray-800 dark:hover:bg-gray-700 dark:focus:ring-gray-700 dark:border-gray-700" on:click={navigator.clipboard.writeText((a / 100) * b)}>Copy</button>
</div>
</form>
