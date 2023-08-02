# GWAC
Documentação Técnica referente a certificação Professional Google Workspace Administrator



<details>
<summary> Gmail  </summary><br/>


Dicas, maneiras de compor e-mails e ferramentas do gmail
<details>
<summary> Como criar um ambiente de trabalho no painel de administrador do Google </summary><br/>

  <details>
<summary> Setar um domínio  </summary><br/>
O primeiro passo é configurar um domínio. Você pode fazer isso registrando um novo domínio com um registrador de domínio ou transferindo um domínio que você já possui para o Google Workspace.
</details>
<details>
<summary> Criar uma conta no workspace do google  </summary><br/>

Depois de configurar um domínio, você precisará criar uma conta no Google Workspace. Você pode fazer isso visitando a página de inscrição do Google Workspace e inserindo as informações do seu domínio.
</details>

<details>
<summary> Logar no console de adm </summary><br/>
Depois de criar uma conta no Google Workspace, você precisará fazer login no console de administrador. Você pode fazer isso visitando a página de login do console de administrador e inserindo as credenciais da sua conta.
  </details>

  <details>
<summary> Configurar O domínio DNS </summary><br/>
O último passo é configurar o domínio DNS. Isso envolverá a adição de registros DNS ao seu domínio para apontar para o Google Workspace.

Os registros DNS específicos que você precisa adicionar dependerão do seu registrador de domínio e do tipo de domínio que você registrou. No entanto, geralmente, você precisará adicionar os seguintes registros DNS:

- Nome do host (A) registro para o endereço IP do servidor do Google Workspace
- Registro MX para o servidor de correio do Google Workspace
- Registro TXT para o domínio do Google Workspace
Depois de adicionar os registros DNS, pode levar algumas horas para que as alterações sejam propagadas. Depois que as alterações forem propagadas, você poderá começar a usar o Google Workspace!

</details>
</details>

<details>
<summary> Opções no Painel de Administrador </summary><br/>

| Opção no Painel de Administrador | Descrição                                        |
|---------------------------------|--------------------------------------------------|
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

</details>

<details>
<summary> Google Cloud Directory Sync  </summary><br/>

Serviço que permite sincronizar usuários, grupos e outros dados de um diretório do Active Directory (AD) com o Google Cloud Platform (GCP). Isso pode ser útil para empresas que desejam usar o GCP, mas que também precisam manter seus usuários e grupos em um diretório do AD.


> **O que é LDAP** -  O LDAP (Lightweight Directory Access Protocol) é um protocolo de acesso a diretórios frequentemente usado pelo Active Directory (AD), que é o serviço de diretório da Microsoft usado em ambientes Windows para gerenciar recursos, autenticação e políticas de segurança.

usa uma série de regras para decidir o que sincronizar
</details>

</details>




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
<details>
<summary> Gerenciamento de Usuários </summary><br/>

<details>
<summary>Como Redefinir Senhas de Usuários</summary><br/>

## Como Redefinir Senhas de Usuários

Para redefinir a senha de um usuário em um sistema de gerenciamento de diretórios, siga as etapas abaixo:

