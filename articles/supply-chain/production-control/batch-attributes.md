---
title: Erämääritteet
description: Tässä ohjeaiheessa on tietoja erämääritteistä. Erämääritteet ovat varastoeriä muodostavien raaka-aineiden ja valmiiden tuotteiden ominaisuuksia. Ohjeaiheessa selvitetään myös, kuinka erämääritteitä määritetään ja kuinka niitä voi hakea eriä varattaessa.
author: ShylaThompson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsBatchAttrib, PdsBatchAttribAssociate, PdsBatchAttribByAttribGroup, PdsBatchAttribByItem, PdsBatchAttribByitemCustomer, PdsBatchAttribGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19271
ms.assetid: 41de0250-4a96-412e-a412-aa06615b6b1d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 325e647185e3eb4c0eacdfd00c320804e31ddb48
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "347626"
---
# <a name="batch-attributes"></a><span data-ttu-id="6b39d-105">Erämääritteet</span><span class="sxs-lookup"><span data-stu-id="6b39d-105">Batch attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b39d-106">Tässä ohjeaiheessa on tietoja erämääritteistä.</span><span class="sxs-lookup"><span data-stu-id="6b39d-106">This topic provides information about batch attributes.</span></span> <span data-ttu-id="6b39d-107">Erämääritteet ovat varastoeriä muodostavien raaka-aineiden ja valmiiden tuotteiden ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="6b39d-107">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="6b39d-108">Ohjeaiheessa selvitetään myös, kuinka erämääritteitä määritetään ja kuinka niitä voi hakea eriä varattaessa.</span><span class="sxs-lookup"><span data-stu-id="6b39d-108">The topic also explains how to assign batch attributes, and how you can search on them when you reserve batches.</span></span>

<span data-ttu-id="6b39d-109">Erämääritteet ovat varastoeriä muodostavien raaka-aineiden ja valmiiden tuotteiden ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="6b39d-109">Batch attributes are characteristics of raw materials and finished products that make up inventory batches.</span></span> <span data-ttu-id="6b39d-110">Erämääritteet voivat vaihdella monen tekijän, esimerkiksi ympäristöolosuhteiden, erän tuottamiseen käytettävien raaka-aineiden laadun tai tuloksena syntyvän lopputuotteen mukaan.</span><span class="sxs-lookup"><span data-stu-id="6b39d-110">Batch attributes can vary, depending on factors such as environmental conditions, the quality of the raw materials that are used to produce the batch, or the outcome of the finished product.</span></span> <span data-ttu-id="6b39d-111">Erämääritteiden määrä ja tyypit voivat vaihdella paljon eri toimialojen välillä.</span><span class="sxs-lookup"><span data-stu-id="6b39d-111">The number and types of batch attributes that are used can vary widely from one industry to another.</span></span> <span data-ttu-id="6b39d-112">Seuraavassa on kaksi esimerkkiä erämääritteiden käyttämisestä:</span><span class="sxs-lookup"><span data-stu-id="6b39d-112">Here are two examples that show how to use batch attributes:</span></span>

-   <span data-ttu-id="6b39d-113">Juustoteollisuudessa maito on yksi juuston raaka-aineista, jolla on eri määritteitä, kuten rasvapitoisuus ja prosenttipaino.</span><span class="sxs-lookup"><span data-stu-id="6b39d-113">In the cheese industry, milk, which is one of the raw materials that are used to produce the cheese, can have attributes such as fat content and percentage weight.</span></span> <span data-ttu-id="6b39d-114">Maidosta tuotetulla juustolla voi olla muita määritteitä, kuten kosteus ja ikä.</span><span class="sxs-lookup"><span data-stu-id="6b39d-114">The cheese that is produced from the milk can have other attributes, such as moisture and age.</span></span>
-   <span data-ttu-id="6b39d-115">Terästeollisuudessa valmistetulla raudalla voi olla määritteitä, kuten magnesiumpitoisuus, hopeapitoisuus ja sinkkipitoisuus prosentteina.</span><span class="sxs-lookup"><span data-stu-id="6b39d-115">In the steel industry, the iron that is produced might have attributes such as the percentages of magnesium content, silver content, and zinc content.</span></span>

<span data-ttu-id="6b39d-116">Määritteiden määrää ja tyyppiä on helpompi hallita erämääriteryhmien avulla.</span><span class="sxs-lookup"><span data-stu-id="6b39d-116">To better manage the number and types of attributes, you can use batch attribute groups.</span></span> <span data-ttu-id="6b39d-117">Näin jokaista määritettä ei tarvitse lisätä erikseen.</span><span class="sxs-lookup"><span data-stu-id="6b39d-117">In this way, you don't have to add each attribute individually.</span></span>

