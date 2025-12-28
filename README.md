# Validação de Formulário (Vanilla JS)

Este projeto implementa uma validação de formulário no front-end usando **JavaScript puro**, sem bibliotecas externas.  
Ele valida campos obrigatórios, usuário, CPF e senha, exibindo mensagens de erro diretamente abaixo dos inputs.

---

## ✅ Funcionalidades

- Remove mensagens de erro antigas antes de validar novamente
- Valida campos vazios (nenhum campo pode ficar em branco)
- Valida **Usuário**
  - Deve ter entre **3 e 12 caracteres**
  - Deve conter apenas **letras e/ou números**
- Valida **CPF** usando uma classe externa `ValidaCPF`
- Valida **Senha**
  - Deve ter entre **6 e 12 caracteres**
  - Senha e repetir senha devem ser iguais
- Só envia o formulário (`submit`) quando **tudo estiver válido**

---

## 🧠 Como funciona

A classe `ValidaFormulario`:

- Captura o formulário `.formulario`
- Intercepta o evento `submit` para impedir o envio automático
- Executa duas validações principais:
  - `camposSaoValidos()` → valida inputs gerais + usuário + CPF
  - `senhasSaoValidas()` → valida regras de senha
- Exibe mensagens de erro com `criaErro(campo, msg)` criando uma `<div class="error-text">`

---

## 📁 Estrutura esperada

Sugestão de estrutura (ajuste conforme seu projeto):

/assets
/css
style.css
/js
main.js
validaCPF.js
index.html


> O arquivo `validaCPF.js` deve definir a classe `ValidaCPF`, usada no `main.js`.

---

## ▶️ Como executar

1. Baixe/clonar o projeto
2. Abra o `index.html` no navegador  
   **ou** use um servidor local (recomendado), por exemplo:
   - Extensão **Live Server** no VSCode

---

## 🔗 Dependências

- Nenhuma biblioteca externa
- Apenas JavaScript no navegador

---

## ⚙️ Requisitos do HTML

Os inputs devem ter classes específicas para que o script funcione:

- `.formulario` no `<form>`
- `.validar` em todo campo que deve ser validado
- `.usuario` no campo de usuário
- `.cpf` no campo de CPF
- `.senha` no campo de senha
- `.repetir-senha` no campo de confirmação de senha

Exemplo:

```html
<form class="formulario">
  <input class="usuario validar">
  <input class="cpf validar">
  <input class="senha validar">
  <input class="repetir-senha validar">
</form>

📜 Licença

Este projeto é livre para uso e estudo.
