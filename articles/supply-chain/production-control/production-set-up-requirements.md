---
title: Tuotantoasetusten vaatimukset
description: Tässä artikkelissa on tietoja asetuksista, jotka on tehtävä ennen tuotannonhallinnan aloittamista.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParameters, RouteOpr, RouteOprTable, WorkCalendarTable, WorkTimeTable, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55561
ms.assetid: 1953059f-478d-4706-b461-25b89ace5fc3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05a4c97697f13a41b65fba0df8c76bf884fc51a9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209368"
---
# <a name="production-setup-requirements"></a><span data-ttu-id="51d35-103">Tuotantoasetusten vaatimukset</span><span class="sxs-lookup"><span data-stu-id="51d35-103">Production setup requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51d35-104">Tässä artikkelissa on tietoja asetuksista, jotka on tehtävä ennen tuotannonhallinnan aloittamista.</span><span class="sxs-lookup"><span data-stu-id="51d35-104">This article provides information about setup requirements before you can work with Production control.</span></span> 

<span data-ttu-id="51d35-105">Tuotannonhallinta on integroitu muiden moduulien ominaisuuksien kanssa.</span><span class="sxs-lookup"><span data-stu-id="51d35-105">Production control is integrated with features in other modules.</span></span> <span data-ttu-id="51d35-106">Siksi voit muuttaa tuotantotilauksia ja varmistaa, että ne päivitetään automaattisesti järjestelmän kaikissa muissa liittyvissä prosesseissa ja laskutoimituksissa.</span><span class="sxs-lookup"><span data-stu-id="51d35-106">This interconnectivity lets you change production orders and make sure that they are automatically updated in all other related processes and calculations in the system.</span></span> <span data-ttu-id="51d35-107">Seuraavat määritysprosessit käsitellään siinä järjestyksessä, missä ne on tehtävä.</span><span class="sxs-lookup"><span data-stu-id="51d35-107">The following setup processes are listed in the order that you should complete them in.</span></span>

## <a name="required-baseline-setup-in-other-modules"></a><span data-ttu-id="51d35-108">Muiden moduulien pakolliset perusasetukset</span><span class="sxs-lookup"><span data-stu-id="51d35-108">Required baseline setup in other modules</span></span>
<span data-ttu-id="51d35-109">Seuraavat tiedot on määritettävä muissa moduuleissa, ennen kuin voit käyttää tuotannonhallintaa.</span><span class="sxs-lookup"><span data-stu-id="51d35-109">Information in other modules must be set up before you can work with Production control.</span></span> <span data-ttu-id="51d35-110">Nämä asetukset sisältävät seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="51d35-110">This setup includes the following tasks:</span></span>

-   <span data-ttu-id="51d35-111">Määritä yrityksen yleiset tiedot.</span><span class="sxs-lookup"><span data-stu-id="51d35-111">Set up general company information.</span></span>
-   <span data-ttu-id="51d35-112">Määritä kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="51d35-112">Set up the general ledger.</span></span>
-   <span data-ttu-id="51d35-113">Määritä nimikeryhmät.</span><span class="sxs-lookup"><span data-stu-id="51d35-113">Define item groups.</span></span>
-   <span data-ttu-id="51d35-114">Määritä nimikeryhmien kirjanpitotilit.</span><span class="sxs-lookup"><span data-stu-id="51d35-114">Set up ledger accounts for item groups.</span></span>
-   <span data-ttu-id="51d35-115">Määritä varastonimikkeiden taulu inventoinnin- ja varastonhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="51d35-115">Set up the inventory item table in Inventory management.</span></span>
-   <span data-ttu-id="51d35-116">Luo tuoterakenteet ja tuoterakenneversiot inventoinnin- ja varastonhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="51d35-116">Create bills of materials (BOMs) and BOM versions in Inventory management.</span></span>

## <a name="required-calendar-and-resource-setup"></a><span data-ttu-id="51d35-117">Kalenterin ja resurssin pakolliset asetukset</span><span class="sxs-lookup"><span data-stu-id="51d35-117">Required calendar and resource setup</span></span>
<span data-ttu-id="51d35-118">Avaa ennen tuotannonhallinnan käyttöä Organisaation hallinto. Luo ja määritä siellä kalenteri ja operatiiviset resurssit seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="51d35-118">Before you use Production control, open Organization administration, and create and define the calendar and operations resources in the following order:</span></span>