## <a name="assign-batch-attributes"></a><span data-ttu-id="6b39d-118">Erämääritteiden liittäminen</span><span class="sxs-lookup"><span data-stu-id="6b39d-118">Assign batch attributes</span></span>
<span data-ttu-id="6b39d-119">Erämääritteet liitetään yksittäisiin tuotteisiin, joita pidetään varastoerissä, tai tuotteisiin, jotka liittyvät tiettyihin asiakkaisiin.</span><span class="sxs-lookup"><span data-stu-id="6b39d-119">You can assign batch attributes to individual products that are held in inventory batches, or you can assign them to products that are associated with specific customers.</span></span> <span data-ttu-id="6b39d-120">Ennen kuin liität erämääritteen asiakastasolla, se täytyy liittää tuotetasolla.</span><span class="sxs-lookup"><span data-stu-id="6b39d-120">Before you can assign a batch attribute at the customer level, you must assign it at the product level.</span></span> <span data-ttu-id="6b39d-121">Tuotteen erädimensioksi on määritettävä **Aktiivinen** seurantadimensioryhmässä.</span><span class="sxs-lookup"><span data-stu-id="6b39d-121">The product must have the batch dimension set to **Active** in the tracking dimension group.</span></span> <span data-ttu-id="6b39d-122">Jos haluat määrittää erämääritteen yksittäiselle tuotteelle, käytä kyseisen tuotteen sivua.</span><span class="sxs-lookup"><span data-stu-id="6b39d-122">To assign a batch attribute to an individual product, use the product-specific page.</span></span> <span data-ttu-id="6b39d-123">Jos määrite koskee tietyn asiakkaan tuotetta, käytä kyseisen asiakkaan sivua.</span><span class="sxs-lookup"><span data-stu-id="6b39d-123">If the attribute is specific to a product for a customer, use the customer-specific page.</span></span> <span data-ttu-id="6b39d-124">Kun lisäät tuotteeseen määritettä, määritä myös muut parametrit.</span><span class="sxs-lookup"><span data-stu-id="6b39d-124">When you add an attribute to a product, you also define other parameters.</span></span> <span data-ttu-id="6b39d-125">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="6b39d-125">Here are some examples:</span></span>

-   <span data-ttu-id="6b39d-126">Määritetyyppien **Kokonaisluku** ja **Nimellinen** minimi- ja maksimialueet.</span><span class="sxs-lookup"><span data-stu-id="6b39d-126">The minimum and maximum ranges for an attribute of the **Integer** or **Fraction** type.</span></span>
-   <span data-ttu-id="6b39d-127">Toleranssitoiminnot määritteelle, jonka tyyppi on **Kokonaisluku** tai **Nimellinen**.</span><span class="sxs-lookup"><span data-stu-id="6b39d-127">The tolerance actions for an attribute of the **Integer** or **Fraction** type.</span></span> <span data-ttu-id="6b39d-128">Jos määritteen arvo on minimi- ja maksimialueen ulkopuolella, toimenpide voi olla varoitus- tai virheilmoitus.</span><span class="sxs-lookup"><span data-stu-id="6b39d-128">If the value of the attribute falls outside the minimum and maximum range, the action can be either a warning message or an error message.</span></span>
-   <span data-ttu-id="6b39d-129">Määritteen kohdearvo.</span><span class="sxs-lookup"><span data-stu-id="6b39d-129">The target value for the attribute.</span></span> <span data-ttu-id="6b39d-130">Arvo on määritteen optimaalinen arvo, joka koskee kaikkia määritetyyppejä.</span><span class="sxs-lookup"><span data-stu-id="6b39d-130">This value is the optimal value of the attribute, and it applies to all attribute types.</span></span>

<span data-ttu-id="6b39d-131">Voit käyttää **Vapautetut tuotteet** -sivulla valittujen tuotteiden sivuja Tuotetietojen hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="6b39d-131">You can access the pages for products that you select on the **Released products** page in Product information management.</span></span> <span data-ttu-id="6b39d-132">Kun olet liittänyt erämääritteet tuotteeseen, voit lisätä määritteille arvoja **Varastoerämääritteet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6b39d-132">After you assign batch attributes to a product, you can add specific values to the attributes on the **Inventory batch attributes** page.</span></span>

## <a name="reserve-batches"></a><span data-ttu-id="6b39d-133">Erien varaaminen</span><span class="sxs-lookup"><span data-stu-id="6b39d-133">Reserve batches</span></span>
<span data-ttu-id="6b39d-134">Voit hakea erämääritteitä tehdessäsi erävarauksia myyntitilaukselle asiakkaan tilauksen täyttämiseksi tai keräillessäsi ja varatessasi eriä tuotantotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="6b39d-134">You can search on batch attributes when you do batch reservations for a sales order to fulfill a customer's order, or when you pick and reserve batches for a production order.</span></span> <span data-ttu-id="6b39d-135">Haun avulla voit etsiä varastoerää, joka sisältää tuotteen, jolla on haluamasi erämäärite.</span><span class="sxs-lookup"><span data-stu-id="6b39d-135">The search helps locate an inventory batch that contains the product that has the batch attribute that you want.</span></span> <span data-ttu-id="6b39d-136">Kun olet paikantanut erän tai erät, voit varata tuotteen lähdevaraston tapahtumariville.</span><span class="sxs-lookup"><span data-stu-id="6b39d-136">After you locate the batch or batches, you can reserve the product to the originating inventory transaction line.</span></span>



