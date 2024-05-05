<script>
  import Navbar from "./components/Navbar.svelte";
  import Sidebar from "./components/Sidebar.svelte";
  import Button from "./components/Button.svelte";
  import Table from "./components/Table.svelte";
  import LoginForm from "./components/LoginForm.svelte";
  import Modal from "./components/Modal.svelte";
  import Footer from "./components/Footer.svelte";

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
  // import { chartType, myData, myOptions } from "./components/chartsjs-repl/settings.js";
  // import Select from "./components/chartsjs-repl/Select.svelte";
  // import Chart from "./components/chartsjs-repl/Chart.svelte";

  // let type = chartType;
  // let data = myData;
  // let options = myOptions;

  // $: config = {
  //   type,
  //   data,
  //   options,
  // };
</script>

<Navbar />

<div class="container">
  <h1>Hello world</h1>
  <p>Press the following button to get started</p>

  <Button onButtonClick={handleButtonClick} buttonText={"Get started"} />

  <div class="mt-5">
    <Table data={tableData} />
  </div>

  <!-- <div class="col-6 offset-3"><LoginForm /></div> -->

  <div class="mt-5">
    <button type="button" class="btn btn-dark" data-bs-toggle="modal" data-bs-target="#exampleModal">
      Launch demo modal
    </button>
    <Modal modalType={"add-user"} />
  </div>

  <br />
  <br />

  <div class="card-1 border rounded">
    <div class="container">
      <div class="row">
        <div class="col mt-3">
          <div
            class="border rounded d-flex justify-content-center align-items-center"
            style="height: 30px; width: 30px;"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-person"
              viewBox="0 0 16 16"
            >
              <path
                d="M8 8a3 3 0 1 0 0-6 3 3 0 0 0 0 6m2-3a2 2 0 1 1-4 0 2 2 0 0 1 4 0m4 8c0 1-1 1-1 1H3s-1 0-1-1 1-4 6-4 6 3 6 4m-1-.004c-.001-.246-.154-.986-.832-1.664C11.516 10.68 10.289 10 8 10s-3.516.68-4.168 1.332c-.678.678-.83 1.418-.832 1.664z"
              />
            </svg>
          </div>
        </div>
        <div class="col mt-3 d-flex justify-content-end">
          <div>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-three-dots-vertical"
              viewBox="0 0 16 16"
            >
              <path
                d="M9.5 13a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0m0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0m0-5a1.5 1.5 0 1 1-3 0 1.5 1.5 0 0 1 3 0"
              />
            </svg>
          </div>
        </div>
      </div>
      <div class="mt-2">
        <p class="fw-light">customer</p>
        <p class="fs-3 fw-bold">2,240</p>
      </div>
    </div>
  </div>
</div>

<Footer />

<!-- <Sidebar /> -->

<!-- <div class="col-6 mt-5">
    <Select bind:type />

    <Chart {config} />
  </div> -->

<style>
  .card-1 {
    height: 160px;
    width: 250px;
  }
</style>
