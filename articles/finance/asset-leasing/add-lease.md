---
title: Vuokrasopimuksen lisääminen tai kopioiminen (esiversio)
description: Tässä aiheessa kuvataan, miten uusi vuokrasopimus luodaan antamalla sille tietoja resurssin vuokrauksesta tai kopioimalla tiedot olemassa olevasta vuokrasopimuksesta.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 325a1b7948f3cb8033fa93b7c36f1f1f6b7dbb27
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220008"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="f4f5a-103">Vuokrasopimuksen lisääminen tai kopioiminen (esiversio)</span><span class="sxs-lookup"><span data-stu-id="f4f5a-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4f5a-104">Tässä ohjeaiheessa kerrotaan, miten vuokrasopimus luodaan alusta alkaen resurssin vuokrauksessa ja miten vuokrasopimus luodaan kopioimalla olemassa oleva vuokrasopimus.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="f4f5a-105">Vuokrasopimuksen luontiprosessi alusta alkaen sisältää uuden vuokrasopimuksen tietojen syöttämisen ja uuden vuokrasopimusaikataulun luomisen.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="f4f5a-106">Kun vähintään yksi vuokrasopimus on määritetty, voi olla helpompaa kopioida tietoja olemassa olevasta vuokrasopimuksesta ja muokata sitten tietoja tarpeen mukaan uuden vuokrasopimuksen luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="f4f5a-107">Vuokrasopimuksen luominen</span><span class="sxs-lookup"><span data-stu-id="f4f5a-107">Create a lease</span></span>

<span data-ttu-id="f4f5a-108">Näiden ohjeiden avulla voit luoda vuokrasopimuksen resurssin vuokrauksessa.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="f4f5a-109">Valitse **Vuokrasopimusyhteenveto**-sivun toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="f4f5a-110">Syötä vuokrasopimuksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-110">Enter the lease information.</span></span> <span data-ttu-id="f4f5a-111">Pakollisilla kentillä on punaiset reunat.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="f4f5a-112">Vuokrasopimusaikataulun luominen</span><span class="sxs-lookup"><span data-stu-id="f4f5a-112">Create a lease schedule</span></span>

<span data-ttu-id="f4f5a-113">Kun olet syöttänyt vuokrasopimuksen tiedot, luo vuokrasopimusaikataulu seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="f4f5a-114">Taloushallinnon dimensiot voivat muuttua mukautettujen taloushallinnon dimensioiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="f4f5a-115">Luo vuokrauskirjat valitsemalla **Luo aikataulut**.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="f4f5a-116">Vuokrauskirjoja ovat maksu, kuoletus, poisto ja kuluaikataulut.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="f4f5a-117">Jos haluat käyttää vuokrauskirjoja ja tarkastella juuri luotuja aikatauluja, valitse **Kirjat**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="f4f5a-118">**Kirjan tiedot** -sivulla on tietoja vuokrasopimuksen kirjaamisesta kirjoihin, jotka on kohdistettu sille.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="f4f5a-119">Tässä voit tarkastella vuokrasopimusaikatauluja.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="f4f5a-120">Maksuaikataulu sisältää syötteet **Maksuaikataulurivit**-välilehdestä **Lisää vuokrasopimus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="f4f5a-121">Voit kuitenkin muuttaa kunkin maksusumman ja muuttuvan maksun.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="f4f5a-122">Vuokrasopimusvelka lasketaan muutetun maksuaikataulun mukaan.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="f4f5a-123">Kun maksuaikataulun tarkastelu on päättynyt, valitse **Vahvista aikataulu**.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="f4f5a-124">Kun aikataulu on vahvistettu, vuokrasopimusta ei enää voi muokata.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4f5a-125">Järjestelmä laskee automaattisesti vuokra-ajan maksuaikatauluriveiltä **Lisää vuokrasopimus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="f4f5a-126">Jos haluat laskea vuokra-ajan kuukausina, järjestelmä löytää alkamis- ja päättymispäivämäärän välisen eron tietyltä maksuaikatauluriviltä.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="f4f5a-127">Sen jälkeen se siirtyy seuraavalle maksuaikatauluriville ja löytää eron uudelleen.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="f4f5a-128">Järjestelmä laskee lopuksi kaikki summat ja määrittää vuokra-ajan kuukausina.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="f4f5a-129">Jos haluat tarkastella laskettuja kauden korkokuluja, avaa **Velan kuoletusaikataulu** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="f4f5a-130">Jos haluat tarkastella laskettua tasapoistoa, avaa **Käyttöomaisuuden poistoaikataulu** -sivu.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="f4f5a-131">Kun olet tarkistanut lasketun summan, voit luoda alkuperäisen tuloutuksen kirjauskansioviennin **Alkuperäinen tuloutus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="f4f5a-132">Näyttöön tulee sanoma, joka ilmaisee, että kirjauskansio on luotu.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4f5a-133">Kirjauskansiovienti kirjataan kirjanpitoon manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="f4f5a-134">Voit tarkistaa ehdotetun alkuperäisen tuloutuksen viennin ennen kirjaamista valitsemalla **Resurssin leasingkirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4f5a-135">Resurssin leasingkirjauskansiota ei voi luoda manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="f4f5a-136">Se luodaan automaattisesti, kun vuokrasopimuksen aikataulut luodaan.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="f4f5a-137">Kun olet tarkistanut alkuperäisen tuloutuksen kirjauskansioviennin ja se on valmis kirjattavaksi, valitse **Kirjaa** ja kirjaa käyttöoikeusomaisuuserä ja vuokrasopimusvelka kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="f4f5a-138">Vuokrasopimuksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="f4f5a-138">Copy a lease</span></span>

