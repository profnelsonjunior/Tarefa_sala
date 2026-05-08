# Atividade: Contador Interativo com JavaScript e CSS

## 📚 Disciplina
Programação Web / Desenvolvimento Front-End

---

## 🎯 Objetivo da Atividade

Desenvolver um contador interativo utilizando:

- HTML
- CSS
- JavaScript

O aluno deverá praticar:

- Eventos JavaScript
- Manipulação do DOM
- Alteração dinâmica de conteúdo
- Estilização com CSS

---

# 📝 Enunciado da Atividade

Crie uma página web contendo um contador interativo com as seguintes funcionalidades:

## ✅ Requisitos Obrigatórios

- Botão para aumentar o número
- Botão para diminuir o número
- Botão para resetar o contador
- Alterar a cor do número:
  - Verde → positivo
  - Vermelho → negativo
  - Azul → zero
- Interface estilizada com CSS

---

# 💻 Código Base da Atividade

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Contador Interativo</title>

  <style>

    body{
      font-family: Arial, sans-serif;
      background: #eef2f7;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    .container{
      background: white;
      padding: 30px;
      border-radius: 15px;
      text-align: center;
      box-shadow: 0px 4px 12px rgba(0,0,0,0.2);
      width: 320px;
    }

    h1{
      color: #333;
    }

    #contador{
      font-size: 60px;
      margin: 20px;
      color: blue;
      transition: 0.3s;
    }

    button{
      padding: 10px 20px;
      margin: 5px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
      transition: 0.3s;
    }

    button:hover{
      transform: scale(1.05);
    }

    .mais{
      background: #28a745;
      color: white;
    }

    .menos{
      background: #dc3545;
      color: white;
    }

    .reset{
      background: #ffc107;
    }

  </style>
</head>

<body>

  <div class="container">

    <h1>Contador</h1>

    <div id="contador">0</div>

    <button class="mais" onclick="aumentar()">+</button>

    <button class="menos" onclick="diminuir()">-</button>

    <button class="reset" onclick="resetar()">Resetar</button>

  </div>

  <script>

    let numero = 0;

    function atualizarTela(){

      const contador = document.getElementById("contador");

      contador.innerText = numero;

      if(numero > 0){
        contador.style.color = "green";
      }

      else if(numero < 0){
        contador.style.color = "red";
      }

      else{
        contador.style.color = "blue";
      }

    }

    function aumentar(){
      numero++;
      atualizarTela();
    }

    function diminuir(){
      numero--;
      atualizarTela();
    }

    function resetar(){
      numero = 0;
      atualizarTela();
    }

  </script>

</body>
</html>
