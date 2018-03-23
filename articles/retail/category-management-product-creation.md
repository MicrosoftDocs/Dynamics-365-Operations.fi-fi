---
title: Tuoteluokan hallinta
description: "Tässä ohjeaiheessa kerrotaan, miten myynninedistämispäälliköt voivat hallita vähittäismyynnin tuotehierarkian ja vapautetun tuotteen tietojen välisiä suhteita vähittäismyynnin tuoteluokkien avulla."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="490c9-103">Parannettu tuotteiden ja luokkien hallinta</span><span class="sxs-lookup"><span data-stu-id="490c9-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="490c9-104">Tässä ohjeaiheessa kerrotaan parannetusta tavasta hallita vähittäismyynnin tuoteluokkia ja tuotteita Dynamics 365 for Retailissa.</span><span class="sxs-lookup"><span data-stu-id="490c9-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="490c9-105">Myynninedistämispäälliköt näkevät näiden parannusten avulla tuoteominaisuuksien yhteisen rakenteen vähittäismyynnin tuotehierarkian ja vapautettujen tuotetietojen välillä.</span><span class="sxs-lookup"><span data-stu-id="490c9-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="490c9-106">Saat lisätietoja vähittäismyynnin tuoteluokkien valitsemalla **Vähittäismyynnin tuotehierarkia** **Luokka- ja tuotehallinta** -työtilassa ja tarkastelemalla **Vähittäismyynnin tuoteluokka** -sivun parannettua rakennetta.</span><span class="sxs-lookup"><span data-stu-id="490c9-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![Luokka- ja tuotehallinta -työtila](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="490c9-108">Aiemmissa versioissa tuotteen ominaisuudet jaettiin **tuotteen perusominaisuuksiin** ja **vähittäismyyntituotteen tuotteenominaisuuksiin** niiden käyttöalueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="490c9-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="490c9-109">**Vähittäismyyntituotteen ominaisuudet** oli käyttöalueeltaan *yleinen*, mikä tarkoitti, että tietyllä **vähittäismyyntituotteen ominaisuudella** sama arvo jaetaan kaikissa yrityksissä.</span><span class="sxs-lookup"><span data-stu-id="490c9-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="490c9-110">**Tuotteen perusominaisuudet** ovat *yrityskohtaisia*.</span><span class="sxs-lookup"><span data-stu-id="490c9-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="490c9-111">Toisin sanoen tietyn **tuotteen perusominaisuuden** arvo voi vaihdella yrityksissä yksittäisten liiketoimintatarpeiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="490c9-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="490c9-112">Parannetussa vähittäismyynnin tuoteluokkarakenteessa tuotteen ominaisuudet erotetaan loogisesti sen perusteella, miten käytettäviä ne ovat ryhmässä, vastaamaan vapautettujen tuotetietojen lomakerakennetta.</span><span class="sxs-lookup"><span data-stu-id="490c9-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![Kenttien ryhmittely käyttöalueen perusteella](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="490c9-114">Ominaisuuksien hallinnan yrityskohtaisille ominaisuuksille voi vaihtaa yleisestä yrityskohtaiseksi.</span><span class="sxs-lookup"><span data-stu-id="490c9-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="490c9-115">Voit tehdä valitsemalla joko **Näytä tai muokkaa kaikissa yrityksissä** tai **Näytä tai muokkaa tietyssä yrityksessä**.</span><span class="sxs-lookup"><span data-stu-id="490c9-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![Näkymän vaihtelu yksittäisen yrityksen ja kaikkien yritysten välillä](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![Näkymän vaihtelu yksittäisen yrityksen ja kaikkien yritysten välillä](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="490c9-118">Edellisiin versioihin verrattuna uudessa vähittäismyynnin tuoteluokkarakenteessa myynninedistämispäällikkö voi myös määrittää oletusarvot lisätuoteominaisuusjoukolle yksittäisellä luokkatasolla.</span><span class="sxs-lookup"><span data-stu-id="490c9-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="490c9-119">Tuotetta luotaessa tuote perii nämä tuoteominaisuuden oletusarvot perustuen liitokseen vähittäismyynnin tuotehierarkian yksittäiseen luokkaan.</span><span class="sxs-lookup"><span data-stu-id="490c9-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="490c9-120">Näitä perittyjä tuoteominaisuuksia voidaan myös muokata kunkin tuotteen kohdalla siten, että vastaavat yksittäisiä liiketoimintatarpeita.</span><span class="sxs-lookup"><span data-stu-id="490c9-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="490c9-121">Valitse ominaisuudet, jotka päivitetään tuotteille vähittäismyynnin tuoteluokkalomakkeessa</span><span class="sxs-lookup"><span data-stu-id="490c9-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="490c9-122">Voit käyttää tätä uutta tuoteominaisuuksien parannettua rakennetta, kun valitset mitkä päivitetyt tuoteominaisuudet on siirrettävä liitettyihin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="490c9-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![Uusi päivitettyjen tuotteiden parannettu näkymä](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="490c9-124">Myynninedistämispäälliköt voivat muokata näitä perittyjä tuoteominaisuuksia tuotekohtaisesti täyttääkseen yksittäisiä liiketoiminnan vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="490c9-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


