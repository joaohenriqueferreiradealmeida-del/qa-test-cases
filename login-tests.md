# Casos de Teste – Login

## Objetivo
Validar o comportamento da funcionalidade de login do sistema, garantindo que apenas usuários com credenciais válidas consigam acessar a aplicação e que mensagens de erro apropriadas sejam exibidas em cenários inválidos.

---

## CT-LOGIN-01 – Login com e-mail sem @

**Objetivo:**  
Validar que o sistema não permite login com e-mail em formato inválido.

**Pré-condição:**  
Usuário não autenticado.

**Passos:**  
1. Acessar a tela de login  
2. Preencher o campo e-mail sem o caractere "@"  
3. Preencher o campo senha com dados válidos  
4. Clicar em "Entrar"

**Resultado esperado:**  
O sistema exibe mensagem de erro informando e-mail inválido e não realiza o login.

**Resultado obtido:**  
O sistema exibe mensagem de erro e bloqueia o login.

**Status:**  
PASS

---

## CT-LOGIN-02 – Login com e-mail inexistente

**Objetivo:**  
Validar que o sistema não permite login com e-mail não cadastrado.

**Pré-condição:**  
Usuário não autenticado.

**Passos:**  
1. Acessar a tela de login  
2. Informar um e-mail não cadastrado  
3. Informar uma senha válida  
4. Clicar em "Entrar"

**Resultado esperado:**  
O sistema exibe mensagem informando que o e-mail não está cadastrado.

**Resultado obtido:**  
O sistema exibe mensagem de erro e não realiza o login.

**Status:**  
PASS

---

## CT-LOGIN-03 – Campo senha vazio

**Objetivo:**  
Validar que o sistema impede login quando o campo senha está vazio.

**Pré-condição:**  
Usuário não autenticado.

**Passos:**  
1. Acessar a tela de login  
2. Preencher o campo e-mail com dados válidos  
3. Deixar o campo senha vazio  
4. Clicar em "Entrar"

**Resultado esperado:**  
O sistema exibe mensagem de campo obrigatório.

**Resultado obtido:**  
O sistema exibe mensagem de campo obrigatório.

**Status:**  
PASS

---

## CT-LOGIN-04 – Login com Caps Lock ativado

**Objetivo:**  
Validar o comportamento do sistema ao realizar login com Caps Lock ativado.

**Pré-condição:**  
Usuário não autenticado.

**Passos:**  
1. Acessar a tela de login  
2. Ativar Caps Lock  
3. Informar e-mail válido  
4. Informar senha válida  
5. Clicar em "Entrar"

**Resultado esperado:**  
O sistema realiza o login ou exibe mensagem de erro sem falha funcional.

**Resultado obtido:**  
O sistema exibe mensagem de credenciais inválidas.

**Status:**  
PASS

---

## CT-LOGIN-05 – Login com e-mail e senha válidos

**Objetivo:**  
Validar que o sistema permite login com credenciais válidas.

**Pré-condição:**  
Usuário cadastrado.

**Passos:**  
1. Acessar a tela de login  
2. Informar e-mail válido  
3. Informar senha válida  
4. Clicar em "Entrar"

**Resultado esperado:**  
O sistema autentica o usuário e redireciona para a página inicial.

**Resultado obtido:**  
O usuário é autenticado com sucesso.

**Status:**  
PASS
