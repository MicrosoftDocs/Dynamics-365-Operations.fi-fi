---
title: "Sijoita budjetoinnin vianmääritys"
description: "Tässä artikkelissa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität toimen budjetointia. Se vastaa usein kysyttyyn kysymykseen, kuinka budjetin kustannustasoja, kompensaatioryhmiä ja kompensaatioruudukoita luodaan."
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f2ef04008a5e6339a2193f9fcc77f2e0e6643557
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="5f612-104">Sijoita budjetoinnin vianmääritys</span><span class="sxs-lookup"><span data-stu-id="5f612-104">Position budgeting troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5f612-105">Tässä artikkelissa on vastauksia kysymyksiin, joita sinulla saattaa olla, kun määrität toimen budjetointia.</span><span class="sxs-lookup"><span data-stu-id="5f612-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="5f612-106">Se vastaa usein kysyttyyn kysymykseen, kuinka budjetin kustannustasoja, kompensaatioryhmiä ja kompensaatioruudukoita luodaan.</span><span class="sxs-lookup"><span data-stu-id="5f612-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="5f612-107">Miksi ennusteen toimen sivua ei löydy henkilöstöhallinnosta?</span><span class="sxs-lookup"><span data-stu-id="5f612-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="5f612-108">Ennusteen toimet on siirretty budjetointiin.</span><span class="sxs-lookup"><span data-stu-id="5f612-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="5f612-109">Miksi en voi poistaa budjetin kustannuselementtiä?</span><span class="sxs-lookup"><span data-stu-id="5f612-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="5f612-110">Et voi poistaa budjetin kustannustasoa, koska se on määritetty ennusteen toimeen.</span><span class="sxs-lookup"><span data-stu-id="5f612-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="5f612-111">Ennen kuin voit poistaa budjetin kustannustason, se on poistettava kaikista ennusteen toimista.</span><span class="sxs-lookup"><span data-stu-id="5f612-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="5f612-112">**Vihje:** Jos haluat etsiä kaikki toimet, jotka on määritetty budjetin kustannustasolle, valitse kustannustaso **Budjetin kustannustasot** -sivulla ja valitse sitten **Päivitä toimet**.</span><span class="sxs-lookup"><span data-stu-id="5f612-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="5f612-113">Ylemmässä ruudukossa näkyvät kustannustasoa käyttävät toimet.</span><span class="sxs-lookup"><span data-stu-id="5f612-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="5f612-114">Kuinka voin poistaa kustannustason useista ennusteen toimista avaamatta jokaista?</span><span class="sxs-lookup"><span data-stu-id="5f612-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="5f612-115">Kustannustasoa ei voi poistaa.</span><span class="sxs-lookup"><span data-stu-id="5f612-115">You can’t remove a cost element.</span></span> <span data-ttu-id="5f612-116">Jos kuitenkin muutat alkamis- ja päättymispäivän budjettisuunnittelujakson päivämäärien ulkopuolelle, kustannustasoa ei enää määritetä ennusteen toimiin kyseisessä budjettisuunnittelujaksossa.</span><span class="sxs-lookup"><span data-stu-id="5f612-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="5f612-117">Voit tehdä tämän avaamalla budjetin kustannustason. Valitse sitten **Kustannuslaskenta**-pikavälilehdellä **Muuta päivämääriä** ja muuta voimassaolopäivämäärää tai vanhentumispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="5f612-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="5f612-118">Päivitä kaikki ennusteen toimet, joihin kustannustaso liittyy valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="5f612-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="5f612-119">**Vihje:** Jos käytät tätä tapaa, huomaa, että se poistaa budjetoidut kustannuselementit **kaikista** ennusteen toimista, joissa alku- ja loppupäivämäärät eivät enää sijoitu määrätyn alueen sisään.</span><span class="sxs-lookup"><span data-stu-id="5f612-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="5f612-120">Jos tämä ei ole aikomuksesi, sinun pitää avata kunkin ennusteen toimi, josta haluat poistaa budjetin kustannuselementin, ja tehdä muutos manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="5f612-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="5f612-121">Miksi en voi syöttää vuosittaista summaa budjetin kustannuselementin Kustannuslaskenta-pikavälilehdessä?</span><span class="sxs-lookup"><span data-stu-id="5f612-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="5f612-122">Et voi kirjoittaa vuosittaista määrää, jos **Laskuperuste**-pikavälilehdellä on budjetin kustannustasoja, koska järjestelmä edellyttää prosenttiosuutta arvon laskemiseksi.</span><span class="sxs-lookup"><span data-stu-id="5f612-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="5f612-123">Jos haluat muuttaa arvoa, poista kaikki budjetin kustannustasot **Laskuperuste**-pikavälilehdestä.</span><span class="sxs-lookup"><span data-stu-id="5f612-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="5f612-124">Miksi en voi muuttaa budjetin kustannustyyppiä Ansio-tyypistä toiseksi budjetin tyypiksi?</span><span class="sxs-lookup"><span data-stu-id="5f612-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="5f612-125">Eräät budjetin kustannustasoista ovat Ansio-kustannustasoja laskennan perusteella.</span><span class="sxs-lookup"><span data-stu-id="5f612-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="5f612-126">Jos haluat muuttaa **Budjetin kustannustyyppi** -kenttää, poista ansion kustannustaso kaikkien budjetin kustannustasojen **Laskuperuste**-pikavälilehdestä.</span><span class="sxs-lookup"><span data-stu-id="5f612-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="5f612-127">Miksi en voi muuttaa budjetin kustannuselementin rivien päivämäärää budjetin kustannuselementissä?</span><span class="sxs-lookup"><span data-stu-id="5f612-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="5f612-128">Et voi muuttaa budjettikustannustason rivin päivämäärää, kun ennusteen toimi käyttää budjetin kustannustasoa.</span><span class="sxs-lookup"><span data-stu-id="5f612-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="5f612-129">Tämä rajoitus auttaa varmistamaan, että ennusteen toimet noudattavat aina budjetin kustannustasojen määrittämiä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="5f612-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="5f612-130">Jos haluat muuttaa päivämäärää, valitse **Kustannuslaskenta**-pikavälilehdessä **Muuta päivämääriä** ja lisää uudet päivämäärät.</span><span class="sxs-lookup"><span data-stu-id="5f612-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="5f612-131">Päivitä kaikki toimet, joihin kustannustaso liittyy valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="5f612-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="5f612-132">Miksi en voi muuttaa budjetin kustannustasoa kompensaatioryhmän sivulla?</span><span class="sxs-lookup"><span data-stu-id="5f612-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="5f612-133">Voit luoda ja muuttaa budjetin kustannustasoja vain **Budjetin kustannustasot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5f612-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="5f612-134">Miksi näyttöön tulee virhesanoma, kun muutan kustannustason päivämäärää ennusteen toimessa?</span><span class="sxs-lookup"><span data-stu-id="5f612-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="5f612-135">Ennusteen toimen kustannustasorivin päivämäärien tulee olla seuraavien alueiden sisällä:</span><span class="sxs-lookup"><span data-stu-id="5f612-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="5f612-136">Toimen aktivointi- ja päättymispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="5f612-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="5f612-137">Budjetin kustannustason voimaantulo- ja vanhentumispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="5f612-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="5f612-138">Ennusteen toimen budjettisuunnitteluprosessin kanssa liitetyn budjettijakson alku- ja loppupäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="5f612-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>





