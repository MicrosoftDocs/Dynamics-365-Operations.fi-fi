---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (15. marraskuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a571568850a675f3472f2b62df33c0c35d905af0
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551377"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a><span data-ttu-id="ebde6-103">Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (15. marraskuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="ebde6-103">What's new or changed in Dynamics 365 Talent - Core HR (November 15, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ebde6-104">**Koontiversio 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="ebde6-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="ebde6-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ebde6-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="ebde6-106">Muut muutokset ja korjaukset</span><span class="sxs-lookup"><span data-stu-id="ebde6-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="ebde6-107">Työntekijän nykyistä toimea ei voi muuttaa tulevaksi avoimeksi toimeksi</span><span class="sxs-lookup"><span data-stu-id="ebde6-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="ebde6-108">Tehdyn muutoksen avulla toimen siirrot voidaan käyttöön, kun toimi on vapaana vain tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="ebde6-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="ebde6-109">Toimi ei näy uutta työntekijää luotaessa</span><span class="sxs-lookup"><span data-stu-id="ebde6-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="ebde6-110">Tehdyn muutoksen avulla näytetään kaikki avoimet toimet, jotka on käytettävissä, kun uusi työntekijöitä palkataan Talentissa.</span><span class="sxs-lookup"><span data-stu-id="ebde6-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="ebde6-111">Tämä sisältää myös historialliset toimet tai toimet, joiden päivämäärä on tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="ebde6-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="ebde6-112">Toimet näkyvät nyt oikein työsuhteen aloituspäivän perusteella.</span><span class="sxs-lookup"><span data-stu-id="ebde6-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="ebde6-113">Työsuhteen päättymispäivän näyttäminen käyttäjäasetusten perusteella</span><span class="sxs-lookup"><span data-stu-id="ebde6-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="ebde6-114">Entisten työntekijöiden luetteloon tehdyn muutoksen avulla työsuhteen päättymispäivää tarkasteltaessa otetaan huomioon työntekijän ensisijaisen aikavyöhykkeen aiheuttamat aikavyöhykepoikkeamat.</span><span class="sxs-lookup"><span data-stu-id="ebde6-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="ebde6-115">Oikeat tiedot eivät näyt Minulle määritetyt työnimikkeet -linkeissä</span><span class="sxs-lookup"><span data-stu-id="ebde6-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="ebde6-116">Tämän muutoksen ansiosta siirtyminen luettelon yksittäisten työnimikkeiden tietoihin näyttää oikeat tiedot valitusta nimikkeestä.</span><span class="sxs-lookup"><span data-stu-id="ebde6-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="ebde6-117">Tämä ongelma esiintyi vain suojauksen lisäasetuksia käytettäessä.</span><span class="sxs-lookup"><span data-stu-id="ebde6-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="ebde6-118">Tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="ebde6-118">Known issue</span></span>

- <span data-ttu-id="ebde6-119">**Ongelma**: kun työntekijään lisätään uusi liite, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina.</span><span class="sxs-lookup"><span data-stu-id="ebde6-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="ebde6-120">**Ongelman kiertäminen:** Varmista ennen liitesivun avaamista, että **Työntekijä**-sivun tietoruudut on suljettu.</span><span class="sxs-lookup"><span data-stu-id="ebde6-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="ebde6-121">Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ebde6-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="ebde6-122">(Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)</span><span class="sxs-lookup"><span data-stu-id="ebde6-122">(This issue will be fixed in the next platform update.)</span></span>
