---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (15. lokakuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/15/2018
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
ms.search.validFrom: 2018-10-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 96f877ae284a0f914bae2d0f5e5f7caf49109511
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896701"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-15-2018"></a><span data-ttu-id="87599-103">Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (15. lokakuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="87599-103">What's new or changed in Dynamics 365 Talent - Core HR (October 15, 2018)</span></span>

<span data-ttu-id="87599-104">**Koontiversio 8.1.1056**</span><span class="sxs-lookup"><span data-stu-id="87599-104">**Build 8.1.1056**</span></span>

<span data-ttu-id="87599-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="87599-105">This topic describes features that are either new or changed in Core HR.</span></span>


## <a name="changes"></a><span data-ttu-id="87599-106">Muutokset</span><span class="sxs-lookup"><span data-stu-id="87599-106">Changes</span></span>
<span data-ttu-id="87599-107">Muiden korjausten lisäksi tähän versioon on tehty seuraavat päivitykset:</span><span class="sxs-lookup"><span data-stu-id="87599-107">In addition to miscellanous fixes, the following updates have been made in this release:</span></span>
- <span data-ttu-id="87599-108">Viimeinen työpäivä määrittään nyt työhönoton yhteydessä tai työsuhteen päättymispäivää määritettäessä.</span><span class="sxs-lookup"><span data-stu-id="87599-108">Last Day worked now set when hiring or setting an employment end date.</span></span>
- <span data-ttu-id="87599-109">Viittaukset yhdysvaltalaiseen lainsäädäntöön poistettu, kun kyse Yhdysvaltojen ulkopuolisista yrityksistä (ACA, ADA ja I9).</span><span class="sxs-lookup"><span data-stu-id="87599-109">US compliance references removed when in non US companies (ACA, ADA, and I9).</span></span>
- <span data-ttu-id="87599-110">Virheelliset päivämäärät (1.1.1900) piilotetaan nyt analyysisivuilla.</span><span class="sxs-lookup"><span data-stu-id="87599-110">Invalid dates (1/1/1900) are now hidden on analytics pages.</span></span>

## <a name="known-issue"></a><span data-ttu-id="87599-111">Tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="87599-111">Known issue</span></span>

<span data-ttu-id="87599-112">**Ongelma:** Lisättäessä uuden liitteen työntekijään, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina. **Ratkaisuehdotus:** Varmista ennen liitesivun avaamista, että olet sulkenut **Työntekijä**-sivulla olevat tietoruudut.</span><span class="sxs-lookup"><span data-stu-id="87599-112">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="87599-113">Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="87599-113">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="87599-114">(Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)</span><span class="sxs-lookup"><span data-stu-id="87599-114">(This issue will be fixed in the next platform update.)</span></span>
