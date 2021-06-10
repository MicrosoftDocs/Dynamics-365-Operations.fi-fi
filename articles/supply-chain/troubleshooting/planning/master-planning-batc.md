---
title: Et voi suodattaa pääsuunnittelunimikkeitä niihin liittyvien kattavuusryhmän arvojen mukaan
description: Et voi suodattaa pääsuunnittelunimikkeitä niihin liittyvien kattavuusryhmän arvojen mukaan.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fa0b614b6710c65811add8725a0e255ce2c34b88
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049465"
---
# <a name="you-cant-filter-master-planning-items-by-their-related-coverage-group-values"></a><span data-ttu-id="7710d-103">Et voi suodattaa pääsuunnittelunimikkeitä niihin liittyvien kattavuusryhmän arvojen mukaan</span><span class="sxs-lookup"><span data-stu-id="7710d-103">You can't filter master planning items by their related coverage group values</span></span>

<span data-ttu-id="7710d-104">Tietopankin numero: 4612572</span><span class="sxs-lookup"><span data-stu-id="7710d-104">KB number: 4612572</span></span>

## <a name="symptoms"></a><span data-ttu-id="7710d-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="7710d-105">Symptoms</span></span>

<span data-ttu-id="7710d-106">Haluat suodattaa kohteet, jotka sisällytetään pääsuunnittelun erätyöhön, aihealuetaulukon liittyvien tietueiden arvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="7710d-106">You want to filter the items that will be included in a master planning batch job, based on the values of related records from the item coverage table.</span></span> <span data-ttu-id="7710d-107">(Haluat esimerkiksi suodattaa nimikkeet niiden **Toimittaja**- ja/tai **Kattavuusryhmä**-arvon mukaan).</span><span class="sxs-lookup"><span data-stu-id="7710d-107">(For example, you want to filter items by their **Vendor** and/or **Coverage group** value).</span></span> <span data-ttu-id="7710d-108">Erätyön suodatinasetuksissa voit luoda liitoksen **Nimike**-taulusta **Nimikkeen kattavuus** -tauluun ja määrittää sitten kyselyn nimikekattavuustaulun kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="7710d-108">The filter setup for the batch job lets you create a join from the **Items** table to the **Item coverage** table, and then specify field values from the item coverage table in your query.</span></span> <span data-ttu-id="7710d-109">Kun nämä asetukset on tehty, järjestelmä luo edelleen suunniteltuja tilauksia koko nimikkeen kattavuutta varten, ei vain niitä nimikkeitä varten, jotka vastaavat nimikkeen kattavuustaulun määritettyjä kenttäarvoja.</span><span class="sxs-lookup"><span data-stu-id="7710d-109">However, after you complete this setup, the system still creates planned orders for the whole item coverage, not just for the items that match the specified field values from the item coverage table.</span></span>

## <a name="resolution"></a><span data-ttu-id="7710d-110">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="7710d-110">Resolution</span></span>

<span data-ttu-id="7710d-111">Erätyön suodatin voi suodattaa vain nimikkeiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="7710d-111">The batch job filter can filter only on items.</span></span> <span data-ttu-id="7710d-112">Vaikka liitoksen voikin lisätä **nimikkeen kattavuustauluun**, tätä taulua vasten muodostetut suodatusasetukset eivät vaikuta kyselyn tulokseen.</span><span class="sxs-lookup"><span data-stu-id="7710d-112">Although you can add a join to the **Item coverage** table, filter settings that you make against that table won't affect the query output.</span></span> <span data-ttu-id="7710d-113">Ajon aikana järjestelmä suunnittelee kaikkia kattavuusryhmiä ja kaikkia suodatetun nimikkeiden muunnelmia.</span><span class="sxs-lookup"><span data-stu-id="7710d-113">At runtime, the system runs planning for all the coverage groups and all the variations that the filtered items have.</span></span> <span data-ttu-id="7710d-114">Kun nimike on jo sisällytetty ajoon, nimikkeen suodattimeen sisältyvät kattavuusryhmät eivät vaikuta suunnittelun tulosteessa.</span><span class="sxs-lookup"><span data-stu-id="7710d-114">After an item is already included in the run, any coverage groups that are included in the item filter a won't affect the planning output.</span></span>
