---
title: Luo työtilauksia ylläpitopyynnöistä
description: Tässä ohjeaiheessa kerrotaan, kuinka työtilauksia luodaan ylläpitopyynnöistä resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23039306bb827beb861eaacc3177f4917fabc8bf
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018093"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="b638b-103">Luo työtilauksia ylläpitopyynnöistä</span><span class="sxs-lookup"><span data-stu-id="b638b-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="b638b-104">Kun olet luonut ylläpitopyyntöjä, voit helposti muuntaa ne työtilauksiksi.</span><span class="sxs-lookup"><span data-stu-id="b638b-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="b638b-105">Tässä aiheessa kuvataan nopein tapa käsitellä ylläpitopyyntöjä, päivittää useita ylläpitopyyntöjä samanaikaisesti ja luoda sitten työtilaus useille ylläpitopyynnöille samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="b638b-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="b638b-106">**Aktiiviset ylläpitopyynnöt** -tai **Omat toiminnallisen sijainnin ylläpitopyynnöt** -sivulla voit käsitellä myös yhtä ylläpitopyyntöä kerrallaan ja muuntaa yhdenylläpito pyynnön työtilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="b638b-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="b638b-107">Jokainen ylläpitopyyntö voi liittyä vain yhteen työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="b638b-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="b638b-108">Useita ylläpitopyyntöjä voidaan kuitenkin sisällyttää yhteen työtilaukseen, vaikka ylläpitopyynnöissä olisi eri resurssit.</span><span class="sxs-lookup"><span data-stu-id="b638b-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="b638b-109">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Kaikki ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="b638b-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="b638b-110">Ennen kuin voit luoda työtilauksen ylläpitopyynnöitä, sinun on valittava vähintään ylläpitotöiden tyyppi ylläpitopyyntöjä varten ja myös ylläpitotyön tyypin variantti ja ala, jos nämä tiedot ovat merkityksellisiä.</span><span class="sxs-lookup"><span data-stu-id="b638b-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="b638b-111">Voit helposti päivittää ylläpitopyynnön tiedot ruudukkonäkymässä.</span><span class="sxs-lookup"><span data-stu-id="b638b-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="b638b-112">Kun olet valmis luomaan työtilauksen, valitse siihen sisällytettävät ylläpitopyynnöt.</span><span class="sxs-lookup"><span data-stu-id="b638b-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="b638b-113">Jos valitset useita ylläpitopyyntöjä, jotka muunnetaan työtilaukseksi, sekä **Resurssit**-kenttä että **Ylläpitotyön tyyppi** -kenttä on määritettävä ennen työtilauksen luomista.</span><span class="sxs-lookup"><span data-stu-id="b638b-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="b638b-114">Jos valitset yhden ylläpitopyynnön, joka muunnetaan työtilaukseksi, vain **Resurssit**-kenttä on määritettävä ennen työtilauksen luomista.</span><span class="sxs-lookup"><span data-stu-id="b638b-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="b638b-115">Kun luot työtilauksen, voit kuitenkin valita ylläpitotyön tyypin (ja siihen liittyvän ylläpitotyön tyypin variantin ja alan, jos nämä tiedot ovat merkityksellisiä) **Luo työtilaus**  valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="b638b-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="b638b-116">Valitse **Työtilaus**.</span><span class="sxs-lookup"><span data-stu-id="b638b-116">Select **Work order**.</span></span>
5. <span data-ttu-id="b638b-117">Määritä **Luo työtilaus** -valintaikkunassa kentät ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="b638b-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="b638b-118">Sanomapalkki saattaa ilmoittaa, että uusi työtilaus on luotu.</span><span class="sxs-lookup"><span data-stu-id="b638b-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="b638b-119">Lisäksi kun luot ylläpitopyyntöön perustuvan työtilauksen ja jos ylläpitopyyntöön liittyvä resurssi sisältyy takuusopimukseen, sanomapalkki ilmoittaa sinulle takuusopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="b638b-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="b638b-120">Valitse **Resurssien hallinta** \> **Yhteiset** \> **Työtilaukset** \> **Kaikki työtilaukset** ja avaa uusi työtilaus.</span><span class="sxs-lookup"><span data-stu-id="b638b-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Uuden työtilauksen avaaminen](media/05-manage-maintenance-requests.png)

