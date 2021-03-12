---
title: Tuotteiden omistajat
description: Tässä aiheessa on tietoja tuotteen omistajista. Tuotteen omistaja on käyttäjäryhmä, joka vastaa tietyistä tuotteista. Vain ryhmän jäsenet voivat vapauttaa kyseisiä tuotteita. Tuotteen omistajaa voidaan käyttää myös hyväksynnän työnkulussa.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 90f5596f9b5fc45e78cc49a3309c45864e07e70b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967330"
---
# <a name="product-owners"></a><span data-ttu-id="1a140-106">Tuotteiden omistajat</span><span class="sxs-lookup"><span data-stu-id="1a140-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a140-107">Tuotteen omistaja on käyttäjäryhmä, joka vastaa tietyistä tuotteista.</span><span class="sxs-lookup"><span data-stu-id="1a140-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="1a140-108">Kun tuotteelle määritetään tuotteen omistajaryhmä, vain kyseisen ryhmän jäsenet voivat vapauttaa tuotteen.</span><span class="sxs-lookup"><span data-stu-id="1a140-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="1a140-109">Tuotteen omistajaa voidaan käyttää myös hyväksynnän työnkulussa suunnittelun muutostenhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="1a140-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="1a140-110">Tuotteen omistajat ovat yleisiä asetuksia.</span><span class="sxs-lookup"><span data-stu-id="1a140-110">Product owners are global settings.</span></span> <span data-ttu-id="1a140-111">Niinpä ne ovat käytettävissä kaikissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="1a140-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="1a140-112">Tuotteen omistajaryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="1a140-112">Create a product owner group</span></span>

<span data-ttu-id="1a140-113">Tuotteen omistajaryhmä luodaan ja siihen lisätään jäseniä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1a140-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="1a140-114">Valitse **Suunnittelun muutostenhallinta \> Määritys \> Tuotteen omistajat**.</span><span class="sxs-lookup"><span data-stu-id="1a140-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="1a140-115">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1a140-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="1a140-116">Anna **Tuotteen omistaja** -kentässä ryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="1a140-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="1a140-117">Anna **Nimi**-kentässä ryhmän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="1a140-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="1a140-118">Lisää **Jäsenet**-pikavälilehdessä työntekijöitä ryhmän jäseniksi.</span><span class="sxs-lookup"><span data-stu-id="1a140-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="1a140-119">Tuotteen omistajan määrittäminen tuotteen omistajalle</span><span class="sxs-lookup"><span data-stu-id="1a140-119">Assign a product owner to a product</span></span>

<span data-ttu-id="1a140-120">Tuotteen omistaja määritetään tuotteelle seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="1a140-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="1a140-121">Avaa liittyvän tuotteen tai päätuotteen **Tuotetiedot**-sivu.</span><span class="sxs-lookup"><span data-stu-id="1a140-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="1a140-122">Määritä **Yleinen**-välilehden **Tuotteen omistaja** -kentässä kyseisen tuotteen omistajaryhmän nimi.</span><span class="sxs-lookup"><span data-stu-id="1a140-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="1a140-123">Kun tuotteen omistajaa määritetään tuotteelle, vain tuotteen omistajaryhmän jäsenet voivat muokata **Tuotteen omistaja** -asetusta.</span><span class="sxs-lookup"><span data-stu-id="1a140-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="1a140-124">Tuotteen omistaja näkyy myös **Vapautetut tuotteet** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1a140-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="1a140-125">Tuotteen omistajat ja tuotteen vapautukset</span><span class="sxs-lookup"><span data-stu-id="1a140-125">Product owners and product releases</span></span>

<span data-ttu-id="1a140-126">Vain tuotteen tuotteen omistajaryhmän jäsenet voivat vapauttaa kyseisen tuotteen.</span><span class="sxs-lookup"><span data-stu-id="1a140-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="1a140-127">Poikkeuksena on kuitenkin tilanne, jossa tuote on alinimike ja sen päätuotteen omistaja julkaisee päätuotteen.</span><span class="sxs-lookup"><span data-stu-id="1a140-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="1a140-128">Jos tuote on siis toisen tuotteen tuoterakenteen osa, järjestelmä ei tarkista kunkin tuoterakenteen nimikkeen tuotteen omistajaa.</span><span class="sxs-lookup"><span data-stu-id="1a140-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="1a140-129">Se tarkistaa vain päänimikkeen tuotteen omistajan.</span><span class="sxs-lookup"><span data-stu-id="1a140-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="1a140-130">Tuote X on esimerkiksi määritetty *Design-kaiuttimet*-tuotteen omistajaryhmään.</span><span class="sxs-lookup"><span data-stu-id="1a140-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="1a140-131">Tuote X on myös tuotteen Y tuoterakenteen osa, ja tuote Y on määritetty *Design-kaiuttimet*-tuotteen omistajaryhmään.</span><span class="sxs-lookup"><span data-stu-id="1a140-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="1a140-132">Jos *Design-kaiuttimet*-tuotteen omistajaryhmä vapauttaa tuotteen Y ja sen tuoterakenteen, tuote X vapautetaan yhdessä tuotteen Y kanssa.</span><span class="sxs-lookup"><span data-stu-id="1a140-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="1a140-133">Tuotteen omistajat ja hyväksynnät</span><span class="sxs-lookup"><span data-stu-id="1a140-133">Product owners and approvals</span></span>

<span data-ttu-id="1a140-134">Koska tuotteen omistajat tietävät, onko tietystä suunnittelun muutoksesta hyötyä tuotteille, heidät kannattaa usein sisällyttää suunnittelun muutostenhallinnan hyväksyntäprosessiin.</span><span class="sxs-lookup"><span data-stu-id="1a140-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="1a140-135">Se voidaan toteuttaa määrittämällä tuotteen omistajat osallistujiksi työnkuluissa, joita käytetään suunnittelun muutostenhallinnassa.</span><span class="sxs-lookup"><span data-stu-id="1a140-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="1a140-136">Järjestelmä määrittää sitten hyväksyntätehtäviä työnkuluissa suunnittelun muutospyyntöjen ja muutostilausten tuotteiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="1a140-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="1a140-137">Lisätietoja on kohdassa [Suunnittelutuotteiden muutosten hallinta](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="1a140-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>
