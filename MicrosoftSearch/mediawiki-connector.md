---
title: Conector MediaWiki para o Microsoft Search
ms.author: v-pamcn
author: monaray
manager: mnirkhe
ms.audience: Admin
ms.topic: article
ms.service: mssearch
localization_priority: Normal
search.appverid:
- BFB160
- MET150
- MOE150
description: Configurar o conector MediaWiki para o Microsoft Search
ms.openlocfilehash: 2aa0ef494aa42b1a7364ec68f6532dec737b9c25
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626959"
---
# <a name="mediawiki-connector"></a><span data-ttu-id="1be18-103">Conector MediaWiki</span><span class="sxs-lookup"><span data-stu-id="1be18-103">MediaWiki connector</span></span>

<span data-ttu-id="1be18-104">Com o conector MediaWiki, sua organização pode descobrir e indexar dados de um wiki criado usando o software do MediaWiki.</span><span class="sxs-lookup"><span data-stu-id="1be18-104">With the MediaWiki connector, your organization can discover and index data from a wiki created by using MediaWiki software.</span></span> <span data-ttu-id="1be18-105">Esse conector indexa o conteúdo especificado à pesquisa da Microsoft e dá suporte a rastreamentos periódicos para manter o índice atualizado.</span><span class="sxs-lookup"><span data-stu-id="1be18-105">This connector indexes specified content into Microsoft Search and supports periodic crawls to keep the index up to date.</span></span>

<span data-ttu-id="1be18-106">Este artigo é para os administradores do Microsoft 365 ou qualquer pessoa que configure, execute e monitore um conector MediaWiki.</span><span class="sxs-lookup"><span data-stu-id="1be18-106">This article is for Microsoft 365 administrators or anyone who configures, runs, and monitors a MediaWiki connector.</span></span> <span data-ttu-id="1be18-107">Ele explica como configurar seus recursos de conector e conector, limitações e técnicas de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="1be18-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="1be18-108">Conectar-se a uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="1be18-108">Connect to a data source</span></span>
<span data-ttu-id="1be18-109">Insira a URL e as credenciais do MediaWiki para autenticar a conexão.</span><span class="sxs-lookup"><span data-stu-id="1be18-109">Enter your MediaWiki URL and credentials for authenticating the connection.</span></span> <span data-ttu-id="1be18-110">Você precisará das seguintes informações: **ID do locatário**, **ID do recurso**, ID do **cliente**e segredo do **cliente**.</span><span class="sxs-lookup"><span data-stu-id="1be18-110">You'll need the following information: **Tenant ID**, **Resource ID**, **Client ID**, and the **Client Secret**.</span></span>

## <a name="manage-the-search-schema"></a><span data-ttu-id="1be18-111">Gerenciar o esquema de pesquisa</span><span class="sxs-lookup"><span data-stu-id="1be18-111">Manage the search schema</span></span>
<span data-ttu-id="1be18-112">Após a conexão bem-sucedida, configure o mapeamento de esquema de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1be18-112">After successful connection, configure the search schema mapping.</span></span> <span data-ttu-id="1be18-113">Você pode escolher quais propriedades tornar **consultáveis**, **pesquisáveis**e **recuperáveis**.</span><span class="sxs-lookup"><span data-stu-id="1be18-113">You can choose which properties to make **queryable**, **searchable**, and **retrievable**.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="1be18-114">Gerenciar permissões de pesquisa</span><span class="sxs-lookup"><span data-stu-id="1be18-114">Manage search permissions</span></span>
<span data-ttu-id="1be18-115">O conector MediaWiki suporta apenas as permissões de pesquisa visíveis para **todos**.</span><span class="sxs-lookup"><span data-stu-id="1be18-115">The MediaWiki connector only supports search permissions visible to **Everyone**.</span></span> <span data-ttu-id="1be18-116">Dados indexados aparecem nos resultados da pesquisa e são visíveis para todos os usuários da organização.</span><span class="sxs-lookup"><span data-stu-id="1be18-116">Indexed data appears in the search results and is visible to all users in the organization.</span></span>

## <a name="set-the-refresh-schedule"></a><span data-ttu-id="1be18-117">Definir o agendamento de atualização</span><span class="sxs-lookup"><span data-stu-id="1be18-117">Set the refresh schedule</span></span> 
<span data-ttu-id="1be18-118">Essa agenda atualiza dados indexados, portanto, as alterações no wiki são refletidas no Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="1be18-118">This schedule refreshes indexed data, so changes to the wiki are reflected in Microsoft Search.</span></span> <span data-ttu-id="1be18-119">Todas as novas páginas, páginas excluídas, conteúdo de página ou alterações de metadados aparecem nos resultados da pesquisa após o intervalo de atualização especificado.</span><span class="sxs-lookup"><span data-stu-id="1be18-119">All new pages, deleted pages, page content, or metadata changes appear in search results after the specified refresh interval.</span></span> <span data-ttu-id="1be18-120">O tempo de rastreamento depende do tamanho do wiki.</span><span class="sxs-lookup"><span data-stu-id="1be18-120">The crawl time is dependent on the size of the wiki.</span></span> <span data-ttu-id="1be18-121">No momento, o conector é rastreado em torno de 50 páginas por minuto.</span><span class="sxs-lookup"><span data-stu-id="1be18-121">Currently the connector crawls at around 50 pages per minute.</span></span>

## <a name="limitations"></a><span data-ttu-id="1be18-122">Limitações</span><span class="sxs-lookup"><span data-stu-id="1be18-122">Limitations</span></span> 
<span data-ttu-id="1be18-123">O conector MediaWiki tem essas limitações na versão prévia:</span><span class="sxs-lookup"><span data-stu-id="1be18-123">The MediaWiki connector has these limitations in the preview release:</span></span>
* <span data-ttu-id="1be18-124">Oferece suporte somente a wikis baseados em nuvem.</span><span class="sxs-lookup"><span data-stu-id="1be18-124">Supports only cloud-based wikis.</span></span>
* <span data-ttu-id="1be18-125">O suporta somente o Basic ou o OAuth 2,0 com a autenticação do Azure Active Directory ou do Azure.</span><span class="sxs-lookup"><span data-stu-id="1be18-125">Supports only Basic or OAuth 2.0 with Azure Active Directory or Azure authentication.</span></span>
* <span data-ttu-id="1be18-126">Não dá suporte à seleção de namespace para indexação.</span><span class="sxs-lookup"><span data-stu-id="1be18-126">Doesn't support namespace selection for indexing.</span></span> <span data-ttu-id="1be18-127">Indexa somente namespaces **principal**, de **categoria**e de **arquivo** .</span><span class="sxs-lookup"><span data-stu-id="1be18-127">Indexes only **Main**, **Category**, and **File** namespaces.</span></span>
* <span data-ttu-id="1be18-128">Não oferece suporte a listas de controle de acesso (ACLs).</span><span class="sxs-lookup"><span data-stu-id="1be18-128">Doesn't support Access Control Lists (ACLs).</span></span> <span data-ttu-id="1be18-129">Portanto, as páginas indexadas são visíveis para todos os usuários da organização.</span><span class="sxs-lookup"><span data-stu-id="1be18-129">Thus, indexed pages are visible to all users in the organization.</span></span>