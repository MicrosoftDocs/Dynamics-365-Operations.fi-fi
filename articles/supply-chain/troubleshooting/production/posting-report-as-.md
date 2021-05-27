---
title: Virhe, kun Valmiiksi ilmoitettujen kirjauskansio on kirjattu
description: Kun kirjaat valmiiksi ilmoitettujen kirjauskansion, näyttöön tulee virhesanoma, jossa sanotaan, että tilattua määrää ei voi pienentää.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026462"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="d821b-103">Virhe, kun Valmiiksi ilmoitettujen kirjauskansio on kirjattu</span><span class="sxs-lookup"><span data-stu-id="d821b-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="d821b-104">Tietopankin numero: 4612891</span><span class="sxs-lookup"><span data-stu-id="d821b-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="d821b-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="d821b-105">Symptoms</span></span>

<span data-ttu-id="d821b-106">Kun kirjaat **Ilmoita valmiiksi** -kirjauskansion, näkyviin tulee virheilmoitus, ja näyttöön tulee seuraava virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="d821b-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="d821b-107">Tilattua määrää ei voi vähentää, koska Tilattu-tilassa olevia avoimia varastotapahtumia ei ole riittävästi.</span><span class="sxs-lookup"><span data-stu-id="d821b-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="d821b-108">Nimikkeet ovat ostettuja, vastaanotettuja tai rekisteröityjä.</span><span class="sxs-lookup"><span data-stu-id="d821b-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="d821b-109">Tämä virhe tapahtuu vain, kun **Virhemäärä**-kenttä on määritetty **Ilmoita valmiiksi** -kirjauskansion ensimmäiselle riville ja **Hyvä määrä** -kentän arvoksi määritetään viimeinen rivi.</span><span class="sxs-lookup"><span data-stu-id="d821b-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="d821b-110">Jos **Virhemäärä**-kenttä on määritetty viimeiselle riville, virhettä ei tapahdu.</span><span class="sxs-lookup"><span data-stu-id="d821b-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="d821b-111">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="d821b-111">Resolution</span></span>

<span data-ttu-id="d821b-112">Voit estää tämän virheen avaamalla **Tuotannonhallinnan parametrit** -sivun ja valitsemalla **Yleiset**-välilehdestä **Lisää jäljellä olevaa määrää virheen määrällä** -asetuksen arvoksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="d821b-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
