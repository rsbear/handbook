<div class="wrapper">
		<slot></slot>
		</div>

<style>
	:global(body, p) {
		margin: 0;
		padding: 0;
		/* background-color: #1F2026; */
	}

	:global(button) {
		outline: 0;
		border: 0;
		height: 28px;
		padding-left: 14px;
		padding-right: 14px;
		background-color: rgb(20,20,20);
		border-radius: 2px;
		color: white;
		font-size: 14px;
		cursor: pointer;
	}

	.wrapper {
		margin-top: 80px;
		display: flex;
		justify-content: center
	}

	:global(.sidebar) {
		width: 200px;
	}

	:global(.content) {
		width: 700px;
		margin-left: 40px;
	}
</style>
