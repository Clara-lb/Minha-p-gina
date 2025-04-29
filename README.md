Olá, esse é meu primeiro código! O código usado para a criação desta página está escrito abaixo!!

1. (HTML)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Minha Página</title>
  <link rel="stylesheet" href="style.css">
  <link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">
</head>
<body>
  <div class="hearts"></div>

  <header>
    <h1>Oi, eu sou a Maria Clara!</h1>
    <p>Bem-vinde ao meu cantinho na web ✨</p>
    <div class="social-buttons">
      <a href="https://instagram.com/clara_lbm" target="_blank">Instagram</a>
      <a href="https://github.com/Clara-lb" target="_blank">GitHub</a>
      <a href="https://www.linkedin.com/in/maria-clara-lima-b-0367b624b/" target="_blank">LinkedIn</a>
    </div>
  </header>

  <section class="sobre-mim fade-in">
    <h2>Sobre Mim</h2>
    <p>Sou estudante de Gestão da informação na UFPE. Amo tecnologia, doces e sonhar alto! 💭</p>
  </section>

  <section class="hobbies fade-in">
    <h2>Meus Hobbies</h2>
    <ul>
      <li>Desenhar 🖌️</li>
      <li>Ouvir música 🎶</li>
      <li>Assistir filmes de animação 📺</li>
      <li>Explorar cafeterias ☕</li>
    </ul>
  </section>

  <section class="projetos fade-in">
    <h2>Projetos</h2>
    <p> Participo do projeto de extensão Holisticamente, que desenvolve diferentes ações na área de saúde e bem-estar. No momento, estou envolvida em uma oficina vinculada ao programa ProIdoso da faculdade, focada no letramento digital de idosos. Nosso objetivo é ensinar tanto a linguagem da internet quanto o uso prático dos celulares, promovendo autonomia e inclusão digital. 💻📚✨</p>
  </section>

  <footer>
    <p>Feito com muito carinho 💖 — Clara 2025</p>
  </footer>
</body>
</html>

2. Style CSS
/* Fonte */
body {
    font-family: 'Poppins', sans-serif;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
    background: linear-gradient(to right, #ffe4e1, #add8e6);
    color: #555;
  }
  
  /* Animação de fundo */
  @keyframes fadeBackground {
    0% { background: #ffe4e1; }
    100% { background: #add8e6; }
  }
  
  /* Corações flutuando */
  .hearts::before, .hearts::after {
    content: "💖";
    position: absolute;
    font-size: 2rem;
    animation: floatHearts 10s linear infinite;
    opacity: 0.7;
  }
  
  .hearts::before {
    top: 100%;
    left: 20%;
  }
  
  .hearts::after {
    top: 120%;
    left: 70%;
  }
  
  @keyframes floatHearts {
    0% {
      transform: translateY(0) rotate(0deg);
    }
    100% {
      transform: translateY(-120vh) rotate(360deg);
    }
  }
  
  /* Cabeçalho */
  header {
    background-color: #ffb6c1;
    color: white;
    padding: 30px;
    text-align: center;
    border-bottom: 4px solid #add8e6;
    position: relative;
    z-index: 1;
  }
  
  /* Botões sociais */
  .social-buttons {
    margin-top: 15px;
  }
  
  .social-buttons a {
    text-decoration: none;
    color: white;
    background-color: #add8e6;
    padding: 10px 20px;
    margin: 0 5px;
    border-radius: 20px;
    transition: background-color 0.3s;
  }
  
  .social-buttons a:hover {
    background-color: #87ceeb; /* azul mais forte */
  }
  
  /* Seções */
  section {
    margin: 20px;
    padding: 20px;
    background: white;
    border-radius: 20px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    position: relative;
    z-index: 1;
  }
  
  /* Títulos */
  h2 {
    color: #ff69b4;
  }
  
  /* Lista */
  ul {
    list-style-type: heart;
    padding-left: 20px;
  }
  
  ul li::marker {
    color: #ff69b4;
  }
  
  /* Rodapé */
  footer {
    background-color: #add8e6;
    color: white;
    text-align: center;
    padding: 15px;
    margin-top: 30px;
    border-top: 4px solid #ffb6c1;
    position: relative;
    z-index: 1;
  }
  
  /* Animação fade-in nas seções */
  .fade-in {
    opacity: 0;
    transform: translateY(30px);
    animation: fadeInUp 1s ease forwards;
    animation-delay: 0.5s;
  }
  
  @keyframes fadeInUp {
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
