---
title: Kuormarivien painokentät eivät vastaa kuormituksen painokenttiä
description: Kuormarivien painokentät eivät vastaa kuormituksen painokenttiä
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 639b82a9d46b74f179d6904d2c3b8e7dfb813b58
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924348"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a><span data-ttu-id="c363c-103">Kuormarivien painokentät eivät vastaa kuormituksen painokenttiä</span><span class="sxs-lookup"><span data-stu-id="c363c-103">The weight fields on load lines don't match the weight fields on the load</span></span>

<span data-ttu-id="c363c-104">Virhekoodit: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span><span class="sxs-lookup"><span data-stu-id="c363c-104">Error codes: WHSLoadWeightOnLinesDoNotMatchLoadWarning</span></span>

## <a name="symptoms"></a><span data-ttu-id="c363c-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="c363c-105">Symptoms</span></span>

<span data-ttu-id="c363c-106">Järjestelmä näyttää seuraavan virhesanoman:</span><span class="sxs-lookup"><span data-stu-id="c363c-106">The system shows the following error message:</span></span>

> <span data-ttu-id="c363c-107">Kuormarivien painokentät eivät vastaa kuormituksen %1 painokenttiä.</span><span class="sxs-lookup"><span data-stu-id="c363c-107">The weight fields on load lines do not match the weight fields on load %1.</span></span> <span data-ttu-id="c363c-108">Suorita Varaston kuorman painon yhdenmukaisuustarkistus, jos haluat laskea painokentät uudelleen.</span><span class="sxs-lookup"><span data-stu-id="c363c-108">Run the Warehouse load weight consistency check to recalculate the weight fields.</span></span>

## <a name="cause"></a><span data-ttu-id="c363c-109">Syy</span><span class="sxs-lookup"><span data-stu-id="c363c-109">Cause</span></span>

<span data-ttu-id="c363c-110">**Nettopaino**- ja **Taarapaino**-kenttien arvona on *0* (nolla) kuormitusrivillä.</span><span class="sxs-lookup"><span data-stu-id="c363c-110">The **Net weight** and **Tara weight** fields are set to *0* (zero) on the load line.</span></span> <span data-ttu-id="c363c-111">Tuotteen painomittauksissa painokentiksi ei kuitenkaan ole määritetty *0*.</span><span class="sxs-lookup"><span data-stu-id="c363c-111">However, the weight fields aren't set to *0* for the weight measurements on the product.</span></span> <span data-ttu-id="c363c-112">Jos kuormitusrivillä ei ole määritetty painokenttiä, kuormitusrivin määrän korjaukset voivat aiheuttaa kuormituksen virheellisen painon laskennan.</span><span class="sxs-lookup"><span data-stu-id="c363c-112">When weight fields aren't set on the load line, any corrections of the quantity on the load line might cause incorrect weight calculation on the load.</span></span> <span data-ttu-id="c363c-113">Tämä ongelma voi ilmetä, jos tuotteen painot on muutettu kuormitusrivin luomisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="c363c-113">This issue might occur if the weights on the product have been changed since the load line was created.</span></span>

## <a name="resolution"></a><span data-ttu-id="c363c-114">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="c363c-114">Resolution</span></span>

<span data-ttu-id="c363c-115">Kun kuormitusrivi luodaan, tuotteen painokentät syötetään siihen oletusarvoisesti.</span><span class="sxs-lookup"><span data-stu-id="c363c-115">By default, when a load line is created, the weight fields from the product are entered on it.</span></span> <span data-ttu-id="c363c-116">Jos paino on nolla, voit laskea sen uudelleen käyttämällä *Varaston kuorman painon yhdenmukaisuustarkistus* -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="c363c-116">If the weight is zero, you can recalculate it by using the *Warehouse load weight consistency check* functionality.</span></span>

