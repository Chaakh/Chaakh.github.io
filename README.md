<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Embedded Website</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            width: 100%;
        }
        iframe {
            width: 100%;
            height: 100%;
            border: none;
        }
        /* Hide specific elements */
        iframe::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 50px; /* Adjust as needed */
            background: white;
            z-index: 1;
        }
    </style>
</head>
<body>
    <iframe src="https://h5.colorpark.cn/#/pages/index/detailsphone?machine_id=1123146"></iframe>
</body>
</html>
