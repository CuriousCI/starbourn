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
		padding: 10px;
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 40%;
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
		margin: 0 2px;
		width: 100%;
		justify-content: center;
		resize: none;

		border-radius: 5px;
		border: 1px solid #dedede;
	}
</style>
