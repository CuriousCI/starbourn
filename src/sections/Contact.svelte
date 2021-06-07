<script>
	function handleSubmit() {}
</script>

<form on:submit|preventDefault={handleSubmit}>
	<input type="text" placeholder="Name" />
	<input type="text" placeholder="Phone Number" />
	<input type="mail" placeholder="Email" />
	<textarea placeholder="Type your message here" cols="30" rows="10" />
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
		/* margin: 0 5px; */
		width: 100%;
		justify-content: center;
		resize: none;

		border-radius: 5px;
		border: 1px solid #dedede;
	}
</style>
