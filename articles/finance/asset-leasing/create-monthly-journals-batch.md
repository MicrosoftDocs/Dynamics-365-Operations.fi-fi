---
title: Kuukausittaisten kirjauskansiovientien luominen erätoimintona
description: Tässä ohje aiheessa selitetään, kuinka kirjauskansiovientejä luodaan eräprosessina. Tämä lisää tehokkuutta, kun kuukausittaiset vuokrakulut tallennetaan.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a2293f6bd3ce66832996652c3bfca0fc4bc73782
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442966"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="cda2b-103">Kuukausittaisten kirjauskansiovientien luominen erätoimintona</span><span class="sxs-lookup"><span data-stu-id="cda2b-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cda2b-104">Tässä ohje aiheessa selitetään, kuinka kirjauskansiovientejä luodaan eräprosessina. Tämä lisää tehokkuutta, kun kuukausittaiset vuokrakulut tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="cda2b-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="cda2b-105">Eräkäsittelyn avulla voidaan luoda kirjauskansiovientejä useista aikatauluista.</span><span class="sxs-lookup"><span data-stu-id="cda2b-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="cda2b-106">Näitä kirjauskansiovientejä voivat olla maksut, velan kuoletus, käyttöoikeusomaisuuserän kuoletus ja toimeenpanokustannusten kulut.</span><span class="sxs-lookup"><span data-stu-id="cda2b-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="cda2b-107">Eräkäsittelyn avulla voit myös tehdä useiden vuokrasopimusten alkuperäisen tuloutuksen samanaikaisesti tai luoda useita siirtymäoikaisuja useille vuokrasopimuksille samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="cda2b-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="cda2b-108">Jos haluat määrittää erätyön tai käsitellä useiden vuokrasopimusten laskut, poistot tai korot, siirry kohtaan **Resurssin vuokraus \> Kausittainen \> Eräkirjauskansion luominen**.</span><span class="sxs-lookup"><span data-stu-id="cda2b-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="cda2b-109">Näyttöön tulevassa valintaikkunassa voit valita aikataulun, josta kirjauskansioviennit tulee luoda.</span><span class="sxs-lookup"><span data-stu-id="cda2b-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="cda2b-110">Voit myös määrittää, suoritetaanko eräkäsittely tietyille entiteeteille, vuokraryhmille vai vuokrasopimuskirjoille.</span><span class="sxs-lookup"><span data-stu-id="cda2b-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="cda2b-111">Seuraavat tapahtumat, kuten velan kuoletusaikataulut, maksut, poistot ja kulut, kirjataan vasta, kun vastaavien vuokrasopimusten alkuperäinen tuloutus on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="cda2b-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="cda2b-112">Kirjauskansioviennit luodaan, mutta niitä ei kirjata, ennen kuin valitset **Suorita**-komennon.</span><span class="sxs-lookup"><span data-stu-id="cda2b-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>
