---
title: Resurssien vuokrauksen käytännöt
description: Tässä ohjeaiheessa käsitellään vuokratun käyttöomaisuuden menetelmiä.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ea89d54f1ce3a1e971d41623bf44f909f7dfdf09
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131281"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="3fb36-103">Resurssien vuokrauksen käytännöt</span><span class="sxs-lookup"><span data-stu-id="3fb36-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fb36-104">Tässä ohjeaiheessa käsitellään vuokratun käyttöomaisuuden menetelmiä.</span><span class="sxs-lookup"><span data-stu-id="3fb36-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="3fb36-105">Vuokramenetelmien avulla määritetään vuokrakirjan aloitusaika.</span><span class="sxs-lookup"><span data-stu-id="3fb36-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="3fb36-106">Jos vuokramenetelmäksi on määritetty **Ei mitään**, aloitupäivämäärä on sama kuin vuokran alkamispäivämäärä (**Vuokran alkamispäivämäärä** -kentän arvo).</span><span class="sxs-lookup"><span data-stu-id="3fb36-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="3fb36-107">Jos vuokramenetelmäksi määritetään **Täysi kuukausi**, aloituspäivä on sen kuukauden ensimmäinen päivä, johon vuokra alkaminen sijoittuu.</span><span class="sxs-lookup"><span data-stu-id="3fb36-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="3fb36-108">Aloituspäivä määrittää velan kuoletuksen ja käyttöomaisuuden poistoaikataulujen kauden alkamispäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="3fb36-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="3fb36-109">Korkokulut ja poistokulut kirjataan vastaavien aikataulujen kauden päättymispäivänä.</span><span class="sxs-lookup"><span data-stu-id="3fb36-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="3fb36-110">Alkuperäinen kirjaus ja oikaisukirjauskansion kirjaus kirjataan aloituspäivänä.</span><span class="sxs-lookup"><span data-stu-id="3fb36-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="3fb36-111">Vuokramenetelmien ominaisuus voidaan ottaa käyttöön ominaisuuksien hallinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="3fb36-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="3fb36-112">Etsi ja valitse **Ominaisuuksien hallinta** -työtilassa toiminto, jonka nimi on **Käyttöomaisuuden vuokrauksen vuokramenetelmät** ja valitse sitten **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="3fb36-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="3fb36-113">Vuokramenetelmät liitetään vuokrakäyttöomaisuuskirjan asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="3fb36-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="3fb36-114">Voit tarkastella tai määrittää vuokramenetelmän noudattamalla näitä vaiheita.</span><span class="sxs-lookup"><span data-stu-id="3fb36-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="3fb36-115">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokrasopimuskirjat**.</span><span class="sxs-lookup"><span data-stu-id="3fb36-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="3fb36-116">Valitse **Vuokramenetelmä** -kentästä jokin seuraavista arvoista.</span><span class="sxs-lookup"><span data-stu-id="3fb36-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="3fb36-117">Leasing-käytäntö</span><span class="sxs-lookup"><span data-stu-id="3fb36-117">Leasing convention</span></span> | <span data-ttu-id="3fb36-118">kuvaus</span><span class="sxs-lookup"><span data-stu-id="3fb36-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="3fb36-119">None</span><span class="sxs-lookup"><span data-stu-id="3fb36-119">None</span></span>               | <span data-ttu-id="3fb36-120">Velan kuoletuksen ja käyttöomaisuuden poistosuunnitelmat alkavat vuokrauksen alkamispäivämääränä, koska aloituspäivä on sama kuin vuokrauksen alkamispäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="3fb36-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="3fb36-121">Päättymispäivä on kuukautta myöhempi.</span><span class="sxs-lookup"><span data-stu-id="3fb36-121">The end date is one month later.</span></span> <span data-ttu-id="3fb36-122">Tämä vuokramenetelmä ei takaa, että korko kirjataan kunkin kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="3fb36-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="3fb36-123">Täysi kuukausi</span><span class="sxs-lookup"><span data-stu-id="3fb36-123">Full month</span></span>         | <span data-ttu-id="3fb36-124">Jos vuokralla on alkamispäivämäärä, joka tapahtuu milloin tahansa kuukauden aikana, velan kuoletuksen ja käyttöomaisuuden poistosuunnitelmat alkavat kerryttää kuluja kyseisen kuukauden ensimmäisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="3fb36-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="3fb36-125">Tämä vuokramenetelmä varmistaa, että korkoa kertyy kunkin kuukauden viimeisenä päivänä koko kuukaudelle.</span><span class="sxs-lookup"><span data-stu-id="3fb36-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="3fb36-126">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3fb36-126">Select **Save**.</span></span>

<span data-ttu-id="3fb36-127">Kun vuokra luodaan, kunkin kirjan aloituspäivä lisätään automaattisesti vuokralle syötettyyn alkamispäivämäärään ja kirjalle määritettyyn vuokramenetelmään.</span><span class="sxs-lookup"><span data-stu-id="3fb36-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>