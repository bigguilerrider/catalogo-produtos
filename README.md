<!DOCTYPE html><html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Catálogo de Produtos</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f8f8f8;
      margin: 0;
      padding: 20px;
    }
    h1 {
      text-align: center;
    }
    .catalogo {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
    }
    .produto {
      background-color: #fff;
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 10px;
      width: 200px;
      text-align: center;
      cursor: pointer;
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    .produto img {
      width: 100%;
      height: auto;
      border-radius: 4px;
    }
    .modal {
      display: none;
      position: fixed;
      z-index: 1000;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0,0,0,0.5);
      justify-content: center;
      align-items: center;
    }
    .modal-content {
      background-color: #fff;
      padding: 20px;
      border-radius: 8px;
      max-width: 500px;
      width: 90%;
      text-align: center;
    }
    .fechar {
      float: right;
      font-size: 24px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Catálogo de Produtos</h1>
  <div class="catalogo">
    <div class="produto" onclick="abrirDetalhes('Produto 1', 'produto1.jpg', 'Descrição técnica do Produto 1')">
      <img src="https://via.placeholder.com/200" alt="Produto 1">
      <p>Produto 1</p>
    </div>
    <div class="produto" onclick="abrirDetalhes('Produto 2', 'produto2.jpg', 'Descrição técnica do Produto 2')">
      <img src="https://via.placeholder.com/200" alt="Produto 2">
      <p>Produto 2</p>
    </div>
    <div class="produto" onclick="abrirDetalhes('Produto 3', 'produto3.jpg', 'Descrição técnica do Produto 3')">
      <img src="https://via.placeholder.com/200" alt="Produto 3">
      <p>Produto 3</p>
    </div>
    <div class="produto" onclick="abrirDetalhes('Produto 4', 'produto4.jpg', 'Descrição técnica do Produto 4')">
      <img src="https://via.placeholder.com/200" alt="Produto 4">
      <p>Produto 4</p>
    </div>
    <div class="produto" onclick="abrirDetalhes('Produto 5', 'produto5.jpg', 'Descrição técnica do Produto 5')">
      <img src="https://via.placeholder.com/200" alt="Produto 5">
      <p>Produto 5</p>
    </div>
  </div>  <div id="modal" class="modal" onclick="fecharModal(event)">
    <div class="modal-content">
      <span class="fechar" onclick="fecharModal(event)">&times;</span>
      <h2 id="titulo-produto"></h2>
      <img id="imagem-produto" src="" alt="" style="width:100%; border-radius:8px; margin: 10px 0;">
      <p id="descricao-produto"></p>
    </div>
  </div>  <script>
    function abrirDetalhes(titulo, imagem, descricao) {
      document.getElementById('titulo-produto').innerText = titulo;
      document.getElementById('imagem-produto').src = imagem;
      document.getElementById('descricao-produto').innerText = descricao;
      document.getElementById('modal').style.display = 'flex';
    }

    function fecharModal(event) {
      if (event.target.classList.contains('modal') || event.target.classList.contains('fechar')) {
        document.getElementById('modal').style.display = 'none';
      }
    }
  </script></body>
</html>
