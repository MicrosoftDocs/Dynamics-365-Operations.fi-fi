---
title: Jaksotuksien yleiskuvaus
description: Tässä artikkelissa esitellään jaksotukset ja annetaan tietoja niiden määrittämisestä ja tapahtumien luomisesta.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 23c6a3402e4bc4a22d764017ba56554001300a67
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "339691"
---
# <a name="accruals-overview"></a><span data-ttu-id="dcb8c-103">Jaksotuksien yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="dcb8c-103">Accruals overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcb8c-104">Tässä artikkelissa esitellään jaksotukset ja annetaan tietoja niiden määrittämisestä ja tapahtumien luomisesta.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-104">This article describes accruals, and provides information about how to set them up and create transactions.</span></span>

<span data-ttu-id="dcb8c-105">Jaksotuksia käytetään jaksotuskirjanpidossa seuraamaan tuottoa, joka todetaan kaudella, jolla se on ansaittu, eikä silloin kun maksu vastaanotetaan, sekä seuraamaan kuluja (kustannuksina), jotka kirjataan kun niitä esiintyy, eikä silloin kun maksu suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-105">Accruals are used in accrual accounting to track revenue that is recognized in the period that it's earned in, not when payment is received, and to track expenses (costs) that are recognized when they occur, not when payment is made.</span></span>

## <a name="accrual-schemes"></a><span data-ttu-id="dcb8c-106">Jaksotusmallit</span><span class="sxs-lookup"><span data-stu-id="dcb8c-106">Accrual schemes</span></span>
<span data-ttu-id="dcb8c-107">Jaksotusmalleja käytetään määrittämään laskennalliset tuotot ja kustannukset, ja samaa jaksotusmallia voidaan käyttää sekä tuottoihin että kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-107">Accrual schemes are used to set up the deferred revenue and costs, and the same accrual scheme can be used for both revenue and costs.</span></span> <span data-ttu-id="dcb8c-108">Kirjanpidon jaksotukset jakavat kirjauskansiorivin tuotot niin, että tuotot ja kustannukset kirjataan oikeille kausille.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-108">Ledger accruals redistribute the costs or revenue of a journal line so that the costs and revenues are recognized in the appropriate periods.</span></span> <span data-ttu-id="dcb8c-109">**Jaksotusmalli** -sivulla voit määrittää debit- ja kredit-tilit, joita käytetään kun jaksotusmalli on käytössä.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-109">On the **Accrual scheme** page, you specify the debit and the credit accounts that will be used when the accrual scheme is applied.</span></span>

-   <span data-ttu-id="dcb8c-110">**Veloitus** – Määrittämäsi päätili korvaa veloituksen päätilin kirjauskansion tositerivillä.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-110">**Debit** – The main account that you define will replace the debit main account on the journal voucher line.</span></span> <span data-ttu-id="dcb8c-111">Tätä tiliä käytetään myös lykkäyksen peruuttamiseen, perustuen kirjanpidon jaksotustapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-111">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>
-   <span data-ttu-id="dcb8c-112">**Luotto** – Määrittämäsi päätili korvaa luoton päätilin kirjauskansion tositerivillä.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-112">**Credit** – the main account that you define will replace the credit main account on the journal voucher line.</span></span> <span data-ttu-id="dcb8c-113">Tätä tiliä käytetään myös lykkäyksen peruuttamiseen, perustuen kirjanpidon jaksotustapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-113">This account will also be used for the reversal of the deferral, based on the ledger accrual transactions.</span></span>

<span data-ttu-id="dcb8c-114">Kun olet määrittänyt, mitä tilejä käytetään, voit määrittää kuinka tositenumero luodaan jaksotustapahtumien luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-114">After you determine which accounts to use, you can specify how the voucher number is created when accrual transactions are created.</span></span> <span data-ttu-id="dcb8c-115">Voit myös määrittää, kuinka usein tapahtumat tapahtuvat, kuinka monta kertaa tapahtumia luodaan ja milloin tapahtumat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-115">You can also specify how often the transactions occur, the number of times that the transactions are created, and when the transactions are posted.</span></span> <span data-ttu-id="dcb8c-116">Jaksotusmallin luomisen jälkeen voit käyttää sitä tietyissä kirjauskansioissa käyttämällä Kirjanpidon jaksotus -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-116">After the accrual scheme has been created, you can use it in some of the journals by using the Ledger accruals function.</span></span>

