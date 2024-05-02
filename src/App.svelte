<script>
  import Navbar from "./components/Navbar.svelte";
  import Sidebar from "./components/Sidebar.svelte";
  import Button from "./components/Button.svelte";

  function handleButtonClick(){
    console.log("handleButtonClick()");
  }
</script>

<Navbar />
<!-- <Sidebar /> -->

<div class="container">
  <h1>Hello world</h1>
  <p>Press the following button to get started</p>
  <Button onButtonClick={handleButtonClick} buttonText={"Get started"} />
</div>
