<script>
	import { goto } from "$app/navigation";
</script>

<svelte:head>
    <title>nick</title>
    <meta name="description" content="Innovative Technology Solutions by TraceValley" />
</svelte:head>

<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lora,700&display=swap">

<main>

    <section class="hero">
        <h1>nick quam</h1>
        <p>a portfolio
		</p>
		<button on:click={() => goto('/projects')}>click here!</button>
    </section>

	  

    <!-- Add your other sections like About, Services, Contact here -->

</main>


<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
		margin: 0;
		margin-top: 10rem;
	}

	h1 {
		width: 100%;
		font-weight: bold;
		font-size: 5rem;
		margin: 0;
		
	}

	p{
		font-style: italic;
		font-size: 1.3rem;
		margin: 0;
	}

	button {
		padding: 10px 20px;
        background-color: #b74d4d;
        color: white;
        border: none;
        border-radius: 7px;
        cursor: pointer;
        margin-top: 50px; /* Space between text and button */


	}

	button:hover{
		background-color: #FF9800;
	}


</style>
