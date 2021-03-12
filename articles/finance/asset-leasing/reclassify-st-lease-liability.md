---
title: Lyhytaikaisen vuokrasopimusvelan osan uudelleenluokitteleminen
description: Tässä ohjeaiheessa selitetään, miten voit luoda kuukausittaisen kirjauskansion, jonka avulla voit luokitella vuokrasopimusvelan lyhytaikaiseksi.
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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 08ca824bb4c4a02a80f2187fb5f8fe4e8b7327c9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992911"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="75c6e-103">Lyhytaikaisen vuokrasopimusvelan osan uudelleenluokitteleminen</span><span class="sxs-lookup"><span data-stu-id="75c6e-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75c6e-104">Tässä ohjeaiheessa selitetään, miten voit luoda kuukausittaisen kirjauskansion, jonka avulla voit luokitella vuokrasopimusvelan lyhytaikaiseksi.</span><span class="sxs-lookup"><span data-stu-id="75c6e-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="75c6e-105">Kun aikataulu, joka on valittu eräprosessissa, on **Lyhytaikaisen vuokrasopimusvelan uudelleenluokittelu**, kirjauskansiovienti luodaan.</span><span class="sxs-lookup"><span data-stu-id="75c6e-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="75c6e-106">Tätä vientiä käytetään kirjattaessa vuokrasopimusvelan nykyinen osa kuukauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="75c6e-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="75c6e-107">Samaan aikaan palautusvienti kirjataan seuraavan kuukauden ensimmäisestä päivästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="75c6e-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="75c6e-108">Vuokrasopimusvelan lyhytaikainen osa näkyy velan kuoletusaikataulussa.</span><span class="sxs-lookup"><span data-stu-id="75c6e-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="75c6e-109">Kun kirjauskansiovienti kirjataan, **Velan uudelleenluokituskirjauskansio luotu** -sarake tulee käyttöön ja kirjauskansion tunnus täytetään aikataulussa.</span><span class="sxs-lookup"><span data-stu-id="75c6e-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="75c6e-110">Voit luoda ja kirjata lyhytaikaisen velan uudelleenluokituskirjauskansioviennin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="75c6e-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="75c6e-111">Siirry kohtaan **Resurssin vuokraus \> Kausittainen \> Eräkirjauskansion luominen**.</span><span class="sxs-lookup"><span data-stu-id="75c6e-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="75c6e-112">Valitse **Eräkirjauskansion luominen** -valintaikkunan **Valitse aikataulu** -kentässä **Lyhytaikaisen vuokrasopimusvelan uudelleenluokittelu**.</span><span class="sxs-lookup"><span data-stu-id="75c6e-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="75c6e-113">Valitse **Vuokraryhmä**-kentässä vuokraryhmä.</span><span class="sxs-lookup"><span data-stu-id="75c6e-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="75c6e-114">Voit myös valita kirjan tunnuksen **Kirjan tunnus** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="75c6e-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="75c6e-115">Ota käyttöön **Kirjaa**-parametri.</span><span class="sxs-lookup"><span data-stu-id="75c6e-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="75c6e-116">Vaihtoehtoisesti voit jättää tämän parametrin pois käytöstä, jos vienti luotava mutta ei kirjattava.</span><span class="sxs-lookup"><span data-stu-id="75c6e-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="75c6e-117">Ota käyttöön **Esikatselu ennen kirjaamista** -parametri, jos haluat tarkastella vientiä ennen sen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="75c6e-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="75c6e-118">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="75c6e-118">Select **OK**.</span></span>
