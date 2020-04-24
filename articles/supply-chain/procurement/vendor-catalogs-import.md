---
title: Tuo toimittajan tuoteluettelot
description: Tässä ohjeaiheessa käsittään toimittajan tuoteluettelon tietojen tuontia.
author: mkirknel
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: mkirknel
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 35b8e2a87708c88b12c5c7605a7977712a35a0f4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207368"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="e5c62-103">Tuo toimittajan tuoteluettelot</span><span class="sxs-lookup"><span data-stu-id="e5c62-103">Import vendor catalogs</span></span>
[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="e5c62-104">Toimittajan tuoteluetteloiden tuonti</span><span class="sxs-lookup"><span data-stu-id="e5c62-104">Vendor catalogs import</span></span>

<span data-ttu-id="e5c62-105">Oston asiantuntijat voivat luoda ja ylläpitää Dynamics 365 Supply Chain Managementissa luetteloita, joita yrityksen työntekijät voivat käyttää tilatessaan nimikkeet ja palvelut sisäiseen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e5c62-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="e5c62-106">Voit luoda tuotteiden hankintaluettelon lisäämällä työntekijöiden käyttöön tarkoitettuja nimikkeitä ja palveluja joko tuomalla tuoteluettelon tietoja tai lisäämällä tuoteluettelon tiedot manuaalisesti päätuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="e5c62-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="e5c62-107">Voit ladata toimittajan lähettämät luettelotiedot Microsoft Dynamics 365 -asiakasohjelmasta.</span><span class="sxs-lookup"><span data-stu-id="e5c62-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="e5c62-108">Toimittajan sinulle CMR-tiedostona eli luettelon ylläpitopyyntönä lähettämien tuotetietojen tiedostomuodon on oltava XML.</span><span class="sxs-lookup"><span data-stu-id="e5c62-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="e5c62-109">CMR-tiedostossa on oltava toimittajan yritykselle toimittamien tuotteiden tiedot.</span><span class="sxs-lookup"><span data-stu-id="e5c62-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>
<span data-ttu-id="e5c62-110">''''</span><span class="sxs-lookup"><span data-stu-id="e5c62-110">''''</span></span>
## <a name="import-vendor-catalog-data"></a><span data-ttu-id="e5c62-111">Toimittajan tuoteluettelon tietojen tuominen</span><span class="sxs-lookup"><span data-stu-id="e5c62-111">Import vendor catalog data</span></span>
<span data-ttu-id="e5c62-112">'' Jos haluat tuoda toimittajan tuoteluettelon tietoja, sinun on suoritettava seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="e5c62-112">'' To import vendor catalog data, you must complete the following tasks:</span></span>

1.  <span data-ttu-id="e5c62-113">Määritä projekti siinä Tietojen hallinta -työtilassa, jossa olet määrittänyt tietojen yhdistämissäännöt.</span><span class="sxs-lookup"><span data-stu-id="e5c62-113">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="e5c62-114">Valitse ensin **Tietojen hallinta** ja sitten **Määritä tietoprojektien roolit**.</span><span class="sxs-lookup"><span data-stu-id="e5c62-114">Select **Data management** and then select **Set up roles for data projects**.</span></span> 
    <span data-ttu-id="e5c62-115">''</span><span class="sxs-lookup"><span data-stu-id="e5c62-115">''</span></span>
2.  <span data-ttu-id="e5c62-116">Määritä hankintaluokkahierarkia ja määritä toimittajat hankintaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="e5c62-116">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="e5c62-117">Jos käytät kauppatavarakoodeja, lisää nämä koodit hankintaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="e5c62-117">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="e5c62-118">Lisätietoja hankintaluokkahierarkian määrittämisestä on kohdassa [Hankintaluokkahierarkian määrittäminen](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="e5c62-118">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>
    <span data-ttu-id="e5c62-119">''</span><span class="sxs-lookup"><span data-stu-id="e5c62-119">''</span></span>
3.  <span data-ttu-id="e5c62-120">Konfiguroi toimittaja luettelon tuontia varten</span><span class="sxs-lookup"><span data-stu-id="e5c62-120">Configure the vendor for catalog import.</span></span> <span data-ttu-id="e5c62-121">Valitse ensin toimittaja ja sitten **Hankinta** > **Asetukset** > **Konfiguroi toimittaja luettelon tuontia varten**.</span><span class="sxs-lookup"><span data-stu-id="e5c62-121">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>
<span data-ttu-id="e5c62-122">''''</span><span class="sxs-lookup"><span data-stu-id="e5c62-122">''''</span></span>
4.  <span data-ttu-id="e5c62-123">Määritä luettelon tuonnin työnkulku.</span><span class="sxs-lookup"><span data-stu-id="e5c62-123">Configure workflow for catalog import.</span></span> <span data-ttu-id="e5c62-124">Luo CMR-tiedostomalli ja jaa se toimittajan kanssa.</span><span class="sxs-lookup"><span data-stu-id="e5c62-124">Create a CMR file template and share this with your vendor.</span></span>

5.  <span data-ttu-id="e5c62-125">Luo toimittajan tuoteluettelot valitsemalla **Hankinta** \> **Yleinen** \> **Luettelot** \> **Toimittajan tuoteluettelot**.</span><span class="sxs-lookup"><span data-stu-id="e5c62-125">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="e5c62-126">Toimittajalta vastaanotetut CMR-tiedostot eli luettelon ylläpitopyynnöt ryhmitetään tässä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e5c62-126">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6.  <span data-ttu-id="e5c62-127">Lataa CMR-tiedosto palvelimeen.</span><span class="sxs-lookup"><span data-stu-id="e5c62-127">Upload the CMR file.</span></span>

7.  <span data-ttu-id="e5c62-128">Arvioi, hyväksy tai hylkää toimittajan tuoteluettelon tuotteet.</span><span class="sxs-lookup"><span data-stu-id="e5c62-128">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="e5c62-129">Tuotteet yhdistetään automaattisesti hankintaluokkiin.</span><span class="sxs-lookup"><span data-stu-id="e5c62-129">The products are automatically mapped to the procurement categories.</span></span> 
    
<span data-ttu-id="e5c62-130">Hyväksytyt tuotteet lisätään päätuotteeseen ja vapautetaan valituille oikeushenkilöille.</span><span class="sxs-lookup"><span data-stu-id="e5c62-130">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="e5c62-131">Vain hyväksytyt tuotteen voidaan lisätä hankintaluetteloon.</span><span class="sxs-lookup"><span data-stu-id="e5c62-131">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="e5c62-132">Luettelon tuontitiedostomallin luominen</span><span class="sxs-lookup"><span data-stu-id="e5c62-132">Generate a catalog import file template</span></span>

<span data-ttu-id="e5c62-133">Luettelon tuontitiedostomalli on XSD-tiedosto, jonka avulla voit luoda CMR-tiedoston toimittajan tuotteille.</span><span class="sxs-lookup"><span data-stu-id="e5c62-133">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="e5c62-134">Voit käyttää CMR-tiedostoa uuden luettelon luomiseen, aiemmin luodun luettelon korvaamiseen tai olemassa olevan luettelon muokkaamiseen.</span><span class="sxs-lookup"><span data-stu-id="e5c62-134">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1.  <span data-ttu-id="e5c62-135">Valitse **Hankinta** \> **Luettelot** \> **Toimittajan tuoteluettelot** ja kaksoisnapsauta käsiteltävää luetteloa.</span><span class="sxs-lookup"><span data-stu-id="e5c62-135">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor catalogs** and double-click the catalog that you want to work with.</span></span>

2.  <span data-ttu-id="e5c62-136">Lataa nykyisen luettelon tuontimalli (XSD-tiedosto).</span><span class="sxs-lookup"><span data-stu-id="e5c62-136">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="e5c62-137">Valitse **Päivitä luettelo** -sivun **toimintoruudun** **Luettelot**-välilehden **Aiheeseen liittyviä tietoja** -ryhmässä ensin **Luo luettelomalli** ja sitten **Hankintamalli**.</span><span class="sxs-lookup"><span data-stu-id="e5c62-137">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    -   <span data-ttu-id="e5c62-138">Voit luoda **Hankintaluokka**-asetuksella luettelomallin, jonka sisältämissä hankintaluokissa toimittaja saa tarjota tuotteita.</span><span class="sxs-lookup"><span data-stu-id="e5c62-138">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="e5c62-139">Valitse **Tallenna nimellä** -valintaruudussa sijainti, johon haluat tallentaa luettelotiedostomallin, ja tallenna tiedosto.</span><span class="sxs-lookup"><span data-stu-id="e5c62-139">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="e5c62-140">Seuraavassa blogikirjoituksessa on lisätietoja ja esimerkkejä: [Dynamics AX:n toimittajien tuoteluettelot](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span><span class="sxs-lookup"><span data-stu-id="e5c62-140">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>
