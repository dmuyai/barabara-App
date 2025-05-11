# barabara-App
Making Services Available, Accessible, and Affordable
Barabara, an app transforming the service industry, locating and making the invisible, the isolated, unrecognized, or undiscovered beneficiaries (consumers, service providers, and partners) visible on the mobile workspace.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Community Services</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <div class="container">
    <h1>Community Services</h1>
    <form id="service-form">
      <input type="text" id="service-name" placeholder="Service Name" required />
      <input type="text" id="service-description" placeholder="Description" required />
      <button type="submit">Add Service</button>
    </form>
    <ul id="service-list"></ul>
  </div>
  <script src="script.js"></script>
</body>
</html>
-----
body {
  font-family: Arial, sans-serif;
  background-color: #f4f4f4;
  margin: 0;
  padding: 0;
}

.container {
  width: 90%;
  max-width: 600px;
  margin: 50px auto;
  background: #fff;
  padding: 20px;
  border-radius: 5px;
}

h1 {
  text-align: center;
}

form {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}

form input {
  padding: 10px;
  margin: 5px 0;
}

form button {
  padding: 10px;
  background: #28a745;
  color: #fff;
  border: none;
  cursor: pointer;
}

form button:hover {
  background: #218838;
}

#service-list {
  list-style-type: none;
  padding: 0;
}

#service-list li {
  background: #e9ecef;
  margin: 5px 0;
  padding: 10px;
  border-radius: 3px;
}
-------
document.getElementById('service-form').addEventListener('submit', function(e) {
  e.preventDefault();

  const name = document.getElementById('service-name').value;
  const description = document.getElementById('service-description').value;

  const li = document.createElement('li');
  li.textContent = `${name}: ${description}`;

  document.getElementById('service-list').appendChild(li);

  // Clear form fields
  document.getElementById('service-name').value = '';
  document.getElementById('service-description').value = '';
});
