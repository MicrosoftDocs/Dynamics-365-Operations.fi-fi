---
title: Näyttöön tule kehote tallentaa nimikkeen kattavuusasetukset, vaikka et olisi tehnyt muutoksia
description: Näyttöön tule kehote tallentaa nimikkeen kattavuusasetukset, vaikka et olisi tehnyt muutoksia.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049464"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="99b97-103">Näyttöön tule kehote tallentaa nimikkeen kattavuusasetukset, vaikka et olisi tehnyt muutoksia</span><span class="sxs-lookup"><span data-stu-id="99b97-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="99b97-104">Tietopankin numero: 4615588</span><span class="sxs-lookup"><span data-stu-id="99b97-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="99b97-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="99b97-105">Symptoms</span></span>

<span data-ttu-id="99b97-106">Joissakin tilanteissa näyttöön saattaa tulla seuraava sanoma, kun **nimikkeen kattavuus** -sivu avataan sen jälkeen, kun nimikkeet on tuotu *nimikkeen kattavuuden V2* -yksikön kautta:</span><span class="sxs-lookup"><span data-stu-id="99b97-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="99b97-107">Haluatko tallentaa muutokset ennen sulkemista?</span><span class="sxs-lookup"><span data-stu-id="99b97-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="99b97-108">Saat tämän viestin, vaikka et ole tehnyt muutoksia.</span><span class="sxs-lookup"><span data-stu-id="99b97-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="99b97-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="99b97-109">Resolution</span></span>

<span data-ttu-id="99b97-110">**Nimikkeen kattavuus** -sivulla on monimutkainen oletuslogiikka, joka saattaa aiheuttaa sen, että viesti näkyy sen jälkeen, kun tietokantaan on tehty suoria muutoksia, esimerkiksi yksikön tuonnin kautta.</span><span class="sxs-lookup"><span data-stu-id="99b97-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="99b97-111">`AREGENERALSETTINGSOVERRIDDEN`-yksikkökentän arvoksi määritetään esimerkiksi *Ei*, mutta tuot tiedoston, joka sisältää uudet tai muokatut arvot esimerkiksi `PRODUCTCOVERAGEGROUPID`- ja/tai `VENDORACCOUNTNUMBER`-kentissä.</span><span class="sxs-lookup"><span data-stu-id="99b97-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="99b97-112">Tässä tapauksessa, koska `AREGENERALSETTINGSOVERRIDDEN`-kentän arvoksi on määritetty *Ei*, arvot poistetaan automaattisesti kentistä, kun **nimikkeen kattavuus** -sivu avataan ensimmäistä kertaa tuonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="99b97-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="99b97-113">Jos tallennat muutokset sanomaruudun kehotteen mukaan, ne tallennetaan tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="99b97-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="99b97-114">Muussa tapauksessa saat saman viestin, kun seuraavan kerran avaat sivun.</span><span class="sxs-lookup"><span data-stu-id="99b97-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="99b97-115">Jos haluat estää tämän toiminnan mutta myös sisällyttää arvoja, kuten `PRODUCTCOVERAGEGROUPID`entiteetin tuonnin kautta, valitse `AREGENERALSETTINGSOVERRIDDEN`-arvoksi *Kyllä*, kun tuot tietoja.</span><span class="sxs-lookup"><span data-stu-id="99b97-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
