<script>
	import Button from '$lib/Button.svelte';
	import Card from '$lib/Card.svelte';
	import Form from '$lib/Form.svelte';
	import InputForm from '$lib/InputForm.svelte';
</script>

<main>
	<Card />
	<Form title="Cadastrar sua organização">
		<div class="section">
			<InputForm typeInput="text" labelName="Nome Responsável" placeholder="Nome completo" />
			<InputForm typeInput="email" labelName="Email" placeholder="exemplo@email.com" />
			<InputForm typeInput="number" labelName="CEP" placeholder="00000-000" />
			<InputForm typeInput="text" labelName="Endereço" placeholder="Rua Exemplo 123" />
			<InputForm typeInput="text" labelName="Bairro" placeholder="Bairro Exemplo" />
			<InputForm typeInput="number" labelName="Whatsapp" placeholder="(00) 00000-000" />
			<InputForm typeInput="password" labelName="Senha" placeholder="*****" />
			<InputForm typeInput="password" labelName="Confirmar Senha" placeholder="*****" />
			<Button title="Cadastrar" />
		</div>
		<a href="/singin">Já possui conta?</a>
	</Form>
</main>

<style lang="sass">
main
  padding: 7rem 11.2rem 0
  display: flex
  justify-content: space-between

  text-align: center 
  margin-bottom: 10rem
  
  .section
    padding: 0 10rem
    display: grid
    gap: 3rem
    text-align: left
  a
    color: $color-blue
    font-size: 1.8rem
    font-weight: 800
    @include hover-btn
</style>
