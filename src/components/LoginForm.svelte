<script>
  import Button from "./Button.svelte";

  let email;
  let password;

  function handleButtonClick() {
    console.log("handleButtonClick");
    console.log("Email: " + email);
    console.log("Password: " + password);
  }
</script>

<div id="wrapper">
  <form class="d-flex flex-column">
    <div class="mb-3">
      <label for="exampleInputEmail1" class="form-label">Email address</label>
      <input
        bind:value={email}
        type="email"
        class="form-control"
        id="exampleInputEmail1"
        aria-describedby="emailHelp"
      />
      <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
    </div>
    <div class="mb-3">
      <label for="exampleInputPassword1" class="form-label">Password</label>
      <input bind:value={password} type="password" class="form-control" id="exampleInputPassword1" />
    </div>
    <div class="mb-3 form-check">
      <input type="checkbox" class="form-check-input" id="exampleCheck1" />
      <label class="form-check-label" for="exampleCheck1">Check me out</label>
    </div>
    <div class="align-self-end">
      <Button onButtonClick={handleButtonClick} buttonText={"Get started"} />
    </div>
  </form>
</div>

<style>
  #wrapper {
    border: 1px solid black;
    border-radius: 0.75rem;
    padding: 1rem;
  }
</style>
