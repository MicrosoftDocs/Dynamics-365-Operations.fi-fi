---
title: Nimike, missä käytetty
description: Tässä ohjeaiheessa selitetään, miten voit saada yleiskuvan siitä, missä nimikettä käytetään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 476b01a4bae34a271203f34481ff18042783d4df
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811260"
---
# <a name="item-where-used"></a><span data-ttu-id="e7b24-103">Nimike, missä käytetty</span><span class="sxs-lookup"><span data-stu-id="e7b24-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e7b24-104">Voit tehdä tietyn nimikkeen laskennan saadaksesi yhteenvedon siitä, missä nimikettä on käytetty käyttöomaisuuden hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="e7b24-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="e7b24-105">Tuloksissa näkyy konteksti, jossa nimikettä on käytetty sen elinkaaren aikana.</span><span class="sxs-lookup"><span data-stu-id="e7b24-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="e7b24-106">**Nimike, missä käytetty** -sivu voidaan avata resurssienhallinnan päävalikosta, ja sitä voi käyttää myös seuraavilta sivuilta:</span><span class="sxs-lookup"><span data-stu-id="e7b24-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="e7b24-107">Resurssien tuoterakenteet</span><span class="sxs-lookup"><span data-stu-id="e7b24-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="e7b24-108">Varaosat oletusresurssityypeissä</span><span class="sxs-lookup"><span data-stu-id="e7b24-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="e7b24-109">Ylläpitotöiden tyyppiluokat ja ylläpitotöiden tyypit, ylläpitotöiden tyyppien variantit, ylläpitotöiden toimialat ja ylläpidon tarkistuslistat</span><span class="sxs-lookup"><span data-stu-id="e7b24-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="e7b24-110">Ylläpitoennuste</span><span class="sxs-lookup"><span data-stu-id="e7b24-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="e7b24-111">Osto ja hankinta</span><span class="sxs-lookup"><span data-stu-id="e7b24-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="e7b24-112">Työtilaus osto</span><span class="sxs-lookup"><span data-stu-id="e7b24-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="e7b24-113">Nimike, missä käytetty -laskelman suorittaminen.</span><span class="sxs-lookup"><span data-stu-id="e7b24-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="e7b24-114">Valitse **Resurssien hallinta** > **Kyselyt** > **Nimike, missä käytetty**tai valitse **Nimike, missä käytetty** -painike on jollakin edellä mainituista sivuista.</span><span class="sxs-lookup"><span data-stu-id="e7b24-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="e7b24-115">Valitse **Nimike, missä käytetty** -valintaikkunassa nimike, jolle haluat tehdä laskun **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e7b24-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="e7b24-116">**Taso** -kentän avulla voit määrittää, miten yksityiskohtaisia nimikeriveistä haluat liittyen toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="e7b24-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="e7b24-117">Jos esimerkiksi lisäät kenttään arvon "1" ja kyseessä on monitasoinen toiminnallinen sijaintirakenne, kaikki toimintosijainnin nimikerivit näkyvät ylimmällä tasolla.</span><span class="sxs-lookup"><span data-stu-id="e7b24-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="e7b24-118">Tämän vuoksi rivin suhde/määrä voidaan lisätä toiminnallisista sijainneista, jotka sijaitsevat alemmalla tasolla.</span><span class="sxs-lookup"><span data-stu-id="e7b24-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="e7b24-119">Jos lisäät arvon "0" **Taso**-kenttään, näkyviin tulee yksityiskohtainen tulos, jossa näkyvät kaikki nimikerivit kaikissa niissä toiminnallisissa sijaintitasoissa, joihin ne liittyvät.</span><span class="sxs-lookup"><span data-stu-id="e7b24-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="e7b24-120">Valitse **Sisällytä** -osan vaihtopainikkeissa arvoksi Kyllä, jos haluat sisällyttää kohteen laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="e7b24-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="e7b24-121">Aloita laskenta valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7b24-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="e7b24-122">Valitse **Nimike, missä käytetty** -välilehden asiaankuuluvat **Ryhmittely ...**-painikkeet tuodaksesi näkyviin laskun vaaditun yksityiskohtaisuuden tason.</span><span class="sxs-lookup"><span data-stu-id="e7b24-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="e7b24-123">Valitut **Ryhmittely...**-painikkeet on korostettu.</span><span class="sxs-lookup"><span data-stu-id="e7b24-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="e7b24-124">Aktivoi painike tai poista se käytöstä napsauttamalla painiketta.</span><span class="sxs-lookup"><span data-stu-id="e7b24-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="e7b24-125">Jos haluat näyttää nimikkeeseen liittyvät dimensiot, valitse **Näytä dimensiot**ja valitse näytettävät dimensiot.</span><span class="sxs-lookup"><span data-stu-id="e7b24-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="e7b24-126">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="e7b24-126">Example</span></span>

<span data-ttu-id="e7b24-127">Alla olevassa näyttökuvassa on esimerkki nimikkeestä, jossa on laskettu Nimike, missä käytetty -lasku nimiketunnukselle "1000".</span><span class="sxs-lookup"><span data-stu-id="e7b24-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Esimerkki nimikkeen käyttöpaikan laskennasta](media/12-controlling-and-reporting.png)

