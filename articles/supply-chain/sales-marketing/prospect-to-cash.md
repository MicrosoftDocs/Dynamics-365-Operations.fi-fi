---
title: "Prospektista käteiseksi"
description: "Tässä ohjeaiheessa on yleiskuvaus Microsoft Dynamics 365 for Finance and Operationsin ja Microsoft Dynamics 365 for Salesin välisestä prospektista käteiseksi -ratkaisusta."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f43b3943ce27c44cc0b4756d1d5f23e3be093273
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="424c0-103">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="424c0-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="424c0-104">Prospektista käteiseksi -ratkaisu mahdollistaa suoran synkronoinnin Dynamics 365 for Finance and Operationsin ja Dynamics 365 for Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="424c0-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="424c0-105">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="424c0-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="424c0-106">Kun tieto kulkee Finance and Operationsin ja Salesin välillä, voit suorittaa myynti- ja markkinointitehtäviä Salesissa sekä käsitellä tilauksen täyttämistä Finance and Operationsin inventoinnin- ja varastonhallinnalla.</span><span class="sxs-lookup"><span data-stu-id="424c0-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="424c0-107">Saat lisätietoja Prospektista käteiseksi -integraatiosta katsomalla lyhyen YouTube-videon:</span><span class="sxs-lookup"><span data-stu-id="424c0-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

[<span data-ttu-id="424c0-108">Prospektista käteiseksi -integrointi (YouTube-video)</span><span class="sxs-lookup"><span data-stu-id="424c0-108">Prospect to cash integration (YouTube video)</span></span>](https://youtu.be/AVV9x5x-XCg) 

<span data-ttu-id="424c0-109">Nykyisessä versiossa prospektista käteiseksi -ratkaisu mahdollistaa seuraavat suoran synkronoinnin tyypit:</span><span class="sxs-lookup"><span data-stu-id="424c0-109">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="424c0-110">Tilien ylläpito Salesissa ja tilien synkronointi suoraan Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="424c0-110">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="424c0-111">Tuotteiden ylläpito Finance and Operationsissa ja synkronointi suoraan Salesiin</span><span class="sxs-lookup"><span data-stu-id="424c0-111">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="424c0-112">Salesin yhteyshenkilöiden ylläpito ja synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="424c0-112">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="424c0-113">Myyntitarjouksien synkronointi suoraan Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="424c0-113">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="424c0-114">Myyntitilausten synkronointi suoraan Salesin ja Finance and Operationsin välillä</span><span class="sxs-lookup"><span data-stu-id="424c0-114">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="424c0-115">Myyntilaskun synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="424c0-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="424c0-116">Finance and Operations -sovelluksen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="424c0-116">System requirements for Finance and Operations</span></span>
<span data-ttu-id="424c0-117">Prospektista käteiseksi -integraatio tuetaan seuraavissa versioissa:</span><span class="sxs-lookup"><span data-stu-id="424c0-117">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="424c0-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (joulukuu 2017)</span><span class="sxs-lookup"><span data-stu-id="424c0-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="424c0-119">Dynamics 365 for Finance and Operations, Enterprise edition (joulukuu 2017) – sovellusversio 7.3.11971.56116 ja ympäristöversio 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="424c0-119">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="424c0-120">Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017)</span><span class="sxs-lookup"><span data-stu-id="424c0-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="424c0-121">Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017) – sekä ympäristöpäivitys 8 (sovellusversio 7.2.11792.56024 ja ympäristöversio 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="424c0-121">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="424c0-122">Seuraavat hotfix-korjaukset ovat pakollisia:</span><span class="sxs-lookup"><span data-stu-id="424c0-122">The following hotfixes are required:</span></span>

  - <span data-ttu-id="424c0-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Salesista Finance and Operationsiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="424c0-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="424c0-124">Se sisältää myös useita parannuksia.</span><span class="sxs-lookup"><span data-stu-id="424c0-124">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="424c0-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – tämän korjaus mahdollistaa myyntitilausrivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="424c0-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="424c0-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="424c0-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="424c0-127">Ainoastaan KB4045570 on asennettava, sillä sen asennus sisältää muiden hotfix-korjausten muutokset.</span><span class="sxs-lookup"><span data-stu-id="424c0-127">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="424c0-128">Dynamics 365 for Finance and Operations -versio 1611 (marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="424c0-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="424c0-129">Dynamics 365 for Finance and Operations -versio 1611 (marraskuu 2016) ja vähintään ympäristöpäivitys 8</span><span class="sxs-lookup"><span data-stu-id="424c0-129">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="424c0-130">Seuraavat hotfix-korjaukset ovat pakollisia:</span><span class="sxs-lookup"><span data-stu-id="424c0-130">The following hotfixes are required:</span></span>

  - <span data-ttu-id="424c0-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointiohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="424c0-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
  - <span data-ttu-id="424c0-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Mahdollistaa myyntitilauksen otsikon ja rivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointiohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="424c0-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
  - <span data-ttu-id="424c0-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Prospektista käteiseksi -integrointia tietoyksiköiden kautta on tuettava.</span><span class="sxs-lookup"><span data-stu-id="424c0-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="424c0-134">Kun hotfix-korjaukset on asennettu, seuraava **SalesPopulateProspectToCash**-lomakkeen erätyö on käynnistettävä.</span><span class="sxs-lookup"><span data-stu-id="424c0-134">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="424c0-135">Tämä lomake on piilotettu, koska sitä tarvitaan vain kerran.</span><span class="sxs-lookup"><span data-stu-id="424c0-135">This form is hidden because you only need it once.</span></span> <span data-ttu-id="424c0-136">Voit käyttää lomaketta kirjautumalla ympäristöön ja lisäämällä seuraavan URL-osoitteeseen selaimen osoitekentässä: *&mi=action:SalesPopulateProspectToCash*, esimerkiksi `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="424c0-136">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="424c0-137">Kun lomake avautuu, valitse OK.</span><span class="sxs-lookup"><span data-stu-id="424c0-137">When the form opens, click OK.</span></span> <span data-ttu-id="424c0-138">**SalesLine**-, **SalesQuotationLine**- ja **CustInvoiceTrans**-taulukkojenn uuteen **LineCreationSequnceNumber**-kenttiin täytetään yksilöivät arvot, jolloin tuoteluettelo päivittyy.</span><span class="sxs-lookup"><span data-stu-id="424c0-138">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="424c0-139">Tämä on välttämätöntä, jotta Prospektista käteiseksi -integrointi toimisi.</span><span class="sxs-lookup"><span data-stu-id="424c0-139">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="424c0-140">Sales-sovelluksen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="424c0-140">System requirements for Sales</span></span>

<span data-ttu-id="424c0-141">Seuraavat komponentit on asennettava, jotta prospektista käteiseksi -ratkaisua voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="424c0-141">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="424c0-142">Dynamics 365 for Sales -versio 1612 (8.2.1.207) (DB 8.2.1.207) online tai uudempi versio</span><span class="sxs-lookup"><span data-stu-id="424c0-142">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="424c0-143">Dynamics 365 for Salesin prospektista käteiseksi -ratkaisu, versio 1.15.0.0 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="424c0-143">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="424c0-144">Ratkaisun voi ladata AppSourcesta.</span><span class="sxs-lookup"><span data-stu-id="424c0-144">The solution is available for download from AppSource.</span></span> <span data-ttu-id="424c0-145">[Lataa Dynamics 365, Prospektista käteiseksi](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="424c0-145">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>

