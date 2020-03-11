---
title: Valikoimien määrittäminen
description: Tässä artikkelissa kuvataan, mikä valikoima on, ja kerrotaan, kuinka voit määrittää valikoimia Dynamics 365 Commerceissa.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 26614d319453041177e8072793f09f52ebfd51fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022411"
---
# <a name="set-up-assortments"></a><span data-ttu-id="7f1ac-103">Valikoimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7f1ac-103">Set up assortments</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f1ac-104">Tässä artikkelissa kuvataan, mikä valikoima on, ja kerrotaan, kuinka voit määrittää valikoimia Dynamics 365 Commerceissa.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-104">This article describes what an assortment is and explains how to set up assortments in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7f1ac-105">Valikoima on kokoelma toisiinsa liittyviä tuotteita, jotka määritetään kaupan kanavalle, kuten myymälälle tai verkkokaupalle.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-105">An assortment is a collection of related products that you assign to a commerce channel, such as a brick-and-mortar store or an online store.</span></span> <span data-ttu-id="7f1ac-106">Voit käyttää valikoimia tunnistamaan tuotteet, jotka ovat myynnissä jokaisessa myymälässä.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-106">You use assortments to identify the products that are available in each store.</span></span> <span data-ttu-id="7f1ac-107">Valikoimaan voi sisältyä tuoteluokkia.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-107">An assortment can include categories of products.</span></span> <span data-ttu-id="7f1ac-108">Siispä kaikki tiettyyn luokkaan määritetyt tuotteet sisältyvät valikoimaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-108">Therefore, all products that are assigned to a specific category are included in the assortment.</span></span> <span data-ttu-id="7f1ac-109">Valikoimaan voi myös sisältyä tiettyjä tuotteita ja tuotevariantteja.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-109">An assortment can also include specific products and specific variants of products.</span></span> <span data-ttu-id="7f1ac-110">Valikoiman määrittämällä voit määrittää tuhansia tuotteita kanaviisi yhdellä kertaa juuri sellaisena yhdistelmänä, joka liikkeissäsi tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-110">By setting up an assortment, you can assign thousands of products to your channels at that same time, in any combination that your stores require.</span></span> <span data-ttu-id="7f1ac-111">Voit määrittää niin monta tuotevalikoimaa kuin on tarpeen.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-111">You can set up as many product assortments as you require.</span></span> <span data-ttu-id="7f1ac-112">Kukin tuote voi kuulua yhteen tai useampaa valikoimaan, ja jokaisen valikoiman voi määrittää yhteen tai useampaan kanavaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-112">Each product can be included in one or more assortments, and each assortment can be assigned to one or more channels.</span></span> <span data-ttu-id="7f1ac-113">Voit esimerkiksi määrittää yhden valikoiman, joka sisältää joukon perustuotteita.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-113">For example, you define one assortment that includes a base set of products.</span></span> <span data-ttu-id="7f1ac-114">Tämä valikoima kuuluu kaikille myymälöille.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-114">All stores receive this assortment.</span></span> <span data-ttu-id="7f1ac-115">Voit sitten määrittää toisen valikoiman, joka sisältää vain suuria urheiluvälineitä.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-115">You then define another assortment that includes only large sporting equipment.</span></span> <span data-ttu-id="7f1ac-116">Vain suuremmat myymäläsi saavat tämän valikoiman.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-116">Only your larger stores receive this assortment.</span></span> <span data-ttu-id="7f1ac-117">Seuraavassa kaaviossa näkyy, kuinka tuotteet voi liittää valikoimiin, ja valikoimat voi liittää kanaviin.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-117">The following diagram shows how products can be assigned to assortments, and how those assortments can be assigned to channels.</span></span>

![Tuotevalikoimien suhteet](./media/assortments_relationship.gif)

## <a name="prerequisites"></a><span data-ttu-id="7f1ac-119">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="7f1ac-119">Prerequisites</span></span>

<span data-ttu-id="7f1ac-120">Ennen kuin voit määrittää valikoiman ja liittää sen kaupan kanavaan, sinun on suoritettava seuraavat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-120">Before you can set up an assortment and assign it to a commerce channel, you must complete the following tasks.</span></span>

