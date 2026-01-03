# Login Test Cases

## CT-LOGIN-001 - Login com email e senha válidos
GIVEN usuário cadastrado  
WHEN informa email e senha válidos  
THEN sistema permite acesso  

Expected Result: Usuário logado  
Actual Result: Usuário logado  
Status: PASS  

---

## CT-LOGIN-002 - Login com senha incorreta
GIVEN usuário cadastrado  
WHEN informa senha inválida  
THEN sistema exibe mensagem de erro  

Expected Result: Sistema bloqueia login  
Actual Result: Sistema exibe mensagem de erro  
Status: PASS  

---

## CT-LOGIN-003 - Login com email inexistente
GIVEN usuário não cadastrado  
WHEN informa email inexistente  
THEN sistema exibe mensagem de erro  

Expected Result: Sistema bloqueia login  
Actual Result: Sistema permite login  
Status: FAIL  
