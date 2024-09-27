<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Group-9</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #F1F1F1; /* Light Gray */
        }
        .container {
            width: 80%;
            margin: 0 auto;
            padding: 20px;
        }
        .header {
            text-align: center;
            padding: 20px 0;
        }
        .header h1 {
            margin: 0;
            color: #FFFFFF;
            background-color: #1A3D7C; /* Dark Blue */
            padding: 20px;
            border-radius: 8px;
        }
        .header h3 {
            color: #1A3D7C; /* Dark Blue */
            margin-top: 10px;
        }
        .team {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
        }
        .member {
            background-color: #FFFFFF; /* White background for cards */
            width: 250px;
            margin: 20px;
            padding: 15px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
            border-radius: 8px;
        }
        .member img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            margin-bottom: 15px;
        }
        .member h3 {
            margin: 10px 0 5px;
            color: #1A3D7C; /* Dark Blue */
        }
        .member p {
            color: #666;
            font-size: 14px;
            margin-bottom: 15px;
        }
        .member a {
            text-decoration: none;
            color: #C19A6B; /* Gold */
            font-weight: bold;
            background-color: #1A3D7C; /* Dark Blue */
            padding: 10px 15px;
            border-radius: 5px;
            display: inline-block;
            transition: background-color 0.3s ease;
        }
        .member a:hover {
            background-color: #C19A6B; /* Gold */
            color: #FFFFFF; /* White text on hover */
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>Meet Our Team</h1>
            <h3>Group-9</h3>
        </div>
        <div class="team">

            <?php
                // PHP array to store team members
                $team = [
                    ['name' => 'John Dred Finez', 'role' => 'Leader', 'img' => '2.jpg', 'link' => 'https://m.facebook.com/jhndrdfnz/'],
                    ['name' => 'Michael Roy Arcilla', 'role' => 'Member', 'img' => '1.jpg', 'link' => 'https://www.facebook.com/michael.arcilla.7140/'],
                    ['name' => 'John Luis Nuza', 'role' => 'Member', 'img' => '3.jpg', 'link' => 'https://www.facebook.com/johnxluis14?mibextid=ZbWKwL'],
                    ['name' => 'John Christian Dimaya', 'role' => 'Member', 'img' => '4.jpg', 'link' => 'https://www.facebook.com/johnchristian.dimaya.5']
                ];

                // Loop through each team member and display their information
                foreach ($team as $member) {
                    echo '
                        <div class="member">
                            <img src="'.$member['img'].'" alt="'.$member['name'].'">
                            <h3>'.$member['name'].'</h3>
                            <p>'.$member['role'].'</p>
                            <a href="'.$member['link'].'">Click Me!</a>
                        </div>
                    ';
                }
            ?>

        </div>
    </div>

    <!-- JavaScript -->
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            const members = document.querySelectorAll('.member');

            members.forEach(member => {
                member.addEventListener('click', function() {
                    alert('You clicked on ' + member.querySelector('h3').textContent);
                });
            });
        });
    </script>
</body>
</html>
