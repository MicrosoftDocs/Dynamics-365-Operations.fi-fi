--- 
title: Toimittajan maksun yleiskatsaus
description: "Tässä tehtävän ohjauksessa kerrotaan toimittajan maksujen luomisessa käytettävistä eri tavoista. Niitä ovat esimerkiksi maksuehdotuksen käyttäminen ja kertaluontoisen maksun syöttäminen."
author: kweekley
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: e9a94231f755ff23bb442d62e90daff8f2d1f4fb
ms.contentlocale: fi-fi
ms.lasthandoff: 10/30/2017

---
# <a name="vendor-payment-overview"></a><span data-ttu-id="63e72-103">Toimittajan maksun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="63e72-103">Vendor payment overview</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63e72-104">Tässä tehtävän ohjauksessa kerrotaan toimittajan maksujen luomisessa käytettävistä eri tavoista. Niitä ovat esimerkiksi maksuehdotuksen käyttäminen ja kertaluontoisen maksun syöttäminen.</span><span class="sxs-lookup"><span data-stu-id="63e72-104">This task guide will walk you through various methods used to create vendor payments, including how to use a payment proposal or manually entering a one-off payment.</span></span> <span data-ttu-id="63e72-105">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="63e72-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="63e72-106">Siirry kohtaan Ostoreskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="63e72-106">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="63e72-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="63e72-107">Click New.</span></span>
3. <span data-ttu-id="63e72-108">Valitse maksukirjauskansio, jonne toimittajan maksut tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="63e72-108">Select the payment journal in which to save the vendor payments.</span></span> 
4. <span data-ttu-id="63e72-109">Valitse kirjauskansio tai syötä se manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="63e72-109">Select the journal or manually enter it.</span></span>
5. <span data-ttu-id="63e72-110">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="63e72-110">Click Lines.</span></span>
6. <span data-ttu-id="63e72-111">Valitse Maksuehdotus.</span><span class="sxs-lookup"><span data-stu-id="63e72-111">Click Payment proposal.</span></span>
7. <span data-ttu-id="63e72-112">Valitse Luo maksuehdotus.</span><span class="sxs-lookup"><span data-stu-id="63e72-112">Click Create payment proposal.</span></span>
    * <span data-ttu-id="63e72-113">Maksuehdotus on kysely, jota käytetään maksun laskujen valitsemisessa.</span><span class="sxs-lookup"><span data-stu-id="63e72-113">The payment proposal is a query used to select invoices for payment.</span></span> <span data-ttu-id="63e72-114">Voit muokata maksettavien laskujen luetteloa ennen toimittajan maksujen luomista.</span><span class="sxs-lookup"><span data-stu-id="63e72-114">You can edit the list of invoices to pay before creating or generating the vendor payments.</span></span>  
8. <span data-ttu-id="63e72-115">Valitse laskut maksua varten eräpäivän, käteisalennuksen tai molempien avulla.</span><span class="sxs-lookup"><span data-stu-id="63e72-115">Select invoices for payment by due date, cash discount, or both.</span></span> 
9. <span data-ttu-id="63e72-116">Syötä päivämäärä eräpäivän tai käteisalennuksen vertailua varten.</span><span class="sxs-lookup"><span data-stu-id="63e72-116">Enter the date for comparing to the due date or cash discount.</span></span> 
10. <span data-ttu-id="63e72-117">Valinnainen: Syötä kaikissa maksuissa käytettävä maksupäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="63e72-117">Optional: Enter a payment date used for all payments.</span></span>
    * <span data-ttu-id="63e72-118">Tähän syötetty päivämäärä on kaikkien luotujen maksujen maksupäivä eräpäivästä tai käteisalennuksen päivästä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="63e72-118">The date entered here will be the payment date for all payments created, regardless of the due date or cash discount date.</span></span>  
11. <span data-ttu-id="63e72-119">Valinnainen: Syötä aikaisin mahdollinen maksupäivä.</span><span class="sxs-lookup"><span data-stu-id="63e72-119">Optional: Enter a minimum payment date which may be used as the payment date.</span></span>
    * <span data-ttu-id="63e72-120">Aikaisin maksupäivä on aikaisin päivä, jolloin maksuja luotiin.</span><span class="sxs-lookup"><span data-stu-id="63e72-120">The minimum payment date will be the earliest date used when creating payments.</span></span> <span data-ttu-id="63e72-121">Jos esimerkiksi laskun eräpäivä on aikaisimman maksupäivän jälkeen, eräpäiväksi tulee maksupäivä aikaisimman maksupäivän sijaan, jotta laskun voi maksaa mahdollisimman myöhään.</span><span class="sxs-lookup"><span data-stu-id="63e72-121">For example, if an invoice has a due date after the minimum payment date, the due date will become the payment date instead of the minimum payment date in order to pay the invoice on the latest possible date.</span></span>  
