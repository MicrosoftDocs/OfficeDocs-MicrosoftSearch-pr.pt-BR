---
title: Azure data Lake Connector para Microsoft Search
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
description: Configurar o conector do Gen2 de armazenamento do Azure data Lake para o Microsoft Search
ms.openlocfilehash: 392960a5f7e6c93442ac7e1f60245217e194b42b
ms.sourcegitcommit: 21361af7c244ffd6ff8689fd0ff0daa359bf4129
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38626467"
---
# <a name="azure-data-lake-storage-gen2-connector-for-microsoft-search"></a><span data-ttu-id="e3919-103">Azure data Lake Storage Gen2 Connector para Microsoft Search</span><span class="sxs-lookup"><span data-stu-id="e3919-103">Azure Data Lake Storage Gen2 connector for Microsoft Search</span></span>

<span data-ttu-id="e3919-104">Com o conector [Gen2 de armazenamento do Azure data Lake](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) , os usuários em sua organização podem pesquisar arquivos e seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e3919-104">With the [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) connector, users in your organization can search for files and their content.</span></span> <span data-ttu-id="e3919-105">Esse conector acessa os dados armazenados em contêineres de blob do Azure e pastas habilitadas para hierarquia dentro de uma conta do Azure data Lake Storage Gen 2.</span><span class="sxs-lookup"><span data-stu-id="e3919-105">This connector accesses data stored in Azure Blob containers and hierarchy-enabled folders within an Azure Data Lake Storage Gen 2 account.</span></span>

