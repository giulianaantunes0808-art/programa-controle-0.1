# programa-controle-0.1
Atividade programação 1.0
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <title>Controle Simples</title>
</head>
<body>
  <h2>Lista de Tarefas</h2>
  <input id="tarefa" placeholder="Digite a tarefa" />
  <button onclick="adicionar()">Adicionar</button>

  <ul id="lista"></ul>

  <script>
    function adicionar() {
      const input = document.getElementById('tarefa');
      const texto = input.value.trim();
      if (!texto) return alert('Digite uma tarefa!');
      const li = document.createElement('li');
      li.textContent = texto;
      li.onclick = () => li.style.textDecoration = li.style.textDecoration === 'line-through' ? '' : 'line-through';
      li.ondblclick = () => li.remove();
      document.getElementById('lista').appendChild(li);
      input.value = '';
      input.focus();
    }
  </script>
</body>
</html>
