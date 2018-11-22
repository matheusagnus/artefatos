|||
|--|--|
|**Título**|Portal da Nuvem Serpro - Guia rápido|
|**Última atualização**|2018-08-13|
|**Autor(es)**|Adriano Martins|
|**Tipo**|Documentos internos|
|**Privacidade**|Ostensivo|
|**Criado em**|2018-08-13|
|**Coautoria**|Carlos Fiuza Villaça; Horácio Ibrahim|
|**Disclosure**|“Este é um documento do SERVIÇO FEDERAL DE PROCESSAMENTO DE DADOS (SERPRO), empresa pública federal regida pelo disposto na Lei Federal nº 5.615, criado exclusivamente a seu(s) destinatário(s) e pode conter informações confidenciais, protegidas por sigilo profissional. Sua utilização desautorizada é ilegal e sujeita o infrator às penas da lei. Se recebeu esse link, documento ou cópia indevidamente, queira, por gentileza, reenviá-la ao emitente, esclarecendo o equívoco."|



# Portal da Nuvem Serpro - Guia rápido

## 1 – INTRODUÇÃO 

A Nuvem SERPRO é um modelo que permite acesso amplo, conveniente e sob demanda a um conjunto compartilhado de recursos computacionais configuráveis. 

O SERPRO oferta o modelo de Infraestrutura como Serviço - ICS com liberdade para o cliente implementar e executar suas aplicações de forma independente. Além disso, oferece diversas aplicações nas quais é possível destacar: 

- Testes de desenvolvimento
- Hospedagem de sites
- Armazenamento, backup e recuperação
- Aplicativos Web

O SERPRO disponibiliza um portal de acesso no qual o cliente poderá realizar a gestão do seu Centro de Dados Virtual, podendo alocar e liberar recursos contratados de acordo com suas necessidades.

## 2 – UTILIZAÇÃO DO PORTAL 

### 2.1 – Tela de login 

Acessar o endereço https://nuvem.serpro.gov.br. Na tela principal, informe o e-mail cadastrado e sua senha.