| <span data-ttu-id="7f1ac-121">Tehtävä</span><span class="sxs-lookup"><span data-stu-id="7f1ac-121">Task</span></span>                              | <span data-ttu-id="7f1ac-122">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="7f1ac-122">Description</span></span> |
|-----------------------------------|-------------|
| <span data-ttu-id="7f1ac-123">Kanavan määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-123">Set up a channel.</span></span>          | <span data-ttu-id="7f1ac-124">Kanavia ovat myymälät, verkkokaupat ja online-kauppapaikat.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-124">Channels represent a brick-and-mortar store, an online store, or an online marketplace.</span></span> <span data-ttu-id="7f1ac-125">Sinun on määritettävä vähintään yksi kanava sekä kaupan asetukset.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-125">You must set up at least one channel and configure the options for the store.</span></span> <span data-ttu-id="7f1ac-126">Määrittämällä valikoimat myymälöille tunnistat tuotteet, jotka ovat saatavilla tietystä myymälästä.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-126">Assortments are assigned to stores to identify the products that a particular store carries.</span></span> |
| <span data-ttu-id="7f1ac-127">Luo organisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-127">Create an organization hierarchy.</span></span> | <span data-ttu-id="7f1ac-128">Kun olet määrittänyt organisaatiosi kaupan kanavat, sinun on määritettävä organisaatiohierarkia, joka vastaa vähittäismyynnin kanaviesi organisaatiorakennetta.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-128">After you set up the commerce channels for your organization, you must configure an organization hierarchy that represents the organizational structure of your channels.</span></span> <span data-ttu-id="7f1ac-129">Organisaatiohierarkiaa voidaan käyttää esimerkiksi valikoimissa, täydennyksissä ja raportoinnissa.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-129">An organization hierarchy can be used for assortments, replenishment, and reporting.</span></span> <span data-ttu-id="7f1ac-130">Voit määrittää valikoimia myymäläryhmille lisäämällä kanavia organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-130">By adding your channels to an organization hierarchy, you can assign assortments to groups of stores.</span></span> <span data-ttu-id="7f1ac-131">Sen sijaan, että määrittäisit valikoiman erikseen kullekin myymälälle, voit määrittää valikoiman organisaation ylätason solmulle.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-131">Instead of assigning the assortment individually to each store, you assign the assortment to the high-level organization node.</span></span> <span data-ttu-id="7f1ac-132">Nyt, milloin tahansa lisäätkin uuden kanavan organisaation ylätason solmuun, kyseinen kanava perii automaattisesti kaikki solmulle määritetyt valikoimat.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-132">Then, whenever a new channel is added to the high-level organization node, that channel automatically inherits any assortments that were assigned to the higher-level organization node.</span></span> <span data-ttu-id="7f1ac-133">Voit määrittää valikoimia ainoastaan kanaville, jotka sisältyvät organisaatiohierarkiaan, jolle on määritetty **Kauppavalikoima**-tarkoitus.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-133">You can assign assortments only to channels that are included in an organization hierarchy that is assigned the **Commerce assortment** purpose.</span></span> |
| <span data-ttu-id="7f1ac-134">Määritä tuotteet.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-134">Define products.</span></span>                  | <span data-ttu-id="7f1ac-135">Ennen kuin voit lisätä tuotteita valikoimaan, sinun on lisättävä ne Commerceen.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-135">Before you can add products to an assortment, you must add them in Commerce.</span></span> <span data-ttu-id="7f1ac-136">Voit lisätä tuotteet manuaalisesti tai voit tuoda ne toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-136">You can add products manually, or you can import them from a vendor.</span></span> <span data-ttu-id="7f1ac-137">Kun olet lisännyt tuotteet, ne tulee vapauttaa yritykselle.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-137">After you add the products, you must release them to a legal entity.</span></span> <span data-ttu-id="7f1ac-138">Vain tuotteet, jotka on vapautettu yritykselle, voidaan tuoda kanavien saataville.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-138">Only products that have been released to a legal entity can be made available to your channels.</span></span> <span data-ttu-id="7f1ac-139">Tuotteet, joita ei ole vielä vapautettu yrityksen käyttöön voidaan lisätä valikoimaan, ja valikoima voidaan hyväksyä.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-139">Products that haven't yet been released to a legal entity can be added to an assortment, and the assortment can be approved.</span></span> <span data-ttu-id="7f1ac-140">Vasta kun tuotteet on vapautettu yritykselle, voidaan ne tuoda kanavien saataville.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-140">However, until the products have been released to a legal entity, they can't be made available to the channels.</span></span> |
| <span data-ttu-id="7f1ac-141">Määritä luokkahierarkia.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-141">Set up a category hierarchy.</span></span>      | <span data-ttu-id="7f1ac-142">Voit kaupan tuotteita luodessasi ryhmitellä ja luokitella ne käyttämällä luokkahierarkia-ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-142">When you create your commerce products, you can group and categorize them by using the category hierarchy feature.</span></span> <span data-ttu-id="7f1ac-143">Voit luoda yhden ydinhierarkian, jonka avulla voit ryhmitellä ja luokitella kaikki kanaviesi kautta tarjoamasi tuotteet.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-143">You can create one core hierarchy to group and categorize all products that you distribute through your channels.</span></span> <span data-ttu-id="7f1ac-144">Voit myös luoda erillisiä, täydentäviä luokkahierarkioita ryhmitelläksesi tai luokitellaksesi tuotteesi erityistarkoituksiin, kuten kampanjoihin tai valikoimiin.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-144">You can also create separate, supplemental category hierarchies to group or categorize your products for special purposes, such as promotions or assortments.</span></span> <span data-ttu-id="7f1ac-145">Luokkahierarkioiden avulla voit määrittää kaikki tietyn luokan tuotteet valikoimaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-145">By using category hierarchies, you can assign all the products in a specific category to an assortment.</span></span> <span data-ttu-id="7f1ac-146">Kaikki tuotteet, jotka lisätään valikoimaan sisältyvään luokkaan sisältyvät automaattisesti valikoimaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-146">Any products that are added to the category that is included in the assortment are automatically included in the assortment.</span></span> <span data-ttu-id="7f1ac-147">Seuraavan kerran, kun kaupan valikoiman ajastustyö suoritetaan, nämä tuotteet tulevat saataville kanaviin, joihin valikoima on määritetty.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-147">Then, the next time that the commerce assortment scheduler is run, these products become available to the channels that the assortment is assigned to.</span></span> |

