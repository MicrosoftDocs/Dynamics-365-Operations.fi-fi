---
title: Oikaisukirjauskansioviennit siirtymän jälkeen resurssin vuokrauksessa
description: Tässä ohjeaiheessa kerrotaan toiminnoista, joiden avulla vuokrauksen portfolio voidaan siirtää uusiin vuokrauksen kirjanpitostandardeihin, ASC 842:een ja IFRS 16:een.
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
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969550"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="a0927-103">Oikaisukirjauskansioviennit siirtymän jälkeen resurssin vuokrauksessa</span><span class="sxs-lookup"><span data-stu-id="a0927-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0927-104">Tässä ohjeaiheessa kerrotaan toiminnoista, joiden avulla vuokrauksen portfolio voidaan siirtää uusiin vuokrauksen kirjanpitostandardeihin: ASC 842 (Accounting Standards Codification Topic 842), joka on US GAAP:n Yhdysvaltojen yleisti hyväksytty kirjanpitostardardi, ja IFRS 16 (International Financial Reporting Standard 16).</span><span class="sxs-lookup"><span data-stu-id="a0927-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="a0927-105">Lisätietoja kirjan määrittämisestä uusiin standardeihin siirtymistä varten on kohdassa [Vuokrasopimuskirjojen määrittäminen](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="a0927-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="a0927-106">Kun luot siirtymän oikaisukirjauskansioviennin, luodaan kirjauskansiovienti.</span><span class="sxs-lookup"><span data-stu-id="a0927-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="a0927-107">Tämä vienti vaikuttaa taseeseen tallentamalla vuokrauksen tänä päivänä uusien standardien mukaan.</span><span class="sxs-lookup"><span data-stu-id="a0927-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="a0927-108">Soveltuvaa resurssitiliä veloitetaan kyseisen päivän kirjanpitoarvon mukaan, ja velkatiliä hyvitetään.</span><span class="sxs-lookup"><span data-stu-id="a0927-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="a0927-109">Ero veloitetaan jäljellä olevista tuotoista tai hyvitetään niille.</span><span class="sxs-lookup"><span data-stu-id="a0927-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="a0927-110">Voit kirjata siirtymän oikaisun uusien kirjanpitostandardien mukaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a0927-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="a0927-111">Valitse **Vuokrasopimusyhteenveto**-sivulla vuokrasopimus ja valitse sitten **Kirjat**.</span><span class="sxs-lookup"><span data-stu-id="a0927-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="a0927-112">Valitse kirjassa **Maksuaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="a0927-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="a0927-113">Valitse **Maksuaikataulu**-valintaikkunassa **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="a0927-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="a0927-114">Sulje sitten valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="a0927-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="a0927-115">Valitse **Siirtymän oikaisu**.</span><span class="sxs-lookup"><span data-stu-id="a0927-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0927-116">Siirtymän oikaisu voidaan luoda vain vuokrasopimuskirjoissa, jotka on liitetty kirjaan, jossa **Siirtymäkirja**-kenttä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a0927-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="a0927-117">Jos **Vuokrauksen alkaminen** -kentän arvo on myöhempi kuin siirron päivämäärä, **Siirtymän oikaisu** -kentän arvoa ei päivitetä.</span><span class="sxs-lookup"><span data-stu-id="a0927-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="a0927-118">Jos haluat tarkastella kirjauskansiovientiä, valitse **Resurssin leasingkirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="a0927-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="a0927-119">Valitse uusi kirjauskansio ja valitse sitten **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="a0927-119">Select the new journal, and then select **Post**.</span></span>
