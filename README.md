<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ecovidyalaya Volunteer Registration & Ticket Booking</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Brick Sans', sans-serif;
            background-color: green;
            color: white;
            text-align: center;
        }
        h1 {
            font-size: 4rem;
            margin-top: 50px;
        }
        h3 {
            font-size: 2rem;
            margin-bottom: 30px;
        }
        .form-container {
            background: rgba(255, 255, 255, 0.2);
            padding: 20px;
            border-radius: 10px;
            width: 80%;
            margin: 20px auto;
        }
        .form-container label {
            display: block;
            text-align: left;
            margin-bottom: 5px;
            font-weight: bold;
        }
        .form-container input {
            width: 100%;
            padding: 8px;
            margin-bottom: 15px;
            border: none;
            border-radius: 5px;
        }
        .form-container button {
            background-color: white;
            color: green;
            border: none;
            padding: 10px;
            width: 100%;
            font-size: 1rem;
            border-radius: 5px;
            cursor: pointer;
        }
        .form-container button:hover {
            background-color: darkgreen;
            color: white;
        }
        .nav-button {
            margin-top: 20px;
            padding: 10px 20px;
            background-color: darkorange;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.2rem;
            cursor: pointer;
            text-decoration: none;
        }
        .nav-button:hover {
            background-color: orangered;
        }
        .section {
            display: none;
        }
        .section.active {
            display: block;
        }
    </style>
</head>
<body>
    <h1>ECOVIDYALAYA</h1>

    <!-- Navigation Buttons -->
    <div>
        <button class="nav-button" onclick="showSection('volunteer')">Go to Volunteer Registration</button>
        <button class="nav-button" onclick="showSection('ticket')">Go to Ticket Booking</button>
    </div>

    <!-- Volunteer Registration Section -->
    <div class="section active" id="volunteer">
        <h3>Become a Volunteer</h3>
        <div class="form-container">
            <form action="https://docs.google.com/forms/d/e/1FAIpQLSftN1w4p6Qghk9L7pS1yHJmJd5c1fgF8bmbc96p4MwDxgfG9g/formResponse" method="POST">
                <label for="name">Name</label>
                <input type="text" id="name" name="entry.123456789" placeholder="Enter your name" required>

                <label for="email">Email</label>
                <input type="email" id="email" name="entry.987654321" placeholder="Enter your email" required>

                <label for="phone">Phone Number</label>
                <input type="text" id="phone" name="entry.1122334455" placeholder="Enter your phone number" required>

                <label for="institution">Institution/Organization</label>
                <input type="text" id="institution" name="entry.2233445566" placeholder="Enter your institution/organization" required>

                <button type="submit">Register</button>
            </form>
        </div>
    </div>

    <!-- Ticket Booking Section -->
    <div class="section" id="ticket">
        <h3>Write Tickets for Ecovidyalaya Exhibition</h3>
        <div class="form-container">
            <form action="https://formsubmit.co/YOUR_EMAIL_ADDRESS" method="POST">
                <input type="hidden" name="_subject" value="Ecovidyalaya Ticket Confirmation">
                <input type="hidden" name="_captcha" value="false">
                <input type="hidden" name="_next" value="YOUR_THANK_YOU_PAGE_URL">

                <label for="name">Name</label>
                <input type="text" id="name" name="name" placeholder="Enter your name" required>

                <label for="email">Email</label>
                <input type="email" id="email" name="email" placeholder="Enter your email" required>

                <button type="submit">Submit</button>
            </form>
        </div>
    </div>

    <script>
        // Function to show the active section and hide others
        function showSection(sectionId) {
            // Hide all sections
            document.querySelectorAll('.section').forEach(function(section) {
                section.classList.remove('active');
            });

            // Show the selected section
            document.getElementById(sectionId).classList.add('active');
        }
    </script>
</body>
</html>
