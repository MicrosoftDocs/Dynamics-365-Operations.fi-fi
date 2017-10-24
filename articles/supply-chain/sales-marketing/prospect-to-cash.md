---
title: "Prospektista käteiseksi"
description: "Tässä ohjeaiheessa on yleiskatsaus prospektista käteiseksi ratkaisusta Dynamics 365 for Salesin ja Dynamics 365 for Finance and Operations, Enterprise editionin välillä."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="6e00c-103">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="6e00c-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6e00c-104">Prospektista käteiseksi ratkaisu synkronoi [tietojen integrointitoiminnolla](/common-data-service/entity-reference/dynamics-365-integration) tietoja Microsoft Dynamics 365 Financen ja Operations, Enterprise editionin ja Dynamics 365 for Salesin esiintymien välillä Common Data Servicen kautta.</span><span class="sxs-lookup"><span data-stu-id="6e00c-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="6e00c-105">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="6e00c-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="6e00c-106">Kun tieto kulkee Finance and Operationsin ja Salesin välillä, voit suorittaa myynti- ja markkinointitehtäviä Salesissa sekä käsitellä tilauksen täyttämistä Finance and Operationsin inventoinnin- ja varastonhallinnalla.</span><span class="sxs-lookup"><span data-stu-id="6e00c-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="6e00c-107">Ratkaisu integroi seuraavat alueet:</span><span class="sxs-lookup"><span data-stu-id="6e00c-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="6e00c-108">Ylläpidä tilejä Salesissa ja synkronoi ne Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="6e00c-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="6e00c-109">Ylläpidä yhteyshenkilöitä Salesissa ja synkronoi ne Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="6e00c-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="6e00c-110">Ylläpidä tuotteita Finance and Operationsissa ja synkronoi ne Salesiin</span><span class="sxs-lookup"><span data-stu-id="6e00c-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="6e00c-111">Luo myyntitarjouksia Salesissa ja synkronoi ne Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="6e00c-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="6e00c-112">Luo myyntitilauksia Finance and Operationsissa ja synkronoi ne Salesiin</span><span class="sxs-lookup"><span data-stu-id="6e00c-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="6e00c-113">Luo myyntilaskuja Finance and Operationsissa ja synkronoi ne Salesiin</span><span class="sxs-lookup"><span data-stu-id="6e00c-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="6e00c-114">Dynamics 365 for Finance and Operations, Enterprise Editionin järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="6e00c-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="6e00c-115">Jotta voit käyttää prospektista käteiseksi -ratkaisua, sinun on asennettava seuraavat:</span><span class="sxs-lookup"><span data-stu-id="6e00c-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="6e00c-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017) ja ympäristöpäivitys 8 (Sovellusversio 7.2.11792.56024 + ympäristö 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="6e00c-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="6e00c-117">Kaksi hotfix-korjausta Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioniin (heinäkuu 2017).</span><span class="sxs-lookup"><span data-stu-id="6e00c-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="6e00c-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - tämän korjaus mahdollistaa myyntitilauksen rivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="6e00c-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="6e00c-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="6e00c-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="6e00c-120">**Huomautus**: ainoastaan KB4036524 on asennettava; sen asennus sisältää KB4036461-päivityksen korjaukset.</span><span class="sxs-lookup"><span data-stu-id="6e00c-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="6e00c-121">Dynamics 365 for Salesin järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="6e00c-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="6e00c-122">Jotta voit käyttää prospektista käteiseksi -ratkaisua, sinun on asennettava seuraavat:</span><span class="sxs-lookup"><span data-stu-id="6e00c-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="6e00c-123">Dynamics 365 for Sales -versio 1612 (8.2.1.207) (DB 8.2.1.207) online tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="6e00c-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="6e00c-124">Dynamics 365 for Salesin prospektista käteiseksi -ratkaisu, versio 1.14.0.0 (v14) tai uudempi.</span><span class="sxs-lookup"><span data-stu-id="6e00c-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="6e00c-125">Asenna Salesin prospektista käteiseksi -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6e00c-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="6e00c-126">Lataa [Dynamics 365 for Salesin prospektista käteiseksi -ratkaisun zip-pakettitiedosto](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSourcesta.</span><span class="sxs-lookup"><span data-stu-id="6e00c-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="6e00c-127">Varmista, että zip-tiedostoa ei ole estetty, jotta et saa virheviestiä "Tuontipakkauksia ei löytynyt", kun asennat ratkaisupaketin.</span><span class="sxs-lookup"><span data-stu-id="6e00c-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="6e00c-128">Voit poistaa eston seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6e00c-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="6e00c-129">Napsauta zip-tiedostoa hiiren kakkospainikkeella.</span><span class="sxs-lookup"><span data-stu-id="6e00c-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="6e00c-130">Valitse **Ominaisuudet** ja valitse sitten **Kumoa esto**.</span><span class="sxs-lookup"><span data-stu-id="6e00c-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="6e00c-131">Pura ja suorita PackageDeployer.exe.</span><span class="sxs-lookup"><span data-stu-id="6e00c-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="6e00c-132">Asenna prospektista käteiseksi -ratkaisu Sales-esiintymään.</span><span class="sxs-lookup"><span data-stu-id="6e00c-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="6e00c-133">Valitse **Office 365** -käyttöönottotyyppi.</span><span class="sxs-lookup"><span data-stu-id="6e00c-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="6e00c-134">Valitse **Näytä laajennettu**</span><span class="sxs-lookup"><span data-stu-id="6e00c-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="6e00c-135">Pika-asennuksen voit aloittaa valitsemalla **alueen**.</span><span class="sxs-lookup"><span data-stu-id="6e00c-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="6e00c-136">Jos valitset **En tiedä**, järjestelmä etsii kaikki alueet, ja asennus kestää kauemmin.</span><span class="sxs-lookup"><span data-stu-id="6e00c-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="6e00c-137">Määritä **käyttäjänimi** ja **salasana** hallinnon käyttäjälle, jolla on käyttöoikeudet asentamiseen.</span><span class="sxs-lookup"><span data-stu-id="6e00c-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

