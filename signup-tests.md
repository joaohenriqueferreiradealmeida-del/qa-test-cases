# Signup Test Cases

## CT-SIGNUP-001 - Cadastro com dados válidos
GIVEN usuário não cadastrado  
WHEN informa dados válidos  
THEN sistema realiza cadastro com sucesso  

Expected Result: Cadastro efetuado  
Actual Result: Cadastro efetuado  
Status: PASS  

---

## CT-SIGNUP-002 - Cadastro com email já existente
GIVEN usuário já cadastrado  
WHEN tenta cadastrar com email existente  
THEN sistema exibe mensagem de erro  

Expected Result: Sistema bloqueia cadastro  
Actual Result: Sistema permite cadastro  
Status: FAIL  