1.  <span data-ttu-id="51d35-119">**Työaikamallit** – määritä tuotannon ajoituksessa käytettävissä olevat ajat määrittämällä työaikamallit.</span><span class="sxs-lookup"><span data-stu-id="51d35-119">**Working time templates** – Set up working time templates to define the times that are available for production scheduling.</span></span>
2.  <span data-ttu-id="51d35-120">**Kalenterit** – määritä tuotannon ajoituksessa käytettävissä olevat päivät määrittämällä työaikakalenterit.</span><span class="sxs-lookup"><span data-stu-id="51d35-120">**Calendars** – Set up working time calendars to define the days of the year that are available for production scheduling.</span></span>
3.  <span data-ttu-id="51d35-121">**Resurssiryhmät** – Ryhmitä operatiiviset resurssit resurssiryhmiksi. Saat tällä tavoin yleiskuvan vapaasta kapasiteetista, kun suoritat aikataulutuksen.</span><span class="sxs-lookup"><span data-stu-id="51d35-121">**Resource groups** – Set up resource groups to group the operations resources, so that you can get an overview of any free capacity when you run scheduling.</span></span> <span data-ttu-id="51d35-122">Resurssiryhmiä ei tarvitse määrittää ennen operatiivisten resurssien määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="51d35-122">You don't have to set up resource groups before you set up operations resources.</span></span> <span data-ttu-id="51d35-123">Resurssien ryhmittäminen on kuitenkin hyvä osata tuotannonhallintaa määritettäessä.</span><span class="sxs-lookup"><span data-stu-id="51d35-123">However, we recommend that you understand how to group resources when you set up Production control.</span></span>
4.  <span data-ttu-id="51d35-124">**Resurssit** – määritä tuotantoprosessin suorittamisessa ja kapasiteettisuunnittelussa käytettävät resurssit määrittämällä operatiiviset resurssit.</span><span class="sxs-lookup"><span data-stu-id="51d35-124">**Resources** – Set up operations resources to define the resources that are used to complete the production process and plan for capacity.</span></span>

## <a name="required-production-parameters-setup"></a><span data-ttu-id="51d35-125">Pakolliset tuotantoparametrien asetukset</span><span class="sxs-lookup"><span data-stu-id="51d35-125">Required production parameters setup</span></span>
<span data-ttu-id="51d35-126">**Tuotannonhallinnan parametrit** – Määritä tuotannon perusparametrit, joiden mukaisesti järjestelmä käsittelee tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="51d35-126">**Production control parameters** – Set up basic production parameters to define how the system handles and processes production orders.</span></span> <span data-ttu-id="51d35-127">Määritä, miten tuotantotilaukset luodaan, arvioidaan, ajoitetaan ja kulutetaan.</span><span class="sxs-lookup"><span data-stu-id="51d35-127">Define how production orders are created, estimated, scheduled, and consumed.</span></span> <span data-ttu-id="51d35-128">Voit myös valita, millaista palautetta haluat ja miten kustannuslaskenta tehdään.</span><span class="sxs-lookup"><span data-stu-id="51d35-128">You can also select what kind of feedback you want and how cost accounting is done.</span></span>

## <a name="required-journal-name-identification"></a><span data-ttu-id="51d35-129">Pakollinen kirjauskansion nimen tunnus</span><span class="sxs-lookup"><span data-stu-id="51d35-129">Required journal name identification</span></span>
<span data-ttu-id="51d35-130">**Tuotantokirjauskansioiden nimet** – Määritä tapahtumien kirjaamiseen käytettyjen tuotantokirjauskansioiden nimet.</span><span class="sxs-lookup"><span data-stu-id="51d35-130">**Production journal names** – Specify the production journal names that are used to record and post transactions.</span></span>

## <a name="setup-if-you-use-operations"></a><span data-ttu-id="51d35-131">Työvaiheita käytettäessä tarvittavat asetukset</span><span class="sxs-lookup"><span data-stu-id="51d35-131">Setup if you use operations</span></span>
<span data-ttu-id="51d35-132">Työvaiheet ilmaisevat tuotteen valmistuksessa suoritettavia tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="51d35-132">Operations represent the specific activities that are completed to produce the finished product.</span></span> <span data-ttu-id="51d35-133">**Huomautus:** Sinun on tiedettävä nimekkeen tuottamisessa tarvittavat tehtävät ja kyseisten tehtävien prioriteetit.</span><span class="sxs-lookup"><span data-stu-id="51d35-133">**Note:** You must know the types of activities that are required in order to produce your item, and the order and priorities of those activities.</span></span> <span data-ttu-id="51d35-134">Lisäksi sinun tiedettävä, mitä resursseja käytetään ja kuinka paljon niitä käytetään.</span><span class="sxs-lookup"><span data-stu-id="51d35-134">You must also know which resources are involved, and how many.</span></span>

1.  <span data-ttu-id="51d35-135">**Työvaiheet** – määritä työvaiheet, jotka ilmaisevat valmiin nimikkeen tuotannossa suoritettavat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="51d35-135">**Operations** – Set up operations to represent the tasks that must be completed to produce the finished item.</span></span>
2.  <span data-ttu-id="51d35-136">**Suhteet** – Muodosta omaisuudet määrittämällä työvaiheiden suhteet.</span><span class="sxs-lookup"><span data-stu-id="51d35-136">**Relations** – Set up operation relations to establish detailed properties.</span></span> <span data-ttu-id="51d35-137">Voit määrittää työvaiheiden suhteet valitsemalla **Työvaiheet**-sivulla **Suhteet**.</span><span class="sxs-lookup"><span data-stu-id="51d35-137">To define operation relations, click **Relations** on the **Operations** page.</span></span>

