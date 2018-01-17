---
title: "Prospektista käteiseksi"
description: "Tässä ohjeaiheessa on yleiskuvaus Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin ja Microsoft Dynamics 365 for Sales -sovelluksen välisestä prospektista käteiseksi -ratkaisusta."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f169b0ee20a7ca0c8d05c8bdcf2c04d411722f01
ms.openlocfilehash: ff166f89d13acbc3aefcbdb39f485881c81cb42c
ms.contentlocale: fi-fi
ms.lasthandoff: 12/21/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="8dd36-103">Prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="8dd36-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8dd36-104">Prospektista käteiseksi -ratkaisu mahdollistaa suoran synkronoinnin Dynamics 365 for Finance and Operations, Enterprise editionin ja Dynamics 365 for Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="8dd36-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="8dd36-105">Tietojen integrointitoiminnon prospektista käteiseksi -mallit mahdollistavat tilien, yhteyshenkilöiden, tuotteiden, myyntitarjousten, myyntitilausten ja myyntilaskujen tietojen kulun Finance and Operationsin ja Salesin välillä.</span><span class="sxs-lookup"><span data-stu-id="8dd36-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="8dd36-106">Kun tieto kulkee Finance and Operationsin ja Salesin välillä, voit suorittaa myynti- ja markkinointitehtäviä Salesissa sekä käsitellä tilauksen täyttämistä Finance and Operationsin inventoinnin- ja varastonhallinnalla.</span><span class="sxs-lookup"><span data-stu-id="8dd36-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span>

<span data-ttu-id="8dd36-107">Nykyisessä versiossa prospektista käteiseksi -ratkaisu mahdollistaa seuraavat suoran synkronoinnin tyypit:</span><span class="sxs-lookup"><span data-stu-id="8dd36-107">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="8dd36-108">Tilien ylläpito Salesissa ja tilien synkronointi suoraan Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-108">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="8dd36-109">Tuotteiden ylläpito Finance and Operationsissa ja synkronointi suoraan Salesiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-109">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="8dd36-110">Salesin yhteyshenkilöiden ylläpito ja synkronointi suoraan Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-110">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="8dd36-111">Myyntitarjouksien synkronointi suoraan Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-111">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="8dd36-112">Myyntitilausten synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-112">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="8dd36-113">Myyntitilausten synkronointi suoraan Salesin ja Finance and Operationsin välillä</span><span class="sxs-lookup"><span data-stu-id="8dd36-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="8dd36-114">Myyntilaskun synkronointi suoraan Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

<span data-ttu-id="8dd36-115">Aiemmissa versiossa prospektista käteiseksi -ratkaisu mahdollistaa seuraavat epäsuoran synkronoinnin tyypit:</span><span class="sxs-lookup"><span data-stu-id="8dd36-115">In earlier versions, the Prospect to cash solution provides the following types of non-direct synchronization:</span></span>

