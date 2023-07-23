# Telecom
---

# Introdução

O presente projeto tem por objetido analisar o comportamento dos clientes de uma empresa de telecominucações, com o intuito de determinar quais planos pré-pagos geram mais receita. 


--- 

# Descrição dos dados

## A tabela users (dados sobre usuários):
* user_id    — identificação do usuário;
* first_name — nome do usuário
* last_name  — último sobrenome do usuário
* age        — idade do usuário (em anos)
* reg_date   — data da inscrição (dd, mm, aa)
* churn_date — a data que o usuário parou de usar o serviço (se o valor for ausente, o plano estava sendo usado quando esse dado foi gerado)
* city       — cidade de residência do usuário
* plan       — nome do plano


## A tabela calls (dados sobre as chamadas)
* id        — identificador de chamada unívoco
* call_date — data da chamada
* duration  — duração da chamada (em minutos)
* user_id   — o identificador do usuário que faz a chamada


## A tabela messages (dados nas mensagens de texto):
* id            — identificador unívoco de mensagem de textos
* message_date  — data da mensagem de texto
* user_id       — o identificador do usuário que envia a mensagem de texto


## A tabela internet (dados sobre sessões web):
* id            — identificador de sessão unívoco
* mb_used       — o volume de dados gasto durante a sessão ( em megabytes)
* session_date  — data da sessão web
* user_id       — identificador do usuário


## A tabela plans(dados sobre os planos):
* plan_name             — o nome do plano de chamadas
* usd_monthly_fee       — preço mensal em dólares dos EUA
* minutes_included      — pacote de minutos mensal
* messages_included     — pacote de mensagens de texto mensal
* mb_per_month_included — pacote de volume de dados (em megabytes)
* usd_per_minute        — preço por minuto depois de exceder o limite do pacote (por exemplo, se o pacote inclui 100 minutos, o primeiro minuto excedente será cobrado)
* usd_per_message       — preço por mensagem de texto depois de exceder o limite do pacote
* usd_per_gb            — preço por gigabyte extra de dados após exceder o limite do pacote (1 GB = 1024 megabytes)



--- 

# Conclusão 


Inicialmente foi feita uma exploração dos dados, onde foi encontrado alguns pequenos erros e surgiu a idéia de criar um Data Frame único com dados tratados para facilitar e tornar a análise mais precisa. 

Bem, observa-se no decorrer da análise a predominância do uso do serviço nos últimos meses do ano, os gráficos mostram uma evolução do uso dos serviços, os motivos podem ser vários, mas não conseguimos precisar o motivo por falta de dados que possam corroborar as teses a serem elaboradas. 

Observa-se ainda que o plano Surf supera o plano Ultimate em quantidade de cliente, assim superando também em receita. Os clientes do plano Surf possuem uma media de limites excedidos muito superiores que o plano Ultimate, chegando a alguns clientes a pagar $590,37 no plano mensal, enquanto no plano ultimate o máximo registrado foi de $182,00. 

O comportamento de uso dos clientes parece não condizer com os planos contratados, superando muito os limites que o plano possui. Mas mesmo com essa discrepância da média dos valores pagos pelos usuários do plano Surf, em relação ao valor do próprio plano, a média de Receita do plano Ultimate é superior em $11,60. Ao todo são 339 clientes do plano Surf no total contra 131 do plano Ultimate.

Os clientes que pagam o excedente do plano Surf possuem uma receita média de $76,06, o que supera a receita média dos clientes do plano Ultimate que é de $72,31, como foi testado estatisticamente e a hipótese de que o plano ultimate teria a receita média maior foi rejeitada. 
    
Isso demonstra que o plano Surf não se adequa estatisticamente às necessidades dos clientes que o assinam, ou vice-versa. Ou seja, não cumpre o que é proposto. Já que a média por usuário do plano Surf é de $60,70/mês, enquanto a do plano Ultimate é de $72,31/mês.
    
A concentração de clientes em uma área mais ativa eletrônicamente como NY também favorece a essa atividade que excede o plano.

Ante o exposto, é aconselhável um programa de *"upgrade"* de plano para clientes que excedem o pacote oferecido pelo Plano Surf, de forma a aumentar a receita média do Plano Ultimate, estabilizando a receira, pois o Plano Surf mesmo com seu excedente e gerando mais receita, está sujeito a variações de acordo com o consumo dos usuários, sendo assim sujeito a mais volatilidade que o plano Ultimate. Essa discrepância de receita entre um e outro pode ser encarado como uma atipicidade pois decorreu de excedentes muito fora da média. 
