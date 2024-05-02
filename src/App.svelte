<script>
  import Navbar from "./components/Navbar.svelte";
  import Sidebar from "./components/Sidebar.svelte";
  import Button from "./components/Button.svelte";
  import Table from "./components/Table.svelte";
  import LoginForm from "./components/LoginForm.svelte";
  import Modal from "./components/Modal.svelte";

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

  /*  ChartJS */
  import { chartType, myData, myOptions } from "./components/chartsjs-repl/settings.js";
  import Select from "./components/chartsjs-repl/Select.svelte";
  import Chart from "./components/chartsjs-repl/Chart.svelte";

  let type = chartType;
  let data = myData;
  let options = myOptions;

  $: config = {
    type,
    data,
    options,
  };
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

  <!-- Button trigger modal -->
  <div class="mt-5">
    <button type="button" class="btn btn-dark" data-bs-toggle="modal" data-bs-target="#exampleModal">
      Launch demo modal
    </button>
    <Modal modalType={"add-user"} />
  </div>
</div>

<div class="col-6 mt-5">
  <Select bind:type />

  <Chart {config} />
</div>
