---
title: Takuukirje
description: "Tässä artikkelissa on tietoja takausasiakirjoista. Takausasiakirjan avulla pankki suostuu maksamaan tietyn summan henkilölle, jos pankin asiakas laiminlyö maksun tai sitoumuksen suorittamisen saajalle."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankLGGuarantee
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 18291
ms.assetid: 5c0b5e37-d51d-4a01-bb37-1882173abb9f
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: d7144a979b98b3dbd2052661945e6d4fe22220a7
ms.contentlocale: fi-fi
ms.lasthandoff: 08/09/2017

---

# <a name="letters-of-guarantee"></a><span data-ttu-id="b9c4e-104">Takuukirje</span><span class="sxs-lookup"><span data-stu-id="b9c4e-104">Letters of guarantee</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b9c4e-105">Tässä artikkelissa on tietoja takausasiakirjoista.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-105">This article provides information about letters of guarantee.</span></span> <span data-ttu-id="b9c4e-106">Takausasiakirjan avulla pankki suostuu maksamaan tietyn summan henkilölle, jos pankin asiakas laiminlyö maksun tai sitoumuksen suorittamisen saajalle.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-106">In a letter of guarantee, a bank agrees to pay a specific amount of money to a person if one of the bank's customers defaults on a payment or obligation to that person.</span></span> 

<span data-ttu-id="b9c4e-107">Takauskirja on pankin (takaaja) keino maksaa sovittu rahasumma toiselle henkilölle (saaja), jos pankin asiakas (päävelallinen) laiminlyö maksun tai sitoumuksen suorittamisen saajalle.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-107">A letter of guarantee is an agreement by a bank (the guarantor) to pay a set amount of money to some person (the beneficiary) if a bank customer (the principal) defaults on a payment or an obligation to the beneficiary.</span></span> <span data-ttu-id="b9c4e-108">Takauskirjoja ei voi siirtää.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-108">Letters of guarantee aren't transferable.</span></span> <span data-ttu-id="b9c4e-109">Ne koskevat ainoastaan sopimuksessa mainittua edunsaajaa.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-109">They apply only to the beneficiary who is named in the agreement.</span></span> <span data-ttu-id="b9c4e-110">Päävelallinen voi pyytää takausasiakirjan arvon suurentamista tai pienentämistä sopimuksen ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-110">The principal can request an increase or decrease in the value of a letter of guarantee, subject to the terms of the agreement.</span></span> 

<span data-ttu-id="b9c4e-111">Jos edunsaaja haluaa realisoida takauskirjan, hänen on lähetettävä alkuperäinen takausasiakirja ja ilmoitettava pankille päämiehen maksukyvyttömyydestä ennen erääntymispäivää.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-111">To liquidate a letter of guarantee, the beneficiary must submit the original letter of guarantee and inform the bank of the principal’s default before the expiration date.</span></span> <span data-ttu-id="b9c4e-112">Pankki maksaa sitten edunsaajan tilille erääntyvän summan takauskirjan ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-112">The bank then pays the amount that is due to the beneficiary's account, according to the terms in the letter of guarantee.</span></span> <span data-ttu-id="b9c4e-113">Pankki ottaa maksusta prosenttiosuuden katteena.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-113">The bank reserves a percentage of the payment as a margin.</span></span> <span data-ttu-id="b9c4e-114">Prosenttiosuus sovitaan ja määritetään sopimuksen ehdoissa.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-114">The percentage is agreed upon and specified in the terms of the agreement.</span></span> 

<span data-ttu-id="b9c4e-115">Voit luoda takauskirjan tarkoitusta seuraavan koodin.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-115">You can create a code to track the purpose of a letter of guarantee.</span></span> <span data-ttu-id="b9c4e-116">Voit myös määrittää syyt, jotka liitetään takauskirjaan sen peruutuksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-116">You can also specify the reasons that can be associated with a letter of guarantee when the letter is canceled.</span></span> <span data-ttu-id="b9c4e-117">Voit tarkastella tarkoituskoodeja ja pankin syitä **Maksun tarkoituskoodit**- ja **Pankin syyt** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-117">You can view the purpose codes and bank reasons on the **Payment purpose codes** and **Bank reasons** pages.</span></span> 

<span data-ttu-id="b9c4e-118">**Takausasiakirja**-sivulla voit suorittaa seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="b9c4e-118">You can use the **Letter of guarantee** page to complete these tasks:</span></span>

-   <span data-ttu-id="b9c4e-119">Luo oikeat kirjanpitomerkinnät ja poista manuaalinen merkintä.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-119">Create correct ledger entries, and eliminate manual entry.</span></span>
-   <span data-ttu-id="b9c4e-120">Kirjaa kaikki raha- ja tietotapahtumat ja seuraa takausasiakirjojen saldoja.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-120">Record all monetary and nonmonetary transactions, and track balances of letters of guarantee.</span></span>
-   <span data-ttu-id="b9c4e-121">Kirjaa takausasiakirjojen tilat ja vanheneminen ja seuraa niitä.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-121">Record and track the status and expiration of letters of guarantee.</span></span>
-   <span data-ttu-id="b9c4e-122">Luo raportti, joka sisältää takausasiakirjat säilyttävien pankkien luettelon.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-122">Generate a report that lists the banks that are holding letters of guarantee.</span></span>

