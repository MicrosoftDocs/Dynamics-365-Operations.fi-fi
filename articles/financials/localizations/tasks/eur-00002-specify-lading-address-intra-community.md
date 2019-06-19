---
title: EUR-00002 Rahtiosoitteen määrittäminen yhteisönsisäiselle tapahtumalle
description: Tässä toimintaohjeessa kuvataan, miten määrität kuormausosoitteen yhteisönsisäiselle kauppatapahtumalle.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid,  VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4db22444bee1590770a47ca5946941b530ae85ce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564413"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a><span data-ttu-id="2d598-103">EUR-00002 Rahtiosoitteen määrittäminen yhteisönsisäiselle tapahtumalle</span><span class="sxs-lookup"><span data-stu-id="2d598-103">EUR-00002 Specifying a lading address for an intra-community transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d598-104">Tässä toimintaohjeessa kuvataan, miten määrität kuormausosoitteen yhteisönsisäiselle kauppatapahtumalle.</span><span class="sxs-lookup"><span data-stu-id="2d598-104">This procedure shows how to specify a lading address for an intra-community trade transaction.</span></span> <span data-ttu-id="2d598-105">Esimerkkinä saksalainen yritys tilaa nimikkeitä toimittajalta, jolla on saksalainen osoite.</span><span class="sxs-lookup"><span data-stu-id="2d598-105">For example, a Germany company orders items from a vendor with a German business address.</span></span> <span data-ttu-id="2d598-106">Toimittajalla on varasto Italiassa ja toimittaa nimikkeet sieltä.</span><span class="sxs-lookup"><span data-stu-id="2d598-106">This vendor has a warehouse in Italy and ships the items from there.</span></span> <span data-ttu-id="2d598-107">Tämä toimitus on raportoitava Intrastatiin.</span><span class="sxs-lookup"><span data-stu-id="2d598-107">This delivery must be reported in the Intrastat.</span></span> <span data-ttu-id="2d598-108">Sama menettely koskee asiakaspalautuksia.</span><span class="sxs-lookup"><span data-stu-id="2d598-108">The same behavior is valid for customer returns.</span></span>
<span data-ttu-id="2d598-109">Tämä menettely koskee kaikkia Euroopan maita/alueita.</span><span class="sxs-lookup"><span data-stu-id="2d598-109">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="2d598-110">Tämä tehtävä luotiin käyttämällä demotietojen DEMF-yritystä niin, että yrityksen ensisijainen osoite on Saksassa.</span><span class="sxs-lookup"><span data-stu-id="2d598-110">The task was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="2d598-111">Intrastat-raportointi on määritettävä ennen tämän menettelyn suorittamista.</span><span class="sxs-lookup"><span data-stu-id="2d598-111">Before you can complete this procedure, you must configure Intrastat reporting.</span></span> <span data-ttu-id="2d598-112">Menettely on tarkoitettu kirjanpitäjille.</span><span class="sxs-lookup"><span data-stu-id="2d598-112">This procedure is intended for accountants.</span></span> <span data-ttu-id="2d598-113">Nämä ohjeet koskevat toimintoa, joka lisättiin Dynamics 365 for Operations -versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="2d598-113">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="2d598-114">Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="2d598-114">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="2d598-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2d598-115">Click New.</span></span>
3. <span data-ttu-id="2d598-116">Anna tai valitse arvo</span><span class="sxs-lookup"><span data-stu-id="2d598-116">Enter or select a value</span></span>
    * <span data-ttu-id="2d598-117">Voit valita esimerkiksi arvon DE-001</span><span class="sxs-lookup"><span data-stu-id="2d598-117">For example, select DE-001.</span></span> <span data-ttu-id="2d598-118">Tällä toimittajalla on saksalainen käyntiosoite.</span><span class="sxs-lookup"><span data-stu-id="2d598-118">This vendor has a German business address.</span></span>  
