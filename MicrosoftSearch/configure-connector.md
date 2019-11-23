---
title: Configurar seu conector criado pela Microsoft para a pesquisa da Microsoft
ms.author: mounika.narayanan
author: monaray
manager: shohara
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Configurar seu conector criado pela Microsoft para a pesquisa da Microsoft
ms.openlocfilehash: 1a3affebc754595eabc40a13402aae6bbb7a1e1c
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626521"
---
# <a name="set-up-your-microsoft-built-connector-for-microsoft-search"></a><span data-ttu-id="0cae5-103">Configurar seu conector criado pela Microsoft para a pesquisa da Microsoft</span><span class="sxs-lookup"><span data-stu-id="0cae5-103">Set up your Microsoft-built connector for Microsoft Search</span></span>

<span data-ttu-id="0cae5-104">Este artigo orienta você pelas etapas de configuração de um conector criado pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0cae5-104">This article guides you through the steps of configuring a Microsoft-built connector.</span></span> <span data-ttu-id="0cae5-105">Descreve o fluxo de configurar uma conexão no [centro de administração](https://admin.microsoft.com)do Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0cae5-105">It outlines the flow of setting up a connection in the Microsoft 365 [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="0cae5-106">Para obter mais detalhes sobre como configurar conectores criados específicos da Microsoft, consulte estes artigos:</span><span class="sxs-lookup"><span data-stu-id="0cae5-106">For more details on how to set up specific Microsoft-built connectors, see these articles:</span></span>
* [<span data-ttu-id="0cae5-107">Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="0cae5-107">Azure Data Lake Storage Gen2</span></span>](azure-data-lake-connector.md)
* [<span data-ttu-id="0cae5-108">Sites empresariais</span><span class="sxs-lookup"><span data-stu-id="0cae5-108">Enterprise websites</span></span>](enterprise-web-connector.md)
* [<span data-ttu-id="0cae5-109">Compartilhamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="0cae5-109">File share</span></span>](file-share-connector.md)
* [<span data-ttu-id="0cae5-110">MediaWiki</span><span class="sxs-lookup"><span data-stu-id="0cae5-110">MediaWiki</span></span>](mediawiki-connector.md)
* [<span data-ttu-id="0cae5-111">Microsoft SQL server</span><span class="sxs-lookup"><span data-stu-id="0cae5-111">Microsoft SQL server</span></span>](MSSQL-connector.md)
* [<span data-ttu-id="0cae5-112">ServiceNow</span><span class="sxs-lookup"><span data-stu-id="0cae5-112">ServiceNow</span></span>](servicenow-connector.md)

## <a name="set-up"></a><span data-ttu-id="0cae5-113">Configurar</span><span class="sxs-lookup"><span data-stu-id="0cae5-113">Set up</span></span>
<span data-ttu-id="0cae5-114">Para configurar qualquer um dos conectores criados pela Microsoft, vá para o [centro de administração](https://admin.microsoft.com):</span><span class="sxs-lookup"><span data-stu-id="0cae5-114">To configure any of the Microsoft-built connectors, go to the [admin center](https://admin.microsoft.com):</span></span>
1. <span data-ttu-id="0cae5-115">Entre em sua conta com as credenciais do [Microsoft 365](https://www.microsoft.com/microsoft-365) Test locatário.</span><span class="sxs-lookup"><span data-stu-id="0cae5-115">Sign in to your account with the credentials for your [Microsoft 365](https://www.microsoft.com/microsoft-365) test tenant.</span></span>
2. <span data-ttu-id="0cae5-116">Vá até **configurações** > \*\*\*\* > **conectores**de pesquisa da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0cae5-116">Go to **Settings** > **Microsoft Search** > **Connectors**.</span></span>
3. <span data-ttu-id="0cae5-117">Selecione **Adicionar um conector**.</span><span class="sxs-lookup"><span data-stu-id="0cae5-117">Select **Add a connector**.</span></span>
4. <span data-ttu-id="0cae5-118">Na lista de conectores disponíveis, selecione o conector de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="0cae5-118">From the list of available connectors, select the connector of your choice.</span></span>

![As fontes de dados disponíveis incluem: ADLS Gen2 Connector, Enterprise sites, ServiceNow, compartilhamento de arquivos, Microsoft SQL Server e MediaWiki.](media/addconnector_final.png)

### <a name="name-the-connector"></a><span data-ttu-id="0cae5-120">Nomear o conector</span><span class="sxs-lookup"><span data-stu-id="0cae5-120">Name the connector</span></span>
<span data-ttu-id="0cae5-121">Para criar uma conexão, primeiro especifique estes atributos:</span><span class="sxs-lookup"><span data-stu-id="0cae5-121">To create a connection, first specify these attributes:</span></span>
1. <span data-ttu-id="0cae5-122">Nome da conexão</span><span class="sxs-lookup"><span data-stu-id="0cae5-122">Name of the connection</span></span>
2. <span data-ttu-id="0cae5-123">ID de conexão</span><span class="sxs-lookup"><span data-stu-id="0cae5-123">Connection ID</span></span>
3. <span data-ttu-id="0cae5-124">Descrição (opcional)</span><span class="sxs-lookup"><span data-stu-id="0cae5-124">Description (optional)</span></span>

<span data-ttu-id="0cae5-125">A ID de conexão cria propriedades implícitas para seu conector.</span><span class="sxs-lookup"><span data-stu-id="0cae5-125">The connection ID creates implicit properties for your connector.</span></span> <span data-ttu-id="0cae5-126">Ele deve conter apenas caracteres alfanuméricos e ter no máximo 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0cae5-126">It must contain only alphanumeric characters and be a maximum of 32 characters.</span></span>

### <a name="connect-to-a-data-source"></a><span data-ttu-id="0cae5-127">Conectar-se a uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="0cae5-127">Connect to a data source</span></span>
<span data-ttu-id="0cae5-128">O processo de conexão de dados varia de acordo com o tipo de conector.</span><span class="sxs-lookup"><span data-stu-id="0cae5-128">The data connection process varies based on the type of connector.</span></span> <span data-ttu-id="0cae5-129">Para saber mais sobre como se conectar à sua fonte de dados local, consulte [install an local data gateway](https://aka.ms/configuregateway).</span><span class="sxs-lookup"><span data-stu-id="0cae5-129">To learn more about connecting to your on-premises data source, see [Install an on-premises data gateway](https://aka.ms/configuregateway).</span></span>

### <a name="select-source-properties"></a><span data-ttu-id="0cae5-130">Selecionar Propriedades de origem</span><span class="sxs-lookup"><span data-stu-id="0cae5-130">Select source properties</span></span>
<span data-ttu-id="0cae5-131">Os campos de dados definidos por sua fonte de dados de terceiros como propriedades de origem são indexados na pesquisa da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0cae5-131">The data fields set by your third-party data source as source properties are indexed into Microsoft Search.</span></span> <span data-ttu-id="0cae5-132">Para modificar essas propriedades, selecione **Editar propriedades** na barra lateral à direita da página **conectores** .</span><span class="sxs-lookup"><span data-stu-id="0cae5-132">To modify these properties, select **Edit properties** in the side bar on the right of the **Connectors** page.</span></span> <span data-ttu-id="0cae5-133">Você pode selecionar **até 64 Propriedades de origem**.</span><span class="sxs-lookup"><span data-stu-id="0cae5-133">You can select **up to 64 source properties**.</span></span>

###  <a name="manage-the-search-schema"></a><span data-ttu-id="0cae5-134">Gerenciar o esquema de pesquisa</span><span class="sxs-lookup"><span data-stu-id="0cae5-134">Manage the search schema</span></span> 
<span data-ttu-id="0cae5-135">Os administradores podem definir os atributos de esquema de pesquisa para controlar a funcionalidade de pesquisa de cada propriedade de origem.</span><span class="sxs-lookup"><span data-stu-id="0cae5-135">Admins can set the search schema attributes to control search functionality of each source property.</span></span> <span data-ttu-id="0cae5-136">Um esquema de pesquisa ajuda a determinar quais resultados são exibidos na página de resultados da pesquisa e quais informações os usuários finais podem exibir e acessar.</span><span class="sxs-lookup"><span data-stu-id="0cae5-136">A search schema helps determine what results display on the search results page and what information end users can view and access.</span></span>

<span data-ttu-id="0cae5-137">Os atributos de esquema de pesquisa incluem **pesquisáveis**, **consultáveis**e **recuperáveis**.</span><span class="sxs-lookup"><span data-stu-id="0cae5-137">Search schema attributes include **searchable**, **queryable**, and **retrievable**.</span></span> <span data-ttu-id="0cae5-138">A tabela a seguir lista cada um dos atributos aos quais os conectores do Microsoft Graph dão suporte e explica suas funções.</span><span class="sxs-lookup"><span data-stu-id="0cae5-138">The following table lists each of the attributes that Microsoft Graph connectors support and explains their functions.</span></span>

<span data-ttu-id="0cae5-139">**Atributo de esquema de pesquisa**</span><span class="sxs-lookup"><span data-stu-id="0cae5-139">**Search schema attribute**</span></span> | <span data-ttu-id="0cae5-140">**Function**</span><span class="sxs-lookup"><span data-stu-id="0cae5-140">**Function**</span></span> | <span data-ttu-id="0cae5-141">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="0cae5-141">**Example**</span></span>
--- | --- | ---
<span data-ttu-id="0cae5-142">PESQUISÁVEIS</span><span class="sxs-lookup"><span data-stu-id="0cae5-142">SEARCHABLE</span></span> | <span data-ttu-id="0cae5-143">Torna o conteúdo de texto de uma propriedade pesquisável.</span><span class="sxs-lookup"><span data-stu-id="0cae5-143">Makes the text content of a property searchable.</span></span> <span data-ttu-id="0cae5-144">O conteúdo da propriedade está incluído no índice de texto completo.</span><span class="sxs-lookup"><span data-stu-id="0cae5-144">Property contents are included in the full-text index.</span></span> | <span data-ttu-id="0cae5-145">Se a propriedade for **título**, uma consulta de **empresa** retornará as respostas que contenham a palavra **Enterprise** em qualquer texto ou título.</span><span class="sxs-lookup"><span data-stu-id="0cae5-145">If the property is **title**, a query for **Enterprise** returns answers that contain the word **Enterprise** in any text or title.</span></span>
<span data-ttu-id="0cae5-146">Question</span><span class="sxs-lookup"><span data-stu-id="0cae5-146">QUERYABLE</span></span> | <span data-ttu-id="0cae5-147">Pesquisa por consulta para uma correspondência de uma determinada propriedade.</span><span class="sxs-lookup"><span data-stu-id="0cae5-147">Searches by query for a match for a particular property.</span></span> <span data-ttu-id="0cae5-148">O nome da propriedade pode ser especificado na consulta de forma programática ou textual.</span><span class="sxs-lookup"><span data-stu-id="0cae5-148">The property name can then be specified in the query either programmatically or verbatim.</span></span> |  <span data-ttu-id="0cae5-149">Se a propriedade **title** for consultável, o título da consulta **: Enterprise** será suportado.</span><span class="sxs-lookup"><span data-stu-id="0cae5-149">If the **Title** property is queryable, then the query **Title: Enterprise** is supported.</span></span>
<span data-ttu-id="0cae5-150">RECUPERÁVEIS</span><span class="sxs-lookup"><span data-stu-id="0cae5-150">RETRIEVABLE</span></span> | <span data-ttu-id="0cae5-151">Somente as propriedades recuperáveis podem ser usadas no tipo de resultado e no resultado da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0cae5-151">Only retrievable properties can be used in the result type and display in the search result.</span></span> | 

<span data-ttu-id="0cae5-152">Para todos os conectores, exceto o conector de compartilhamento de arquivos, os tipos personalizados devem ser definidos manualmente.</span><span class="sxs-lookup"><span data-stu-id="0cae5-152">For all connectors except the file share connector, custom types must be set manually.</span></span> <span data-ttu-id="0cae5-153">Para ativar os recursos de pesquisa para cada campo, você precisa de um esquema de pesquisa mapeado para uma lista de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0cae5-153">To activate search capabilities for each field, you need a search schema mapped to a list of properties.</span></span> <span data-ttu-id="0cae5-154">O assistente de conexão seleciona automaticamente um esquema de pesquisa com base no conjunto de propriedades de origem que você escolher.</span><span class="sxs-lookup"><span data-stu-id="0cae5-154">The connection wizard automatically selects a search schema based on the set of source properties you choose.</span></span> <span data-ttu-id="0cae5-155">Você pode modificar esse esquema marcando as caixas de seleção de cada propriedade e atributo na página de esquema de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0cae5-155">You can modify this schema by selecting the check boxes for each property and attribute in the search schema page.</span></span>

![O esquema de um conector pode ser personalizado adicionando ou removendo funções de consulta, pesquisa e recuperação.](media/manageschema.png)

<span data-ttu-id="0cae5-157">Essas restrições e recomendações se aplicam às configurações de esquema de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="0cae5-157">These restrictions and recommendations apply to search schema settings:</span></span>
* <span data-ttu-id="0cae5-158">Para conectores que indexam tipos personalizados, recomendamos que você **não** marque o campo que contém o conteúdo principal que pode ser **recuperado**.</span><span class="sxs-lookup"><span data-stu-id="0cae5-158">For connectors that index custom types, we recommend that you **do not** mark the field that contains the main content **retrievable**.</span></span> <span data-ttu-id="0cae5-159">Problemas de desempenho significativos ocorrem quando os resultados da pesquisa são renderizados com esse atributo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0cae5-159">Significant performance issues occur when search results render with that search attribute.</span></span> <span data-ttu-id="0cae5-160">Um exemplo é o campo de conteúdo de **texto** para um artigo da base de dados de conhecimento do [ServiceNow](https://www.servicenow.com) .</span><span class="sxs-lookup"><span data-stu-id="0cae5-160">An example is the **Text** content field for a [ServiceNow](https://www.servicenow.com) knowledge-base article.</span></span>
* <span data-ttu-id="0cae5-161">Somente as propriedades marcadas como recuperáveis são renderizadas nos resultados da pesquisa e podem ser usadas para criar tipos de resultados modernos (MRTs).</span><span class="sxs-lookup"><span data-stu-id="0cae5-161">Only properties marked as retrievable render in the search results and can be used to create modern result types (MRTs).</span></span>
* <span data-ttu-id="0cae5-162">Somente as propriedades de cadeia de caracteres podem ser marcadas como pesquisáveis.</span><span class="sxs-lookup"><span data-stu-id="0cae5-162">Only string properties can be marked searchable.</span></span>

> [!Note]
> <span data-ttu-id="0cae5-163">Após criar uma conexão, você **não poderá** modificar o esquema.</span><span class="sxs-lookup"><span data-stu-id="0cae5-163">After you create a connection, you **can't** modify the schema.</span></span> <span data-ttu-id="0cae5-164">Para fazer isso, você precisa excluir sua conexão e criar uma nova.</span><span class="sxs-lookup"><span data-stu-id="0cae5-164">To do that, you need to delete your connection and create a new one.</span></span>

###  <a name="manage-search-permissions"></a><span data-ttu-id="0cae5-165">Gerenciar permissões de pesquisa</span><span class="sxs-lookup"><span data-stu-id="0cae5-165">Manage search permissions</span></span>
<span data-ttu-id="0cae5-166">As listas de controle de acesso (ACLs) determinam quais usuários em sua organização podem acessar cada item de dados.</span><span class="sxs-lookup"><span data-stu-id="0cae5-166">Access Control Lists (ACLs) determine which users in your organization can access each item of data.</span></span> <span data-ttu-id="0cae5-167">O conector de compartilhamento de arquivos suporta apenas as ACLs que podem ser mapeadas para o [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/).</span><span class="sxs-lookup"><span data-stu-id="0cae5-167">The file share connector supports only ACLs that can be mapped to [Azure Active Directory (Azure AD)](https://docs.microsoft.com/azure/active-directory/).</span></span> <span data-ttu-id="0cae5-168">Todos os outros conectores dão suporte a permissões de pesquisa que são visíveis para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="0cae5-168">All the other connectors support search permissions that are visible to all users.</span></span>

### <a name="set-the-refresh-schedule"></a><span data-ttu-id="0cae5-169">Definir o agendamento de atualização</span><span class="sxs-lookup"><span data-stu-id="0cae5-169">Set the refresh schedule</span></span>
<span data-ttu-id="0cae5-170">O agendamento de atualização determina com que frequência seus dados serão sincronizados com o índice no Microsoft Graph e no Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="0cae5-170">The refresh schedule determines how often your data is synced with the index in Microsoft Graph and Microsoft Search.</span></span> <span data-ttu-id="0cae5-171">Você pode agendar a atualização de duas maneiras: rastreamento completo ou rastreamento incremental.</span><span class="sxs-lookup"><span data-stu-id="0cae5-171">You can schedule the refresh in two ways: full crawl or incremental crawl.</span></span>

<span data-ttu-id="0cae5-172">Com um **rastreamento completo**, o mecanismo de pesquisa processa e indexa todos os itens na fonte de conteúdo, independentemente dos rastreamentos anteriores.</span><span class="sxs-lookup"><span data-stu-id="0cae5-172">With a **full crawl**, the search engine processes and indexes every item in the content source, regardless of previous crawls.</span></span> <span data-ttu-id="0cae5-173">O rastreamento completo funciona melhor nessas situações:</span><span class="sxs-lookup"><span data-stu-id="0cae5-173">Full crawl works best in these situations:</span></span>
* <span data-ttu-id="0cae5-174">É necessário detectar exclusões de dados.</span><span class="sxs-lookup"><span data-stu-id="0cae5-174">You need to detect deletions of data.</span></span>
* <span data-ttu-id="0cae5-175">O rastreamento incremental não pôde rastrear o conteúdo para erros.</span><span class="sxs-lookup"><span data-stu-id="0cae5-175">The incremental crawl failed to crawl content for errors.</span></span>
* <span data-ttu-id="0cae5-176">É necessária uma atualização de software para o Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="0cae5-176">A software update for Microsoft Search is required.</span></span> <span data-ttu-id="0cae5-177">As atualizações modificam o esquema de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0cae5-177">Updates modify the search schema.</span></span>
* <span data-ttu-id="0cae5-178">ACLs foram modificadas.</span><span class="sxs-lookup"><span data-stu-id="0cae5-178">ACLs were modified.</span></span>
* <span data-ttu-id="0cae5-179">As regras de rastreamento foram modificadas.</span><span class="sxs-lookup"><span data-stu-id="0cae5-179">Crawl rules were modified.</span></span>

<span data-ttu-id="0cae5-180">Com um **rastreamento incremental**, o mecanismo de pesquisa pode processar e indexar somente os itens que foram criados ou modificados desde o último rastreamento bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0cae5-180">With an **incremental crawl**, the search engine can process and index only the items that were created or modified since the last successful crawl.</span></span> <span data-ttu-id="0cae5-181">Portanto, nem todos os dados na fonte de conteúdo são re-indexados.</span><span class="sxs-lookup"><span data-stu-id="0cae5-181">Therefore, not all the data in the content source is re-indexed.</span></span> <span data-ttu-id="0cae5-182">Os rastreamentos incrementais funcionam melhor para detectar conteúdo, metadados, permissões e outras atualizações.</span><span class="sxs-lookup"><span data-stu-id="0cae5-182">Incremental crawls works best to detect content, metadata, permission, and other updates.</span></span>

<span data-ttu-id="0cae5-183">Os rastreamentos incrementais são muito mais rápidos do que os rastreamentos completos porque não foram processados itens não alterados.</span><span class="sxs-lookup"><span data-stu-id="0cae5-183">Incremental crawls are much faster than full crawls because unchanged items aren’t processed.</span></span> <span data-ttu-id="0cae5-184">Para manter uma sincronização de dados precisa entre a fonte de conteúdo e o índice de pesquisa, você precisa executar os dois rastreamentos periodicamente.</span><span class="sxs-lookup"><span data-stu-id="0cae5-184">To maintain an accurate data sync between the content source and the search index, you need to run both crawls periodically.</span></span>

<span data-ttu-id="0cae5-185">Cada conector terá um conjunto ideal diferente de agendas de atualização com base na frequência com que os dados são modificados e o tipo de modificações.</span><span class="sxs-lookup"><span data-stu-id="0cae5-185">Each connector will have a different optimal set of refresh schedules based on how often data is modified and the type of modifications.</span></span>

![Configurações de rastreamento incremental e intervalo de rastreamento completo mostrando a incremental em 15 minutos e rastreamento completo em 1 semana.](media/refreshschedule.png)

### <a name="review-connector-settings"></a><span data-ttu-id="0cae5-187">Revisar configurações do conector</span><span class="sxs-lookup"><span data-stu-id="0cae5-187">Review connector settings</span></span>
<span data-ttu-id="0cae5-188">Depois de configurar seu conector, o [centro de administração](https://admin.microsoft.com) leva você para uma página onde você pode examinar suas configurações.</span><span class="sxs-lookup"><span data-stu-id="0cae5-188">After you configure your connector, the [admin center](https://admin.microsoft.com) takes you to a page where you can review your settings.</span></span> <span data-ttu-id="0cae5-189">Você pode voltar pelo processo de configuração para editar qualquer configuração antes de confirmar a conexão.</span><span class="sxs-lookup"><span data-stu-id="0cae5-189">You can go back through the configuration process to edit any setting before you confirm the connection.</span></span> <span data-ttu-id="0cae5-190">Para saber mais, confira [gerenciar seu conector](manage-connector.md).</span><span class="sxs-lookup"><span data-stu-id="0cae5-190">To learn more, see [Manage your connector](manage-connector.md).</span></span>

## <a name="next-steps-customize-the-search-results-page"></a><span data-ttu-id="0cae5-191">Próximas etapas: personalizar a página de resultados de pesquisa</span><span class="sxs-lookup"><span data-stu-id="0cae5-191">Next steps: Customize the search results page</span></span>
<span data-ttu-id="0cae5-192">Com a interface de usuário do Microsoft Search (UI), os usuários finais podem pesquisar conteúdo de seus aplicativos de produtividade do [microsoft 365](https://www.microsoft.com/microsoft-365) e do ecossistema mais amplo da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0cae5-192">With the Microsoft Search user interface (UI), your end users can search content from your [Microsoft 365](https://www.microsoft.com/microsoft-365) productivity apps and the broader Microsoft ecosystem.</span></span> <span data-ttu-id="0cae5-193">Uma vertical de pesquisa refere-se às guias mostradas quando um usuário exibe seus resultados de pesquisa no [SharePoint](http://sharepoint.com/), no [Microsoft Office](https://Office.com)e no Microsoft Search no [Bing](https://Bing.com).</span><span class="sxs-lookup"><span data-stu-id="0cae5-193">A search vertical refers to the tabs that are shown when a user views their search results in [SharePoint](http://sharepoint.com/), [Microsoft Office](https://Office.com), and Microsoft Search in [Bing](https://Bing.com).</span></span> <span data-ttu-id="0cae5-194">Você pode personalizar os verticais de pesquisa para restringir os resultados, de modo que apenas um determinado tipo de resultados de pesquisa seja exibido.</span><span class="sxs-lookup"><span data-stu-id="0cae5-194">You can customize search verticals to narrow down results, so that only a certain type of search results is displayed.</span></span> <span data-ttu-id="0cae5-195">Essas verticais aparecem como uma guia na parte superior da página de resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0cae5-195">These verticals appear as a tab on the top of the search results page.</span></span> <span data-ttu-id="0cae5-196">Um tipo de resultado moderno (MRT) é a interface do usuário que designa como os resultados são apresentados.</span><span class="sxs-lookup"><span data-stu-id="0cae5-196">A modern result type (MRT) is the UI that designates how results are presented.</span></span>

<span data-ttu-id="0cae5-197">Você deve criar seus próprios tipos de resultados e verticais, de modo que os usuários finais possam exibir os resultados de pesquisa de novas conexões.</span><span class="sxs-lookup"><span data-stu-id="0cae5-197">You must create your own verticals and result types, so end users can view search results from new connections.</span></span> <span data-ttu-id="0cae5-198">Sem esta etapa, os dados da sua conexão não aparecerão na página de resultados da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="0cae5-198">Without this step, data from your connection won’t show up on the search results page.</span></span>

<span data-ttu-id="0cae5-199">Para saber mais sobre como criar seus verticais e MRTs, confira [personalização da página de resultados da pesquisa](customize-search-page.md).</span><span class="sxs-lookup"><span data-stu-id="0cae5-199">To learn more about how to create your verticals and MRTs, see [Search results page customization](customize-search-page.md).</span></span>

## <a name="how-do-i-know-this-worked"></a><span data-ttu-id="0cae5-200">Como saber se funcionou?</span><span class="sxs-lookup"><span data-stu-id="0cae5-200">How do I know this worked?</span></span>
<span data-ttu-id="0cae5-201">Vá para a lista de suas conexões publicadas na guia **conectores** do [centro de administração](https://admin.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="0cae5-201">Go to the list of your published connections under the **Connectors** tab in the [admin center](https://admin.microsoft.com).</span></span> <span data-ttu-id="0cae5-202">Para saber como fazer atualizações e exclusões, confira [gerenciar o conector](manage-connector.md).</span><span class="sxs-lookup"><span data-stu-id="0cae5-202">To learn how to make updates and deletions, see [Manage your connector](manage-connector.md).</span></span>