<script>
	import Screen from "../Screen.svelte"
	import platform from 'platform'

	const os = platform.os.toString()
	const win = "https://www.adobe.com/go/ConnectShell11"
	const mac = "https://www.adobe.com/go/ConnectMac11Plus"
	const main = os === "Windows" ? win : os === '' ? '' : ''

	console.log(os)

	export let link
</script>

<Screen>
	<div class="text-size-5">Welcome to Limelight!</div>
	<div class="text">
		Click the download button to download the Adobe Connect platform. You can also choose from one of the available download options below.
	</div>
	<div class="download-area">
		<div class="download-main">
			<button>Download Adobe Connect</button>
		</div>
		<div class="separator"></div>
		<div class="download-options">
			<button>Download for Windows (10 or higher)</button>
			<button>Download for MacOS (OS X 10.15 or higher)</button>
			<button>Download for ChromeBook or Linux</button>
		</div>
	</div>
	<hr/>
	<div class="text">Already have the Adobe Connect application? Click here to launch the meeting!</div>
</Screen>

<style>
	button {
		padding: 15px 20px;
		border: none;
		border-radius: 4px;
		background-color: hsl(78, 100%, 42%);
		color: white;
		transition: background-color 0.1s ease-in-out;
	}
	button:hover {
		background-color: hsl(78, 100%, 47%);
	}
	button:active {
		background-color: hsl(78, 100%, 37%);
	}
	.download-area {
		display: flex;
		justify-content: center;
		align-items: center;
	}
	.download-main {
		margin-right: 50px;
	}
	.download-options {
		display: flex;
		flex-direction: column;
	}
	.download-options button {
		margin-bottom: 10px;
	}
</style>
