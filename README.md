THIS IS CSS CODE. 
#It tell us how the front of the web page will look like

body {
  font-family: Arial, sans-serif;
  background-color: #f4f6f9;
  margin: 0;
  padding: 0;
}

div {
  text-align: center;
}

nav {
  background-color: #2563eb;
  color: white;
  padding: 15px;
  display: flex;
  justify-content: space-between;
}

button {
  background-color: #2563eb;
  color: white;
  border: none;
  padding: 8px 15px;
  border-radius: 5px;
  cursor: pointer;
}

h2 {
  margin-top: 30px;
}

div > div {
  background: white;
  margin: 20px auto;
  padding: 15px;
  width: 300px;
  border-radius: 10px;
  box-shadow: 0px 2px 5px rgba(0,0,0,0.2);
}


HERE WE USED THE REACT COMPONENT
#it shows what will be displayed in the job board


import './App.css'; 
import { useState } from 'react';
import Login from "./Login";
import ApplyForm from "./ApplyForm";
import CandidateDashboard from "./CandidateDashboard";
import EmployerDashboard from "./EmployerDashboard";
function App() {
 const [search, setSearch] = useState("");
  return (
    <div>
      <nav>
        <h1>Job Board</h1>
        <button>Login</button>
      </nav>

      <h2>Find Your Dream Job</h2>
      <input
  type="text"
  placeholder="Search Jobs..."
  value={search}
  onChange={(e) => setSearch(e.target.value)}
/>
      <p>Browse the latest job opportunities.</p>

      <h3>Featured Jobs</h3>
    {search === "" || "Frontend Developer".toLowerCase().includes(search.toLowerCase()) ? (

      <div>
        <h4>Frontend Developer</h4>
        <p>Google</p>
        <button>Apply</button>

      </div>
    ) : null}

      <div>
        <h4>Backend Developer</h4>
        <p>Microsoft</p>
        <button>Apply</button>
      </div>

      <div>
        <h4>UI/UX Designer</h4>
        <p>Amazon</p>
        <button>Apply</button>
      </div>
      <hr />

<Login />

<hr />

<ApplyForm />

<hr />

<CandidateDashboard />

<hr />

<EmployerDashboard />
    </div>
  );
}

export default App;



#this part creates the job application form

function ApplyForm() {
  return (
    <div>
      <h2>Job Application Form</h2>

      <input type="text" placeholder="Enter Name" />
      <br /><br />

      <input type="email" placeholder="Enter Email" />
      <br /><br />

      <button>Submit</button>
    </div>
  );
}

export default ApplyForm;



#it displays the candidate dashboard

function CandidateDashboard() {
  return (
    <div>
      <h2>Candidate Dashboard</h2>
      <p>Applied Jobs: 2</p>
    </div>
  );
}

export default CandidateDashboard;




#IT DISPLAYS THE EMPLOYER DASHBOARD

function EmployerDashboard() {
  return (
    <div>
      <h2>Employer Dashboard</h2>
      <button>Add Job</button>
    </div>
  );
}

export default EmployerDashboard;




#WE WROTE THIS CODE FOR THE STYLING PART ON HOW THE BOARD WILL LOOK LIKE

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background-color: #f4f6f9;
}




#HERE WE CREATED THE LOGIN PAGE


function Login() {
  return (
    <div>
      <h2>Login Page</h2>

      <input type="email" placeholder="Email" />
      <br /><br />

      <input type="password" placeholder="Password" />
      <br /><br />

      <button>Login</button>
    </div>
  );
}

export default Login;





#HERE OUR REACT APPLICATION STARTED

import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App.jsx'
import './index.css'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
)
