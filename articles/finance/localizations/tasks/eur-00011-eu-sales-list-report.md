---
title: EUR-00011 EU:n myyntiluetteloraportin luominen
description: Tässä menettelyssä käsitellään EU-myyntiluettelon raportin muodostamista.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdedf153ae17ac90032e8998ce3b97ba9b734b64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227978"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a><span data-ttu-id="7c9e8-103">EUR-00011 EU:n myyntiluetteloraportin luominen</span><span class="sxs-lookup"><span data-stu-id="7c9e8-103">EUR-00011 Generate the EU sales list report</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c9e8-104">Tässä menettelyssä käsitellään EU-myyntiluettelon raportin muodostamista.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-104">This procedure walks you through generating the EU sales list report.</span></span> <span data-ttu-id="7c9e8-105">Tällaisia toimintoja ovat yhteisön sisäisen kaupan tapahtumien siirtäminen EU-myyntiluetteloon ja raportin muodostaminen.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-105">This includes transferring intra-community trade transactions to the EU sales list and running the report.</span></span> <span data-ttu-id="7c9e8-106">Menettely sisältää myös yhteisön sisäisen kauppatapahtuman luomisen demokäyttöön.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-106">This procedure also includes creating an intra-community trade transaction for demo purposes.</span></span> <span data-ttu-id="7c9e8-107">Lisätietoja EU:n myyntiluettelon raportoinnista ja edellytyksistä on ohjeissa.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-107">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="7c9e8-108">Tämä menettely koskee kaikkia Euroopan maita/alueita.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-108">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="7c9e8-109">Menettelyssä on käytetty DEMF-yrityksen demotietoja ja Saksaa esimerkkinä kotimaasta tai -alueesta.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-109">The procedure was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="7c9e8-110">Menettelyssä käytetään myös Portugalia esimerkkinä EU-maasta tai -alueesta.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-110">The procedure also uses Portugal as an exemplar EU country/region.</span></span> <span data-ttu-id="7c9e8-111">EU-myyntiluettelon raportointi on määritettävä ennen tämän menettelyn suorittamista.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-111">Before you can complete this procedure, you must configure EU sales list reporting.</span></span>

