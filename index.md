<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500;700&display=swap" rel="stylesheet">
    <title>Document</title>
    <style>
        :root{
            --very-light-pink: #c7c7c7;
            --text-input-field: #f7f7f7;
            --hospital-green: #acd9b2;
            --white: #FFFFFF;
            --black: #000000;
            --sm: 14px;
            --md: 16px;
            --lg: 18px;
        }
        body{
            font-family: 'Quicksand', sans-serif;
            margin: 0;
        }
       
        .login{
            width: 100%;
            height: 100vh;
            display: grid;
            place-items: center;
        }
        .form-container{
            display: grid;
            /*Aun no entiendo esto del todo*/
            grid-template-rows: auto 1fr auto;
            width: 300px;
        }
        .logo{
            width: 150px;
            margin-bottom: 48px;
            justify-self: center;
            /*para que no aparezca en desktop*/
            display: none;
        }
        
        
        .lab{
            font-size: var(--sm);
            font-weight: bold;
            margin-bottom: 4px;

        }
        .input{
            background-color: var(--text-input-field);
            border: none;
            border-radius: 8px;
            height: 32px;
            font-size: var(--md);
            padding: 6px;
            margin-bottom: 12px;

        }

        .input-email{
            margin-bottom: 22px;
        }

        .form{
            display: flex;
            /*Permite que ambos form esten posicionados uno encima de otro, flex por default agrupa elementos en una misma fila*/
            flex-direction: column;
        }
        
        .form a{
            color: var(--hospital-green);
            font-size: var(--sm);
            text-align: center;
            text-decoration: none;
            margin-bottom: 54px;
        }
        .pimary-button{
            background: var(--hospital-green);
            border-radius: 8px;
            border: none;
            color: var(--white);
            width: 100%;
            cursor: pointer;
            font-size: var(--md);
            font-weight: bold;
            height: 50px;
        }

        .secondary-button{
            background: var(--white);
            border-radius: 8px;
            border: 1px solid var(--hospital-green);
            color: var(--hospital-green);
            width: 100%;
            cursor: pointer;
            font-size: var(--md);
            font-weight: bold;
            height: 50px;
        }
        .login-button{
            margin-top: 12px;
            margin-bottom: 30px;
        }
        @media (max-width:600px){
            .logo{
                display: block;
            }
        }
    </style>
</head>
<body>
    <div class="login">
        <div class="form-container">
            <img src="./curso-frontend-developer-practico/logos/logo_yard_sale.svg" alt="logo" class="logo">

           <form action="/" class="form">
            <label for="email" class="label">Email Address</label>
            <input type="text" id="email" placeholder="Platzi@example.com" class="input input-email">

            <label for="new-password" class="label">Password</label>
            <input type="password" id="new-password" placeholder="*********" class="input input-password">
            <input type="submit" value="Log in" class="pimary-button login-button">
            <a href="/">Forgot my password</a>
            </form>

            <button class="secondary-button signup-button">Sign up</button>
        </div>
    </div>
</body>
</html>
