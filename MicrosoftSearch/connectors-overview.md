---
title: Visão geral dos Conectores do Microsoft Graph
ms.author: mecampos
author: mecampos
manager: umas
audience: Admin
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Visão geral dos conectores do Microsoft Graph para Pesquisa da Microsoft
ms.openlocfilehash: 1b3ea74cf571b1b5a048695633f6b9f698a21bf5
ms.sourcegitcommit: f76ade4c8fed0fee9c36d067b3ca8288c6c980aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "50508909"
---
<!---Previous ms.author: monaray --->

# <a name="overview-of-microsoft-graph-connectors"></a>Visão geral dos conectores do Microsoft Graph

[A Pesquisa da Microsoft](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) indexa todos os dados do [Microsoft 365](https://www.microsoft.com/microsoft-365) para torná-los pesquisáveis para usuários. Com os conectores do Microsoft Graph, sua organização pode indexar dados de terceiros para que apareçam nos resultados da Pesquisa da Microsoft. Esse recurso expande os tipos de fontes de conteúdo pesquisáveis em seus aplicativos de produtividade do Microsoft 365 e no ecossistema da Microsoft mais amplo. Os dados de terceiros podem ser hospedados no local ou nas nuvens públicas ou privadas.

<!---link Microsoft Graph reference in line 19 when we have access to relevant documentation--->

Este artigo destina-se a ajudar os administradores do Microsoft 365 a localizar os recursos disponíveis para responder às seguintes perguntas:

* [Quais fontes de dados podem ser conectadas à Pesquisa da Microsoft?](#what-data-sources-can-be-connected-to-microsoft-search)
* [Como faço para gerenciar minhas conexões?](#how-do-i-manage-my-connections)
* [Quais são os requisitos de licença e os termos de uso para conectores do Graph?](#what-are-the-license-requirements-and-terms-of-use-for-graph-connectors)
* [Quais são os recursos de visualização?](#what-are-the-preview-features)
* [Como personalizar e configurar os resultados da pesquisa?](#how-do-i-customize-and-configure-search-results)
* [Como faço para pesquisar dados do meu conector de um aplicativo personalizado?](#how-do-i-search-my-connector-data-from-a-custom-application)
* [Como personalizar os resultados da pesquisa?](#how-do-i-customize-search-results)
* [Quais são as limitações do conector](#what-are-the-connector-limitations)

<!---Modify to another note that is more accurate after rollout completion--->
> [!IMPORTANT]
> Os conectores do Microsoft Graph e as APIs de Pesquisa da Microsoft agora estão geralmente disponíveis. As primeiras versões serão para clientes configurados para lançamento direcionado. Se você quiser usar um conector Graph em seu locatário, os usuários e administradores devem optar [pela versão direcionada.](https://docs.microsoft.com/microsoft-365/admin/manage/release-options-in-office-365?view=o365-worldwide&preserve-view=true)

<!---Add Value, scenario, example, and/or graphic in December updates--->
<!---Probably remove architecture section below
## Architecture

The following architectural diagram of the Microsoft Graph platform shows how Graph connector content flows through content indexing to user results in [Microsoft Search](https://docs.microsoft.com/microsoftsearch/overview-microsoft-search) clients. The rest of this section explains each of the key building blocks in the diagram.

![Diagram: on-premises and cloud-based data is pulled by connectors and indexed by the Microsoft Search API, and then the Microsoft Search service delivers the results to users.](media/connectors-overview/highlevel-connectors.png)
Graph connectors can pull data from cloud-based (SaaS) data sources and on-premises data stores. The above diagram shows connections to only two data sources, but you can add connections to up ten sources per tenant.

The Microsoft Graph Connectors API instantiates one connection per data source. Then, the API indexes and stores the data. Established connections interact with Microsoft Search, so users can get search results.

You can use the Microsoft 365 [admin center](https://admin.microsoft.com) to setup and manage any of the Graph connectors by Microsoft. The admin center has a simple user interface that makes it easy to establish the connection to your data source, and monitor connection status and utilization.

***Edit paragraph below***
To create a **connection** to a data source, admins need authenticated access to the data and the entire content repository. The data is fed to the graph connector service for indexing.--->

## <a name="what-data-sources-can-be-connected-to-microsoft-search"></a>Quais fontes de dados podem ser conectadas à Pesquisa da Microsoft?

A Microsoft fornece 9 conectores do Graph e nossos parceiros de ecossistema criaram mais de 100 conectores graph. Você também pode criar seu próprio conector do Graph.

### <a name="graph-connectors-by-microsoft"></a>Conectores de gráfico da Microsoft

Você pode se conectar às seguintes fontes de dados usando conectores graph criados pela Microsoft:

<!---Add links below when new docs are created--->
* [Azure Data Lake Storage Gen2](azure-data-lake-connector.md)
* [Azure DevOps](azure-devops-connector.md)
* [Azure SQL e Microsoft SQL Server](MSSQL-connector.md)
* [Sites empresariais](enterprise-web-connector.md)
* [MediaWiki](mediawiki-connector.md)
* [Compartilhamento de arquivos](fileshare-connector.md)
* [Oracle SQL (visualização)](OracleSQL-connector.md)
* [Salesforce (visualização)](salesforce-connector.md)
* [ServiceNow](servicenow-connector.md)

A [galeria de conectores do Graph](connectors-gallery.md) contém uma breve descrição de cada um desses conectores do Graph. Se você estiver pronto para conectar uma dessas fontes de dados [](configure-connector.md) ao seu locatário, leia a visão geral da Instalação e quaisquer outros artigos na seção Conectores de Instalação da Microsoft que se apliquem à sua fonte de dados.

### <a name="graph-connectors-by-our-partners"></a>Conectores de gráfico por nossos parceiros

A [galeria de conectores](connectors-gallery.md) do Microsoft Graph inclui uma breve descrição de cada um dos conectores do Graph criados por nossos parceiros e um link para o site de cada parceiro. Para saber mais, entre em contato diretamente com cada parceiro.

### <a name="build-your-own-graph-connector"></a>Criar seu próprio conector do Graph

Você pode criar seu próprio conector do Graph, se preferir. Para obter mais informações sobre como criar conectores do Graph, consulte [a Visão geral da API de Pesquisa da Microsoft no Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).

## <a name="how-do-i-manage-my-connections"></a>Como faço para gerenciar minhas conexões?

Você pode gerenciar suas conexões na [guia Conectores](https://admin.microsoft.com/Adminportal/Home#/MicrosoftSearch/Connectors) no Centro de administração [do Microsoft 365.](https://admin.microsoft.com/) Para obter mais informações sobre como gerenciar conexões, consulte: [Gerenciar suas conexões](manage-connector.md).

## <a name="what-are-the-license-requirements-and-terms-of-use-for-graph-connectors"></a>Quais são os requisitos de licença e os termos de uso para conectores do Graph?

Você precisa de uma licença válida do Microsoft 365 ou office 365 e cota suficiente de Conectores do Graph para que os usuários em sua organização visualizam dados de conectores em seus resultados de pesquisa.

Para saber mais, confira [Requisitos de licença e preços](licensing.md) e Termos de [uso.](terms-of-use.md)

## <a name="what-are-the-preview-features"></a>Quais são os recursos de visualização?

Embora os conectores do Microsoft Graph e as APIs de Pesquisa da Microsoft agora estão geralmente disponíveis, há vários recursos que estão na visualização.

O conjunto de conectores e recursos na visualização inclui:

* [Conector do Azure DevOps](azure-devops-connector.md)
* [Conector do Salesforce](salesforce-connector.md)
* [Conector ServiceNow](servicenow-connector.md) com permissões de pesquisa que usam ACLs de origem
* [Gerenciar tipos de cluster](result-cluster.md)

## <a name="how-do-i-customize-and-configure-search-results"></a>Como personalizar e configurar os resultados da pesquisa?

Há muitas maneiras de personalizar e configurar os resultados da pesquisa. Confira os seguintes artigos para saber mais:

* [Gerenciar verticais e tipos de resultados](customize-search-page.md)
* [Gerenciar layouts de resultados de pesquisa](customize-results-layout.md)
* [Gerenciar tipos de cluster](result-cluster.md)
* [Gerenciar filtros personalizados](custom-filters.md)

## <a name="how-do-i-search-my-connector-data-from-a-custom-application"></a>Como faço para pesquisar dados do meu conector de um aplicativo personalizado?

Depois que os dados personalizados são indexados, os [desenvolvedores podem consultar esses dados.](https://docs.microsoft.com/graph/search-concept-custom-types) Você pode exibir seus dados em qualquer aplicativo. Para obter mais informações, consulte [Visão geral da API de Pesquisa da Microsoft no Microsoft Graph](https://docs.microsoft.com/graph/search-concept-overview).

## <a name="how-do-i-customize-search-results"></a>Como personalizar os resultados da pesquisa?

A próxima etapa é personalizar os resultados da pesquisa conforme recomendado neste artigo Como personalizar e configurar os resultados [da pesquisa?](#how-do-i-customize-and-configure-search-results). Para saber mais sobre como personalizar os resultados da pesquisa, consulte [Personalizar a página de resultados da pesquisa.](https://docs.microsoft.com/microsoftsearch/configure-connector#next-steps-customize-the-search-results-page)

## <a name="what-are-the-connector-limitations"></a>Quais são as limitações do conector?

* Quando você **publica** um conector criado pela Microsoft, pode levar alguns minutos para que a conexão seja criada. Durante esse tempo, a conexão mostrará seu status como pendente.

* O Centro de administração do [Microsoft 365](https://admin.microsoft.com) não dá suporte à edição do **esquema** de pesquisa depois que uma conexão é publicada. Para editar o esquema de pesquisa, exclua sua conexão e crie um novo.

* A produtividade de ingestão é acelerada em cerca de quatro itens por segundo.

* Não há suporte para atualizações de esquema. Depois de criar uma configuração de conexão, não há como atualizar o esquema. Você só pode excluir e re-criar a conexão.

* Há um limite de conexão. Cada locatário pode criar até 10 conexões.

* O suporte de edição para conexão não está disponível. Depois que a conexão tiver sido criada, você não poderá editá-la ou alterá-la. Se precisar alterar qualquer detalhe, exclua e recrie a conexão.
