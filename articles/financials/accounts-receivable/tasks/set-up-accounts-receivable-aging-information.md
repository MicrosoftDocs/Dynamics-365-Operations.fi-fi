---
title: Määritä ja luo myyntireskontran erääntymistiedot
description: Tämän ohjauksen avulla opit määrittämään erääntymiskauden ja asiakkaiden saldojen erääntymisen sekä tarkastelemaan erääntyneiden saldojen luettelon saldoja ja Perintä-sivua.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fd8738cfd3466464c9fec1760e9a369ff3a4a67
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "334631"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a><span data-ttu-id="8c0d1-103">Määritä ja luo myyntireskontran erääntymistiedot</span><span class="sxs-lookup"><span data-stu-id="8c0d1-103">Set up and generate accounts receivable aging information</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c0d1-104">Tämän ohjauksen avulla opit määrittämään erääntymiskauden ja asiakkaiden saldojen erääntymisen sekä tarkastelemaan erääntyneiden saldojen luettelon saldoja ja Perintä-sivua.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-104">This guide will help you set up an aging period definition, age customer balances, and view balances in the Aged balance list and the Collections page.</span></span> <span data-ttu-id="8c0d1-105">Tässä tallenteessa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-105">This recording uses the USMF demo company.</span></span>


## <a name="create-an-aging-period-definition"></a><span data-ttu-id="8c0d1-106">Luo erääntymiskausien määritys.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-106">Create an aging period definition</span></span>
1. <span data-ttu-id="8c0d1-107">Siirry kohtaan Luotonvalvonta > Asetukset > Erääntymiskausien määritykset.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-107">Go to Credit and collections > Setup > Aging period definitions.</span></span>
2. <span data-ttu-id="8c0d1-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-108">Click New.</span></span>
3. <span data-ttu-id="8c0d1-109">Kirjoita arvo Erääntymiskauden määritys -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-109">In the Aging period definition field, type a value.</span></span>
4. <span data-ttu-id="8c0d1-110">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8c0d1-111">Lisää uusi erääntymiskausi valitsemalla alla oleva Lisää.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-111">Click Add below to insert a new aging period.</span></span>
6. <span data-ttu-id="8c0d1-112">Syötä Kausi-kenttään erääntymisraporteissa näkyvä kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-112">In the Period field, enter the description to show on aging reports.</span></span>
7. <span data-ttu-id="8c0d1-113">Syötä Yksikkö-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-113">In the Unit field, enter a number.</span></span>
8. <span data-ttu-id="8c0d1-114">Valitse vaihtoehto Aikaväli-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-114">In the Interval field, select an option.</span></span>
    * <span data-ttu-id="8c0d1-115">Kirjanpitokausi on sama kuin kirjanpitokalenterin kausi.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-115">Ledger period matches the period to your ledger calendar.</span></span> <span data-ttu-id="8c0d1-116">Päivä, viikko, kuukausi, neljännesvuosi ja vuodet määrittävät aikavälin koon päivämäärätyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-116">Day, week, month, quarter and years define the size of the interval by date type.</span></span> <span data-ttu-id="8c0d1-117">Jos valittuna on Rajoittamaton, kaikki edellistä kautta aiemmat tai edellisen kauden jälkeiset tapahtumat valitaan sen perusteella, onko kyseessä ensimmäinen vai viimeinen kausi.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-117">Unlimited selects all transactions before or after the previous period, depending on whether it is the first or last period.</span></span>  
9. <span data-ttu-id="8c0d1-118">Valitse vaihtoehto Erääntymisen ilmaisin -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-118">In the Aging indicator field, select an option.</span></span>
10. <span data-ttu-id="8c0d1-119">Valitse kausi ruudukon yläosassa.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-119">Select the period at the top of the grid.</span></span> <span data-ttu-id="8c0d1-120">Päivitä kuvaukseen erääntymiskauden määrityksen vanhimman kauden kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-120">Update the description to describe the oldest period in the aging period definition</span></span>
11. <span data-ttu-id="8c0d1-121">Syötä Kausi-kenttään erääntymiskauden uusi kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-121">In the Period field, enter the new description of the aging period.</span></span>
12. <span data-ttu-id="8c0d1-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-122">Close the page.</span></span>

