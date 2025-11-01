<html lang="pl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Strona z tłem i nawigacją</title>
  <style>
    /* Reset podstawowych stylów */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    /* Ustawienia dla body, aby tło było pełne i responsywne */
  body {
      height: 100vh;
      background-image: url('images/ChybaTerazDobrze.jpg');
      background-size: cover;
      background-position: center;
      display: flex;
      flex-direction: column;
      justify-content: flex-end; /* Ustawienie elementów na dole */
      font-family: Arial, sans-serif;
    }

    /* Styl dla linku na dole */
  .next-link {
      display: block;
      text-align: center;
      padding: 20px;
      background: rgba(255, 255, 255, 0.7);
      font-size: 1.2em;
      text-decoration: none;
      color: #333;
      transition: background 0.3s, color 0.3s;
    }

    /* Efekt hover dla linku */
  .next-link:hover {
      background: rgba(255, 255, 255, 1);
      color: #000;
    }

    /* Dla urządzeń mobilnych można dodać dodatkowe media query, jeśli potrzebujesz */
  @media (max-width: 600px) {
      .next-link {
        font-size: 1em;
        padding: 15px;
      }
    }
  </style>
</head>
<body>
  <!-- Link do następnej strony na dole -->
  <a href="page2.html" class="next-link">nasze zwierzaki</a>
</body>
</html>