<span data-ttu-id="e3919-106">Este artigo é para os administradores do [Microsoft 365](https://www.microsoft.com/microsoft-365) ou qualquer pessoa que configure, execute e monitore um conector de Gen2 de armazenamento do Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="e3919-106">This article is for [Microsoft 365](https://www.microsoft.com/microsoft-365) administrators or anyone who configures, runs, and monitors an Azure Data Lake Storage Gen2 connector.</span></span> <span data-ttu-id="e3919-107">Ele explica como configurar seus recursos de conector e conector, limitações e técnicas de solução de problemas.</span><span class="sxs-lookup"><span data-stu-id="e3919-107">It explains how to configure your connector and connector capabilities, limitations, and troubleshooting techniques.</span></span>

## <a name="connect-to-a-data-source"></a><span data-ttu-id="e3919-108">Conectar-se a uma fonte de dados</span><span class="sxs-lookup"><span data-stu-id="e3919-108">Connect to a data source</span></span>

### <a name="primary-storage-connection-string"></a><span data-ttu-id="e3919-109">Cadeia de conexão de armazenamento principal</span><span class="sxs-lookup"><span data-stu-id="e3919-109">Primary storage connection string</span></span> 
<span data-ttu-id="e3919-110">Na tela **autenticação e configuração** , forneça a cadeia de conexão de armazenamento principal.</span><span class="sxs-lookup"><span data-stu-id="e3919-110">On the **Authentication and config** screen, provide the Primary Storage Connection String.</span></span> <span data-ttu-id="e3919-111">Essa cadeia de caracteres é necessária para permitir o acesso à sua conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e3919-111">That string is required to allow access to your storage account.</span></span> <span data-ttu-id="e3919-112">Para encontrar a cadeia de conexão, vá para o [portal do Azure](https://ms.portal.azure.com/#home) e navegue até a seção **chaves** da conta do [Gen2 de armazenamento do Azure data Lake](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) .</span><span class="sxs-lookup"><span data-stu-id="e3919-112">To find your connection string, go to the [Azure portal](https://ms.portal.azure.com/#home) and navigate to the **Keys** section of the [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span> <span data-ttu-id="e3919-113">Copie e cole a cadeia de conexão no campo apropriado na tela.</span><span class="sxs-lookup"><span data-stu-id="e3919-113">Copy and paste the connection string in the appropriate field on the screen.</span></span>

<span data-ttu-id="e3919-114">Se não quiser fornecer o **AccountKey** (um parâmetro na cadeia de conexão de armazenamento principal), você terá que conceder acesso de leitura ao nosso serviço de conectores do Graph.</span><span class="sxs-lookup"><span data-stu-id="e3919-114">If you don't want to provide the **AccountKey** (a parameter in the primary storage connection string), you have to grant read access to our Graph Connectors Service.</span></span> <span data-ttu-id="e3919-115">Na guia **controle de acesso** de sua conta do Gen2 de armazenamento do Azure data Lake, siga as instruções nessa página para conceder acesso ao seguinte aplicativo:</span><span class="sxs-lookup"><span data-stu-id="e3919-115">In the **Access Control** tab of your Azure Data Lake Storage Gen2 account, follow the instructions on that page to grant access to the following app:</span></span>
* <span data-ttu-id="e3919-116">**ID do aplicativo de terceiros:** 56c1da01-2129-48f7-9355-af6d59d42766</span><span class="sxs-lookup"><span data-stu-id="e3919-116">**First Party App ID:** 56c1da01-2129-48f7-9355-af6d59d42766</span></span>
* <span data-ttu-id="e3919-117">**Nome do aplicativo de parte inicial:** Serviço do conector do Graph</span><span class="sxs-lookup"><span data-stu-id="e3919-117">**First Party App Name:** Graph Connector Service</span></span>

### <a name="storage-account-and-queue-notifications-optional"></a><span data-ttu-id="e3919-118">Notificações de conta e fila de armazenamento (opcional)</span><span class="sxs-lookup"><span data-stu-id="e3919-118">Storage account and queue notifications (Optional)</span></span>
<span data-ttu-id="e3919-119">O suporte para processar alterações em tempo real no serviço de conectores do Graph pode ser adicionado no futuro.</span><span class="sxs-lookup"><span data-stu-id="e3919-119">Support to process changes in real time in the Graph Connectors Service might be added in the future.</span></span> <span data-ttu-id="e3919-120">Nesse caso, monitoraremos as notificações de alteração [do Gen2 de armazenamento do Azure data Lake](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) armazenadas em uma fila.</span><span class="sxs-lookup"><span data-stu-id="e3919-120">In that case, we'll monitor [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) change notifications stored in a queue.</span></span> <span data-ttu-id="e3919-121">Você precisará criar uma fila na mesma conta que seu Gen2 de armazenamento do Azure data Lake ou em outra conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e3919-121">You'll need to create a queue in the same account as your Azure Data Lake Storage Gen2 or in another storage account.</span></span>

<span data-ttu-id="e3919-122">Depois de criar uma fila, vá para a guia **eventos** na página fila para configurar a **assinatura do evento**.</span><span class="sxs-lookup"><span data-stu-id="e3919-122">After you create a queue, go to the **Events** tab on the queue page to configure **Event Subscription**.</span></span> <span data-ttu-id="e3919-123">Escolha todos os eventos BLOB que a fila receberá e conecte a fila à conta do Gen2 de armazenamento do Azure data Lake.</span><span class="sxs-lookup"><span data-stu-id="e3919-123">Choose all the Blob events that the queue will receive, and connect the queue to the Azure Data Lake Storage Gen2 account.</span></span>

## <a name="manage-the-search-schema"></a><span data-ttu-id="e3919-124">Gerenciar o esquema de pesquisa</span><span class="sxs-lookup"><span data-stu-id="e3919-124">Manage the search schema</span></span>
<span data-ttu-id="e3919-125">Na tela **gerenciar esquema** , você tem a opção de alterar os atributos de esquema (**consultável**, **pesquisável**e **recuperável**) associados às propriedades gerenciadas.</span><span class="sxs-lookup"><span data-stu-id="e3919-125">On the **Manage Schema** screen, you have the option to change the schema attributes (**queryable**, **searchable**, and **retrievable**) associated with the managed properties.</span></span> <span data-ttu-id="e3919-126">Esses atributos de propriedade gerenciada são dados indexados de sua conta [do Gen2 de armazenamento do Azure data Lake](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) .</span><span class="sxs-lookup"><span data-stu-id="e3919-126">These managed property attributes are data indexed from your [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) account.</span></span>

## <a name="manage-search-permissions"></a><span data-ttu-id="e3919-127">Gerenciar permissões de pesquisa</span><span class="sxs-lookup"><span data-stu-id="e3919-127">Manage search permissions</span></span>
<span data-ttu-id="e3919-128">Na tela **gerenciar permissões de pesquisa** , você pode optar por absorver as listas de controle de acesso (ACLs) da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e3919-128">On the **Manage search permissions** screen, you can choose to ingest the Access Control Lists (ACLs) from your storage account.</span></span> <span data-ttu-id="e3919-129">Quando essas permissões de pesquisa são definidas, o conteúdo da pesquisa é cortado com base nas permissões atribuídas ao usuário conectado do [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) que está pesquisando o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e3919-129">When these search permissions are set, search content is trimmed based on the permissions assigned to the signed-in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/) user searching the content.</span></span> <span data-ttu-id="e3919-130">Como alternativa, você pode escolher tornar todo o conteúdo indexado da conta de armazenamento visível para todos em sua organização.</span><span class="sxs-lookup"><span data-stu-id="e3919-130">Alternatively, you can choose to make all the content indexed from your storage account visible to everyone in your organization.</span></span> <span data-ttu-id="e3919-131">Nesse caso, todos em sua organização terão acesso a todos os dados em sua conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e3919-131">In this case, everyone in your organization will have access to all the data in your storage account.</span></span>
 
