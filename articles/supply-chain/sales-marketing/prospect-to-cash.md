---
title: Prospektista käteiseksi
description: Tässä ohjeaiheessa on yleiskuvaus Dynamics 365 Supply Chain Managementin ja Dynamics 365 Salesin välisestä Prospektista käteiseksi -ratkaisusta.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1a96b7cfa57ec72b25f21d94fadb2fbf9bc6ea3b
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251351"
---
# <a name="prospect-to-cash"></a><span data-ttu-id="bc6f6-103">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="bc6f6-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc6f6-104">Prospektista käteiseksi -ratkaisu mahdollistaa suoran synkronoinnin Dynamics 365 Supply Chain Managementin ja Dynamics 365 Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="bc6f6-105">Tietojen integrointitoiminnon Prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices.</span></span> <span data-ttu-id="bc6f6-106">Kun tietoja siirretään, voit suorittaa myynti- ja markkinointitehtäviä Salesissa sekä käsitellä tilausten täyttämistä Financen inventoinnin- ja varastonhallinnalla.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-106">While data is flowing, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Supply Chain Management.</span></span> 

<span data-ttu-id="bc6f6-107">Lisätietoja Prospektista käteiseksi -integroinnista on lyhyessä YouTube-videossa [Prospektista käteiseksi -integrointi](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span><span class="sxs-lookup"><span data-stu-id="bc6f6-107">For more information about the Prospect to cash integration, watch the short YouTube video [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span></span>

<span data-ttu-id="bc6f6-108">Nykyisessä versiossa prospektista käteiseksi -ratkaisu mahdollistaa seuraavat suoran synkronoinnin tyypit:</span><span class="sxs-lookup"><span data-stu-id="bc6f6-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="bc6f6-109">Tilien ylläpito Salesissa ja tilien synkronointi suoraan Salesista Supply Chain Managementiin</span><span class="sxs-lookup"><span data-stu-id="bc6f6-109">Maintain accounts in Sales and sync them directly from Sales to Supply Chain Management</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="bc6f6-110">Tuotteiden ylläpito Supply Chain Managementissa ja tuotteiden synkronointi suoraan Salesiin</span><span class="sxs-lookup"><span data-stu-id="bc6f6-110">Maintain products in Supply Chain Management and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="bc6f6-111">Yhteyshenkilöiden ylläpito Salessa ja yhteyshenkilöiden tai asiakkaiden synkronointi suoraan Supply Chain Managementiin</span><span class="sxs-lookup"><span data-stu-id="bc6f6-111">Maintain contacts in Sales and sync them directly to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="bc6f6-112">Myyntitarjousten synkronointi suoraan Salesista Supply Chain Managementiin</span><span class="sxs-lookup"><span data-stu-id="bc6f6-112">Synchronize sales quotation directly from Sales to Supply Chain Management</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="bc6f6-113">Myyntitilausten synkronointi suoraan Salesin ja Supply Chain Managementin välillä</span><span class="sxs-lookup"><span data-stu-id="bc6f6-113">Synchronize sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="bc6f6-114">Myyntilaskujen synkronointi suoraan Supply Chain Managementista Salesiin</span><span class="sxs-lookup"><span data-stu-id="bc6f6-114">Synchronize sales invoice directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="bc6f6-115">Supply Chain Managementin järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="bc6f6-115">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="bc6f6-116">Prospektista käteiseksi -integraatio tuetaan seuraavissa versioissa:</span><span class="sxs-lookup"><span data-stu-id="bc6f6-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="bc6f6-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (joulukuu 2017)</span><span class="sxs-lookup"><span data-stu-id="bc6f6-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="bc6f6-118">Dynamics 365 for Finance and Operations, Enterprise edition (joulukuu 2017) – sovelluksen koontiversio 7.3.11971.56116 ja Platform Update 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="bc6f6-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="bc6f6-119">Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017)</span><span class="sxs-lookup"><span data-stu-id="bc6f6-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="bc6f6-120">Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017) – platform update 8 (sovelluksen 7.2.11792.56024 ja ympäristön koontiversio 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="bc6f6-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="bc6f6-121">Seuraavat hotfix-korjaukset ovat pakollisia:</span><span class="sxs-lookup"><span data-stu-id="bc6f6-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="bc6f6-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – Tämä korjaus mahdollistaa myyntitilausten synkronoinnin Salesista Supply Chain Managementiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Supply Chain Management via the Data Integration feature.</span></span> <span data-ttu-id="bc6f6-123">Se sisältää myös useita parannuksia.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="bc6f6-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tämä korjaus mahdollistaa myyntitilausten rivien synkronoinnin Supply Chain Managementista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="bc6f6-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – Tämä korjaus mahdollistaa myyntitilausten synkronoinnin Supply Chain Managementista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bc6f6-126">Ainoastaan KB4045570 on asennettava, sillä sen asennus sisältää muiden hotfix-korjausten muutokset.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="bc6f6-127">Dynamics 365 for Finance and Operationsin versio 1611 (marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="bc6f6-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="bc6f6-128">Dynamics 365 for Finance and Operationsin versio 1611 (marraskuu 2016) ja platform update 8 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="bc6f6-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="bc6f6-129">Seuraavat hotfix-korjaukset ovat pakollisia:</span><span class="sxs-lookup"><span data-stu-id="bc6f6-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="bc6f6-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Mahdollistaa myyntitilausten synkronoinnin Supply Chain Managementista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Supply Chain Management to Sales.</span></span> 
  - <span data-ttu-id="bc6f6-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Mahdollistaa myyntitilausten otsikoiden ja rivien synkronoinnin Supply Chain Managementista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Supply Chain Management to Sales.</span></span>
  - <span data-ttu-id="bc6f6-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Prospektista käteiseksi -integrointia tietoyksiköiden kautta on tuettava.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="bc6f6-133">Kun hotfix-korjaukset on asennettu, seuraava **SalesPopulateProspectToCash**-lomakkeen erätyö on käynnistettävä.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="bc6f6-134">Tämä lomake on piilotettu, koska sitä tarvitaan vain kerran.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="bc6f6-135">Voit käyttää lomaketta kirjautumalla ympäristöön ja lisäämällä seuraavan URL-osoitteeseen selaimen osoitekentässä: *&mi=action:SalesPopulateProspectToCash*, esimerkiksi `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="bc6f6-136">Kun lomake avautuu, valitse OK.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-136">When the form opens, click OK.</span></span> <span data-ttu-id="bc6f6-137">**SalesLine**-, **SalesQuotationLine**- ja **CustInvoiceTrans**-taulukkojenn uuteen **LineCreationSequnceNumber**-kenttiin täytetään yksilöivät arvot, jolloin tuoteluettelo päivittyy.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="bc6f6-138">Tämä on välttämätöntä, jotta Prospektista käteiseksi -integrointi toimisi.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="bc6f6-139">Sales-sovelluksen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="bc6f6-139">System requirements for Sales</span></span>

<span data-ttu-id="bc6f6-140">Seuraavat komponentit on asennettava, jotta prospektista käteiseksi -ratkaisua voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="bc6f6-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="bc6f6-141">Dynamics 365 Sales -versio 1612 (8.2.1.207) (DB 8.2.1.207) online tai uudempi versio</span><span class="sxs-lookup"><span data-stu-id="bc6f6-141">Dynamics 365 Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="bc6f6-142">Dynamics 365 Salesin Prospektista käteiseksi -ratkaisun versio 1.15.0.0 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-142">Prospect to cash solution for Dynamics 365 Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="bc6f6-143">Ratkaisun voi ladata AppSourcesta.</span><span class="sxs-lookup"><span data-stu-id="bc6f6-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="bc6f6-144">[Lataa Dynamics 365, Prospektista käteiseksi](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="bc6f6-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
