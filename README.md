<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Mini Instagram</title>
</head>
<body>
  <header>
    <h1>Mini Instagram</h1>
    <p>Um clone pobre, mas honesto.</p>
    <hr>
  </header>
  <section>
    <h2>Publicar uma foto</h2>
    <form>
      <label>Usuário:</label><br>
      <input type="text" placeholder="Seu nome"><br><br>
      <label>Legenda:</label><br>
      <textarea rows="3" cols="40" placeholder="Escreva algo..."></textarea><br><br>
      <label>Imagem:</label><br>
      <input type="file" accept="image/*"><br><br>
      <input type="submit" value="Publicar">
    </form>
  </section>
  <hr>
  <section>
    <h2>Feed</h2>
    <article>
      <h3>@maria</h3>
      <img src="https://via.placeholder.com/300" alt="Foto de exemplo"><br>
      <p>"Acordei cedo, tomei café e já cansei."</p>
      <p>❤️ 132 curtidas</p>
    </article>
    <article>
      <h3>@joao</h3>
      <img src="https://via.placeholder.com/300" alt="Foto de exemplo"><br>
      <p>"Mais um dia sem ser contratado pelo Instagram."</p>
      <p>❤️ 87 curtidas</p>
    </article>
  </section>
  <footer>
    <hr>
    <p>© 2025 Mini Instagram - Feito com HTML puro e paciência</p>
  </footer>
</body>
</html>