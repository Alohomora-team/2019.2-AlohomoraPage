# Alohomora - Portaria Virtual

#### Versão 1.1

## Histórico de Revisão
| Data | Versão | Descrição | Autor |
| ---- | ------ | --------- | ----- |
| 20/09/2019 | 1.0 | Formatação da estrutura e criação do documento | Aline Lermen, Rodrigo Lima
| 25/09/2019 | 1.1 | Edição e complemento dos tópicos 2.2, 2.3, 3.6, 4.2, 4.4, 5, 6 | Luis Fernando Furtado, João Luis Baraky
| 29/09/2019 | 1.2 | Correção de erros ortográficos e de sintaxe| João Luis Baraky, Victor Jorge Gonçalves
| 04/10/2019 | 1.3 | Adição do licenciamento do projeto | João Luis Baraky, Victor Jorge Gonçalves


## Sumário
__[1. Introdução ](#1-introducao)__\
[1.1 Objetivo ](#11-objetivo)\
[1.2 Escopo ](#12-escopo)\
[1.3 Definições, Acrônimos e Abreviações ](#13-definicoes-acronimos-e-abreviacoes)\
[1.4 Referências ](#14-referencias)\
[1.5 Visão Geral ](#15-visao-geral)

__[2. Posicionamento ](#2-posicionamento)__\
[2.1 Oportunidade de Negócios ](#21-oportunidade-de-negocios)\
[2.2 Instruções do Problema ](#22-instrucao-do-problema)\
[2.3 Instrução da Posição do Produto ](#23-instrucao-da-posicao-do-produto)


__[3. Descrições da Parte Interessada e do Usuário ](#3-descricoes-da-parte-interessada-e-do-usuario)__\
[3.1 Resumo da Parte Interessada ](#31-resumo-da-parte-interessada)\
[3.2 Resumo do Usuário ](#32-resumo-do-usuario)\
[3.3 Ambiente do Usuário ](#33-ambiente-do-usuario)\
[3.4 Perfis das Partes Interessadas ](#34-perfis-das-partes-interessadas)\
[3.4.1 Equipe de Desenvolvimento ](#341-equipe-de-desenvolvimento)\
[3.4.2 Equipe de Engenharia de Produto ](#342-equipe-de-engenharia-de-produto)\
[3.4.3 Professores ](#343-professores)\
[3.5 Perfis dos Usuários ](#35-perfis-dos-usuarios)\
[3.6 Principais Necessidades da Parte Interessada e Usuários ](#36-principais-necessidades-por-parte-do-condominio-moradores-e-usuarios)

__[4. Visão Geral do Produto ](#4-visao-geral-do-produto)__\
[4.1 Perspectiva do Produto ](#41-perspectiva-do-produto)\
[4.2 Resumo dos Recursos ](#42-resumo-dos-recursos)\
[4.3 Suposições e Dependências ](#43-suposicoes-e-dependencias)\
[4.4 Licenciamento ](#44-licenciamento)

__[5. Recursos do Produto ](#5-recursos-do-produto)__\
[5.1 Interação com o sistema via voz ](#51-interacao-com-o-sistema-alohomora-via-voz)\
[5.2 Interação da aplicação com o usuário via Bot ](#52-interacao-da-aplicacao-com-o-usuario-via-bot-telegram)

__[6. Restrições ](#6-restricoes)__\
[6.1 Restrição de Design ](#61-restricao-de-design)\
[6.2 Restrição de implementação ](#62-restricao-de-implementacao)\
[6.3 Restrição de uso ](#63-restricao-de-uso)



## 1. Introdução
### 1.1 Objetivo
O documento visa definir e apontar as características gerais do projeto portaria virtual Alohomora, esclarecendo seu propósito, sua utilidade e funcionamento sem se aprofundar em termos técnicos.

### 1.2 Escopo
A portaria virtual Alohomora tem como objetivo automatizar as funções exercidas por um porteiro e de autenticar usuários por voz, gerenciando o fluxo de pessoas que entram e saem de um condomínio. A funcionalidade é baseada na ideia de que um morador ou funcionário do condomínio tenha sua entrada permitida ao ter sua voz reconhecida e autenticada pelo sistema. Para isso, é necessário que haja um cadastro prévio deles.

Para visitantes, o protocolo é diferente. Ao chegar à portaria, o indivíduo será questionado se possui cadastro: em caso negativo, será requerido dele alguns dados, como o nome e CPF. Após a verificação do cadastro, o visitante dirá para qual apartamento deseja ir e o sistema enviará uma notificação para o morador para que tome a decisão sobre a entrada do visitante.

### 1.3 Definições, acrônimos e abreviações
| Acrônimo/Abreviação | Definição |
| ------------------- | --------- |
| UnB | Universidade de Brasília |
| EPS | Engenharia de Produto de *Software* |
| MDS | Métodos de Desenvolvimento de *Software* |

### 1.4 Referências
IBM Knowledge Center - Documento de Visão: A estrutura de tópicos do documento de visão. Disponível em: [https://www.ibm.com/support/knowledgecenter/pt-br/SSWMEQ_4.0.6/com.ibm.rational.rrm.help.doc/topics/r_vision_doc.html](https://www.ibm.com/support/knowledgecenter/pt-br/SSWMEQ_4.0.6/com.ibm.rational.rrm.help.doc/topics/r_vision_doc.html). Acesso em: 20 set. 2019;
		LIMA, Eduardo; TAIRA, Luís; PATROCÍNIO, Sofia; PEREIRA, Samuel; GOUVEIA, Micaella; RIOS, Calebe; MUNIZ, Amanda; DUARTE, Indiara; RIBEIRO, Luciana. Projeto Gaia: DocVisao. Disponível em: [https://github.com/fga-eps-mds/2019.1-Gaia/blob/master/docs/produto/DocVisao.md](https://github.com/fga-eps-mds/2019.1-Gaia/blob/master/docs/produto/DocVisao.md). Acesso em: 20 set. 2019.

### 1.5 Visão geral
Este documento apresenta a visão do projeto Alohomora,  descrevendo seu planejamento geral e expondo tópicos que especificam a descrição do problema a ser solucionado e como o produto pretende solucioná-lo. Aqui também são identificadas as partes constituintes do processo (partes interessadas e  usuários) e apresentados os recursos e restrições que envolvem o uso do produto.


## 2. Posicionamento
### 2.1 Oportunidade de Negócios
No mundo atual, a tecnologia tem abrangido diferentes áreas e facilitado diversos processos. Em um condomínio residencial, tanto os moradores quanto os visitantes precisam se identificar no momento em que desejam acessar o local. Entretanto, estes últimos necessitam de autorização para efetivar o acesso, outorgada pelo morador cujo apartamento deseja-se visitar.

Baseando-se nisso e dispondo de um sistema de biometria por voz, Alohomora procura automatizar, em certo nível, a dinâmica de permissão de entrada e também reduzir gastos do condomínio. A intenção é funcionar como um sistema seguro e prático para o reconhecimento de um morador e interação com o mesmo, através de um chatbot, para notificá-lo da chegada de um visitante.



### 2.2 Instrução do Problema
| O problema de | afeta | O impacto do problema é | Uma solução bem sucedida incluiria |
| :-----------: | :---: | :---------------------: | :--------------------------------------: |
| segurança em condomínio | moradores de condomínios | alto gasto com segurança no condomínio | a automação do processo de autorização de entrada no condomínio e redução de gastos |

### 2.3 Instrução da Posição do Produto
| Para | que | Alohomora | que | Diferente de | nosso produto |
| ---- | --- | --------- | --- | ------------ | ------------- |
| moradores de condomínios | precisam ter sua identidade verificada para serem autorizados a entrar e precisam ir até o interfone responder uma solicitação do porteiro | é um sistema de portaria virtual com a autenticação via biometria vocal | automatiza as funções de portaria de um condomínio | sistema de portaria convencional | fornece uma forma mais cômoda de o proprietário se autenticar e permitir a entrada de visitantes. |
| visitantes de condomínios | precisam ter sua identidade verificada e notificada ao morador cujo apartamento desejam visitar | possui um chatbot integrado | notifica o morador sobre a chegada do visitante e aguarda instrução | sistema de portaria convencional | executa a função de portaria de forma totalmente automatizada |


## 3. Descrições da Parte Interessada e do Usuário
### 3.1 Resumo da Parte Interessada
| Nome | Descrição | Responsabilidade |
| ---- | ----- | ---------- |
| Equipe de desenvolvimento | Estudantes da disciplina de MDS na UnB - Gama | Desenvolver e testar o *software*; documentar |
| Equipe de engenharia de produto | Estudantes da disciplina de EPS na UnB - Gama | Gerenciar a equipe, coordenar decisões a respeito do produto; documentar |
| Professores | Professores das disciplinas de EPS e MDS na UnB-Gama | Orientar os estudantes das equipes acima mencionadas e avaliar o projeto desenvolvido |

### 3.2 Resumo do Usuário
| Nome | Descrição |
| ---- | ----- |
| Moradores | Indivíduos que moram no condomínio e recebem visitantes|
| Visitantes |  Interessados em visitar algum apartamento/casa do condomínio

### 3.3 Ambiente do Usuário
Dois ambientes principais são preparados para uso.

É disponibilizado aos usuários um dispositivo/aparelho que possui um microfone para o reconhecimento de voz. Esse aparelho é para uso compartilhado. Além desse, os moradores interagem com o chatbot, através do aplicativo Telegram, necessitando de uma conta no mesmo e conexão com a internet.


### 3.4 Perfis das Partes Interessadas
#### 3.4.1 Equipe de desenvolvimento
| Representantes | Tipo | Responsabilidade | Critério de sucesso | Envolvimento |
| -------------- | ---- | ---------------- | ----------------------- | ------------ |
| Aline Lermen, João Baraky, Luis Furtado, Paulo Batista, Rodrigo Lima, Victor Silva | Estudantes de MDS na UnB-Gama | Desenvolver e testar o *software* | Cumprir o prazo estipulado para desenvolvimento do produto, atendendo todos os requisitos | Alto

#### 3.4.2 Equipe de engenharia de produto
| Representantes | Tipo | Responsabilidade | Critério de sucesso | Envolvimento |
| -------------- | ---- | ---------------- | ----------------------- | ------------ |
| Felipe Borges, Mateus Nóbrega, Samuel Borges | Estudantes de EPS na UnB-Gama | Gerenciar a equipe, coordenar decisões a respeito do produto | Cumprir o prazo estipulado, garantindo a qualidade da entrega | Alto |

#### 3.4.3 Professores
| Representantes | Tipo | Responsabilidade | Critério de sucesso | Envolvimento |
| -------------- | ---- | ---------------- | ----------------------- | ------------ |
| Carla Rocha, Joenio Marques | Professores das disciplinas de EPS e MDS pela UnB-Gama | Orientar os estudantes e avaliar o produto | Avaliar os diferentes aspectos do produto| Médio |

### 3.5 Perfis dos Usuários
| Representantes | Tipo | Responsabilidade | Critério de sucesso | Envolvimento |
| -------------- | ---- | ---------------- | ----------------------- | ------------ |
| Moradores de condomínios | Usuário frequente | | ter sua entrada verificada com segurança e praticidade; ser notificado sobre a chegada de visitantes | Alto |
| Visitantes | Usuário | | ter sua entrada autorizada (ou não) pelo morador, através de interação com o chatbot | Médio |

### 3.6 Principais Necessidades por Parte do Condomínio, Moradores e Usuários

#### Condomínio
| Necessidade | Prioridade | Solução Atual | Solução Proposta | Interesse |
| ----------- | ---------- | ------------- | ---------------- | --------- |
| Redução de custos em segurança e padronização do serviço | Alta | Sistema de portaria convencional onde depende de funcionários para resolver o problema | Substituição pela portaria virtual Alohomora, que opera 100% automatizada | Redução nos custos do condomínio relacionados a segurança |

#### Morador
| Necessidade | Prioridade | Solução Atual | Solução Proposta | Interesse |
| ----------- | ---------- | ------------- | ---------------- | --------- |
| Automação e segurança no processo de entrada de moradores no condomínio | Alta | Funcionários geralmente controlam a entrada de moradores ou o condomínio possui algum sistema de biometria (por exemplo, digital) | Sistema de biometria por voz que confirme a identidade do morador para permitir sua entrada | Maior comodidade do morador ao gerenciar a entrada de visitantes |

#### Usuário
-------
| Necessidade | Prioridade | Solução Atual | Solução Proposta | Interesse |
| ----------- | ---------- | ------------- | ---------------- | --------- |
| Automação no controle de visitas ao condomínio | Alta | Funcionários controlam o fluxo de visitantes no condomínio, informando sua chegada ao morador do apartamento de destino e autorizando a entrada, caso seja a instrução do morador responsável | Chatbot para notificar o morador da chegada do visitante e agir como uma ferramenta para permitir (ou não) o acesso do mesmo ao condomínio | Padronização da operação |


## 4. Visão Geral do Produto
### 4.1 Perspectiva do Produto
O projeto Alohomora busca atuar como uma portaria virtual, a qual intenciona a automação do controle de acesso ao condomínio. O sistema reconhece a voz dos moradores, previamente cadastrados. Assim, caso seja verificada sua identidade, o morador é autorizado a entrar. O sistema também conta com um chatbot, o qual realizará a interação com o morador, informando-o da chegada de um visitante e aguardando instruções para prosseguir: aceitar ou negar o acesso do visitante ao condomínio.

### 4.2 Resumo dos Recursos

| Benefício para o condomínio | Recursos |
| ------------------------ | ------------------- |
| Redução de custos com segurança e padronização do serviço | Presença de um sistema de autenticação por voz para substituir a portaria convencional |

| Benefício para o morador | Recursos |
| ------------------------ | ------------------- |
| Segurança nas permissões de acesso (de moradores e visitantes) ao condomínio, comodidade no gerenciamento de entrada de visitantes | Presença de um sistema de autenticação por voz, para garantir a veracidade na identificação do morador |

| Benefício para o visitante | Recursos |
| ------------------------ | ------------------- |
| Agilidade na comunicação com o sistema para validar a entrada de um visitante | Disposição de um chatbot para comunicação com o morador responsável pelo visitante |

### 4.3 Suposições e dependências
- o sistema Alohomora será utilizado em condomínios residenciais, que possuam algum representante para atuar como administrador;

- o morador deverá estar conectado à internet para ser informado da chegada de um visitante.

### 4.4 Licenciamento

- MIT License


## 5. Recursos do Produto

### 5.1 Interação com o sistema Alohomora via voz
A comunicação de nossa aplicação com o usuário, a fim de tomadas de decições para qual a ação que o usuário resolva tomar.

### 5.2 Interação da aplicação com o usuário via Bot Telegram
A finalidade é de conseguir gerenciar os cadastros, fazer a comunicação de dados com determinados usuários e notificar entrada de um visitante para moradores.

## 6. Restrições

### 6.1 Restrição de design
Para o serviço ser executado, deve haver os componentes de hardware necessários para poder integrar com o sistema do software Alohomora.

### 6.2 Restrição de implementação
A implementação deve seguir de forma que seja padronizada de acordo com o modelo servido pela aplicação Alohomora.

### 6.3 Restrição de uso
O usuário (morador) deve possuir conexão com a internet e uma conta no aplicativo Telegram.

