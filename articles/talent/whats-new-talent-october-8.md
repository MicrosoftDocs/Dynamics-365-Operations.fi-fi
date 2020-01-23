---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (8. lokakuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 30c148a1bf27a221c1d4feacbe89cabfc412872c
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897339"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-8-2018"></a><span data-ttu-id="c9ca7-103">Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (8. lokakuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="c9ca7-103">What's new or changed in Dynamics 365 Talent - Core HR (October 8, 2018)</span></span>

<span data-ttu-id="c9ca7-104">**Koontiversio 8.1.1050.0**</span><span class="sxs-lookup"><span data-stu-id="c9ca7-104">**Build 8.1.1050.0**</span></span>

<span data-ttu-id="c9ca7-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-other-dates-to-be-used-on-leave-tier-basis-leave-management"></a><span data-ttu-id="c9ca7-106">Muiden päivämäärien käytön salliminen lomatason perusteessa (lomien hallinta)</span><span class="sxs-lookup"><span data-stu-id="c9ca7-106">Allow other dates to be used on leave tier basis (Leave Management)</span></span>

<span data-ttu-id="c9ca7-107">Kun työntekijöille myönnetään lomia, palkkiotason peruste määrittää, kuinka paljon lomaa työntekijälle kertyy.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-107">When awarding leave to employees, the award tier basis determines how much time off an employee accrues.</span></span> <span data-ttu-id="c9ca7-108">Tällä hetkellä nämä tasot perustuvat työntekijän aloituspäivään ja ikälisäpäivään.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-108">Currently, these tiers are based on employee start date and seniority date.</span></span> <span data-ttu-id="c9ca7-109">Joissakin skenaarioissa organisaatiot tarvitsevat tasojen perusteeksi muita päivämääriä, kuten vuosipäivän tai alkuperäisen työsuhteen alkamispäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-109">In some scenarios, organizations need these tiers to be based on other dates, like anniversary date or original hire date.</span></span> <span data-ttu-id="c9ca7-110">Näitä päivämääriä käytetään jo lomasuunnitelmassa määrittämään kertyminen. Lisäyksenä mahdollisuus määrittää näiden samojen päivämäärien avulla kertynyt summa, kun työntekijä määritetään suunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-110">These dates are already used on the leave plan to determine when accruals happen, the ability for these same dates to be used when an employee is enrolled in a plan have been added to determine the accrual amount.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="c9ca7-111">Muut muutokset</span><span class="sxs-lookup"><span data-stu-id="c9ca7-111">Other changes</span></span>
<span data-ttu-id="c9ca7-112">Tähän versioon sisältyy muita korjauksia.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-112">Miscellanous fixes have been included in this release.</span></span>

## <a name="known-issue"></a><span data-ttu-id="c9ca7-113">Tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="c9ca7-113">Known issue</span></span>

<span data-ttu-id="c9ca7-114">**Ongelma:** Lisättäessä uuden liitteen työntekijään, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina. **Ratkaisuehdotus:** Varmista ennen liitesivun avaamista, että olet sulkenut **Työntekijä**-sivulla olevat tietoruudut.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-114">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="c9ca7-115">Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="c9ca7-115">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="c9ca7-116">(Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)</span><span class="sxs-lookup"><span data-stu-id="c9ca7-116">(This issue will be fixed in the next platform update.)</span></span>
