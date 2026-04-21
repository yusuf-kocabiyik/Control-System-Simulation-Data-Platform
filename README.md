# Control-System-Simulation-Data-Platform

<p>
This project provides a backend service for storing and managing control system simulation results.
It enables integration of MATLAB/Simulink-generated data with a RESTful API using Spring Boot and PostgreSQL.
</p>



<h2>Overview</h2>
<p>
The system is designed to handle simulation data produced from control system models (e.g., DC motor simulations).
It allows simulation outputs to be stored, retrieved, and organized for further analysis.
</p>

<hr>

<h2> Features</h2>
<ul>
  <li>Store simulation results via REST API</li>
  <li>Manage simulation runs and parameters</li>
  <li>Handle time-series data (e.g., speed, error, control signals)</li>
  <li>Retrieve and review simulation results</li>
</ul>


<h2> System Architecture</h2>
<ul>
  <li><b>Data Source:</b> MATLAB / Simulink simulation outputs</li>
  <li><b>Backend:</b> Spring Boot REST API</li>
  <li><b>Database:</b> PostgreSQL</li>
</ul>


<h2>Data Model</h2>

<h3>Simulation Run</h3>
<ul>
  <li>Simulation name</li>
  <li>Controller parameters (e.g., Kp, Ki, Kd)</li>
  <li>Reference values</li>
  <li>Run timestamp</li>
</ul>

<h3>Simulation Data</h3>
<ul>
  <li>Time</li>
  <li>Reference signal</li>
  <li>Measured output</li>
  <li>Error</li>
  <li>Control input</li>
</ul>



<h2>API Endpoints (Example)</h2>
<ul>
  <li><b>POST /api/simulations</b> → Save simulation data</li>
  <li><b>GET /api/simulations</b> → List simulations</li>
  <li><b>GET /api/simulations/{id}</b> → Get simulation details</li>
</ul>

<h2>Technologies</h2>
<ul>
  <li>Java</li>
  <li>Spring Boot</li>
  <li>PostgreSQL</li>
  <li>JPA / Hibernate</li>
</ul>


<h2> Project Structure</h2>
<ul>
  <li><b>/controller</b> → REST API endpoints</li>
  <li><b>/service</b> → Business logic</li>
  <li><b>/repository</b> → Data access layer</li>
  <li><b>/entity</b> → Database models</li>
</ul>

<h2>Status</h2>
<p>
This project is under development. Core functionality for data storage and retrieval is being implemented.
</p>

<h2> Notes</h2>
<p>
The platform is intended to support control system analysis by enabling structured storage and access to simulation data.
Future improvements may include data visualization.
</p>