<span data-ttu-id="7c9e8-112">Menettely on tarkoitettu kirjanpitäjille.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-112">This procedure is intended for accountants.</span></span>


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a><span data-ttu-id="7c9e8-113">Luo yhteisön sisäinen myyntitapahtuma demokäyttöä varten</span><span class="sxs-lookup"><span data-stu-id="7c9e8-113">Create an intra-community sales transaction for demo purposes</span></span>
1. <span data-ttu-id="7c9e8-114">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-114">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="7c9e8-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-115">Click New.</span></span>
3. <span data-ttu-id="7c9e8-116">Kirjoita Asiakastili-kenttään PRT-001.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-116">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="7c9e8-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-117">Click OK.</span></span>
5. <span data-ttu-id="7c9e8-118">Kirjoita Nimiketunnus-kenttään D0001.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-118">In the Item number field, type 'D0001'.</span></span>
6. <span data-ttu-id="7c9e8-119">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-119">Expand the Line details section.</span></span>
7. <span data-ttu-id="7c9e8-120">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-120">Click the Setup tab.</span></span>
8. <span data-ttu-id="7c9e8-121">Kirjoita Nimikkeen arvonlisäveroryhmä -kenttään FULL.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-121">In the Item sales tax group field, type 'FULL'.</span></span>
9. <span data-ttu-id="7c9e8-122">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-122">Click Add line.</span></span>
10. <span data-ttu-id="7c9e8-123">Kirjoita Nimiketunnus-kenttään D0003.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-123">In the Item number field, type 'D0003'.</span></span>
11. <span data-ttu-id="7c9e8-124">Kirjoita Nimikkeen arvonlisäveroryhmä -kenttään RED.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-124">In the Item sales tax group field, type 'RED'.</span></span>
12. <span data-ttu-id="7c9e8-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-125">Click Save.</span></span>
13. <span data-ttu-id="7c9e8-126">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-126">On the Action Pane, click Invoice.</span></span>
14. <span data-ttu-id="7c9e8-127">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-127">Click Invoice.</span></span>
15. <span data-ttu-id="7c9e8-128">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-128">Expand the Parameters section.</span></span>
16. <span data-ttu-id="7c9e8-129">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-129">In the Quantity field, select 'All'.</span></span>
17. <span data-ttu-id="7c9e8-130">Laajenna osa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-130">Expand the Setup section.</span></span>
18. <span data-ttu-id="7c9e8-131">Lisää Laskun päivämäärä -kenttään päivämäärä 11.1.2016.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-131">In the Invoice date field, set the date to '01/11/2016'.</span></span>
19. <span data-ttu-id="7c9e8-132">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-132">Click OK.</span></span>
20. <span data-ttu-id="7c9e8-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-133">Click OK.</span></span>

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a><span data-ttu-id="7c9e8-134">Siirrä yhteisön sisäisen kaupan tapahtumat EU-myyntiluetteloon</span><span class="sxs-lookup"><span data-stu-id="7c9e8-134">Transfer intra-community trade transactions to the EU sales list</span></span>
1. <span data-ttu-id="7c9e8-135">Valitse Vero > Ilmoitukset > Ulkomaankauppa > EU-myyntiluettelo.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-135">Go to Tax > Declarations > Foreign trade > EU sales list.</span></span>
2. <span data-ttu-id="7c9e8-136">Valitse Siirrä.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-136">Click Transfer.</span></span>
3. <span data-ttu-id="7c9e8-137">Siirrä nimiketapahtumat valitsemalla Nimike-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-137">Select Yes in the Item field to transfer item transactions.</span></span>
4. <span data-ttu-id="7c9e8-138">Siirrä palvelutapahtumat valitsemalla Palvelu-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-138">Select Yes in the Service field to transfer service transactions.</span></span>
    * <span data-ttu-id="7c9e8-139">Voit myös määrittää lisäsuodattimia siirrettäville yhteisön sisäisen kaupan tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-139">You can also specify additional filters on intra-community trade transactions to transfer.</span></span>  
5. <span data-ttu-id="7c9e8-140">Valitse Siirrä.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-140">Click Transfer.</span></span>
    * <span data-ttu-id="7c9e8-141">Tarkista, että yhteisön sisäiset myyntitapahtumat on siirretty EU-myyntiluetteloon.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-141">Verify that the intra-community sales transaction is successfully transferred to the EU sales list.</span></span>  

## <a name="generate-the-eu-sales-list-report"></a><span data-ttu-id="7c9e8-142"> EU-myyntiluettelon raportin luominen</span><span class="sxs-lookup"><span data-stu-id="7c9e8-142">Generate the EU sales list report</span></span>
1. <span data-ttu-id="7c9e8-143">Valitse Raportointi.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-143">Click Reporting.</span></span>
2. <span data-ttu-id="7c9e8-144">Valitse Raportointikausi-kentässä Kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-144">In the Reporting period field, select 'Monthly'.</span></span>
3. <span data-ttu-id="7c9e8-145">Lisää Päivämäärästä-kenttään päivämäärä 1.1.2016.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-145">In the From date field, set the date to '01/01/2016'.</span></span>
4. <span data-ttu-id="7c9e8-146">Valitse Luo tiedosto -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-146">Select Yes in the Generate file field.</span></span>
5. <span data-ttu-id="7c9e8-147">Valitse Luo raportti -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-147">Select Yes in the Generate report field.</span></span>
6. <span data-ttu-id="7c9e8-148">Kirjoita Tiedostonimi-kenttään EUSalesList.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-148">In the File name field, type 'EUSalesList'.</span></span>
7. <span data-ttu-id="7c9e8-149">Kirjoita Raporttitiedoston nimi -kenttään EUSalesList.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-149">In the Report file name field, type 'EUSalesList'.</span></span>
8. <span data-ttu-id="7c9e8-150">Kirjoita EU-myyntiluettelon rekisteröintitunnus -kenttään 123.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-150">In the EU Sales List Registration ID field, type '123'.</span></span>
    * <span data-ttu-id="7c9e8-151">Tämä kenttä on käytettävissä vain Saksassa.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-151">This field is only available for Germany.</span></span>  
    * <span data-ttu-id="7c9e8-152">Voit myös määrittää lisäsuodattimia raporttiin sisällytettäville yhteisön sisäisen kaupan tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-152">You can also specify additional filters on intra-community trade transactions to include in the report.</span></span>  