## <a name="setup-if-you-use-routes"></a><span data-ttu-id="51d35-138">Reitityksiä käytettäessä tarvittavat asetukset</span><span class="sxs-lookup"><span data-stu-id="51d35-138">Setup if you use routes</span></span>
<span data-ttu-id="51d35-139">Jos käytät reitityksiä, jokaiselle tuotantoreititykselle on määritettävä työvaiheet.</span><span class="sxs-lookup"><span data-stu-id="51d35-139">If you're working with routes, operations must be defined for every production route that you set up.</span></span> <span data-ttu-id="51d35-140">Reititys kuvaa, miten nimike etenee työvaiheesta toiseen tuotantoprosessin alusta loppuun.</span><span class="sxs-lookup"><span data-stu-id="51d35-140">The route represents the path that the item takes from operation to operation, from the start of the production process to the end.</span></span>

1.  <span data-ttu-id="51d35-141">**Kustannusluokat** – määritä kustannusluokat, joiden mukaan määritettyjen prosessien tuntikustannukset ja asetusajat muodostuvat.</span><span class="sxs-lookup"><span data-stu-id="51d35-141">**Cost categories** – Set up cost categories to define the cost per hour of specified processes and setup times.</span></span>
2.  <span data-ttu-id="51d35-142">**Kustannusryhmät** – luo ja ylläpidä eri kustannuslaskennan tyyppejä määrittämällä kustannusryhmiä.</span><span class="sxs-lookup"><span data-stu-id="51d35-142">**Cost groups** – Set up cost groups to create and maintain different types of costing.</span></span>
3.  <span data-ttu-id="51d35-143">**Reititysryhmät** – Määritä reititysryhmien avulla reititysten ryhmiin liittyvät parametrit.</span><span class="sxs-lookup"><span data-stu-id="51d35-143">**Route groups** – Set up route groups to define parameters that are related to groups of routes.</span></span> <span data-ttu-id="51d35-144">Reititysryhmät on määritettävä ennen tuotantoreititysten luontia.</span><span class="sxs-lookup"><span data-stu-id="51d35-144">You must set up route groups before you can create production routes.</span></span>
4.  <span data-ttu-id="51d35-145">**Reitit** – määritä ensin tuotantoreititykset ja reitityksen työvaiheiden oletusasetukset, joilla hallitaan ajoitusta, kustannuslaskentaa ja hinnoittelua sekä tilaraporttia.</span><span class="sxs-lookup"><span data-stu-id="51d35-145">**Routes** – Set up production routes, and define default settings to control scheduling, costing, and pricing of route operations, and to control progress reporting.</span></span>
5.  <span data-ttu-id="51d35-146">**Reittiversio** – Ota tuotannon nimikevariaatiot käyttöön määrittämällä reititysversiot.</span><span class="sxs-lookup"><span data-stu-id="51d35-146">**Route version** – Set up route versions to enable item variations in production.</span></span>

## <a name="optional-advanced-settings"></a><span data-ttu-id="51d35-147">Valinnaiset lisäasetukset</span><span class="sxs-lookup"><span data-stu-id="51d35-147">Optional advanced settings</span></span>
1.  <span data-ttu-id="51d35-148">**Tuotantoryhmät** – Määritä tuotantoryhmät luomaan tuotetilausten ja kirjanpitotilien väliset suhteet.</span><span class="sxs-lookup"><span data-stu-id="51d35-148">**Production groups** – Set up production groups to establish relationships between the production order and ledger accounts.</span></span> <span data-ttu-id="51d35-149">Kirjanpitotileillä tilaukset kirjataan tai ryhmitetään raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="51d35-149">The ledger accounts are used to post or group orders for reporting.</span></span>
2.  <span data-ttu-id="51d35-150">**Tuotantopoolit** – luo tuotantopooleja, joilla tuotantotilauksia ryhmitellään kiireellisten tuotantotilausten käsittelyä varten tai tilausryhmien poistamista ja kirjaamista varten.</span><span class="sxs-lookup"><span data-stu-id="51d35-150">**Production pools** – Create production pools to group production orders so that you can process urgent production orders, or delete and post groups of orders.</span></span>
3.  <span data-ttu-id="51d35-151">**Ominaisuudet** – Määritä ominaisuudet luomaan erityismääritteet, jotka resursseille määritettyinä ohjaavat tuotantojen tilausta.</span><span class="sxs-lookup"><span data-stu-id="51d35-151">**Properties** – Define properties to create special attributes that you can assign to your resources to control the order of productions.</span></span> <span data-ttu-id="51d35-152">Nämä määritteet on yhdistetty työaikamalliin.</span><span class="sxs-lookup"><span data-stu-id="51d35-152">These attributes are connected to the working time template.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]