1. Acesse o [Console de administração](https://admin.example.com) do sistema.

2. Navegue até a seção "Usuários" ou "Gerenciamento de Usuários".

3. Localize o usuário cuja senha você deseja redefinir e clique em "Editar" ou no ícone de configurações.

4. Encontre a opção para redefinir a senha do usuário. Geralmente, é indicado por um botão ou link com o rótulo "Redefinir Senha" ou "Alterar Senha".

5. Digite a nova senha para o usuário. Dependendo das políticas de segurança, a senha pode precisar atender a requisitos específicos, como comprimento mínimo ou inclusão de caracteres especiais.

6. Salve as alterações e informe ao usuário sua nova senha.

Lembre-se de seguir as políticas de segurança recomendadas para a definição de senhas, como não reutilizar senhas antigas e incentivar o uso de senhas fortes e exclusivas para cada usuário.

> **Dica:** Considere implementar uma política de alteração periódica de senhas para manter a segurança das contas dos usuários.

</details>

<details>
<summary>Como Renomear um Usuário</summary><br/>

1. Acesse o [Console de administração](https://admin.example.com) do sistema.

2. Navegue até a seção "Usuários" ou "Gerenciamento de Usuários".

3. Localize o usuário que você deseja renomear e clique em "Editar" ou no ícone de configurações.

4. Encontre a opção para alterar o nome do usuário e insira o novo nome.

5. Salve as alterações.

</details>

<details>
<summary>Como Suspender um Usuário</summary><br/>

1. Acesse o [Console de administração](https://admin.example.com) do sistema.

2. Navegue até a seção "Usuários" ou "Gerenciamento de Usuários".

3. Localize o usuário que você deseja suspender e clique em "Editar" ou no ícone de configurações.

4. Procure pela opção de "Suspender" ou "Desativar" o usuário e selecione-a.

5. Confirme a suspensão e salve as alterações.

</details>

<details>
<summary>Como Reativar um Usuário Suspenso</summary><br/>

1. Acesse o [Console de administração](https://admin.example.com) do sistema.

2. Navegue até a seção "Usuários" ou "Gerenciamento de Usuários".

3. Localize o usuário suspenso que você deseja reativar e clique em "Editar" ou no ícone de configurações.

4. Procure pela opção de "Reativar" o usuário e selecione-a.

5. Confirme a reativação e salve as alterações.

</details>

<details>
<summary>Como Deletar um Usuário</summary><br/>

1. Acesse o [Console de administração](https://admin.example.com) do sistema.

2. Navegue até a seção "Usuários" ou "Gerenciamento de Usuários".

3. Localize o usuário que você deseja deletar e clique em "Editar" ou no ícone de configurações.

4. Procure pela opção de "Deletar" ou "Remover" o usuário e selecione-a.

5. Confirme a exclusão e prossiga com a remoção do usuário.

> **Cuidado:** A exclusão de um usuário geralmente é uma ação permanente e irreversível. Certifique-se de que deseja excluir o usuário antes de prosseguir.

</details>

</details>



<details>
<summary> Estruturas Organizacional </summary><br/>

Uma estrutura organizacional é um modelo que descreve como uma organização é dividida em departamentos, equipes e cargos.

Dividida em Unidades Organizacionais (OUs), definem o controle de aplicações e serviços, o controle pode ser no mesmo nível ou hierarquico

<details>
<summary> Como criar uma Unidade Organizacional (OU)</summary><br/>

Acesse o Console de administração do Google Workspace.
1. Clique em Configurações.
2. Clique em Usuários.
3. Clique em Unidades organizacionais.
4. Clique em Criar unidade organizacional.
5. Insira um nome para a unidade organizacional.
6. Selecione o tipo de unidade organizacional.
7. Selecione os usuários que deseja adicionar à unidade organizacional.
8. Escolha as permissões que deseja conceder à unidade organizacional.
9. Clique em Criar.

  
</details>

<details>
<summary> Como Restringir um serviço </summary><br/>

## Configuração de Restrição de Serviços Adicionais no Google Workspace

1. Acesse o **Console de administração** do Google Workspace.
2. Clique em **Apps**.
3. Clique em **Serviços adicionais**.
4. Selecione o **serviço adicional** que você deseja restringir.
5. Clique nos 3 pontos na coluna **Ações**.
6. Clique em **DESATIVAR para todos**.

</details>




  
</details>

<details>
<summary> Permissões de Superadministrador</summary><br/>


<details>
<summary> Como adicionar um super adminstrador  </summary><br/>

 Para adicionar um superadministrador siga esses passos 
 1. Users
 2. Entre no perfil no usuário
 3. Admin Roles
 4. Assign Roles
 5. Super Administrador
 6. Save
  
</details>
Como criar uma role de administrador
1. Admin roles
2. Create new Roles
3. Continue
4. Selecione os privilégios
5. Create Role

</details>

Ativar e desativar Recursos

Como desativar um serviço
1. Apps
2. Google Workspace
3. Serviço
4. 3 bolinhas
5. Turn off for everyone
> para desativar para uma OU específica, selecione-a no menu da esquerda

Controle de atualizações 
1. Account settings
2. Preferences
3. New feature
4. Save
> As opções de controle de atualização são

Setar políticas de compliance 
Anexar rodapé ao e-mail
1. Apps
2. Google Workspace
3. Gmail
4. Compliance
5. Configure
6. Save
Bloquear Vídeos, músicas, mídeas, anexos e outras coisas
1. Apps
2. Google Workspace
3. Gmail
4. Compliance
5. Configure
6. Marque "Remover anexos da caixa de mensagem"
7. Salvar 

Google Calendar 
Setar visibilidade e opções de compartilharmento
1. apps
2. Google Workspace
3. Calendar
4. Configurações de compartilhamento
5. Compartilhamento externo - Livre/Ocupado
6. Compartilhamento interno - Todas as informações
7. Save

Drive e docs

Permissão de compartilhamento com parceiros mas sem públicar na web 
1. Apps
2. Google Workspace
3. Drive and Docs
4. opções de compartilhamento
5. selecione a caixa "compartilhamento para fora do domínio permitido"
6. deselecione a caixa " Quando compartilhado fora do doínios, usuários do domínio podem públicar o link na internet
7. Salve

Transferindo a propriedade de um arquivo
1. Apps
2. Google Workspace
3. Drive and Docs
4. Transferir propriedade 
5. Coloque os nomes
6. Salvar

Recuperando arquivos deletados
1. Users
2. Ache o usuário
3. Mais
4. Restaurar dados

Ativar vizualização offline
1. Apps
2. Google Workspace
3. Drive and Docs
4. Features e aplicações
5. offline vizualization
6. Salvar

Setar políoticas de compartilhamento 
1. Apps
2. Google Workspace
3. Drive and Docs
4. opções de compartilhamento

Criar um drive compartilhado
1. Apps
2. Google Workspace
3. Drive and Docs
4. Drives compartilhados
5. Criar



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



<details>
<summary> </summary><br/>
</details>


















