4. <span data-ttu-id="2d598-119">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2d598-119">Click OK.</span></span>
5. <span data-ttu-id="2d598-120">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="2d598-120">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="2d598-121">Syötä tai valitse Nimiketunnus-kentän arvoksi D0001.</span><span class="sxs-lookup"><span data-stu-id="2d598-121">In the Item number field, enter or select a value D0001.</span></span>
7. <span data-ttu-id="2d598-122">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2d598-122">Click Save.</span></span>
8. <span data-ttu-id="2d598-123">Valitse toimintoruudussa Vastaanota.</span><span class="sxs-lookup"><span data-stu-id="2d598-123">On the Action Pane, click Receive.</span></span>
9. <span data-ttu-id="2d598-124">Valitse Kuljetustiedot.</span><span class="sxs-lookup"><span data-stu-id="2d598-124">Click Transportation details.</span></span>
10. <span data-ttu-id="2d598-125">Syötä päivämäärä ja kellonaika Kuormauspäivämäärä ja -aika -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2d598-125">In the Loading date and time field, enter a date and time.</span></span>
11. <span data-ttu-id="2d598-126">Valitse Lisää uusi osoite.</span><span class="sxs-lookup"><span data-stu-id="2d598-126">Click Add address.</span></span>
12. <span data-ttu-id="2d598-127">Valitse Uusi ja luo uusi osoite, jonka tarkoitus on Kuormaus.</span><span class="sxs-lookup"><span data-stu-id="2d598-127">Click New and create new address with purpose Lading.</span></span>
13. <span data-ttu-id="2d598-128">Kirjoita Nimi tai kuvaus -kenttään "italialainen".</span><span class="sxs-lookup"><span data-stu-id="2d598-128">In the Name or description field, type 'Italian'.</span></span>
14. <span data-ttu-id="2d598-129">Valitse arvoksi Kuormaus.</span><span class="sxs-lookup"><span data-stu-id="2d598-129">Select Lading as the value.</span></span>
    * <span data-ttu-id="2d598-130">Huomaa, että osoitteen tarkoituksen tulee olla Kuormaus.</span><span class="sxs-lookup"><span data-stu-id="2d598-130">Note that that address purpose must be Lading.</span></span>  
15. <span data-ttu-id="2d598-131">Syötä tai valitse arvoksi ITA Maa/alue-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2d598-131">In the Country/region field, enter or select a value ITA.</span></span>
16. <span data-ttu-id="2d598-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2d598-132">Click Save.</span></span>
17. <span data-ttu-id="2d598-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2d598-133">Close the page.</span></span>
18. <span data-ttu-id="2d598-134">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="2d598-134">Click Save.</span></span>
    * <span data-ttu-id="2d598-135">Varmista, että kuormausosoite on oikein.</span><span class="sxs-lookup"><span data-stu-id="2d598-135">Verify that the lading address is correct.</span></span>  
19. <span data-ttu-id="2d598-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2d598-136">Close the page.</span></span>
20. <span data-ttu-id="2d598-137">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="2d598-137">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="2d598-138">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="2d598-138">Click Confirm.</span></span>
22. <span data-ttu-id="2d598-139">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="2d598-139">On the Action Pane, click Invoice.</span></span>
23. <span data-ttu-id="2d598-140">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="2d598-140">Click Invoice.</span></span>
24. <span data-ttu-id="2d598-141">Kirjoita arvo Numero-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2d598-141">In the Number field, type a value.</span></span>
25. <span data-ttu-id="2d598-142">Kirjoita päivämäärä Laskun päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2d598-142">In the Invoice date field, enter a date.</span></span>
26. <span data-ttu-id="2d598-143">Valitse Oletusarvo kohteesta: Tuotteen vastaanottomäärä, kun haluat avata valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="2d598-143">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
27. <span data-ttu-id="2d598-144">Valitse "Tilattu määrä" -vaihtoehto Rivien oletusmäärä -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2d598-144">In the Default quantity for lines field, select 'Ordered quantity'.</span></span>
28. <span data-ttu-id="2d598-145">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2d598-145">Click OK.</span></span>
29. <span data-ttu-id="2d598-146">Valitse Kuljetustiedot.</span><span class="sxs-lookup"><span data-stu-id="2d598-146">Click Transportation details.</span></span>
    * <span data-ttu-id="2d598-147">Varmista, että tavarat toimitettiin Italiasta.</span><span class="sxs-lookup"><span data-stu-id="2d598-147">Verify that goods were shipped from Italy.</span></span> <span data-ttu-id="2d598-148">Voit muokata kuormauksen tietoja tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="2d598-148">If necessary, you can edit the lading details.</span></span>  
30. <span data-ttu-id="2d598-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2d598-149">Close the page.</span></span>
31. <span data-ttu-id="2d598-150">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="2d598-150">Click Post.</span></span>
32. <span data-ttu-id="2d598-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2d598-151">Close the page.</span></span>
33. <span data-ttu-id="2d598-152">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="2d598-152">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
34. <span data-ttu-id="2d598-153">Valitse Siirrä.</span><span class="sxs-lookup"><span data-stu-id="2d598-153">Click Transfer.</span></span>
35. <span data-ttu-id="2d598-154">Valitse Toimittajan lasku -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="2d598-154">Select Yes in the Vendor invoice field.</span></span>
36. <span data-ttu-id="2d598-155">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="2d598-155">Click OK.</span></span>
37. <span data-ttu-id="2d598-156">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="2d598-156">Click the General tab.</span></span>
    * <span data-ttu-id="2d598-157">Etsi juuri luotu rivi ja varmista, että lähettäjä toimitti tavarat Italiasta.</span><span class="sxs-lookup"><span data-stu-id="2d598-157">Find a newly created line and verify that the sender shipped the goods from Italy.</span></span>  