1. <span data-ttu-id="c363c-117">Valitse **Järjestelmän hallinta \> Kausittaiset tehtävät \> Tietokanta \> Yhdenmukaisuustarkistus**.</span><span class="sxs-lookup"><span data-stu-id="c363c-117">Go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="c363c-118">**Yhdenmukaisuustarkistus**-valintaikkunassa aseta **Moduuli**-kentän arvoksi *Varastonhallinta*.</span><span class="sxs-lookup"><span data-stu-id="c363c-118">In the **Consistency check** dialog box, set the **Module** field to *Warehouse management*.</span></span>
1. <span data-ttu-id="c363c-119">Valitse **Tarkista/korjaa**-kentässä *Korjaa virhe*.</span><span class="sxs-lookup"><span data-stu-id="c363c-119">Set the **Check/Fix** field to *Fix error*.</span></span>
1. <span data-ttu-id="c363c-120">Valitse valintaruutuluettelosta **Varaston kuorman painon yhdenmukaisuustarkistus** -valintaruutu ja varmista, että vain tämän valintaruudun rivi on korostettuna.</span><span class="sxs-lookup"><span data-stu-id="c363c-120">In the checkbox list, select the **Warehouse load weight consistency check** checkbox, and make sure that only the row for this checkbox is highlighted.</span></span>
1. <span data-ttu-id="c363c-121">Valitse valintaruutuluettelon yläosasta kolmen pisteen painike (**...**) ja valitse valikosta **Valintaikkuna**.</span><span class="sxs-lookup"><span data-stu-id="c363c-121">At the top of the checkbox list, select the ellipsis button (**...**), and then select **Dialog** on the menu.</span></span>
1. <span data-ttu-id="c363c-122">**Varaston kuorman painon yhdenmukaisuustarkistus** -valintaikkunassa määritä seuraavat kentät määrittämään ehdot, joiden yhdenmukaisuustarkistuksessa tarkistetaan:</span><span class="sxs-lookup"><span data-stu-id="c363c-122">In the **Warehouse load weight consistency check** dialog box, set the following fields to specify the criteria that the consistency check should run for:</span></span>

    - <span data-ttu-id="c363c-123">**Kuorman tunnus:** Määritä kuorman tunnus.</span><span class="sxs-lookup"><span data-stu-id="c363c-123">**Load ID:** Specify a load ID.</span></span> <span data-ttu-id="c363c-124">Jätä tämä kenttä tyhjäksi, jotta voit tarkistaa kaikki kuormatunnukset.</span><span class="sxs-lookup"><span data-stu-id="c363c-124">Leave this blank to check all load IDs.</span></span>
    - <span data-ttu-id="c363c-125">**Nimiketunnus:** Määritä nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="c363c-125">**Item number:** Specify an item number.</span></span> <span data-ttu-id="c363c-126">Jätä tämä kenttä tyhjäksi, jotta voit tarkistaa kaikki nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="c363c-126">Leave this blank to check all items.</span></span>
    - <span data-ttu-id="c363c-127">**Laske kuorman paino aina uudelleen:** Määritä tämän asetuksen arvoksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="c363c-127">**Always recalculate weight on loads:** Set this option to *Yes*.</span></span>
    - <span data-ttu-id="c363c-128">**Salli painojen korvaaminen kuormariveillä:** Määritä tämän asetuksen arvoksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="c363c-128">**Allow overwrite of weight on load lines:** Set this option to *Yes*.</span></span>

1. <span data-ttu-id="c363c-129">Valitse **OK**, jos haluat sulkea **Varaston kuorman painon yhdenmukaisuustarkistus** -valintaikkunan.</span><span class="sxs-lookup"><span data-stu-id="c363c-129">Select **OK** to close the **Warehouse load weight consistency check** dialog box.</span></span>
1. <span data-ttu-id="c363c-130">Valitse kolmen pisteen painike ja valitse sitten valikosta **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="c363c-130">Select the ellipsis button, and then select **Execute** on the menu.</span></span>

<span data-ttu-id="c363c-131">Paino lasketaan uudelleen määrittämiesi ehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="c363c-131">The weight is recalculated based on the criteria that you specified.</span></span> <span data-ttu-id="c363c-132">Valitsemalla **Sanoman tiedot** -linkin voit tarkastella yhdenmukaisuustarkistustuloksen tulosta.</span><span class="sxs-lookup"><span data-stu-id="c363c-132">Select the **Message details** link to view the result of the consistency check.</span></span>
