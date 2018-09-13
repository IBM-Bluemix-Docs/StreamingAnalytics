---

copyright:
  years: 2017, 2018
lastupdated: "2018-07-24"

---

<!-- Attribute definitions -->
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Concedendo Permissões a Usuários

Com uma conta do {{site.data.keyword.Bluemix_notm}}, você tem privilégios administrativos na organização ou espaço sob sua conta para executar todas as operações no {{site.data.keyword.streaminganalyticsshort}}. No entanto, ao
integrar outros usuários à sua conta, é necessário gerenciar suas permissões para que eles tenham os privilégios necessários
para operar instâncias de serviço em sua conta.

No {{site.data.keyword.streaminganalyticsshort}}, o acesso às operações de gerenciamento de serviço é controlado pelos
seguintes níveis de permissão:

| Operação | Necessário {{site.data.keyword.Bluemix_notm}} permissões | Permissões Necessárias do IAM |
|-----------|------------------------------|--------------------------|
| Criar ou excluir um serviço | Função de Desenvolvedor para o {{site.data.keyword.Bluemix_notm}} espaço | Nenhum |
| Visualize o painel de serviço | Função de Desenvolvedor para o {{site.data.keyword.Bluemix_notm}} espaço | Viewer e acima |
| Redimensione o serviço   | Função de Desenvolvedor para o {{site.data.keyword.Bluemix_notm}} espaço | Editor e acima |
| Gere chaves de serviço usando a CLI CF ou a UI do {{site.data.keyword.Bluemix_notm}} | Função de Desenvolvedor para o {{site.data.keyword.Bluemix_notm}} espaço | Nenhum |

Para integrar novos usuários à sua conta:

1.	Efetue logon no [{{site.data.keyword.Bluemix_notm}} painel](https://console.bluemix.net).

2.	Clique em **Gerenciar-> Conta-> Usuários**.

3.	Na página **Gerenciamento de usuário**, clique em **Convidar usuários**.

4.	Insira o IBMid do usuário que deseja convidar.

5.	Na seção Acesso, expanda **Serviços ativados de identidade e acesso** e selecione os valores a
seguir:

	a.	Serviços: selecione **Todos os serviços ativados de identidade e acesso**.

	b.	Região: Selecione **Sul**.

	c.	Instância de serviço: selecione **Todas as instâncias de serviço atuais**.

	d.	Funções: escolha uma função para o usuário. Membros com a função de Visualizador tem acesso somente leitura ao {{site.data.keyword.streaminganalyticsshort}}. Membros com a função Editor designada e privilégios acima podem modificar o serviço do
{{site.data.keyword.streaminganalyticsshort}}.

6.	Expanda o **acesso ao Cloud Foundry** e selecione a organização à qual deseja dar acesso de
usuário.

	a. Selecione uma função no nível de organização para seu usuário.

	b.	Escolha sul dos EUA por região.

	c.	Selecione o espaço ao qual deseja conceder o acesso de usuário.

	e.	Selecione a função que deseja designar ao usuário. Para visualizar o painel de serviço e executar tarefas, como gerar chaves de serviço, deve-se designar a função de Desenvolvedor.
