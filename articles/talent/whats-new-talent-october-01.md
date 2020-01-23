---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (1. lokakuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 10/01/2018
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
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f872b0907e0f48e0b734c87f0b8fb1a4cfe20cb0
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896678"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-1-2018"></a><span data-ttu-id="7d0ce-103">Dynamics 365 Talent: Core HR:n uudet tai muuttuneet ominaisuudet (1. lokakuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="7d0ce-103">What's new or changed in Dynamics 365 Talent: Core HR (October 1, 2018)</span></span>

<span data-ttu-id="7d0ce-104">**Koontiversio 8.1.1035.0**</span><span class="sxs-lookup"><span data-stu-id="7d0ce-104">**Build 8.1.1035.0**</span></span>

<span data-ttu-id="7d0ce-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="turn-off-electronic-payment-validation"></a><span data-ttu-id="7d0ce-106">Sähköisten maksujen oikeellisuustarkistuksen poistaminen käytöstä</span><span class="sxs-lookup"><span data-stu-id="7d0ce-106">Turn off electronic payment validation</span></span>

<span data-ttu-id="7d0ce-107">Sähköisten maksujen tietojen oikeellisuustarkistus suoritetaan, jos määritit suoritukset suoraa talletusta varten joko **Työntekijän itsepalvelun** työtilassa (ESS) tai suoraan työntekijän lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-107">Electronic payment information validation occurs if you set up disbursements for direct deposit either through **Employee self-service** workspace (ESS) or directly on the employee form.</span></span> <span data-ttu-id="7d0ce-108">Tämän vaihtoehdon avulla voit joustavasti poistaa oikeellisuustarkistuksen, jos sitä ei tarvita määrien ja jäännösarvojen oikeellisuustarkistuksia varten.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-108">This option gives you the flexibility to remove that validation if you do not require the validation checks for amounts and remainder values.</span></span> <span data-ttu-id="7d0ce-109">Tämä toiminto on hyödyllinen integroitaessa ulkoista palkkajärjestelmää, jossa on erilaiset vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-109">This feature is helpful if you're integrating with an external payroll system that has different requirements.</span></span>

## <a name="manager-self-service---add-goals-for-team-members-through-the-team-performance-goals-tile"></a><span data-ttu-id="7d0ce-110">Esimiehen itsepalvelu – Lisää tavoitteet tiimin jäsenille Tiimin suorituskykytavoitteet -ruudussa</span><span class="sxs-lookup"><span data-stu-id="7d0ce-110">Manager self-service - Add goals for team members through the Team performance goals tile</span></span>

<span data-ttu-id="7d0ce-111">Ennen tätä versiota esimiehet pystyivät lisäämään tavoitteita työntekijöille erikseen kuhunkin työntekijään liittyvien suorituskykytavoitteiden kautta.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-111">Prior to this release, managers can add goals to their employees individually through the performance goals associated to each employee.</span></span> <span data-ttu-id="7d0ce-112">Tämän päivityksen myötä esimiehet voivat luoda **Tiimin suorituskykytavoitteet** -ruudussa uusia tavoitteita valitsemalla jonkin suoran alaisensa.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-112">With this update, managers can access the **Team performance goals** tile and create new goals by selecting any of their direct reports.</span></span>

## <a name="manager-self-service---add-reviews-for-team-members-through-the-team-performance-reviews-tile"></a><span data-ttu-id="7d0ce-113">Esimiehen itsepalvelu – Lisää arvioinnit tiimin jäsenille Tiimin suorituskykyarvioinnit -ruudussa</span><span class="sxs-lookup"><span data-stu-id="7d0ce-113">Manager self-service - Add reviews for team members through the Team performance reviews tile</span></span>

<span data-ttu-id="7d0ce-114">Ennen tätä versiota esimiehet pystyivät lisäämään arvioita työntekijöille erikseen kuhunkin työntekijään liittyvien arviointien kautta.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-114">Prior to this release, managers can add reviews to their employees individually through the reviews associated to each employee.</span></span> <span data-ttu-id="7d0ce-115">Tämän päivityksen myötä esimiehet voivat luoda **Tiimin suorituskykyarvioinnit** -ruudussa uusia arviointeja valitsemalla jonkin suoran alaisensa.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-115">With this update, managers can access the **Team performance reviews** tile and create new reviews by selecting any of their direct reports.</span></span>

## <a name="configure-proration-options-by-leave-plan"></a><span data-ttu-id="7d0ce-116">Suhteellisen jaon asetusten määrittäminen lomasuunnitelman mukaan</span><span class="sxs-lookup"><span data-stu-id="7d0ce-116">Configure proration options by leave plan</span></span>

<span data-ttu-id="7d0ce-117">Organisaatiot myöntävät poissaoloja eri tavalla sen mukaan, milloin työntekijät liittyvät yritykseen ja lähtevät yrityksestä.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-117">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="7d0ce-118">Joissakin organisaatioissa työntekijät saavat palkkion täysimääräisen kohdistuksen aloituspäivänä kun taas toisissa palkkioon sovelletaan suhteellista jakoa.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-118">For some organizations, employees are awarded their full allocation on their start date while others prorate the award.</span></span> <span data-ttu-id="7d0ce-119">Tässä versiossa on uusia vaihtoehtoja sen valintaan, miten palkkioiden ja jaksotusten suhteellista jakoa sovelletaan työntekijöihin, jotka liittyvät organisaatioon tai lähtevät siitä.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-119">New options are provided in this release to choose how to prorate the awards and accruals for joiners and leavers in an organization.</span></span> <span data-ttu-id="7d0ce-120">Vaihtoehtoja ovat suhteutettu, täysi jaksotus ja ei jaksotusta.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-120">Options include: Prorated, Full accrual, and No accrual.</span></span>

## <a name="other-changes"></a><span data-ttu-id="7d0ce-121">Muut muutokset</span><span class="sxs-lookup"><span data-stu-id="7d0ce-121">Other changes</span></span>

-   <span data-ttu-id="7d0ce-122">Työntekijän yksikköä päivitetty – **Henkilötiedot**-ruutua voidaan nyt päivittää Excel-lisäosien/tietojen hallinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-122">Employee entity updated - The **Personal** title can now be updated using the Excel add-in/data management.</span></span>

-   <span data-ttu-id="7d0ce-123">Suojauksen muutos, jotta voidaan poistaa **Poista**- ja **Poista aktivointi** -painikkeet työntekijän itsepalvelussa maksutietojen osalta.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-123">Security change to allow removal of the **Delete** and **Deactivate** buttons in employee self-service for payment information.</span></span>

## <a name="known-issue"></a><span data-ttu-id="7d0ce-124">Tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="7d0ce-124">Known issue</span></span>

-   <span data-ttu-id="7d0ce-125">**Ongelma:** Lisättäessä uuden liitteen työntekijään, **Uusi**- ja **Muokkaa**-painikkeet näkyvät harmaina. **Ratkaisuehdotus:** Varmista ennen liitesivun avaamista, että olet sulkenut **Työntekijä**-sivulla olevat tietoruudut.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-125">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="7d0ce-126">Kun tietoruudut on suljettu ladattaessa **Työntekijä**-sivua, **Liitteet**-painikkeet otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7d0ce-126">If the FactBoxes are closed when the **Worker** page is loaded, the **Attachments** buttons will be enabled.</span></span> <span data-ttu-id="7d0ce-127">(Tämä ongelma korjataan seuraavassa ympäristöpäivityksessä.)</span><span class="sxs-lookup"><span data-stu-id="7d0ce-127">(This issue will be fixed in the next platform update.)</span></span>
