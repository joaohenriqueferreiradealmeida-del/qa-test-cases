# Testes de Login e Cadastro de Usuário

## Sistema
Aplicação web de cadastro e login de usuários

## Objetivo
Validar o funcionamento do fluxo de cadastro e autenticação de usuários,
garantindo que regras de negócio, validações e mensagens ao usuário estejam corretas.

---

## CT-LOGIN-01 – Login com email e senha válidos

**Pré-condição:**  
Usuário já cadastrado no sistema

**Passos:**  
1. Acessar a página de login  
2. Informar email válido  
3. Informar senha válida  
4. Clicar em “Entrar”

**Resultado esperado:**  
Usuário é autenticado e redirecionado para a área logada do sistema

---

## CT-LOGIN-02 – Login com senha inválida

**Pré-condição:**  
Usuário já cadastrado no sistema

**Passos:**  
1. Acessar a página de login  
2. Informar email válido  
3. Informar senha inválida  
4. Clicar em “Entrar”

**Resultado esperado:**  
Sistema exibe mensagem de erro informando credenciais inválidas
