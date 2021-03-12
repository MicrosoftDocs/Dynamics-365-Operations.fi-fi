---
title: Velka-, resurssi- ja kulutapahtumien tarkasteleminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit tarkastella vuokratun omaisuuden tapahtumia. Näihin tapahtumiin sisältyvät vuokrasopimusvelkatapahtumat ja kulutapahtumat, jotka on kirjattu.
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
ms.openlocfilehash: 76c7eff17df92b01317544112099e391fd05d105
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995365"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="97e8b-104">Velka-, resurssi- ja kulutapahtumien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="97e8b-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97e8b-105">Tässä ohjeaiheessa kerrotaan, kuinka voit tarkastella vuokratun omaisuuden tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="97e8b-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="97e8b-106">Näihin tapahtumiin sisältyvät vuokrasopimusvelkatapahtumat ja kulutapahtumat, jotka on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="97e8b-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="97e8b-107">Velan ja käyttöoikeusomaisuuserän kirjanpitoarvoja käytetään useissa raporteissa.</span><span class="sxs-lookup"><span data-stu-id="97e8b-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="97e8b-108">Niitä käytetään myös oikaisuarvojen laskemiseen.</span><span class="sxs-lookup"><span data-stu-id="97e8b-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="97e8b-109">Velkatapahtumat</span><span class="sxs-lookup"><span data-stu-id="97e8b-109">Liability transactions</span></span>

<span data-ttu-id="97e8b-110">Voit tarkastella vuokrasopimusvelkatapahtumia valitsemalla vuokrasopimuksen **Vuokrasopimusyhteenveto**-sivulla ja valitsemalla sitten **Kirjat**, jos haluat avata vuokrasopimustietueeseen liitetyt kirjat.</span><span class="sxs-lookup"><span data-stu-id="97e8b-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="97e8b-111">Kun alkuperäisen tuloutuksen jälkeen lasku tai korkokirjauskansio on kirjattu, valitse **Velkatapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="97e8b-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="97e8b-112">**Velkatapahtumat**-sivulla näkyvät tapahtumat, jotka joko lisäävät tai pienentävät vuokrasopimusvelkaa.</span><span class="sxs-lookup"><span data-stu-id="97e8b-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="97e8b-113">Tällä sivulla olevat negatiiviset summat edustavat hyvitystapahtumia vakiosovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="97e8b-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="97e8b-114">Mahdolliset korkokertymät näkyvät negatiivisina arvoina ja lisäävät vuokrasopimusvelan kokonaisarvoa.</span><span class="sxs-lookup"><span data-stu-id="97e8b-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="97e8b-115">Kaikki vuokrauksen oikaisut näkyvät positiivisina tai negatiivisena arvoina vuokrasopimuskirjan luonteen ja vaikutuksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="97e8b-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="97e8b-116">Valitun vuokrauksen vuokrasopimusvelan tämänhetkinen nettosaldo yhteensä näkyy sivun vasemmassa alareunassa.</span><span class="sxs-lookup"><span data-stu-id="97e8b-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="97e8b-117">Resurssitapahtumat</span><span class="sxs-lookup"><span data-stu-id="97e8b-117">Asset transactions</span></span>

<span data-ttu-id="97e8b-118">Voit tarkastella vuokrauksen resurssin tapahtumia, valitse vuokrasopimus **Vuokrasopimusyhteenveto**-sivulla ja valitse sitten **Kirjat**, jos haluat avata vuokrasopimustietueeseen liitetyt vuokrasopimuskirjat.</span><span class="sxs-lookup"><span data-stu-id="97e8b-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="97e8b-119">Valitse sitten **Resurssitapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="97e8b-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="97e8b-120">**Resurssitapahtuma**-sivulla näkyvät tapahtumat, jotka joko lisäävät tai pienentävät vuokrauksen resurssia ja kumulatiivisia poistotilejä.</span><span class="sxs-lookup"><span data-stu-id="97e8b-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="97e8b-121">Veloitukset näkyvät positiivisina arvoina, ja hyvitykset näytetään negatiivisina arvoina **Velkatapahtumat**-sivun tapaan.</span><span class="sxs-lookup"><span data-stu-id="97e8b-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="97e8b-122">Kirjatun alkuperäisen tuloutuksen ja kumulatiivisen poiston seuraava arvo näkyvät sivun vasemmassa alareunassa resurssin saldona.</span><span class="sxs-lookup"><span data-stu-id="97e8b-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="97e8b-123">Kulutapahtumat</span><span class="sxs-lookup"><span data-stu-id="97e8b-123">Expenses transactions</span></span>

<span data-ttu-id="97e8b-124">Voit tarkastella vuokrauksen kulutapahtumia, valitse vuokrasopimus **Vuokrasopimusyhteenveto**-sivulla ja valitse sitten **Kirjat**, jos haluat avata vuokrasopimustietueeseen liitetyt vuokrasopimuskirjat.</span><span class="sxs-lookup"><span data-stu-id="97e8b-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="97e8b-125">Valitse sitten **Kulutapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="97e8b-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="97e8b-126">**Kulutapahtumat**-sivulla näkyvät kaikki vuokrasopimukseen kirjatut kulut, kuten korkokulut, poistokulut ja mahdolliset toimeenpanokustannukset.</span><span class="sxs-lookup"><span data-stu-id="97e8b-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>