![enter image description here](//home/77767233120/Documentos/Imagens/CPS_Tela01.jpg)

### 2.2 – Tela de acesso 

Na tela abaixo, clique no link ‘Infraestrutura como Serviço’ no quadro de verde para prosseguir e acessar a tela do Dashboard.

### 2.3 – Dashboard 

A tela do Dashboard apresenta o painel de indicadores que já foram criados pelo usuário, tais como: quantidade de instâncias (máquinas), memória RAM, vCPUs e etc. 

Além disso, é possível criar instâncias clicando no item 'Instâncias' localizado no painel esquerdo do Dashboard. 

### 2.4 –  Instâncias 

Na tela abaixo são mostradas as instâncias já criadas pelo usuário e suas características (nome, tipo, estado ip e etc.). 

#### 2.4.1 – Criando uma nova instância

Na tela abaixo, clique no botão 'Criar instância'.

A seguinte tela será apresentada. Selecione o sistema operacional desejado dentre os disponíveis.
Na tela seguinte, selecione a configuração básica da instância, a qual inclui quantidade de CPUs virtuais, memória RAM e espaço em disco.

Na etapa de configuração de rede, os seguintes itens devem ser definidos:

Os grupos de segurança para definir as regras de firewall que serão aplicadas à instância o uso do par de chaves dentre as disponíveis ou a geração de um novo. O par de chaves permite uma conexão segura à instância que está sendo criada. O sistema guardará a sua chave pública e só permitirá acesso à instância com a chave privada. 
A chave privada deve ser salva nessa etapa da criação da instância, pois não será possível fazer o download da chave novamente. 
A rede privada que será associada à nova instância. 

Pares de chave são credenciais SSH injetadas nas imagens quando instanciadas. Criar um novo par de chaves registrará a chave pública e baixará a chave privada (um arquivo .pem). 

Proteja e utilize a chave como você faria normalmente com qualquer chave privada SSH. 
Ao final, clique no botão 'Revisar e Finalizar'.

Revise a configuração da sua instância antes de concluir. A instância será iniciada automaticamente após a confirmação. 

Clique botão 'Voltar' caso necessite realizar alguma correção ou em 'Confirmar' caso esteja tudo ok. Ao clicar no botão 'Confirmar' a sua máquina será criada.

### 2.5 – Volumes 

#### 2.5.1 – Associando volumes

Nessa etapa é possível criar e associar volumes de disco para instâncias já criadas.

Para associar um volume, clique no item 'Volume' localizado no painel esquerdo. A seguinte tela será mostrada. Selecione um volume de disco existente na tabela apresentada no painel direito. Na coluna 'Ações' selecione a instância para a qual deve ser associado o volume de disco.

#### 2.5.2 – Criando volumes

Na tela abaixo, clique no botão 'Criar volume'.

Após clicar no botão 'Criar volume', a seguinte tela será apresentada. Preencha os campos Nome, Descrição, Tamanho (em GB) e A partir da Origem e, em seguida, clique no botão 'Salvar'.

#### 2.5.3 - Criando Snapshots

Snapshots permitem ao administrador criar uma 'foto instantânea' de um volume lógico em um determinado período. Com esta ferramenta, apenas é salvo o estado do volume no momento que o snapshot foi feito. Exemplo: às 12h foi feito o snapshot de um volume, sendo que às 12h15 foi feita uma alteração do mesmo, que não deveria ser feita. Com o snapshot, o usuário poderá restaurar o estado do volume exatamente como estava às 12h.

### 2.6 - Imagens

Para criar uma imagem, clique no item 'Imagens' localizado no painel esquerdo. A seguinte tela será mostrada. Selecione uma imagem existente na tabela apresentada no painel direito. Na coluna 'Ações' clique no botão 'Lançar' para concluir a ação.

### 2.7 – Segurança 

Para criar um novo grupo de segurança, clique no item 'Segurança' localizado no painel esquerdo. A seguinte tela será mostrada. Clique no botão 'Criar Grupo de Segurança'.

Após clicar no botão 'Criar Grupo de Segurança', a seguinte tela será mostrada. Preencha os campos Nome do Grupo e Descrição do Grupo e, em seguida, clique no botão 'Salvar Grupo'.

Após a criação do grupo, a opção 'Regras' será apresentada. Clique no botão para 'Nova regra' para criar uma nova regra de segurança. Preencha os campos Regra, Direção, Protocolo, Intervalo de Portas, Origem e Prefixo Local e, em seguida, clique no botão 'Salvar regra'.

É possível também utilizar uma regra existente. Para isso, selecione uma regra na tabela e, em seguida, clique no botão 'Atualizar Grupo'.

### 2.8 – Topologia de redes 

Para verificar a topologia de rede utilizada, clique no item 'Redes' localizado no painel esquerdo. A seguinte tela será mostrada.

#### 2.8.1 – Criando redes

Para criar uma nova rede, clique na aba 'Redes' e, em seguida, clique no botão '+Criar Rede'.

Após clicar no botão '+Criar Rede', a seguinte janela será mostrada. Preencha os campos Nome, Endereço de Rede e IP do Gateway e, em seguida, clique no botão 'Próximo'.

Após clicar no botão 'Próximo', a seguinte tela será apresentada. Preencha os campos Habilitar DHCP, Pools de Alocação e Servidores de nome DNS de acordo com as especificações da sua rede. Ao final, clique no botão 'Confirmar'.

### 2.9 – Relatório de Uso 

Para gerar relatórios de uso da infraestrutura como serviço, clique no item 'Relatórios' localizado no painel esquerdo. A seguinte tela será mostrada.

Informe o período para o qual deve ser gerado relatório de uso de recursos. Para isso, preencha os campos Dt. Inicial e Dt. Final e, em seguida, clique no botão 'Consultar'. O relatório de uso será apresentado na tela principal.


