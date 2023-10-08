<script>
	import Button from '$lib/Button.svelte';
	import Card from '$lib/Card.svelte';
	import Form from '$lib/Form.svelte';
	import InputForm from '$lib/InputForm.svelte';

	function navigateToSignUp() {
		window.location.href = '/singup';
	}
</script>

<main>
	<Card />
	<Form>
		<div class="section">
			<InputForm typeInput="text" labelName="Email" placeholder="exemplo@email.com" />
			<InputForm typeInput="password" labelName="Senha" placeholder="*****" />
		</div>

		<div class="section">
			<Button title="Login" colorBtn="blue" />
			<Button title="Cadastrar minha organização" colorBtn="white" onClick={navigateToSignUp} />
		</div>
	</Form>
</main>

<style lang="sass">
main
	padding: 7rem 11.2rem 0
	display: flex
	justify-content: space-between

	.section
		display: grid
		gap: 2.2rem
		width: 43rem
</style>
