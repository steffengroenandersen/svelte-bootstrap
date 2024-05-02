<script>
  import Navbar from "./components/Navbar.svelte";
  import Sidebar from "./components/Sidebar.svelte";
  import Button from "./components/Button.svelte";
  import Table from "./components/Table.svelte";
  import LoginForm from "./components/LoginForm.svelte";

  /* Function for button */
  function handleButtonClick() {
    console.log("handleButtonClick()");
  }

  /* Data for table */
  let tableData = `  <thead>
    <tr>
      <th scope="col">#</th>
      <th scope="col">First</th>
      <th scope="col">Last</th>
      <th scope="col">Handle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">1</th>
      <td>Mark</td>
      <td>Otto</td>
      <td>@mdo</td>
    </tr>
    <tr>
      <th scope="row">2</th>
      <td>Jacob</td>
      <td>Thornton</td>
      <td>@fat</td>
    </tr>
    <tr>
      <th scope="row">3</th>
      <td colspan="2">Larry the Bird</td>
      <td>@twitter</td>
    </tr>
  </tbody>`;
</script>

<Navbar />
<!-- <Sidebar /> -->

<div class="container">
  <h1>Hello world</h1>
  <p>Press the following button to get started</p>
  <Button onButtonClick={handleButtonClick} buttonText={"Get started"} />

  <div class="mt-5">
    <Table data={tableData} />
  </div>

  <div class="col-6 offset-3"><LoginForm /></div>
</div>