12. <span data-ttu-id="63e72-122">Syötä Sisällytettävät tietueet -kohtaan kyselyn lisärajoitukset.</span><span class="sxs-lookup"><span data-stu-id="63e72-122">Enter additional query restrictions under Records to include.</span></span>
    * <span data-ttu-id="63e72-123">Suodattimen avulla voi rajata maksua varten valittuja laskuja toimittajaryhmän tai maksutavan perusteella.</span><span class="sxs-lookup"><span data-stu-id="63e72-123">The filter is often used to restrict the invoices selected for payment by vendor group or method of payment.</span></span> <span data-ttu-id="63e72-124">Voit lisätä esimerkiksi suodattimen, jos haluat maksaa laskut vain sekkimaksuna tässä maksuajossa.</span><span class="sxs-lookup"><span data-stu-id="63e72-124">For example, you may add a filter to only pay invoices by check in this pay run.</span></span>  
13. <span data-ttu-id="63e72-125">Syötä kyselyn lisärajoitukset tai maksun oletusarvot.</span><span class="sxs-lookup"><span data-stu-id="63e72-125">Enter additional query restriction or payment defaults.</span></span> 
    * <span data-ttu-id="63e72-126">Lisäparametrien avulla voi määrittää maksun valuutan tai tämän maksuajon keskitetyt maksut.</span><span class="sxs-lookup"><span data-stu-id="63e72-126">The additional parameters can be used to define the payment currency or to enable centralized payments for this pay run.</span></span>  
14. <span data-ttu-id="63e72-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="63e72-127">Click OK.</span></span>
    * <span data-ttu-id="63e72-128">Kun olet valinnut OK, näkyviin tulevat kyselyn tulokset.</span><span class="sxs-lookup"><span data-stu-id="63e72-128">After clicking OK, the results of the query will appear.</span></span> <span data-ttu-id="63e72-129">Jos et halua esikatsella maksettavien laskujen luetteloa, voit siirtyä takaisin Parametrit-pikavälilehteen ja muuttaa Luo maksut ilman laskun esikatselua -kohdan asetukseksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="63e72-129">If you don't want to preview the list of invoices selected to pay, you can go back to the Parameters fast tab and change the setting Create payments without invoice preview = Yes.</span></span>  
15. <span data-ttu-id="63e72-130">Valitse Näytä maksun yleiskatsaus -painike, kun haluat tarkastella toimittajalle valitusta laskusta luotavia maksuja.</span><span class="sxs-lookup"><span data-stu-id="63e72-130">Choose the Show payment overview button to view the payments that will be created for the vendor on the invoice selected.</span></span>
16. <span data-ttu-id="63e72-131">Valitse Piilota maksun yleiskatsaus -painike, kun haluat piilottaa maksut.</span><span class="sxs-lookup"><span data-stu-id="63e72-131">Choose the Hide payment overview button to hide the payments.</span></span> 
17. <span data-ttu-id="63e72-132">Valitse Luo maksut.</span><span class="sxs-lookup"><span data-stu-id="63e72-132">Click Create payments.</span></span>
    * <span data-ttu-id="63e72-133">Napsauta ruudukkoa hiiren kakkospainikkeella ja tuo laskuluettelo Exceliin, ennen kuin valitset Luo maksut -painikkeen.</span><span class="sxs-lookup"><span data-stu-id="63e72-133">Before choosing Create payments, you can right click on the grid and export the list of invoices to Excel.</span></span> <span data-ttu-id="63e72-134">Luo maksut -painike luo toimittajan maksut maksukirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="63e72-134">The Create payments button will create the vendor payments in the payment journal.</span></span>  
18. <span data-ttu-id="63e72-135">Skannaa maksut ja varmista, että kaikille maksuille on määritetty maksutapa.</span><span class="sxs-lookup"><span data-stu-id="63e72-135">Scan your payments and make sure the method of payment is defined for all payments.</span></span> 
    * <span data-ttu-id="63e72-136">Jos luotavana on maksuja, kuten sekin tulostaminen tai sähköisen maksun luominen, maksutapa on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="63e72-136">If you generate the payments, such as printing a check or creating an electronic payment, the method of payment must be defined.</span></span> <span data-ttu-id="63e72-137">Maksutavan oletusarvo saadaan pankkitilistä, jolle maksu tehdään.</span><span class="sxs-lookup"><span data-stu-id="63e72-137">The method of payment will also default the bank account from the payment will be made.</span></span>  
19. <span data-ttu-id="63e72-138">Luo kertaluonteinen maksu valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="63e72-138">Click New to create a one-off payment.</span></span>
    * <span data-ttu-id="63e72-139">Kertaluonteinen maksu voidaan lisätä maksukirjauskansioon milloin tahansa ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="63e72-139">A one-off payment can be added to a payment journal at any time prior to posting.</span></span> <span data-ttu-id="63e72-140">Tämä tehdään valitsemalla Uusi-painike ja lisäämällä maksun tiedot manuaalisesti mieluummin kuin maksuehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="63e72-140">This is done by clicking the New button and adding the payment information manually, rather than using the Payment proposal.</span></span>  
