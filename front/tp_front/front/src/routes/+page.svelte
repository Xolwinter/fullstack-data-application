<script>
    console.log("hello terminal");
    let elementAnswer = ""
    //fetch('https://jsonplaceholder.typicode.com/todos/1').then((response)=>console.log("Response to JSON placeholder : ",response))

    let q = async function getResultFromURL(url){
        await fetch(url).then((response)=> {
            console.log("1")
            elementAnswer = response.ok
        })
    }
    function handleClick() {
		alert('clicked')
	}
</script>

<div class="flex justify-center justify-items-center grid grid-flow-row auto-rows-max p-10">
    <p>Hello</p>
    <a class="underline" href="https://svelte.dev/tutorial/basics">Link to Svelte tutorial</a>
    <a class="underline" href="https://tailwindcss.com/docs/text-color">Link to Tailwind CSS docs</a>

    <p> The answer will be shown here {elementAnswer} </p>

    <button
        class="m-3 p-3 text-white bg-green-400"
        on:click={handleClick}
    >
        button
    </button>
</div>