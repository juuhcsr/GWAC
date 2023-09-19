# GWAC
Documentação Técnica referente a certificação Professional Google Workspace Administrator.

Essa documentação visa ajudar a entender os principais tópicos e a se preparar para o conteúdo da prova de Professional Google Workspace Administrator.

  A maior parte da prova tem configurações de Gmail ou configurações no próprio painel de administrador do google. Os principais assuntos pra lembrar dessa parte da prova é sobre os protocolos de segurança como SPF, DMARC e DKIM, sobre regras de roteamento, as principais opções de compliance e outros assuntos que veremos nesse doc.


<details>
<summary> Opções no Painel de Administrador </summary><br/>

Uma das coisas importantes pra prova é lembrar onde cada coisa pode ser encontrada dentro do painel de administrador como funções de usuários, as funções de compliance, os principais relatórios, onde configurar cada coisa. A tabela abaixo mostra as principais opções dentro do painel de administrador:

| Opção no Painel de Administrador | Descrição                                        |
|:---------------------------------:|:--------------------------------------------------:|
| Users                           | Gerenciamento de usuários do sistema, incluindo adição, edição e exclusão de contas. |
| Domain                          | Configurações relacionadas aos domínios do sistema. |
| Billing                         | Gerenciamento de informações de faturamento e pagamentos. |
| Groups                          | Configuração de grupos com permissões específicas para usuários. |
| Apps                            | Configurações relacionadas a aplicativos conectados ou integrados ao sistema. |
| Devices                         | Gerenciamento de dispositivos associados ao sistema, se aplicável. |
| Account Settings                | Configurações gerais da conta do administrador. |
| Organization Units              | Configuração de unidades organizacionais para estruturar usuários ou recursos. |
| Security                        | Configurações relacionadas à segurança do sistema, como autenticação e permissões. |
| Reports                         | Relatórios e análises detalhadas sobre o desempenho e uso do sistema. |

Seguindo essa lógica, podemos seguir os seguintes caminhos para obter relatórios específicos, é importante lembrar que cada um desses relatórios entregam diferentes tipos de dados:

|Relatório|	Caminho|
|:-:|:-:|
|Relatórios Específicos |	Reports > Audit/Investigation > Events|
|Roteamento de E-mail |	Apps > Google Workspace > Gmail > Routing|
|Relatórios Gerais ( Em gráficos ) |	Reports > Reports > Apps Reports > Accounts|
|Relatórios ( Em tabelas) |	Reports > Reports > Account reports > Accounts|
|Compliance ( Gmail )	| Apps > Google Workspace > Gmail > Compliance|

</details>

---

<details>
<summary> Funções administrativas </summary><br/>

Uma das boas práticas do google é a prática do privilégio mínimo onde cada usuário tem acesso às ferramentas e aos recursos necessários para as tarefas diárias. 

Para lidar com essa prática, podemos segmentar as funções administrativas dentro de uma empresa de modo que os colaboradores tenham acesso somente ao necessário.



|Função Administrativa |	Responsável Por |
|:-:|:-:|
|Superadministrador |	Gerencia todos os aspectos da Organização, incluindo recursos e privilégios. Recebe notificações importantes.|
|Administrador de Grupos |	Controla tarefas de Grupos do Google, gerencia perfis, cria e gerencia grupos, e adiciona marcadores de segurança.|
|Administrador de Gerenciamento de Usuários |	Realiza ações dos usuários, gerencia perfis e configurações de segurança.|
|Administrador de Atendimento ao Usuário |	Redefine senhas para usuários, visualiza perfis e estrutura organizacional.|
|Administrador de Serviços |	Gerencia dispositivos e configurações de serviços, ativa/desativa serviços e recursos.|
|Administrador de Dispositivo Móvel |	Gerencia dispositivos móveis, aplicativos e políticas de dispositivo.|
|Administrador de Armazenamento |	Gerencia o armazenamento, define limites, visualiza uso e acessa relatórios do Google Drive.|
|Administrador do Google Voice |	Gerencia configurações do Google Voice, números e licenças de usuário.|
|Administrador Revendedor e Administrador  Revendedor Indireto |	Funções exclusivas para revendedores autorizados do Google Workspace.|