20. <span data-ttu-id="63e72-141">Valitse toimittaja, jolle maksu tehdään.</span><span class="sxs-lookup"><span data-stu-id="63e72-141">Select the vendor to whom the payment will be made.</span></span>
21. <span data-ttu-id="63e72-142">Jos maksettava lasku on olemassa, valitse maksun lasku valitsemalla Selvitä tapahtumat -kohta.</span><span class="sxs-lookup"><span data-stu-id="63e72-142">If an invoice exists to pay, select Settle transactions to select the invoice for payment.</span></span>
    * <span data-ttu-id="63e72-143">Jos tämä on ennakkomaksu, vaihe on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="63e72-143">If this is a prepayment, this step is optional.</span></span> <span data-ttu-id="63e72-144">Voit luoda maksun valitsemalla ainoatakaan laskua.</span><span class="sxs-lookup"><span data-stu-id="63e72-144">You can create the payment without selecting any invoice.</span></span>  
22. <span data-ttu-id="63e72-145">Merkitse kaikki maksettavat laskut.</span><span class="sxs-lookup"><span data-stu-id="63e72-145">Mark any invoices that will be paid.</span></span>
    * <span data-ttu-id="63e72-146">Jos valitset maksun laskut Selvitä tapahtumat -kohdan avulla, maksusumma lasketaan automaattisesti maksua varten merkittyjen laskujen ja Täsmäytettävä summa -kohtaan syötetyn summan perusteella.</span><span class="sxs-lookup"><span data-stu-id="63e72-146">If you use the Settle transactions to select the invoices for payment, the payment amount will automatically be calculated based on what invoices you mark for payment, and what amount you enter in the Amount to settle.</span></span>  
23. <span data-ttu-id="63e72-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="63e72-147">Click OK.</span></span>
24. <span data-ttu-id="63e72-148">Jos haluat poistaa maksun, merkitse rivi.</span><span class="sxs-lookup"><span data-stu-id="63e72-148">If you want to delete a payment, mark the row.</span></span>
25. <span data-ttu-id="63e72-149">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="63e72-149">Click Delete.</span></span>
    * <span data-ttu-id="63e72-150">Maksun poistaminen poistaa vain maksun.</span><span class="sxs-lookup"><span data-stu-id="63e72-150">Deleting a payment will only delete the payment.</span></span> <span data-ttu-id="63e72-151">Maksua varten merkityt laskut ovat yhä käytettävissä toisessa maksussa maksamista varten.</span><span class="sxs-lookup"><span data-stu-id="63e72-151">Any invoices marked for payment will still be available to be paid by another payment.</span></span>  
26. <span data-ttu-id="63e72-152">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="63e72-152">Click Yes.</span></span>
27. <span data-ttu-id="63e72-153">Valitse Luo maksu, kun haluat tulostaa sekkejä tai luoda sähköisen maksutiedoston.</span><span class="sxs-lookup"><span data-stu-id="63e72-153">Choose Generate payment to print Checks or create the electronic payment file.</span></span>
28. <span data-ttu-id="63e72-154">Valitse luotava maksutapa.</span><span class="sxs-lookup"><span data-stu-id="63e72-154">Select the method of payment that you want to generate.</span></span>
    * <span data-ttu-id="63e72-155">Maksukirjauskansio voi sisältää sekä sekkimaksuja että sähköisiä maksuja. Siellä voi kuitenkin luoda vain yhden maksutyypin kerralla.</span><span class="sxs-lookup"><span data-stu-id="63e72-155">The payment journal can contain payments for both Checks and electronic payments, but you can only generate one payment type at a time.</span></span>  
29. <span data-ttu-id="63e72-156">Valitse pankkitili, jolta maksut luodaan.</span><span class="sxs-lookup"><span data-stu-id="63e72-156">Select the bank account from which to generate the payments.</span></span>
30. <span data-ttu-id="63e72-157">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="63e72-157">Click OK.</span></span>
    * <span data-ttu-id="63e72-158">Maksut luodaan vain valittua maksutapaa ja pankkitiliä vastaaville maksuille.</span><span class="sxs-lookup"><span data-stu-id="63e72-158">Payments will only be generated for payments that match the Method of payment and Bank account you selected.</span></span>  
31. <span data-ttu-id="63e72-159">Jos olet luomassa sekkejä, valitse Asiakirja, jolloin sekeille valitaan oikea tulostuskohde.</span><span class="sxs-lookup"><span data-stu-id="63e72-159">If you are generating Checks, choose Document to ensure the correct print destination for the Checks.</span></span>
32. <span data-ttu-id="63e72-160">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="63e72-160">Click OK.</span></span>
33. <span data-ttu-id="63e72-161">Luo maksut valitsemalla OK.</span><span class="sxs-lookup"><span data-stu-id="63e72-161">Click OK to generate the payments.</span></span>
34. <span data-ttu-id="63e72-162">Valitse Kirjaa, jos kaikki maksut on hyväksytty ja luotu.</span><span class="sxs-lookup"><span data-stu-id="63e72-162">Click Post if all the payments are approved and generated.</span></span> 