## <a name="age-the-balances"></a><span data-ttu-id="8c0d1-123">Saldojen erääntyminen</span><span class="sxs-lookup"><span data-stu-id="8c0d1-123">Age the balances</span></span>
1. <span data-ttu-id="8c0d1-124">Siirry kohtaan Luotonvalvonta > Kausittaiset tehtävät > Eräännytä asiakkaan saldot.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-124">Go to Credit and collections > Periodic tasks > Age customer balances.</span></span>
2. <span data-ttu-id="8c0d1-125">Valitse Erääntymiskauden määritys -kentässä luomasi erääntymiskauden määritys.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-125">In the Aging period definition field, select the aging period definition that you created.</span></span>
    * <span data-ttu-id="8c0d1-126">Kullakin erääntymiskauden määrityksellä voi olla yksi aktiviinen tilannevedos.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-126">You can have one active snapshot for each aging period definition.</span></span>  
    * <span data-ttu-id="8c0d1-127">Kaikki asiakkaat käsitellään oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-127">All customers are processed by default.</span></span> <span data-ttu-id="8c0d1-128">Voit laskea yksittäisten perintöjen asiakasjoukon tämän valinnan perusteella.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-128">You can use this selection to calculate a single collections pool of customers.</span></span>  
    * <span data-ttu-id="8c0d1-129">Valitse sen tapahtuman päivämäärä, jota haluat käyttää erääntymisessä.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-129">Select the date from the transaction that you will use for the aging.</span></span>  
    * <span data-ttu-id="8c0d1-130">Valitse erääntymiselle alkaen-päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-130">Select an "as of" date for aging.</span></span> <span data-ttu-id="8c0d1-131">Oletusarvo on tänään. Voit kuitenkin muuttaa kentän arvoksi Valittu päivämäärä, jolloin voit valita haluamasi päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-131">The default is today but, if you change this field to Selected date, you will be able to pick the date that you want.</span></span> <span data-ttu-id="8c0d1-132">Käytä eräkäsittelyssä kuluvaa päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-132">For batch processing, use Today's date.</span></span>  
3. <span data-ttu-id="8c0d1-133">Laajenna yritysalue.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-133">Expand the Company range.</span></span> <span data-ttu-id="8c0d1-134">Voit valita yrityksiä tilannevedokseen.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-134">You can select the companies that will be included in the snapshot.</span></span> <span data-ttu-id="8c0d1-135">Nykyinen yritys on valittuna oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-135">The current company is selected by default.</span></span>
4. <span data-ttu-id="8c0d1-136">Aloita tilannevedoksen käsittely valitsemalla OK.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-136">Click Ok to process the snapshot.</span></span> <span data-ttu-id="8c0d1-137">Tähän kuluu jonkin aikaa, joten odota, kunnes liukusäädin katoaa. Tarkista sitten viestikeskuksen viestit.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-137">It will take some time so wait for the slider to disappear and check the message center for a message.</span></span>

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a><span data-ttu-id="8c0d1-138">Saldojen tarkasteleminen erääntyneiden saldojen luettelossa ja Perintä-sivulla</span><span class="sxs-lookup"><span data-stu-id="8c0d1-138">View the balances on the Aged balances list and on the Collection page</span></span>
1. <span data-ttu-id="8c0d1-139">Siirry kohtaan Luotonvalvonta > Perintä > Erääntyneet saldot.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-139">Go to Credit and collections > Collections > Aged balances.</span></span>
    * <span data-ttu-id="8c0d1-140">Luettelosivulla näkyvät asiakkaan saldot.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-140">The list page shows the balances for the customer.</span></span> <span data-ttu-id="8c0d1-141">Erääntymiskuvake osoittaa vanhimman tapahtuman erääntymiskauden.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-141">The aging icon shows the aging period for the oldest transaction.</span></span>  
2. <span data-ttu-id="8c0d1-142">Valitse asiakas, jolla on saldo.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-142">Select a customer with a balance.</span></span>
3. <span data-ttu-id="8c0d1-143">Laajenna Erääntyminen-tietoruutua niin, että erääntyvät saldot näkyvät.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-143">Expand the Aging fact box area to view the aged balances.</span></span>
    * <span data-ttu-id="8c0d1-144">Tietokentän erääntymiskauden määritys saadaan parametreissa määritetystä erääntymiskauden oletusmäärityksestä.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-144">The aging period definition for the fact box is taken from the default aging period definition specified in the parameters.</span></span> <span data-ttu-id="8c0d1-145">Arvon voi muuttaa keräysvalikon avulla.</span><span class="sxs-lookup"><span data-stu-id="8c0d1-145">You can change it using the Collect menu.</span></span>  

