<script>
  export let buttonText;
  export let onButtonClick;


</script>

<button on:click={() => onButtonClick()} type="button" class="btn btn-dark">{buttonText}</button>
