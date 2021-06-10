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

<form on:submit|preventDefault={handleSubmit}>
	<input type="text" placeholder="Name" bind:value={name} />
	<input type="text" placeholder="Phone Number" bind:value={number} />
	<input type="mail" placeholder="Email" bind:value={email} />
	<textarea
		placeholder="Type your message here"
		cols="30"
		rows="10"
		bind:value={message}
	/>
	<input type="submit" />
</form>

<style>
	form {
		padding: 20px;
		display: flex;
		flex-direction: column;
		gap: 5px;
		align-items: center;
		width: clamp(300px, 40%, 1000px);
		height: 30vh;
		background-color: #ededed;
		border-radius: 4px;
	}

	input[type='submit'] {
		background-image: linear-gradient(to right, #5d526e, #5ebbe6);
	}

	input {
		height: 30px;
	}

	input,
	textarea {
		padding: 5px;
		width: 100%;
		justify-content: center;
		resize: none;

		border-radius: 5px;
		border: 1px solid #dedede;
	}
</style>
