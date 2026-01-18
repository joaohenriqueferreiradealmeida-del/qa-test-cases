**# Bug Reports – File Upload**

**## Objective**
Identify functional, validation, security, and usability issues related to file upload functionality, ensuring data integrity, system stability, and proper user feedback.

**## Scope:**
These bug reports cover scenarios related to:
- File format validation
- File size limits
- Upload interruptions
- Error handling and messaging
- Security validation of uploaded files

**## Out of Scope:**
- File download functionality
- File storage infrastructure performance
- User permissions and access control

**## Test Environment:**
- Application Type: Web Application
- Module: File Upload
- Browser: Google Chrome
- Operating System: Windows
- Environment: Test / Staging

**## Preconditions:**
- System is online and accessible
- User is authenticated
- File upload functionality is enabled

**## Test Type:**
- Manual Testing
- Functional Testing
- Validation Testing
- Security Testing
- Negative Testing

--- 

**CT-BUG-01 – Sistema aceita arquivo com formato não permitido**

**Descrição:**
O sistema permite o upload de arquivos com extensões não suportadas, violando as regras de validação de formato.

**Pré-condições:**
- Sistema online
- Usuário autenticado
- Módulo de upload disponível

**Passos para reprodução:**
1. Acessar o sistema
2. Selecionar um arquivo com formato inválido (ex: .exe, .bat)
3. Escolher o destino do arquivo
4. Clicar em “Fazer upload”

**Resultado esperado:**
- Campo de upload destacado em vermelho
- Mensagem informando formato inválido
- Lista de formatos permitidos exibida
- Botão de upload desabilitado

**Resultado obtido:**
- O sistema aceita o arquivo
- Upload realizado com sucesso

**Severidade:** Baixa
**Prioridade:** Baixa
**Status:** Aberto

---

**CT-BUG-02 – Upload permite arquivo acima do tamanho máximo permitido**

**Descrição:**
O sistema permite o upload de arquivos que excedem o limite máximo configurado.

**Pré-condições:**
- Sistema online
- Usuário autenticado
- Upload habilitado

**Passos para reprodução:**
1. Acessar o sistema
2. Selecionar um arquivo acima do tamanho permitido
3. Escolher o destino
4. Clicar em “Fazer upload”

**Resultado esperado:**
- Mensagem informando que o tamanho excede o limite
- Indicação do tamanho máximo permitido
- Botão de upload desabilitado

**Resultado obtido:**
Upload realizado normalmente

**Severidade:** Baixa
**Prioridade:** Baixa
**Status:** Aberto

---

**CT-BUG-03 – Falha no upload sem feedback ao usuário**

**Descrição:**
Quando o upload falha, o sistema não exibe nenhuma mensagem informando o erro ao usuário.

**Pré-condições:**
- Sistema online
- Usuário autenticado

**Passos para reprodução:**
1. Acessar o sistema
2. Selecionar um arquivo válido
3. Iniciar o upload
4. Simular falha durante o processo

**Resultado esperado:**
- Mensagem explicando o motivo da falha
- Opção para tentar novamente

**Resultado obtido:**
- Barra de progresso trava
- Nenhuma mensagem exibida

**Severidade:** Baixa
**Prioridade:** Baixa
**Status:** Aberto

---

**CT-BUG-04 – Sistema não valida o conteúdo real do arquivo**

**Descrição:**
O sistema valida apenas a extensão do arquivo, não o seu conteúdo real, permitindo upload de arquivos maliciosos.

**Pré-condições:**
- Estar na tela de upload de imagem de perfil
- Arquivo script.php renomeado para foto.jpg

**Passos para reprodução:**
1. Selecionar o arquivo renomeado
2. Clicar em “Enviar”

**Resultado esperado:**
- Upload rejeitado
- Mensagem informando que o arquivo não é uma imagem válida

**Resultado obtido:**
- Upload aceito
- Arquivo salvo no servidor

**Severidade:** Alta
**Prioridade:** Alta
**Status:** Aberto

---

**CT-BUG-05 – Exibição de mensagem técnica ao usuário**

**Descrição:**
Mensagens técnicas internas são exibidas ao usuário final em caso de erro no upload.

**Pré-condições:**
- Sistema online
- Usuário autenticado

**Passos para reprodução:**
1. Enviar um arquivo que ultrapasse o tempo limite do servidor

**Resultado esperado:**
- Mensagem genérica e amigável (ex: “Não foi possível completar o upload. Tente novamente.”)

**Resultado obtido:**
- Exibição de erro técnico (ex: SQLSTATE, Error 500)

**Severidade:** Baixa
**Prioridade:** Média
**Status:** Aberto

---

**CT-BUG-06 – Sistema permite upload sem seleção de arquivo**

**Descrição:**
O sistema permite iniciar o upload sem que nenhum arquivo tenha sido selecionado.

**Pré-condições:**
- Sistema online
- Usuário autenticado

**Passos para reprodução:**
- Acessar o sistema
- Selecionar apenas o destino
- Clicar em “Fazer upload”

**Resultado esperado:**
- Alerta solicitando a seleção de um arquivo
- Botão desabilitado até a seleção

**Resultado obtido:**
- Barra de carregamento infinita
- Erro interno após atualização da página

**Severidade:** Média
**Prioridade:** Alta
**Status:** Aberto

---
