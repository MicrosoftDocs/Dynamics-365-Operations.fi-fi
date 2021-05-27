---
title: Taloushallinnon dimensioyhdistelmät
description: Tässä aiheessa kuvataan taloushallinnon dimensioyhdistelmiä ja muutamia niiden käytön optimointivihjeitä.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021825"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="5a67e-103">Taloushallinnon dimensioyhdistelmät</span><span class="sxs-lookup"><span data-stu-id="5a67e-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a67e-104">Tässä aiheessa kuvataan taloushallinnon dimensioyhdistelmiä ja muutamia niiden käytön optimointivihjeitä.</span><span class="sxs-lookup"><span data-stu-id="5a67e-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="5a67e-105">Dimensioyhdistelmä on tilattu luettelo taloushallinnon dimensioista, joita voidaan käyttää kirjanpitotietojen yhteenvetoon käyttäjän määrittämällä tavalla.</span><span class="sxs-lookup"><span data-stu-id="5a67e-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="5a67e-106">Dimensioyhdistelmien ensisijainen käyttö on pääyhdistelmän määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="5a67e-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="5a67e-107">Ainoa vakiodimensioyhdistelmä on dimensioyhdistelmä, joka sisältää vain päätilin.</span><span class="sxs-lookup"><span data-stu-id="5a67e-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="5a67e-108">**Taloushallinnon dimensioyhdistelmät** -sivulla voit luoda ja hallita taloushallinnon dimensioyhdistelmiä.</span><span class="sxs-lookup"><span data-stu-id="5a67e-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="5a67e-109">Dimension asettamat saldot</span><span class="sxs-lookup"><span data-stu-id="5a67e-109">Dimension set balances</span></span>

<span data-ttu-id="5a67e-110">Dimensioyhdistelmällä voi olla saldoja, jotka perustuvat sen taloushallinnon dimensioihin.</span><span class="sxs-lookup"><span data-stu-id="5a67e-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="5a67e-111">Saldot löytyvät kirjanpidosta ja perustuvat dimensioyhdistelmän määritykseen.</span><span class="sxs-lookup"><span data-stu-id="5a67e-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="5a67e-112">Saldojen yhteenveto tehdään kirjanpitotietojen perusteella, jotta niiden suorituskykyä voidaan parantaa niiden noutaessa (esimerkiksi kun pääkirja luodaan).</span><span class="sxs-lookup"><span data-stu-id="5a67e-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="5a67e-113">Luo saldot</span><span class="sxs-lookup"><span data-stu-id="5a67e-113">Create balances</span></span>

<span data-ttu-id="5a67e-114">**Luo saldot** -painikkeella voit alustaa sellaisen dimensioyhdistelmän saldot, jossa ei ole saldoja.</span><span class="sxs-lookup"><span data-stu-id="5a67e-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="5a67e-115">On suositeltavaa rajoittaa saldojen dimensioyhdistelmien määrää, koska saldopäivitykset vaikuttavat kaikkiin kirjanpidon kirjaustapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="5a67e-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="5a67e-116">Päivitä saldot</span><span class="sxs-lookup"><span data-stu-id="5a67e-116">Update balances</span></span>

<span data-ttu-id="5a67e-117">**Päivitä saldot** -painikkeella voit sisällyttää saldoihin viimeisimmän kirjanpidon kirjaustehtävän.</span><span class="sxs-lookup"><span data-stu-id="5a67e-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="5a67e-118">Saldopäivitykset ovat kevyitä toimintoja.</span><span class="sxs-lookup"><span data-stu-id="5a67e-118">Balance updates are light operations.</span></span> <span data-ttu-id="5a67e-119">Niiden täytyy käsitellä vain kirjanpidon kirjaustehtävää, joka on tapahtunut edellisen päivityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="5a67e-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="5a67e-120">Päätaseen näyttö pakottaa päivityksen varmistamaan, että näkyvillä olevat saldot ovat ajan tasalla.</span><span class="sxs-lookup"><span data-stu-id="5a67e-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="5a67e-121">Kannattaa käyttää toistuvaa erätyötä, jotta useimmin käytettyjen dimensioyhdistelmien päivitykset ovat nopeita.</span><span class="sxs-lookup"><span data-stu-id="5a67e-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="5a67e-122">Näin voit vähentää päätasaldoon kuluvaa aikaa, jonka käyttäjien on odotettava.</span><span class="sxs-lookup"><span data-stu-id="5a67e-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="5a67e-123">Muodosta saldot uudelleen</span><span class="sxs-lookup"><span data-stu-id="5a67e-123">Rebuild balances</span></span>

<span data-ttu-id="5a67e-124">**Muodosta uudelleen saldot** -painikkeella voit luoda saldot uudelleen tyhjästä.</span><span class="sxs-lookup"><span data-stu-id="5a67e-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="5a67e-125">Näin voit varmistaa, että ne vastaavat kirjanpidon tietoja.</span><span class="sxs-lookup"><span data-stu-id="5a67e-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="5a67e-126">Saldojen uudelleenrakentaminen edellyttää paljon käsittelyä, eikä sitä yleensä tarvitse tehdä.</span><span class="sxs-lookup"><span data-stu-id="5a67e-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="5a67e-127">Jos tilanne on skenaario, jossa saldot täytyy rakentaa säännöllisesti uudelleen, on suositeltavaa ottaa yhteyttä asiakastukeen.</span><span class="sxs-lookup"><span data-stu-id="5a67e-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="5a67e-128">Asiakastuen avulla voit selvittää, miksi saldot eivät vastaa kirjanpidon tietoja.</span><span class="sxs-lookup"><span data-stu-id="5a67e-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="5a67e-129">Tyhjennä saldot</span><span class="sxs-lookup"><span data-stu-id="5a67e-129">Clear balances</span></span>

<span data-ttu-id="5a67e-130">**Poista saldot** -painikkeella voit poistaa saldot ja lopettaa mahdolliset lisäpäivitykset.</span><span class="sxs-lookup"><span data-stu-id="5a67e-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="5a67e-131">Dimensioyhdistelmä ei enää vaikuta kirjanpidon kirjaustapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="5a67e-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="5a67e-132">Lisätietoja on kohdassa [Taloudelliset dimensiot](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="5a67e-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
