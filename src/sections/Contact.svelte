<script>
	const API_KEY =
			'1097da24f17a4b18c5eaca607a801608aff0498298bdbfd4482ac1f7039a25da',
		URL = 'https://api.mailslurp.com/';

	let name, email, number, message;

	async function handleSubmit() {
		const response = await fetch(`${URL}sendEmail`, {
			method: 'POST',
			headers: {
				'X-Api-Key': API_KEY,
				'Content-Type': 'application/json',
			},
			body: JSON.stringify({
				body: message,
				senderId: null,
				subject: `${name} - ${number}`,
				to: 'cicioionut328@gmail.com',
			}),
		});
		console.log(response);

		name = email = number = message = '';
	}
</script>

<form
	on:submit|preventDefault={handleSubmit}
	class="w-1/3 h-2/3 flex flex-col items-center gap-1 text-black"
>
	<input type="text" placeholder="Name" bind:value={name} />
	<input type="text" placeholder="Phone Number" bind:value={number} />
	<input type="email" placeholder="Email" bind:value={email} />
	<textarea
		placeholder="Type your message here"
		cols="30"
		rows="10"
		bind:value={message}
	/>
	<input type="submit" class="self-end" />
</form>

<style>
	input[type='text'],
	input[type='email'],
	textarea {
		padding: 5px;
		width: 100%;
	}
</style>
