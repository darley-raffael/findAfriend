<script lang="ts">
	export let title = 'Seja bem vindo!';
</script>

<div class="form-container">
	<h2>{title}</h2>
	<form action="">
		<slot />
	</form>
</div>

<style lang="sass">
.form-container
  min-width: 60rem
  max-width: 6.5rem
  display: flex
  flex-direction: column
  h2
    font-size: 5.4rem
    font-weight: 700
    line-break: auto // isso faz 
    width: 100%
    box-sizing: border-box
  form
    width: 100%
    display: flex
    flex-direction: column
    gap: 6.1rem

</style>
