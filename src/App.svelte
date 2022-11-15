<script>
	import Nav from "./components/Nav.svelte"
	import Welcome from "./components/screens/Welcome.svelte"
	import Pop from "./components/Pop.svelte"

	const url = window.location.search
	const params = new URLSearchParams(url)
	const room = params.get("ref")?.toLowerCase()
	const guestType = params.get("t")
	
	if (!/^\w{2,4}\d{4}\-[p|g|b|y|o]$/.test(room) && !/^((purple|green|blue|yellow|orange)suite)$/.test(room))
	console.error("Exiting", `'${room}' isn't a valid job number`)
	
	const link = `connectpro:https://limelight.adobeconnect.com/${room}?guestName=test`

	// console.log(room)
	// console.log(guestType)
	// console.log(link)

	// console.log(platform.os)
</script>

<Nav />
<Welcome {link}/>