9. <span data-ttu-id="7c9e8-153">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-153">Click OK.</span></span>
    * <span data-ttu-id="7c9e8-154">Tarkista, että avautuvassa ponnahdusikkunassa varmistetaan tiedoston ja valvontaraportin latautuminen.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-154">Verify that pop-up windows appear to confirm that the file and the control report are being downloaded.</span></span>  

## <a name="mark-eu-sales-list-lines-as-reported"></a><span data-ttu-id="7c9e8-155">Merkitse EU-myyntiluettelon rivien tilaksi Raportoitu</span><span class="sxs-lookup"><span data-stu-id="7c9e8-155">Mark EU sales list lines as Reported</span></span>
1. <span data-ttu-id="7c9e8-156">Valitse Merkitse.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-156">Click Mark.</span></span>
2. <span data-ttu-id="7c9e8-157">Valitse Merkitse raportoiduksi.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-157">Click Mark as reported.</span></span>
3. <span data-ttu-id="7c9e8-158">Valitse luettelosta Laskun päivämäärä -kentän rivi.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-158">In the list, select the row for the Invoice date field.</span></span>
4. <span data-ttu-id="7c9e8-159">Kirjoita Ehdot-kenttään 01/01/2016..01/31/2016.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-159">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="7c9e8-160">Valitse luettelosta Raportoinnin tila -kentän rivi.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-160">In the list, select the row for the Reporting status field.</span></span>
6. <span data-ttu-id="7c9e8-161">Valitse Ehdot-kentässä Sisällytetty.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-161">In the Criteria field, select 'Included'.</span></span>
    * <span data-ttu-id="7c9e8-162">Voit myös määrittää lisäsuodattimia raportoiduiksi merkittäville yhteisön sisäisen kaupan tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-162">You can also specify additional filters on intra-community trade transactions to mark as Reported.</span></span>  
7. <span data-ttu-id="7c9e8-163">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-163">Click OK.</span></span>
8. <span data-ttu-id="7c9e8-164">Valitse Valinta-kentässä Raportoitu.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-164">In the Selection field, select 'Reported'.</span></span>

## <a name="mark-eu-sales-list-lines-as-closed"></a><span data-ttu-id="7c9e8-165">Merkitse EU-myyntiluettelon rivien tilaksi Suljettu</span><span class="sxs-lookup"><span data-stu-id="7c9e8-165">Mark EU sales list lines as Closed</span></span>
1. <span data-ttu-id="7c9e8-166">Valitse Merkitse.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-166">Click Mark.</span></span>
2. <span data-ttu-id="7c9e8-167">Valitse Merkitse suljetuksi.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-167">Click Mark as closed.</span></span>
3. <span data-ttu-id="7c9e8-168">Merkitse luettelossa Laskun päivämäärä -kentän rivi.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-168">In the list, mark the row for the Invoice date field.</span></span>
4. <span data-ttu-id="7c9e8-169">Kirjoita Ehdot-kenttään 01/01/2016..01/31/2016.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-169">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="7c9e8-170">Merkitse luettelossa Raportoinnin tila -kentän rivi.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-170">In the list, mark the row for the Reporting status field.</span></span>
6. <span data-ttu-id="7c9e8-171">Valitse Ehdot-kentässä Raportoitu.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-171">In the Criteria field, select 'Reported'.</span></span>
    * <span data-ttu-id="7c9e8-172">Voit myös määrittää lisäsuodattimia suljetuiksi merkittäville yhteisön sisäisen kaupan tapahtumille.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-172">You can also specify additional filters on intra-community trade transactions to mark as Closed.</span></span>  
7. <span data-ttu-id="7c9e8-173">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-173">Click OK.</span></span>
8. <span data-ttu-id="7c9e8-174">Valitse Valinta-kentässä Suljettu.</span><span class="sxs-lookup"><span data-stu-id="7c9e8-174">In the Selection field, select 'Closed'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]