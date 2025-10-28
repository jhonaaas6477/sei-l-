<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Exercício de CSS</title>

  <style>
    /* Seletor por TAG */
    body {
      background-color: #f2f2f2;
      font-family: Arial, sans-serif;
    }

    h1 {
      color: blue;
      text-align: center;
    }

    /* Seletor por CLASSE */
    .destaque {
      color: red;
      font-weight: bold;
    }

    /* Seletor por ID */
    #rodape {
      background-color: #222;
      color: white;
      text-align: center;
      padding: 10px;
      margin-top: 20px;
    }

    /* Seletor por TAG */
    h2 {
      color: green;
    }
  </style>
</head>
<body>

  <h1>Loja Bigjohn Supplements</h1>
  <p>Confira alguns produtos:</p>

  <h2>Whey Protein</h2>
  <p>Suplemento para ganhar massa muscular.</p>

  <h2 class="destaque">Creatina</h2>
  <p>Ajuda a aumentar força e energia.</p>

  <h2>BCAA</h2>
  <p>Auxilia na recuperação muscular.</p>

  <div id="rodape">
    © 2025 Bigjohn Supplements
  </div>

</body>
</html>