## <a name="set-the-refresh-schedule"></a><span data-ttu-id="e3919-132">Definir o agendamento de atualização</span><span class="sxs-lookup"><span data-stu-id="e3919-132">Set the refresh schedule</span></span>
<span data-ttu-id="e3919-133">Na tela **configurações de atualização** , você pode definir o intervalo de rastreamento incremental e o intervalo de rastreamento completo.</span><span class="sxs-lookup"><span data-stu-id="e3919-133">On the **Refresh Settings** screen, you can set the incremental crawl interval and the full crawl interval.</span></span> <span data-ttu-id="e3919-134">Os intervalos padrão para o conector do [Gen2 de armazenamento do Azure data Lake](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) são 15 minutos para um rastreamento incremental e uma semana para um rastreamento completo.</span><span class="sxs-lookup"><span data-stu-id="e3919-134">The default intervals for the [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) connector are 15 minutes for an incremental crawl and one week for a full crawl.</span></span>
 
## <a name="limitations"></a><span data-ttu-id="e3919-135">Limitações</span><span class="sxs-lookup"><span data-stu-id="e3919-135">Limitations</span></span>
<span data-ttu-id="e3919-136">Atualmente, o acesso multiprotocolo [do Gen2 de armazenamento do data Lake do Azure](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) está disponível somente no centro dos Estados Unidos, oeste dos EUA, Canadá, leste dos EUA, leste da Ásia, nordeste da Europa, leste da Ásia, sudoeste da Europa, oeste da Austrália, oeste leste, leste asiático, West US2 e Brasil Sul.</span><span class="sxs-lookup"><span data-stu-id="e3919-136">Currently, [Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-introduction) Multi-Protocol Access is available only in the Central US, West Central US, Canada Central, East US, East Asia, North Europe, East US2, South East Asia, West Europe, West US, Australia East, Japan East, West US2, and Brazil South.</span></span>

<span data-ttu-id="e3919-137">Para obter atualizações e mais informações, consulte [acesso multiprotocolo no Azure data Lake Storage (versão prévia)](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-multi-protocol-access).</span><span class="sxs-lookup"><span data-stu-id="e3919-137">For updates and more information, see  [Multi-protocol access on Azure Data Lake Storage (preview)](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-multi-protocol-access).</span></span>