</details>

---

<details>
<summary> Autenticação Google </summary><br/>

A autenticação do Google usa vários serviços, os principais conceitos vão de SSO a IDP e SP, vamos ver eles agora:

|Serviço|	Explicação
|IDP ( Identity provider)	Provedor de identidade que autentica usuários e emite tokens de segurança
|SP ( Service  Provider )	Servidor que aceita tokens e da acesso aos usuários
|LDAP ( Lightweight directory access protocol)	Protocolo que permite que os usários acessem dados no servidor ( Esse é o protocolo usado pelo servidor AD ( Active Directory) 
|SAML ( Security Assertion Markup Language )	Protocolo de autenticação, quando um usuário tenta acessar um app que usa saml, o SP solicita o IDP para autenticar o usuário

</details>

O último passo é configurar o domínio DNS. Isso envolverá a adição de registros DNS ao seu domínio para apontar para o Google Workspace.

Os registros DNS específicos que você precisa adicionar dependerão do seu registrador de domínio e do tipo de domínio que você registrou. No entanto, geralmente, você precisará adicionar os seguintes registros DNS:

- Nome do host (A) registro para o endereço IP do servidor do Google Workspace
- Registro MX para o servidor de correio do Google Workspace
- Registro TXT para o domínio do Google Workspace
Depois de adicionar os registros DNS, pode levar algumas horas para que as alterações sejam propagadas. Depois que as alterações forem propagadas, você poderá começar a usar o Google Workspace!


<details>
<summary> Google Cloud Directory Sync  </summary><br/>

Serviço que permite sincronizar usuários, grupos e outros dados de um diretório do Active Directory (AD) com o Google Cloud Platform (GCP). Isso pode ser útil para empresas que desejam usar o GCP, mas que também precisam manter seus usuários e grupos em um diretório do AD.


> **O que é LDAP** -  O LDAP (Lightweight Directory Access Protocol) é um protocolo de acesso a diretórios frequentemente usado pelo Active Directory (AD), que é o serviço de diretório da Microsoft usado em ambientes Windows para gerenciar recursos, autenticação e políticas de segurança.

usa uma série de regras para decidir o que sincronizar
</details>
</details>


---

<details>
<summary> Google Groups </summary><br/>

Grupos são usados para agrupar usuários com base em critérios compartilhados, enquanto Unidades Organizacionais (OUs) criam uma estrutura hierárquica para organizar usuários e recursos em uma organização.

Os grupos tem a função de decidir quais recursos serão compartilhados com maior prioridade que as OUs, por exemplo, grupos de OUs diferentes podem ter uma mesma permissão.

Grupos podem ser utilizados para evitar a modificação de OUs
  
<details>
<summary> Como criar grupos em uma organização </summary><br/>

Para criar um grupo em uma organização, você pode seguir estas etapas:

1. Acesse o [Console de administração do Google Workspace](https://admin.google.com).
2. Clique em "Diretórios".
3. Clique em "Grupos".
4. Clique em "Criar grupo".
5. Insira um nome para o grupo.
6. Selecione os usuários que deseja adicionar ao grupo.
7. Escolha as permissões que deseja conceder ao grupo.
8. Clique em "Criar".

  Para criar um grupo com todos de uma organização
  
 ```shell
everyone@dominio.com.br
```

> Uma opção interessante, é criar públicos-alvo (target audience) eles servem pra criar um espaço de compartilhamento de arquivos.

</details>
</details>

---


<details>
<summary> Permissões de Superadministrador</summary><br/>
</details>


Google Vault

Aplicativo para reter, manter, buscar e exportar dados.


Introdução aos domínios

Alias Domain - domínio secundário ligado ao principal

Serviços de migração

| Serviço                                       | Sigla | Uso                                                                                  |
|-----------------------------------------------|-------|--------------------------------------------------------------------------------------|
| G Workspace Migration for Microsoft Exchange      | GWMME | Migração de dados do Microsoft Exchange para o G Suite                               |
| Data Migration Service (DMS)                  | DMS   | Migração de dados para o G Suite de uma variedade de fontes, incluindo servidores locais, armazenamento em nuvem e sistemas de terceiros|
| Google Workspace Directory Sync               | GCDS | Sincronização de diretórios do Google Workspace com um diretório local ou LDAP         |
| Directory Sync for Microsoft Outlook           | GCDSFO | Sincronização de diretórios do Microsoft Outlook com o Google Workspace               |


Segurança

Ativar verificação em duas etapas
1. Segurança
2. 2- step verification
3. Allow 2SV
4. Save

Forçar senhas fortes
1. Segurança
2. password management
3. Config
4. Save

Bloquear apps não seguros
1. Securit
2. Less secure apps
3. Disable less secure apps
save

Opções de segurança dos usuários
- Restar senha
- Ver chaves de segurança
- Verificar verificação em duas etapas (2sv)
- Recuperar inforamções
- Requerer mudança de senha
- Desabilitar desafio de login
- Restar cookies de Sing-in
- ver e remover apps de terceiros 

Introdução a SSO Single Sign on
Idp - Identity provider - provedor de identidade
Sp - Service provider - Provedor de serviço
Ldap - Consulta acesso de diretórios em serviços Web

Google Workspace - mail

Dns - Domain Name System - sistema de gerenciamento de domínios 
Mx Records - Tipo de registro DNS que define os servidores de e-mail para um domínio.
Txt records - Inforamações de textos para fora do domínio
Cname Records - Informações de domínio mas baseado em domíonios 
A Record - Linka o domínio a um ip de um computador
NS Record - determina com servidor vai comunicar as informações dns 

Opções de segurança de Gmail

SPF - Sender Policy framework - Estrutura da política do remetente -  mecanismo de autenticação de e-mail que ajuda a evitar o spam e a falsificação de e-mail.
Dkim - Domain Keys Identified Mail Standard - Prevenção de Spoofing adicionando um header personalizado ao e-mail.
DMarc - Domain based message authentication - fala pro e-mail como lidar com mensagens SPF/DKIM

Configurando dkim
1. apps
2. Google Workspace
3. Gmail
4. autenticação de E-mails
5. Checar o status

pop - sincronização do gmail e outros serviços de email
Imap - sincroniza a conta em vários dispositivos

prevenção spam e pishing

Como criar uma whitelist de e-mails
1. apps
2. Google Workspace
3. Gmail
4. Spam, phishging e malware
5. email whitelist
6. adicionar o ip ou domínio
7. salvar

Compliance

Regras de complicance escaneiam e-mails e podem bloquear caso a mensagem bata com alguma regra criada, as mensagens podem ser:
- Rejeitadas antes de chegar ao receptor
- Enviada para quarentena para ser analisada por um administrador
- Editada antes de ser enviada
- Enviada como SPAM

Opções de compliance
- Emails e chat auto-deletion
- OCR for e-mail attachments
- Restricted delivery
- security sandbox

| Serviço                   | Uso                                                                                     |
|---------------------------|-----------------------------------------------------------------------------------------|
| Emails e chat auto-deletion | Os usuários podem definir um intervalo de tempo após o qual os e-mails e as mensagens de bate-papo serão excluídos automaticamente. Isso pode ajudar a proteger a privacidade dos usuários e a evitar o armazenamento de informações confidenciais por muito tempo. |
| OCR for e-mail attachments | Os usuários podem usar a tecnologia OCR para converter anexos de e-mail em texto. Isso pode ser útil para visualizar anexos que não são suportados por um programa de e-mail ou para extrair informações de anexos que não são formatados em um formato legível por humanos. |
| Restricted delivery       | Os usuários podem restringir a entrega de e-mails a certos endereços de e-mail ou domínios. Isso pode ser útil para evitar que e-mails sejam entregues a pessoas ou organizações indesejadas. |
| Security sandbox          | Os usuários podem usar uma sandbox de segurança para executar arquivos e aplicativos em um ambiente isolado. Isso pode ajudar a proteger os usuários contra malware e outros ataques. |




fases de migração de deployment

- Core it
- Early adopters
- Global go-live


### Core it (adição de usuários)
- Criação do design técnico
- Confirmação e testes do setup
- Identificar pontos de integração
- Familiarizar com ferramentas e tecnologias

### Early Adopters (5 - 15% da força de trabalho)
- Validar a migração
- Obter feedbacks
- Testes de mudança de gerenciamento
- Adição e configuração de usuários, grupos e contatos
> Designe google guides para ajudar com a organização

- nessa fase, o mx record envia primeiro para o servidor do google os e-mails e depois roteia para o servidor legado
  
### Global go live (100% da força de trabalho) 
- Inclusão de todos os funcionários
- Fácil acesso a treinamento requerido


Google Cloud directory sync 

sincornização de usuários do serviço LDAP

 para sincronizar senhas, use o gps - google password sync

 não é recomendado sincronizar OUs e calendários 


Mail routing

Determine como os emails são roteados e armazenados

| Tipo de roteamento | Definição                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------|
| Direct delivery    | O e-mail é entregue diretamente ao servidor de e-mail do destinatário.                                            |
| Dual delivery      | O e-mail é entregue ao servidor de e-mail do destinatário e a um serviço de entrega alternativo, como uma caixa de entrada de spam ou um serviço de arquivamento. |
| Split delivery     |Envio de e-mails para vários sistemas . |
| catch all | redirecionamento de e-mails invalidos |
| Redirecionamento | redireciona os e-mails para outra caixa de entrada |

> para evitar dados deletados e empregados demitidos, de pra eles uma lience de archived user (Archived user) e extenda o tempo da caixa de entrada


> a tecnologia utiliza para ver as configurações de aplicativos de terceiros é o Oauth

> Para ver um overview dos usuários reports>audit>tokens

> SAML - serviço de autenticação segura eficiente

> Para migrar um serviço Imap, use a ferramente data migration

> um funcionário foi demitido, para receber os e-mails enviados para ele, voce pode mapear a caixa de entrada com um map to map para receber os e-mails (

> apps>gwsp>gmail>routing)

> Um usuário perdeu o laptop com idp, para encerrar a seção dele, peça pra um adimistrador encerrar o SSO

> Domínio teste : domain-name.test.google-a.com

> O da colab seria julio.ferrer@colaborativaeduc.test.google-a.com

> Para splitar e-mails para servidor legado, é ncessário adicionar o servidor host e mudar a rota de envio para externa

> O Oauth é o protocolo de autorização que permite que aplicativos terceiros (third-party) acessem recursos em nome do usuário

> O dlp (data loss protection) é um serviço para efvitar o compartilhamento de informações esnsíveis

> Google workspace update blog - todos up updates do google workspace

> google workspace release calendar - datas de todas as atualizações

> existem dois tipos de atualizações

> training or resource launcher - mudanças mais tardias

> rapid release feature launch - assim que lançar os usuários vão receber as alterações

> Para adicionar arquivos CSV para usuários é obrigatório: primeiro nome, último nome, senha, e-mail e OU

> Um usuário deletado só pode ter seus dados recuperados dentro de 20 dias.

> para restaura-lo o seu nome não pode ter sido dado pra outra pessoa ou grupo

> Security sandbox só está disponível para versões enterprise

> Para dar permissões a apps terceiros, você precisa dos escopos de autorização e do client ID

> Para provisionar usuários em massa, use o GAM

> Google workspace sync for microsoft outllok GWSMO

> Comprehensive mail storage- verifica se o e-mail foi enviado

> admin toolbox - ferramentas de administrador

> para ver se um e-mail foi enviado, verifique o log dele

> directory api - adicione aliases a domínios

> para ver reports de usuários ( home>reports>apps reports:accounts

> tipos de reports user reports ( contas/uso de apps e segurança)

> apps reports - todos os serviços do google


Security investigation tool

Ferramenta de logs para analisar e tomar ações

> podemos suspoender ou restaurar usuários
> Para usar, precisa das permissões (require reviewer e view email content)
> só pra liçença bussiness plus pra cima
> Serve para deletar e-mails maliciosos e revisar atividade
> Identificar, triar e tomar ações de segurança e privacidade no seu domínio



> Content-aware - somente dispositivos da empresa podem logar no sistema
> tipos de acesso de grupos - public, team e restricted 

> email spoofing - conteúdo alterado por falta de configuração

> Bimi - brand indications for message indentification, serve para adicionar uma logo da sua marca

txt e cname records
txt record armazena textos, o cname mapeia dominios
exemplo de txt record : v=spf1 include:_spf.google.com -all

use txt record para: autenticação de domínio, configurar spf e dmairc, adicionar retrições de acesso, enviar emails evertificar integridade do domínio
use cname record para: criar apelidos de domínios, apontar e migrar domínios para diferentes provedores

serviços de e-mails
Registros SPF - protege seu domínio de ser usado p enviar spam
assinatura DLOM - criptografia que protegej o conteúdo de e-mail
Autenticação DMArc - gerencia mensagens verificar SPF e DKim
Bimi - Criação de marcas com dmarc

passos para autenticar e-mail para g-mails
1. garanta entrega e envite falsificações com SPF
2. Aumente a segurtança do e-mail enviado com DKIM
3. evite seu domínio de ser usado para enviar spam com dmarc
4. adicione a logo da sua marca com o BIMi

O header do e-mail é usado para definir as rotas e meios de autenticação


google toolbox 
browser toolbox - problemas de conectividade
dns verification - testes como integridade e configurações
enconding/decodign - debugar problemas com codificações
log analyzer - erros e avisos em arquivos e ferramentas
mail - análise do cabeçalho do e-mail para ver entrega e roteamento 
tipos de login challenge
1. mobile devices login challenge
employee id login challenge
recovery email login challenge

no google cloud directory sync podem ser sincornizados
- unidades organizacionais
- Contas de uusários
- Perfis
- Grupos
- Esquemas
- Contatos
- Recursos de calendário
- Liçensas
mensagens, eventos e arquivos não são compartilhados

Funções administrativas 
- superamdminsitrador
- Administrador de grupos
- Administrador de central de ajuda
- Administrador de gerenciamento de usuários
- Administrador de serviços
- Administrador míovel
- Administrador de armazenamneto
- Administrador de revendedor

> Servidor Ldap (lightwheight directory access protocol) - serviços ad do outlook

SSO e IDP

Sso - unifica métodos de login com google
IDP - gerencia credenciais e fornece a autenticação
SAML - SEcurity assertion markup language ( protocolo de autenticação )

quando um uusário tenta acessar umSAML o SP(service provider) solicita o IDP para autenticar o usuário.

Target audience - publico alvo - grupo de usuários para compartilhar itens, ajudam a melhorar se gurança e facilitam o compartilamento adequado 
Content- aware access - para usuários conectarem de casa em computador pessoais, configure o endpoint verification

security sandbox - ferramenta que abre o e-mail em espaço sandbox para detectar malwares em anexo de -emails.


<details>
<summary> </summary><br/>
</details>




