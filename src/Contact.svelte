<div id="Get in Touch" class="window contacts">
    <h1>Get in Touch</h1>
    <p>Let the magic begin</p>
    <form on:submit|preventDefault>
        <input type="text" placeholder="Name" />
        <input type="text" placeholder="Phone Number" />
        <input type="mail" placeholder="Email" />
        <textarea
            placeholder="Type your message here"
            cols="30"
            rows="10"
        />
        <input type="submit" />
    </form> 
</div>

<style>
    form {
		display: flex;
		flex-direction: column;
		width: 40%;
		background-color: #ededed;
	}

	input[type=submit]{

		background-image: linear-gradient(to right,#5d526e, #5ebbe6);
	}

	input, textarea{

		margin: auto;
		margin-top: 5px;
		margin-bottom: 5px;
		width: 90%;
		justify-content: center;
		resize: none;

		height: 10%;

		border-radius: 45px;
		border: 1px solid #dedede;

		/* box-sizing: border-box; */
	}
</style>