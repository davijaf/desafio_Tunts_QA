# desafio_Tunts_QA
Planejamento de Teste

## Objetivo: 
O objetivo do teste é garantir que o formulário está aceitando as entradas corretamente e gravando os dados corretamente no banco de dados.

## Escopo:
1. O teste em si consistirá em preencher o formulário de cadastro com diferentes valores e verificar se o formulário está tratando cada entrada de forma correta. 
2. Algumas verificações incluem:
*  validar o nome para garantir que não contém números ou caracteres especiais, verificar se o nome tem no máximo 50 caracteres, 
*  validar o endereço de e-mail para garantir que está no formato correto, 
*  validar a senha para garantir que contém pelo menos um caractere especial, um número e uma letra, e 
*  verificar se a senha digitada no campo "repetir senha" é a mesma que foi digitada no campo "senha". 
3. Depois de preencher o formulário com as entradas corretas, o teste verificará se o botão "cadastrar" é habilitado e, em seguida, clicará no botão para verificar se os dados são gravados corretamente no banco de dados.
4. Verificar se o formulário de cadastro simples está aceitando as entradas e gravando os dados corretamente no banco de dados, considerando que o e-mail de cadastro não é pré-existente no banco de dados.

## Recursos necessários:
Acesso ao formulário de cadastro simples.
Acesso ao banco de dados para verificar se os dados estão sendo gravados corretamente.

## Entradas: 
* “nome”, 
* “e-mail”, 
* “senha”,
* “repetir senha”,
* botão “cadastrar”.

## Cenário de teste (Execução):
1. Acesse a página do formulário de cadastro.
2. Verifique se o botão "cadastrar" encontra-se desabilitado.
3. Tente preencher o campo "nome" com caracteres especiais e números.
4. Verifique se o campo "nome" foi invalidado e exibe a mensagem de erro "O campo nome não pode conter números ou caracteres especiais.".
5. Tente preencher o campo "nome" acima de 50 caracteres do tipo letras.
6. Ao tentar digitar o 51º caractere verifique se exibe a mensagem de erro "O campo nome aceita apenas 50 caracteres no máximo".
7. Preencha o campo "nome" com "Davi José" e saia do campo.
8. Verifique se o campo "nome" foi validado com sucesso.
9. Preencha o campo "e-mail" com "davijose_gmail.com" e saia do campo.
10. Verifique se o campo "e-mail" foi invalidado e exibe a mensagem de erro "O campo e-mail só permite e-mail’s válidos no formato: nome@email.algo."
11. Preencha o campo "e-mail" com "davijose@gmail.com" e saia do campo.
12. Verifique se o campo "e-mail" foi validado com sucesso.
13. Preencha o campo "senha" com "senha123" e saia do campo.
14. Verifique se o campo "senha" foi invalidado e exibe a mensagem de erro "Lembre-se que deverá ser informado no mínimo 4 caracteres (Ao menos uma letra, um caractere especial e um número)."
15. Preencha o campo "senha" com "S12@" e saia do campo.
16. Verifique se o campo "senha" foi validado com sucesso.
17. Tente preencher o campo "repetir senha" com uma senha diferente da escrita no campo "senha".
18. Verifique se o campo "repetir senha" foi invalidado e exibe a mensagem de erro "As senhas não coincidem".
19. Preencha o campo "repetir senha" com a mesma senha escrita no campo "senha".
20. Verifique se o campo "repetir senha" foi validado com sucesso.
21. Verifique se o botão "cadastrar" está habilitado.
22. Ao concluir o preenchimento, altere os campos com preenchimentos contrários às regras, um por vez.
23. Verifique se o botão "cadastrar" está desabilitado. 
24. Retome os preenchimento dos campos: "nome" com "Davi José", "e-mail" com "davijose@gmail.com", "senha" com "S12@" e "repetir senha" com "S12@"
25. Verifique se o botão "cadastrar" está habilitado.
26. Clique no botão "cadastrar".
27. Verifique se o cadastro foi realizado com sucesso e armazenado com sucesso em um banco de dados local.
28. Verifique se a mensagem de sucesso "Cadastro realizado com sucesso!" é exibida para o usuário.
29. Refaça o preenchimento do formulário de cadastro simples utilizando o e-mail “davijose@gmail.com”, atentando aos critérios exigidos para os outros campos.
30. Clique no botão "cadastrar".
31. Verifique se o cadastro foi recusado e exibe a mensagem de erro "“E-mail” já cadastrado, o cadastro não pode ser finalizado. ".

## Saídas esperadas:
* Todos os campos são inválidos antes do preenchimento correto ser realizado.
* O campo "repetir senha" é invalidado e exibe a mensagem de erro "As senhas não coincidem" quando as senhas não são iguais.
* O botão "cadastrar" só está habilitado quando não há pendências nos campos de “nome”, “e-mail”, “senha” e “repetir senha”.
* O cadastro é realizado com sucesso e armazenado com sucesso em um banco de dados local apenas para e-mail inexistente (único) no banco de dados.

## Condições de saída: 
* O teste é encerrado quando o aviso de sucesso é exibido.