<span data-ttu-id="b9c4e-123">Seuraava taulukko sisältää toiminnot, jotka takausasiakirjalle voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-123">The following table describes the actions that you can perform on a letter of guarantee.</span></span>

| <span data-ttu-id="b9c4e-124">Toiminto</span><span class="sxs-lookup"><span data-stu-id="b9c4e-124">Action</span></span>              | <span data-ttu-id="b9c4e-125">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="b9c4e-125">Purpose</span></span>                                                                                                                   |
|---------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c4e-126">Lähetä pankille</span><span class="sxs-lookup"><span data-stu-id="b9c4e-126">Submit to bank</span></span>      | <span data-ttu-id="b9c4e-127">Lähetä pankille takausasiakirjapyyntö</span><span class="sxs-lookup"><span data-stu-id="b9c4e-127">Submit the letter of guarantee request to the bank.</span></span>                                                                       |
| <span data-ttu-id="b9c4e-128">Vastaanota pankilta</span><span class="sxs-lookup"><span data-stu-id="b9c4e-128">Receive from bank</span></span>   | <span data-ttu-id="b9c4e-129">Kun pankki hyväksyy lähetetyn pyynnön, voit noutaa takausasiakirjan pankista.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-129">After the bank agrees to the submitted request, collect the letter of guarantee from the bank.</span></span>                            |
| <span data-ttu-id="b9c4e-130">Anna edunsaajalle</span><span class="sxs-lookup"><span data-stu-id="b9c4e-130">Give to beneficiary</span></span> | <span data-ttu-id="b9c4e-131">Kun saat takausasiakirjan pankista, anna se edunsaajalle.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-131">After you receive the letter of guarantee from the bank, provide the letter of guarantee to the beneficiary.</span></span>              |
| <span data-ttu-id="b9c4e-132">Kasvata arvoa</span><span class="sxs-lookup"><span data-stu-id="b9c4e-132">Increase value</span></span>      | <span data-ttu-id="b9c4e-133">Edunsaajan ja päävelallisen suostumuksella voit suurentaa rahamääräistä arvoa.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-133">If the beneficiary and the principal agree, increase the monetary value.</span></span>                                                  |
| <span data-ttu-id="b9c4e-134">Pienennä arvoa</span><span class="sxs-lookup"><span data-stu-id="b9c4e-134">Decrease value</span></span>      | <span data-ttu-id="b9c4e-135">Edunsaajan ja päävelallisen suostumuksella voit pienentää rahamääräistä arvoa.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-135">If the beneficiary and the principal agree, decrease the monetary value.</span></span>                                                  |
| <span data-ttu-id="b9c4e-136">Laajenna</span><span class="sxs-lookup"><span data-stu-id="b9c4e-136">Extend</span></span>              | <span data-ttu-id="b9c4e-137">Kun takausasiakirja on annettu edunsaajalle, voit pidentää voimassaoloaikaa, jos pidennys on mahdollinen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-137">After you provide the letter of guarantee to the beneficiary, extend the period of validity, if an extension is required.</span></span> |
| <span data-ttu-id="b9c4e-138">Peruuta</span><span class="sxs-lookup"><span data-stu-id="b9c4e-138">Cancel</span></span>              | <span data-ttu-id="b9c4e-139">Kun tarkoitusta, johon takausasiakirja pyydettiin, ei enää ole, voit peruuttaa sopimuksen.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-139">When the purpose that the letter of guarantee was requested for no longer applies, cancel the agreement.</span></span>                  |
| <span data-ttu-id="b9c4e-140">Realisoi</span><span class="sxs-lookup"><span data-stu-id="b9c4e-140">Liquidate</span></span>           | <span data-ttu-id="b9c4e-141">Kun edunsaaja esittää takausasiakirjan pankille, takausasiakirja maksetaan käteisellä.</span><span class="sxs-lookup"><span data-stu-id="b9c4e-141">When the beneficiary presents the letter of guarantee to the bank, cash out the letter of guarantee.</span></span>                      |


<span data-ttu-id="b9c4e-142">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="b9c4e-142">For more information, see the following topics:</span></span>

[<span data-ttu-id="b9c4e-143">Takausasiakirjan tapahtuma</span><span class="sxs-lookup"><span data-stu-id="b9c4e-143">Letter of guarantee transaction</span></span>](tasks/letter-guarantee-transaction.md)

[<span data-ttu-id="b9c4e-144">Määritä pankin limiitit ja kirjausprofiilit takauskirjoja varten</span><span class="sxs-lookup"><span data-stu-id="b9c4e-144">Set up bank facilities and posting profiles for letters of guarantee</span></span>](tasks/set-up-bank-facilities-posting-profiles.md)