<span data-ttu-id="f4f5a-139">Käyttöomaisuuden vuokrauksen avulla voit kopioida vuokrasopimuksen tiedot ja luoda uuden vuokrasopimuksen samoilla tiedoilla.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="f4f5a-140">Tämän jälkeen voit muuttaa vuokrasopimuksen kenttiä, ennen kuin luot kopioidun vuokrasopimuksen aikataulut.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="f4f5a-141">Valitse **Vuokrasopimusyhteenveto**-sivulla kopioita vuokrasopimus ja valitse sitten toimintoruudussa **Kopioi vuokrasopimus**.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f4f5a-142">Jos **Manuaalinen**-parametri on poistettu käytöstä vuokrasopimusten tunnusten numerojärjestystä varten, seuraava numero luodaan automaattisesti kopioidun vuokrasopimuksen tunnukselle.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="f4f5a-143">Jos **Manuaalinen**-parametri on otettu käyttöön, näytössä on sanoma, jossa pyydetään syöttämään vuokrasopimuksen tunnus ennen vuokrasopimuksen kopioimista.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="f4f5a-144">Valitse **Kopioi**.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-144">Select **Copy**.</span></span> <span data-ttu-id="f4f5a-145">Valitun vuokrasopimuksen tiedot kopioidaan uuteen vuokrasopimukseen.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="f4f5a-146">Tämän jälkeen voit muokata uuden vuokrasopimuksen tietoja ennen sen tallentamista. Voit myös luoda vuokrasopimuksen aikataulut.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="f4f5a-147">Resurssin leasingkirjauskansio</span><span class="sxs-lookup"><span data-stu-id="f4f5a-147">Asset leasing journal</span></span>

<span data-ttu-id="f4f5a-148">Kaikki resurssin vuokrauksessa luodut kirjauskansioviennit sisältyvät resurssin leasingkirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="f4f5a-149">**Resurssin leasingkirjauskansio** -sivulla (**Resurssin vuokraus \> Kirjauskansioviennit \> Resurssin leasingkirjauskansio**) voit suodattaa kirjauksen tilan mukaan, tarkastella tiettyjä kirjauskansiovientejä ja tositteita ja kirjata kirjaamattomia kirjauskansiovientejä.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="f4f5a-150">Resurssin leasingkirjauskansiota ei voi luoda manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="f4f5a-151">Se luodaan automaattisesti, kun vuokrasopimuksen aikataulut luodaan.</span><span class="sxs-lookup"><span data-stu-id="f4f5a-151">It's automatically created when lease schedules are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]