## <a name="ledger-accruals"></a><span data-ttu-id="dcb8c-117">Kirjanpidon jaksotukset</span><span class="sxs-lookup"><span data-stu-id="dcb8c-117">Ledger accruals</span></span>
<span data-ttu-id="dcb8c-118">Kirjauskansiota syötettäessä napsauta **Kirjanpidon jaksotukset** **Toiminnot**-valikossa.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-118">When you enter a journal, you can click **Ledger accruals** on the **Functions** menu.</span></span> <span data-ttu-id="dcb8c-119">Tämän jälkeen valitessasi jaksotusmallin näet kirjauskansion perustemäärän, jota ulottuu kauden yli, jaksotusmallin määräämästi.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-119">Then, when you select the accrual scheme, you will see the base amount from the journal that will be spread over the period, as determined by the accrual scheme.</span></span> <span data-ttu-id="dcb8c-120">Esimerkiksi, jos maksat työntekijän vakuutuksen koko vuodeksi tammikuussa ja maksettava summa on 12 000 euroa, sinun on tunnistettava tämä kulu kuukausittain.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-120">For example, if you pay an employee's insurance for the whole year in January, and the amount is 12,000, you must recognize that expense each month.</span></span> <span data-ttu-id="dcb8c-121">Voit valita alkamispäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-121">You can select the start date.</span></span> <span data-ttu-id="dcb8c-122">Voit myös määrittää perustuuko jaksotettava summa tiliin vai vastatiliin.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-122">You can also specify whether the amount that is accrued is based on the account or the offset account.</span></span> <span data-ttu-id="dcb8c-123">Kun olet tehnyt valintasi, valitse **Tapahtumat** tarkastellaksesi kaikkia tapahtumia, jotka on luotu jaksotusmallin perusteella.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-123">After you make your selections, click **Transactions** to view all the transactions that have been created based on the accrual scheme.</span></span> <span data-ttu-id="dcb8c-124">Esimerkiksi jos jaat 12 000 euron vakuutuksen kulut koko vuodelle näet 1 000 joka kuukausi.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-124">For example, if you spread the 12,000 in insurance expenses over the year, you will see 1,000 for each month.</span></span> <span data-ttu-id="dcb8c-125">Kun olet kirjannut päiväkirjan, voit tarkastella tapahtumia käyttämällä **Tositetapahtumat** -kyselysivulla.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-125">After you post the journal, you can view the transactions by using the **Voucher transactions** inquiry page.</span></span> <span data-ttu-id="dcb8c-126">Jos jaksotusmallia ei voida käyttää (esimerkiksi kun on kyse myyntitilauksen laskusta tai ostotilauksen laskusta), voit kirjata ennakkoon maksetun summan kreditiin ja kulusumman debetiin.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-126">If an accrual scheme can't be applied (for example, when a sales order invoice or purchase order invoice is involved), you can credit the prepaid amount and debit the expense amount.</span></span> <span data-ttu-id="dcb8c-127">Voit valita **Vastatilin** kun käytät jaksotusmallia.</span><span class="sxs-lookup"><span data-stu-id="dcb8c-127">You can then select **Offset** when you apply the accrual scheme.</span></span>


<span data-ttu-id="dcb8c-128">Lisätietoja on ohjeaiheissa [Jaksotusmallien luominen](tasks/create-accrual-schemes.md) ja [Kirjanpidon jaksotustapahtumien luominen](tasks/create-ledger-accrual-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="dcb8c-128">For more information, see [Create accrual schemes](tasks/create-accrual-schemes.md) and [Create ledger accrual transactions](tasks/create-ledger-accrual-transactions.md).</span></span>
