---
title: Kuukausittaisten kirjauskansiovientien luominen erätoimintona
description: Tässä ohje aiheessa selitetään, kuinka kirjauskansiovientejä luodaan eräprosessina. Tämä lisää tehokkuutta, kun kuukausittaiset vuokrakulut tallennetaan.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ca84e56569ea5ddbb4d5335d0944a6bd8a50a1b1
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881201"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="ec6b2-103">Kuukausittaisten kirjauskansiovientien luominen erätoimintona</span><span class="sxs-lookup"><span data-stu-id="ec6b2-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec6b2-104">Tässä ohje aiheessa selitetään, kuinka kirjauskansiovientejä luodaan eräprosessina. Tämä lisää tehokkuutta, kun kuukausittaiset vuokrakulut tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="ec6b2-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="ec6b2-105">Eräkäsittelyn avulla voidaan luoda kirjauskansiovientejä useista aikatauluista.</span><span class="sxs-lookup"><span data-stu-id="ec6b2-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="ec6b2-106">Näitä kirjauskansiovientejä voivat olla maksut, velan kuoletus, käyttöoikeusomaisuuserän kuoletus ja toimeenpanokustannusten kulut.</span><span class="sxs-lookup"><span data-stu-id="ec6b2-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="ec6b2-107">Eräkäsittelyn avulla voit myös tehdä useiden vuokrasopimusten alkuperäisen tuloutuksen samanaikaisesti tai luoda useita siirtymäoikaisuja useille vuokrasopimuksille samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="ec6b2-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="ec6b2-108">Jos haluat määrittää erätyön tai käsitellä useiden vuokrasopimusten laskut, poistot tai korot, siirry kohtaan **Resurssin vuokraus \> Kausittainen \> Eräkirjauskansion luominen**.</span><span class="sxs-lookup"><span data-stu-id="ec6b2-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="ec6b2-109">Näyttöön tulevassa valintaikkunassa voit valita aikataulun, josta kirjauskansioviennit tulee luoda.</span><span class="sxs-lookup"><span data-stu-id="ec6b2-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="ec6b2-110">Voit myös määrittää, suoritetaanko eräkäsittely tietyille entiteeteille, vuokraryhmille vai vuokrasopimuskirjoille.</span><span class="sxs-lookup"><span data-stu-id="ec6b2-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="ec6b2-111">Seuraavat tapahtumat, kuten velan kuoletusaikataulut, maksut, poistot ja kulut, kirjataan vasta, kun vastaavien vuokrasopimusten alkuperäinen tuloutus on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="ec6b2-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="ec6b2-112">Kirjauskansioviennit luodaan, mutta niitä ei kirjata, ennen kuin valitset **Suorita**-komennon.</span><span class="sxs-lookup"><span data-stu-id="ec6b2-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
