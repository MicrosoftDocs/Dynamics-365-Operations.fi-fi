---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (16. lokakuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
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
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5f2aea5fcc81d0b4c1d8a392a3e56c888440a94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461016"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-october-16-2018"></a><span data-ttu-id="f292c-103">Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (16. lokakuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="f292c-103">What's new or changed in Dynamics 365 Talent - Core HR (October 16, 2018)</span></span>

<span data-ttu-id="f292c-104">**Koontiversio 8.1.1067**</span><span class="sxs-lookup"><span data-stu-id="f292c-104">**Build 8.1.1067**</span></span>

<span data-ttu-id="f292c-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="f292c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="allow-managers-to-update-time-off-requests"></a><span data-ttu-id="f292c-106">Esimiehet saavat päivittää poissaolopyynnöt</span><span class="sxs-lookup"><span data-stu-id="f292c-106">Allow managers to update time off requests</span></span>

<span data-ttu-id="f292c-107">Työntekijän poissaolopyyntöjä on ehkä päivitettävä sen jälkeen, kun ne hyväksytty työnkulun kautta.</span><span class="sxs-lookup"><span data-stu-id="f292c-107">Employee time off requests may need to be updated after they are approved through the workflow.</span></span> <span data-ttu-id="f292c-108">Monissa tapauksissa esimies tekee nämä päivityksen työntekijän puolesta.</span><span class="sxs-lookup"><span data-stu-id="f292c-108">In many cases, the manager makes these updates on the employee’s behalf.</span></span> <span data-ttu-id="f292c-109">Tämän uuden ominaisuuden ansiosta esimiehet voivat päivittää tai peruuttaa poissaolopyynnöt työntekijöiden puolesta.</span><span class="sxs-lookup"><span data-stu-id="f292c-109">This new feature provides the ability for managers to update time off or cancel time off requests on behalf of their employees.</span></span> <span data-ttu-id="f292c-110">Toimintoa hallitaan **Tee jonkun puolesta** -parametrilla, joka voidaan määrittää **Henkilöstöparametrit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="f292c-110">This capability is controlled by the **Work on behalf** parameter that can be set on the **Human Resource Parameters** page.</span></span> 
 
## <a name="allow-hr-to-update-time-off-requests"></a><span data-ttu-id="f292c-111">Henkilöstöhallinto saa päivittää poissaolopyynnöt</span><span class="sxs-lookup"><span data-stu-id="f292c-111">Allow HR to update time off requests</span></span>

<span data-ttu-id="f292c-112">Edellä kuvatun toiminnon tavoin henkilöstöhallinnon on ehkä päivitettävä työntekijän poissaolopyyntöjä sen jälkeen, kun ne on jo hyväksytty työnkulun kautta.</span><span class="sxs-lookup"><span data-stu-id="f292c-112">Similar to the feature above, employee time off requests may need to be updated by HR after they have been previously approved through the workflow.</span></span> <span data-ttu-id="f292c-113">Henkilöstöhallinnon käyttäjät voivat päivittää poissaolopyynnöt tällä ominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="f292c-113">This feature provides the ability for HR users to update time off requests.</span></span> <span data-ttu-id="f292c-114">Toiminto otetaan käyttöön **Henkilöt**-työtilassa ja **Työntekijä**-sivulla uudella **Näytä poissaoloaika** -asetuksella.</span><span class="sxs-lookup"><span data-stu-id="f292c-114">The capability is enabled in the **People** workspace and on the **Worker** page, using a new option called **View time off**.</span></span> <span data-ttu-id="f292c-115">Henkilöstöhallinnon käyttäjät voivat tarkastella näillä sivuilla pyyntöjä ja päivittää poissaolotapahtumia samalla tavoin kuin esimiehet suorittavat näitä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="f292c-115">On those pages, HR users can view requests and update time off transactions, similar to how managers can perform these actions.</span></span>

<span data-ttu-id="f292c-116">Tämän toiminnon käyttöä hallitaan seuraavalla suojausvelvollisuudella:</span><span class="sxs-lookup"><span data-stu-id="f292c-116">The security duty that controls access to this functionality is:</span></span>
- <span data-ttu-id="f292c-117">Velvollisuus: Ylläpidä työntekijäkohtaisia loma- ja poissaoloprosesseja.</span><span class="sxs-lookup"><span data-stu-id="f292c-117">Duty: Maintain worker-specific leave and absence processes.</span></span>
- <span data-ttu-id="f292c-118">Käyttöoikeus: Ylläpidä kaikkien työntekijöiden loma- ja poissaolopyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="f292c-118">Privilege: Maintain leave and absence requests for all workers.</span></span>

## <a name="other-changes"></a><span data-ttu-id="f292c-119">Muut muutokset</span><span class="sxs-lookup"><span data-stu-id="f292c-119">Other changes</span></span>
<span data-ttu-id="f292c-120">Tässä versiossa on tehty seuraavat päivitykset:</span><span class="sxs-lookup"><span data-stu-id="f292c-120">The following updates have been made in this release:</span></span>
- <span data-ttu-id="f292c-121">Työntekijän työhönottotoimintoja on muutettu siten, että eivät enää juutu **Työnkulku valmis** -tilaan.</span><span class="sxs-lookup"><span data-stu-id="f292c-121">Changes to worker hire actions so that they are no longer "stuck" in **Workflow complete** state.</span></span>
- <span data-ttu-id="f292c-122">Työntekijätietue voidaan nyt luoda ilman työsuhteen alkamispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="f292c-122">Employment record can now be created without an employment start date.</span></span>
- <span data-ttu-id="f292c-123">Työntekijän itsepalvelu -kohdassa näkyvän kurssin Dynamics 365 Talent -rekisteröitymispäivässä käytetään nyt aikavyöhykepoikkeamaa.</span><span class="sxs-lookup"><span data-stu-id="f292c-123">The Dynamics 365 Talent registration date for a course shown in Employee self-service now applies the time zone offset to the date.</span></span>
- <span data-ttu-id="f292c-124">Excel-tiedostot voidaan tuoda useita kertoja ilman virheilmoituksia, kun käytössä on **työntekijäyksikkö**.</span><span class="sxs-lookup"><span data-stu-id="f292c-124">Excel files can be imported multiple times without any errors using **Employee Entity**.</span></span>

## <a name="known-issue"></a><span data-ttu-id="f292c-125">Tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="f292c-125">Known issue</span></span>

- <span data-ttu-id="f292c-126">**Ongelma**: kun työntekijään lisätään uusi liite, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina.</span><span class="sxs-lookup"><span data-stu-id="f292c-126">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="f292c-127">**Ongelman kiertäminen:** Varmista ennen liitesivun avaamista, että **Työntekijä**-sivun tietoruudut on suljettu.</span><span class="sxs-lookup"><span data-stu-id="f292c-127">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="f292c-128">Jos tietoruudut ovat suljettuja **Työntekijä**-sivua ladattaessa, liitepainikkeet otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="f292c-128">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="f292c-129">(Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)</span><span class="sxs-lookup"><span data-stu-id="f292c-129">(This issue will be fixed in the next platform update.)</span></span>
