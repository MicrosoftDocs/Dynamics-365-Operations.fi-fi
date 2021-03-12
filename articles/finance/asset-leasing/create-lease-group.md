---
title: Vuokraryhmän luominen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää vuokraryhmät. Vuokraryhmät ovat pakollisia uusien vuokrasopimusten luomiseksi.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2c06f6f943c8a47fbe650a67017b95d799914a0e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971350"
---
# <a name="create-a-lease-group"></a><span data-ttu-id="c2d4d-104">Vuokraryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="c2d4d-104">Create a lease group</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2d4d-105">Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää vuokraryhmät.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-105">This topic explains how to set up lease groups.</span></span> <span data-ttu-id="c2d4d-106">Vuokraryhmät ovat pakollisia uusien vuokrasopimusten luomiseksi.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-106">Lease groups are required to create new leases.</span></span> <span data-ttu-id="c2d4d-107">Vuokrasopimuskirjat liittyvät kuhunkin vuokraryhmään.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-107">Lease books are associated with each lease group.</span></span> <span data-ttu-id="c2d4d-108">Vuokrasopimusryhmät määrittävät oletuskirjat, jotka jokaiselle vuokrasopimukselle on luotava.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-108">Lease books determine the default books that must be created for each lease.</span></span> <span data-ttu-id="c2d4d-109">Voit määrittää erityistilejä vuokraryhmälle **Vuokrasopimuksen kirjauksen parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-109">You can assign specific accounts to a lease group on the **Lease posting parameters** page.</span></span>

## <a name="create-a-lease-book-and-add-a-lease-group"></a><span data-ttu-id="c2d4d-110">Vuokrasopimuskirjan luominen ja vuokraryhmän lisääminen</span><span class="sxs-lookup"><span data-stu-id="c2d4d-110">Create a lease book and add a lease group</span></span>

1. <span data-ttu-id="c2d4d-111">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokraryhmät**.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-111">Go to **Asset leasing \> Setup \> Lease groups**.</span></span>
2. <span data-ttu-id="c2d4d-112">Lisää vuokraryhmä valitsemalla toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-112">On the Action Pane, select **New** to add a lease group.</span></span> <span data-ttu-id="c2d4d-113">Rivi lisätään ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-113">A line is added to the grid.</span></span>
3. <span data-ttu-id="c2d4d-114">Syötä **Vuokraryhmä**-kentän uudelle riville arvo.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-114">On the new line, in the **Lease group** field, enter a value.</span></span>
4. <span data-ttu-id="c2d4d-115">Anna arvo **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-115">In the **Description** field, enter a value.</span></span>

<span data-ttu-id="c2d4d-116">Juuri syöttämäsi tiedot lisätään **Vuokraryhmä**-kenttään **Lisää vuokrasopimus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-116">The information that you just entered is added to the **Lease group** field on the **Add lease** page.</span></span>

## <a name="associate-a-book-with-a-lease-group"></a><span data-ttu-id="c2d4d-117">Kirjan liittäminen vuokraryhmään</span><span class="sxs-lookup"><span data-stu-id="c2d4d-117">Associate a book with a lease group</span></span>

<span data-ttu-id="c2d4d-118">Kun olet luonut vuokraryhmiä, voit liittää kirjoja kuhunkin ryhmään.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-118">After you create lease groups, you can assign books to each group.</span></span> <span data-ttu-id="c2d4d-119">Kun luot vuokrasopimuksen ja määrität sen vuokraryhmälle, järjestelmä luo kullekin kyseiseen vuokraryhmään liittyvälle kirjalle aikataulujoukon.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-119">When you create a lease and assign it to a lease group, the system creates a set of schedules for each book that is associated with that lease group.</span></span>

> [!NOTE]
> <span data-ttu-id="c2d4d-120">Kirjat on määritettävä, ennen kuin ne voidaan liittää vuokraryhmään.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-120">Books must be set up before they can be assigned to a lease group.</span></span>

1. <span data-ttu-id="c2d4d-121">Siirry kohtaan **Resurssin vuokraus \> Asetukset \> Vuokraryhmä**.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-121">Go to **Asset leasing \> Setup \> Lease group**.</span></span>
2. <span data-ttu-id="c2d4d-122">Valitse vuokraryhmä ja valitse sitten **Kirjat**.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-122">Select a lease group, and then select **Books**.</span></span>
3. <span data-ttu-id="c2d4d-123">Valitse **Uusi** ja valitse sitten **Kirjan tyyppi** -kentässä vuokraryhmään liitettävä kirja.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-123">Select **New**, and then, in the **Book type** field, select the book to assign to the lease group.</span></span> <span data-ttu-id="c2d4d-124">Voit liittää vuokraryhmään useita kirjoja, jos vuokrasopimus on otettava huomioon eri tavoin.</span><span class="sxs-lookup"><span data-stu-id="c2d4d-124">You can assign multiple books to a lease group if a lease must be accounted for in different ways.</span></span>
