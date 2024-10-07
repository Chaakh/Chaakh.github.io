<?php
session_start();
$isAuthenticated = isset($_SESSION['authenticated']) && $_SESSION['authenticated'] === true;
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Phone Case Design Service</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            font-family: Arial, sans-serif;
        }
        <?php if ($isAuthenticated): ?>
        iframe {
            border: none;
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
        }
        <?php else: ?>
        .login-container {
            width: 300px;
            margin: 100px auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        input[type="email"], input[type="text"], input[type="submit"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            box-sizing: border-box;
        }
        input[type="submit"] {
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        input[type="submit"]:hover {
            background-color: #45a049;
        }
        <?php endif; ?>
    </style>
</head>
<body>
    <?php if ($isAuthenticated): ?>
        <iframe src="https://h5.colorpark.cn/#/pages/index/detailsphone?machine_id=1123146" frameborder="0"></iframe>
    <?php else: ?>
        <div class="login-container">
            <h2>Login to Access Design Service</h2>
            <form action="validate.php" method="post">
                <input type="email" name="email" placeholder="Email" required>
                <input type="text" name="order_number" placeholder="Order Number" required>
                <input type="submit" value="Access Design Service">
            </form>
        </div>
    <?php endif; ?>
</body>
</html>
