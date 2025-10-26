<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <title>Mini Instagram</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #fafafa;
      color: #333;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: white;
      padding: 20px;
      text-align: center;
      border-bottom: 1px solid #ddd;
      box-shadow: 0 1px 5px rgba(0,0,0,0.1);
    }

    section {
      max-width: 600px;
      margin: 20px auto;
      background-color: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 1px 5px rgba(0,0,0,0.1);
    }

    input, textarea {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }

    input[type="submit"] {
      background-color: #0095f6;
      color: white;
      border: none;
      cursor: pointer;
      font-weight: bold;
      transition: 0.3s;
    }

    input[type="submit"]:hover {
      background-color: #007bd6;
    }

    img {
      width: 100%;
      border-radius: 10px;
      margin-top: 10px;
    }

    article {
      border-top: 1px solid #ddd;
      padding-top: 15px;
      margin-top: 15px;
    }

    .like-btn {
      color: #ff3333;
      cursor: pointer;
      font-weight: bold;
      transition: 0.2s;
    }

    .like-btn:hover {
      transform: scale(1.1);
    }

    footer {
      text-align: center;
      padding: 15px;
      color: #777;
      font-size: 14px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Mini Instagram</h1>
    <p>Agora com um toque de CSS3 e JS.</p>
  </header>

  <section>
    <h2>Publicar uma foto</h2>
    <form id="postForm">
      <label>Usuário:</label>
      <input type="text" id="user" placeholder="Seu nome">

      <label>Legenda:</label>
      <textarea id="caption" rows="3" placeholder="Escreva algo..."></textarea>

      <label>Imagem (URL):</label>
      <input type="text" id="imageUrl" placeholder="Cole o link da imagem">

      <input type="submit" value="Publicar">
    </form>
  </section>

  <section id="feed">
    <h2>Feed</h2>
  </section>

  <footer>
    <p>© 2025 Mini Instagram - Feito em HTML, CSS e JS</p>
  </footer>

  <script>
    const form = document.getElementById('postForm');
    const feed = document.getElementById('feed');

    form.addEventListener('submit', function(event) {
      event.preventDefault();
      const user = document.getElementById('user').value.trim();
      const caption = document.getElementById('caption').value.trim();
      const imageUrl = document.getElementById('imageUrl').value.trim();

      if (!user || !caption || !imageUrl) {
        alert("Preencha todos os campos antes de postar!");
        return;
      }

      const article = document.createElement('article');
      article.innerHTML = `
        <h3>@${user}</h3>
        <img src="${imageUrl}" alt="Publicação de ${user}">
        <p>${caption}</p>
        <p><span class="like-btn">❤️ Curtir</span> <span class="like-count">0</span> curtidas</p>
      `;

      const likeBtn = article.querySelector('.like-btn');
      const likeCount = article.querySelector('.like-count');
      let count = 0;

      likeBtn.addEventListener('click', () => {
        count++;
        likeCount.textContent = count;
      });

      feed.prepend(article);
      form.reset();
    });
  </script>
</body>
</html>