<script>
		import synapse from '$lib/images/AppIconSynapse.png';
		import nickq from '$lib/images/AppIcon@3x.png';
		import lockbox from '$lib/images/AppIconLockBox@3x.png';
		import dotdotdot from '$lib/images/AppIcon...@3x.png';

</script>

<svelte:head>
	<title>projects</title>
	<meta name="description" content="About this app" />
</svelte:head>

<div class="text-column">
	<div class="glass-effect">
        <div class="block">
           <div class="content">
			<img src="{nickq}" alt='synapse-logo' class="nickq-img"/>
			<h2><strong>www.nickquam.com</strong></h2>
               <p>✅ SvelteKit<br/>
				✅ GitHub and Cloudflare<br/>
				✅ webhooks
			   </p>
			   <a href="https://www.nickquam.com" target="_blank">
				<button>link</button>
			   </a>
               
           </div>
       </div>
   </div>
   <div class="glass-effect">
	<div class="block">
	   <div class="content">
		   <img src="{lockbox}" alt='synapse-logo' class="lockbox-img"/>
		   <h2><strong>www.lockboxlabs.com</strong></h2>
		   <p>✅ React and JavaScript<br/>
			✅ GitHub and Cloudflare<br/>
			✅ webhooks
		   </p>
		   <a href="https://www.lockboxlabs.com" target="_blank">
				<button>link</button>
		   </a>
	   </div>
   </div>
   </div>
   <div class="glass-effect">
	<div class="block">
	   <div class="content">
		   <img src="{synapse}" alt='synapse-logo' class="nickimg"/>
		   <h2><strong>Synapse | Brain Games</strong></h2>
		   <p>✅ SwiftUI<br/>
			✅ GitHub and Xcode<br/>
			✅ IOS
		   </p>
		   <a href="https://apps.apple.com/us/app/synapse-brain-games/id6457516219" target="_blank">
			<button>link</button>
		  </a>
		  
	   </div>
   </div>
   </div>
   <div class="glass-effect">
	<div class="block">
	   <div class="content">
		   <img src="{dotdotdot}" alt='synapse-logo' class="dotdotdot-img"/>
		   <h2><strong>coming soon...</strong></h2>

		  
	   </div>
   </div>
   </div>
   
</div>

<style>
.text-column {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1rem;
  align-items: start;
  justify-content: center;
  text-align: center;
}

.glass-effect {
  background-color: rgba(0, 0, 0, 0.5);
  border-radius: 30px;
  aspect-ratio: 1 / 1; /* or you could use height: 300px; */
  position: relative;
  box-shadow: 0 2px 30px 10px rgba(0, 0, 0, 0.3);
}

.block {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  padding: 30px;
  display: flex;
  flex-direction: column;
  justify-content: center; /* Add this to vertically center your content */
}

button {
  border-radius: 8px;
  border: 1px solid transparent;
  padding: 0.6em 1.2em;
  font-size: 1em;
  font-weight: 500;
  font-family: inherit;
  background-color: rgb(53, 118, 248);
  cursor: pointer;
  transition: border-color 0.25s;
  color: white;
}
button:hover {
  border-color: #ffffff;
}
button:focus,
button:focus-visible {
  outline: 4px auto -webkit-focus-ring-color;
}

.nickq-img {
  width: 130px; /* Adjust as needed */
  height: auto; /* Maintains aspect ratio */
  border-radius: 15px; /* Adjust for desired roundness */
}

.lockbox-img {
  width: 130px; /* Adjust as needed */
  height: auto; /* Maintains aspect ratio */
  border-radius: 15px; /* Adjust for desired roundness */
}

.dotdotdot-img {
  width: 130px; /* Adjust as needed */
  height: auto; /* Maintains aspect ratio */
  border-radius: 15px; /* Adjust for desired roundness */
  opacity: 50%;
}

.block .content {
  max-width: 100%; /* ensures content does not exceed the block width */
  max-height: 100%; /* ensures content does not exceed the block height */
  overflow: auto; /* adds scrollbars if content overflows */
}

/* Set a max-width for images based on the container size */
.nickq-img, .lockbox-img, .dotdotdot-img {
  max-width: 90%; /* adjust percentage as needed */
  height: auto; /* maintains aspect ratio */
  margin: 0 auto; /* centers image in the block */
}


</style>
