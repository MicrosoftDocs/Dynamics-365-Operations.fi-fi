---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (24. syyskuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
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
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 078b513b828b97a5cfaf613970edd581fb091f9e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551319"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-24-2018"></a><span data-ttu-id="3a083-103">Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (24. syyskuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="3a083-103">What's new or changed in Dynamics 365 Talent - Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3a083-104">**Koontiversio 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="3a083-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="3a083-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="3a083-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="3a083-106">Valuutta lisätty etuihin</span><span class="sxs-lookup"><span data-stu-id="3a083-106">Currency added to Benefits</span></span>

<span data-ttu-id="3a083-107">Etusuunnitelmia on päivitetty sisältämään edun valuutta.</span><span class="sxs-lookup"><span data-stu-id="3a083-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="3a083-108">Tämä uusi kenttä on käytettävissä myös työntekijän kirjatuissa eduissa.</span><span class="sxs-lookup"><span data-stu-id="3a083-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="3a083-109">Uusi kenttä on osa Etujen ylläpito- ja Näytä etuluettelo -suojausoikeutta.</span><span class="sxs-lookup"><span data-stu-id="3a083-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="3a083-110">Suhteellisen jaon prosessin päivittäminen – Lomat ja poissaolot</span><span class="sxs-lookup"><span data-stu-id="3a083-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="3a083-111">Organisaatiot myöntävät poissaoloja eri tavalla sen mukaan, milloin työntekijät liittyvät yritykseen ja lähtevät yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="3a083-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="3a083-112">Kun työntekijät lähtevät organisaatiosta, palkkio voidaan päättää irtisanomispäivänä tai jaksotusprosessi voidaan pysäyttää viimeisenä työpäivänä.</span><span class="sxs-lookup"><span data-stu-id="3a083-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="3a083-113">Nämä muutokset antavat organisaatioille mahdollisuuden valita, milloin ne päättävät työsuhteen irtisanomisprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="3a083-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="3a083-114">Nämä uudet vaihtoehdot kuuluvat työntekijän irtisanomisoikeuksiin ja esimiehen itsepalvelun kautta suoritettavaan työntekijän työsuhteen irtisanomiseen.</span><span class="sxs-lookup"><span data-stu-id="3a083-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="3a083-115">Muut muutokset</span><span class="sxs-lookup"><span data-stu-id="3a083-115">Other changes</span></span>

<span data-ttu-id="3a083-116">Tämä versio sisältää useita muita ohjelmavirhekorjauksia.</span><span class="sxs-lookup"><span data-stu-id="3a083-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="3a083-117">Tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="3a083-117">Known Issue</span></span>

-   <span data-ttu-id="3a083-118">**Ongelma:** Lisättäessä uuden liitteen työntekijään, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina. **Ratkaisuehdotus:** Varmista ennen liitesivun avaamista, että olet sulkenut **Työntekijä**-sivulla olevat tietoruudut.</span><span class="sxs-lookup"><span data-stu-id="3a083-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="3a083-119">Kun tietoruudut on suljettu ladattaessa **Työntekijä**-sivua, Liitteet-painikkeet otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="3a083-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="3a083-120">(Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)</span><span class="sxs-lookup"><span data-stu-id="3a083-120">(This issue will be fixed in the next platform update.)</span></span>
