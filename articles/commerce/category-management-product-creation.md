---
title: Tuoteluokkien ja tuotteiden hallinta
description: Tässä ohjeaiheessa kerrotaan, miten myynninedistämispäälliköt voivat hallita tuotehierarkian ja vapautetun tuotteen tietojen välisiä suhteita Commercen tuoteluokkien avulla.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: EcoResCategorySearchList, EcoResAttribute, COODualUseCategories, EcoResProductCategory, EcoResCategoryAddProduct, EcoResAttributeValue
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 95a4bac6beeaf5fad449027d93132fc1499288a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215483"
---
# <a name="manage-product-categories-and-products"></a><span data-ttu-id="f7ced-103">Tuoteluokkien ja tuotteiden hallinta</span><span class="sxs-lookup"><span data-stu-id="f7ced-103">Manage product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="f7ced-104">Tässä ohjeaiheessa kerrotaan parannetusta tavasta hallita Dynamics 365 Commercen tuoteluokkia ja tuotteita.</span><span class="sxs-lookup"><span data-stu-id="f7ced-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f7ced-105">Myynninedistämispäälliköt näkevät näiden parannusten avulla tuoteominaisuuksien rakenteen, jonka tuotehierarkia ja vapautetut tuotetiedot jakavat.</span><span class="sxs-lookup"><span data-stu-id="f7ced-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="f7ced-106">Saat lisätietoja tuoteluokkien hallinnasta valitsemalla **Luokka- ja tuotehallinta** -työtilassa **Commercen tuotehierarkia** -ruudun.</span><span class="sxs-lookup"><span data-stu-id="f7ced-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Commerce product hierarchy** tile.</span></span>

<span data-ttu-id="f7ced-107">Kiinnitä huomiota avautuvan **Commercen tuotehierarkia** -sivun parannuksiin.</span><span class="sxs-lookup"><span data-stu-id="f7ced-107">Notice the enhanced structure of the **Commerce product hierarchy** page that appears.</span></span> <span data-ttu-id="f7ced-108">Aiemmissa sovelluksen versioissa tuotteen ominaisuudet jaettiin *tuotteen perusominaisuuksiin* ja *vähittäismyyntituotteen tuotteenominaisuuksiin* niiden käyttöalueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="f7ced-108">In previous versions of the app, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="f7ced-109">Vähittäismyyntituotteen ominaisuuksien käyttöalue on *yleinen*.</span><span class="sxs-lookup"><span data-stu-id="f7ced-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="f7ced-110">Toisin sanoen tietyn tuoteominaisuuden arvot jaettiin kaikkiin yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="f7ced-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="f7ced-111">Tuotteen perusominaisuudet ovat sen sijaan *yrityskohtaisia*.</span><span class="sxs-lookup"><span data-stu-id="f7ced-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="f7ced-112">Toisin sanoen tietyn tuotteen perusominaisuuden arvo voi vaihdella yrityksissä kun yrityksen yksittäisten liiketoimintatarpeiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="f7ced-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="f7ced-113">Parannetussa tuoteluokkarakenteessa tuotteen ominaisuudet erotetaan loogisesti sen perusteella, miten niitä voi käyttää ryhmässä, jotta ne vastaavat vapautettujen tuotetietojen lomakerakennetta.</span><span class="sxs-lookup"><span data-stu-id="f7ced-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![Kenttien ryhmittely ominaisuuksien käyttöalueen perusteella](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="f7ced-115">Yrityskohtaisten ominaisuuksien hallinnan voi vaihtaa yleisestä yrityskohtaiseksi.</span><span class="sxs-lookup"><span data-stu-id="f7ced-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="f7ced-116">Voit hallita ominaisuuksia kaikissa yrityksissä valitsemalla **Näytä kaikissa yrityksissä** (tai **Muokkaa kaikissa yrityksissä**).</span><span class="sxs-lookup"><span data-stu-id="f7ced-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![Näyttäminen tai muokkaaminen kaikissa yrityksissä](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="f7ced-118">Voit hallita tietyn yrityksen ominaisuuksia valitsemalla **Näytä tietyssä yrityksessä** (tai **Muokkaa tietyssä yrityksessä**).</span><span class="sxs-lookup"><span data-stu-id="f7ced-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![Näyttäminen tai muokkaaminen tietyssä yrityksessä](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="f7ced-120">Parannetussa tuoteluokkarakenteessa myynninedistämispäällikkö voi nyt myös määrittää oletusarvot lisätuoteominaisuusjoukolle yksittäisellä luokkatasolla.</span><span class="sxs-lookup"><span data-stu-id="f7ced-120">Additionally, in the enhanced product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="f7ced-121">Kun tuotteet sitten luodaan, ne perivät tuoteominaisuuksiensa oletusarvot sen perusteella, mikä on kyseisten ominaisuuksien liitos yksittäiseen tuotehierarkialuokkaan.</span><span class="sxs-lookup"><span data-stu-id="f7ced-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="f7ced-122">Näitä perittyjä tuoteominaisuuksia voidaan myös muokata kunkin tuotteen kohdalla siten, että ne vastaavat yksittäisiä liiketoimintatarpeita.</span><span class="sxs-lookup"><span data-stu-id="f7ced-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a><span data-ttu-id="f7ced-123">Commercen tuotehierarkiasivulla päivitettävien tuoteominaisuuksien valinta</span><span class="sxs-lookup"><span data-stu-id="f7ced-123">Selecting properties to update products on the Commerce product hierarchy page</span></span>

<span data-ttu-id="f7ced-124">Voit käyttää uutta tuoteominaisuuksien parannettua rakennetta, kun valitset, mitkä päivitetyt tuoteominaisuudet on siirrettävä liitettyihin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="f7ced-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="f7ced-125">Valitse **Commercen tuotehierarkia** -sivun toimintoruudussa **Luokka** ja avaa sitten **Päivitä tuotteet** -valintaikkuna valitsemalla **Päivitä tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="f7ced-125">On the **Commerce product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![Päivitä tuotteet -valintaikkuna.](media/NewUpdateProductsEnhancedView.PNG)


[!INCLUDE[footer-include](../includes/footer-banner.md)]