- [<span data-ttu-id="8dd36-116">Ylläpidä tilejä Salesissa ja synkronoi ne Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="8dd36-116">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
- [<span data-ttu-id="8dd36-117">Yhteyshenkilöiden ylläpito Salesissa ja niiden synkronointi Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-117">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
- [<span data-ttu-id="8dd36-118">Tuotteiden ylläpito Finance and Operationsissa ja niiden synkronointi Salesiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-118">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
- [<span data-ttu-id="8dd36-119">Myyntitarjousten luominen Salesissa ja niiden synkronointi Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-119">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
- [<span data-ttu-id="8dd36-120">Myyntitilausten luominen Finance and Operationsissa ja niiden synkronointi Salesiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-120">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
- [<span data-ttu-id="8dd36-121">Luo myyntilaskuja Finance and Operationsissa ja synkronoi ne Salesiin</span><span class="sxs-lookup"><span data-stu-id="8dd36-121">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="8dd36-122">Finance and Operations -sovelluksen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="8dd36-122">System requirements for Finance and Operations</span></span>

<span data-ttu-id="8dd36-123">Seuraavat komponentit on asennettava, jotta prospektista käteiseksi -ratkaisua voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="8dd36-123">To use the Prospect to cash solution, you must install the following components:</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="8dd36-124">Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017)</span><span class="sxs-lookup"><span data-stu-id="8dd36-124">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="8dd36-125">Dynamics 365 for Finance and Operations, Enterprise edition (heinäkuu 2017) ja ympäristöpäivitys 8 (sovellusversio 7.2.11792.56024 ja ympäristöversio 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="8dd36-125">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212)</span></span>
- <span data-ttu-id="8dd36-126">Seuraavat hotfix-korjaukset ovat pakollisia:</span><span class="sxs-lookup"><span data-stu-id="8dd36-126">The following hotfixes are required:</span></span>

    - <span data-ttu-id="8dd36-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Salesista Finance and Operationsiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="8dd36-127">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="8dd36-128">Se sisältää myös useita parannuksia.</span><span class="sxs-lookup"><span data-stu-id="8dd36-128">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="8dd36-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – tämän korjaus mahdollistaa myyntitilausrivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="8dd36-129">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="8dd36-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – tämän korjaus mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointitoiminnolla.</span><span class="sxs-lookup"><span data-stu-id="8dd36-130">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8dd36-131">Ainoastaan KB4045570 on asennettava, sillä sen asennus sisältää muiden hotfix-korjausten muutokset.</span><span class="sxs-lookup"><span data-stu-id="8dd36-131">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="8dd36-132">Dynamics 365 for Finance and Operations -versio 1611 (marraskuu 2016)</span><span class="sxs-lookup"><span data-stu-id="8dd36-132">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span> 

- <span data-ttu-id="8dd36-133">Dynamics 365 for Finance and Operations -versio 1611 (marraskuu 2016) ja vähintään ympäristöpäivitys 8</span><span class="sxs-lookup"><span data-stu-id="8dd36-133">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="8dd36-134">Seuraavat hotfix-korjaukset ovat pakollisia:</span><span class="sxs-lookup"><span data-stu-id="8dd36-134">The following hotfixes are required:</span></span>

    - <span data-ttu-id="8dd36-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Mahdollistaa myyntitilauksen synkronoinnin Finance and Operationsista Salesiin tietojen integrointiohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="8dd36-135">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="8dd36-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Mahdollistaa myyntitilauksen otsikon ja rivin synkronoinnin Finance and Operationsista Salesiin tietojen integrointiohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="8dd36-136">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="8dd36-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Prospektista käteiseksi -integrointia tietoyksiköiden kautta on tuettava.</span><span class="sxs-lookup"><span data-stu-id="8dd36-137">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8dd36-138">Kun hotfix-korjaukset on asennettu, seuraava **SalesPopulateProspectToCash**-lomakkeen erätyö on käynnistettävä.</span><span class="sxs-lookup"><span data-stu-id="8dd36-138">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="8dd36-139">Tämä lomake on piilotettu, koska sitä tarvitaan vain kerran.</span><span class="sxs-lookup"><span data-stu-id="8dd36-139">This form is hidden because you only need it once.</span></span> <span data-ttu-id="8dd36-140">Voit käyttää lomaketta kirjautumalla ympäristöön ja lisäämällä seuraavan URL-osoitteeseen selainosoitteessasi: &mi=action:SalesPopulateProspectToCash, kuten https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span><span class="sxs-lookup"><span data-stu-id="8dd36-140">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash.</span></span> <span data-ttu-id="8dd36-141">Kun lomake avautuu, valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8dd36-141">When the form opens, click OK.</span></span> <span data-ttu-id="8dd36-142">**SalesLine**-, **SalesQuotationLine**- ja **CustInvoiceTrans**-taulukkojenn uuteen **LineCreationSequnceNumber**-kenttiin täytetään yksilöivät arvot, jolloin tuoteluettelo päivittyy.</span><span class="sxs-lookup"><span data-stu-id="8dd36-142">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="8dd36-143">Tämä on välttämätöntä, jotta Prospektista käteiseksi -integrointi toimisi.</span><span class="sxs-lookup"><span data-stu-id="8dd36-143">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="8dd36-144">Sales-sovelluksen järjestelmävaatimukset</span><span class="sxs-lookup"><span data-stu-id="8dd36-144">System requirements for Sales</span></span>

<span data-ttu-id="8dd36-145">Seuraavat komponentit on asennettava, jotta prospektista käteiseksi -ratkaisua voi käyttää:</span><span class="sxs-lookup"><span data-stu-id="8dd36-145">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="8dd36-146">Dynamics 365 for Sales -versio 1612 (8.2.1.207) (DB 8.2.1.207) online</span><span class="sxs-lookup"><span data-stu-id="8dd36-146">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="8dd36-147">Dynamics 365 for Salesin prospektista käteiseksi -ratkaisu, versio 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="8dd36-147">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

   > [!NOTE]
   >
   > <span data-ttu-id="8dd36-148">Malleja, joiden versio on 1.0.0.0 tai 1.0.0.1, tuetaan prospektista käteiseksi -ratkaisussa Dynamics 365 for Sales -versiossa 1.14.1.0</span><span class="sxs-lookup"><span data-stu-id="8dd36-148">Templates with version 1.0.0.0 and 1.0.0.1 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.14.1.0</span></span>
   >
   > <span data-ttu-id="8dd36-149">Malleja, joiden versio on 2.0.0.0 tai 2.1.0.0, tuetaan prospektista käteiseksi -ratkaisussa Dynamics 365 for Sales -versiossa 1.15.0.0</span><span class="sxs-lookup"><span data-stu-id="8dd36-149">Templates with version 2.0.0.0 and 2.1.0.0 are supported on Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="8dd36-150">Asenna Salesin prospektista käteiseksi -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8dd36-150">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="8dd36-151">Lataa [Dynamics 365 for Salesin prospektista käteiseksi -ratkaisun zip-pakettitiedosto](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSourcesta.</span><span class="sxs-lookup"><span data-stu-id="8dd36-151">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="8dd36-152">Varmista, että zip-tiedoston esto on poistettu.</span><span class="sxs-lookup"><span data-stu-id="8dd36-152">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="8dd36-153">Muussa tapauksessa saat seuraavan virhesanoman, kun yrität asentaa ratkaisupakettia: Tuontipaketteja ei löytynyt.</span><span class="sxs-lookup"><span data-stu-id="8dd36-153">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="8dd36-154">Voit poistaa zip-tiedoston eston napsauttamalla sitä hiiren kakkospainikkeella ja valitsemalla **Ominaisuudet**-kohdan.</span><span class="sxs-lookup"><span data-stu-id="8dd36-154">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="8dd36-155">Valitse **Poista esto**.</span><span class="sxs-lookup"><span data-stu-id="8dd36-155">Select **Unblock**.</span></span>
3. <span data-ttu-id="8dd36-156">Pura ja suorita **PackageDeployer.exe**.</span><span class="sxs-lookup"><span data-stu-id="8dd36-156">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="8dd36-157">Asenna prospektista käteiseksi -ratkaisu Sales-esiintymään:</span><span class="sxs-lookup"><span data-stu-id="8dd36-157">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="8dd36-158">Valitse käyttöönottotyypiksi **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="8dd36-158">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="8dd36-159">Valitse **Näytä laajennettu**</span><span class="sxs-lookup"><span data-stu-id="8dd36-159">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="8dd36-160">Aloita pika-asennus valitsemalla alue.</span><span class="sxs-lookup"><span data-stu-id="8dd36-160">For a quick installation, select a region.</span></span> <span data-ttu-id="8dd36-161">Jos valitset **En tiedä**, järjestelmä etsii kaikki alueet, ja asennus kestää kauemmin.</span><span class="sxs-lookup"><span data-stu-id="8dd36-161">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="8dd36-162">Anna asennusoikeudet omaavan järjestelmänvalvojan käyttäjänimi ja salasana.</span><span class="sxs-lookup"><span data-stu-id="8dd36-162">Enter the user name and password of an admin user who has installation rights.</span></span>