## <a name="setting-up-an-assortment"></a><span data-ttu-id="7f1ac-148">Valikoiman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7f1ac-148">Setting up an assortment</span></span>

<span data-ttu-id="7f1ac-149">Kun olet määrittänyt edellytykset, voit luoda valikoiman ja määrittää sen kanaville.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-149">After you complete the prerequisites, you can create an assortment and assign it to your channels.</span></span> <span data-ttu-id="7f1ac-150">Kun määrität valikoimaa, tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="7f1ac-150">To set up an assortment, you must complete the following tasks.</span></span>

1. <span data-ttu-id="7f1ac-151">Luo uusi valikoima tai kopioi aiemmin luotu valikoima.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-151">Create a new assortment, or copy an existing assortment.</span></span>
2. <span data-ttu-id="7f1ac-152">Valitse kanavat tai kanavien ylätason ryhmät, joita valikoima koskee.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-152">Select the channels or the high-level groups of channels that the assortment applies to.</span></span>
3. <span data-ttu-id="7f1ac-153">Lisää tuoteluokkia, yksittäisiä tuotteita tai tuotevariantteja valikoimaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-153">Add product categories, individual products, or product variants to the assortment.</span></span> <span data-ttu-id="7f1ac-154">Voit sisällyttää kaikki tietyn luokan tuotteet tai ohittaa tietyt tuotteet valikoimaan kuuluvasta luokasta.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-154">You can include all products in a specific category, or you can exclude selected products from a category that is included in the assortment.</span></span>
4. <span data-ttu-id="7f1ac-155">Julkaise valikoima.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-155">Publish the assortment.</span></span> <span data-ttu-id="7f1ac-156">Valikoiman ajastus suoritetaan automaattisesti, kun valikoima julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-156">When you publish an assortment, the assortment scheduler is automatically run.</span></span> <span data-ttu-id="7f1ac-157">Tämä prosessi luo tuoteluettelon.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-157">This process generates the list of products.</span></span> <span data-ttu-id="7f1ac-158">Kun tämä prosessi on valmis, tuotteet vapautuvat kanaville, joille tuotevalikoima on määritetty.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-158">When this process is completed, the products become available to the channels that the product assortment is assigned to.</span></span> <span data-ttu-id="7f1ac-159">Jos julkaistuun valikoimaan tai sille määritettyihin kanaviin tehdään muutoksia, valikoima on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-159">If changes are made to an assortment that has been published, or to the channels that the assortment is assigned to, the assortment must be updated.</span></span> <span data-ttu-id="7f1ac-160">Aja valikoimien ajastustyö komentojonotyönä päivittääksesi valikoiman muutosten yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="7f1ac-160">To update the assortment when changes are made, you can run the assortment scheduler as a batch job.</span></span>