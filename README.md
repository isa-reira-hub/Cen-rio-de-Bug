# Cenário do Bug: Envio de Depoimento
#
### Link de acesso
https://teste-qa.icasei.com.br/depoimentos
#
### Descrição 
O usuário consegue inserir todas as informações no formulário, mas não consegue concluir, pois o botão não aciona nenhuma ação.
![bug depoimento](https://github.com/isa-reira-hub/Teste-Analista-de-Qualidade/assets/158104466/1e568274-b8ea-42e5-ad75-83dc624437b5)
#
#
### Passos para reproduzir o bug
1. Ir para o link de acesso
2. Preencher todo o formulário
3. Aceitar a _Autorização de exibição_
4. Clicar no botão de _Enviar_
#
#
### Comportamento esperado
* Após o preenchimento do formulário e a aceitação dos termos, o usuário deve concluir apertando no botão enviar.

### Comportamento Atual
* Nada acontece ao clicar no botão de enviar.
#
### Ambiente 
* Sistema Operacional: Windows 10
* Navegador/Versão: Edge Versão 126.0.2592.68 (Compilação oficial) (64 bits)
#
### Prioridade
* **Bloqueador** - Esse bug paralisa completamente os usuários de fazer depoimentos
#
### Identificação do bug
- Passo 1: Verificar se o botão está disparando algum evento.
- Passo 2: Abrir o DevTools e verificar se há algum erro no console
- Passo 3: Abrir a aba de rede do DevTools e inspecionar a requisição gerada.

- Foi verificado que o botão está funcionando, mas possui erro.
- Ao clicar no botão foi visto que o seguinte erro é gerado no console do navegador:
![print log](https://github.com/isa-reira-hub/Teste-Analista-de-Qualidade/assets/158104466/d27e3b93-6bf5-48e4-9221-297e9b735f3a)

- Ao verificar a aba de rede e inspecionar a requisição gerada retornou erro de código 500:
![image](https://github.com/isa-reira-hub/Cen-rio-de-Bug/assets/158104466/09358c46-ac3c-42d8-9027-bb7431b66123)

#### Endpoint: 
https://teste-qa.icasei.com.br/api/send-testimonials
#### Payload: 
    "avalie": "5",
    "email": "qualquer@gmail.com",
    "depoimento": "teste"

#### Resposta recebida: 
    "message": "Internal Server Error"

#### Erro 500 durante o envio de dados via POST
Descrição:
- Durante o envio de dados via POST para a API, ocorre um erro interno do servidor com a mensagem "Erro 500".

Possíveis Causas:
- Problemas de configuração no servidor.
- Erros no código do lado do servidor.
#
### Após identificado:
- Com base nas informações coletadas, abra um card ou relatório de bug com as especificações detalhadas.
- Notifique a equipe de desenvolvimento para que eles possam investigar e corrigir o problema.
- Ficar dispónível para qualquer dúvida remanescente.


