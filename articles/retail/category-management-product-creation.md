---
title: Tuoteluokkien hallinta ja luonti
description: "Tässä aiheessa käsitellään parannuksia, jotka on tehty vähittäismyynnin tuoteryhmien hallintaan. Myynninedistämispäälliköt saavat näiden parannusten avulla korrelaation Vähittäismyynnin tuotehierarkian ja vapautettujen tuotetietojen välille."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 6b9afb40b68b672514c083d99efbc9bd098dd561
ms.openlocfilehash: b158ff5b277c125e0aa158c071007ed8a0f25482
ms.contentlocale: fi-fi
ms.lasthandoff: 10/03/2017

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="fd60a-104">Tuoteluokkien hallinta ja luonti</span><span class="sxs-lookup"><span data-stu-id="fd60a-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="fd60a-105">Vähittäismyynnin tuoteluokkien hallintaan tehtyjen parannusten avulla myynninedistämispäälliköt saavat korrelaation Retailin tuotehierarkian ja vapautettujen tuotetietojen välille.</span><span class="sxs-lookup"><span data-stu-id="fd60a-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="fd60a-106">Näitä parannuksia voit tarkastella valitsemalla **Luokka- ja tuotehallinta** -työtilassa **Vähittäismyynnin tuotehierarkia** -kohdan, joka avaa **Vähittäismyynnin tuoteluokan uusi rakenne** -sivun.</span><span class="sxs-lookup"><span data-stu-id="fd60a-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="fd60a-107">Aiemmissa versioissa tuotteen ominaisuudet jaettiin perustuotteen ominaisuuksiin ja vähittäismyynnin tuotteenominaisuuksiin niiden käyttöalueen mukaan.</span><span class="sxs-lookup"><span data-stu-id="fd60a-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="fd60a-108">Vähittäismyyntituotteen ominaisuudet olivat *yleisiä*.</span><span class="sxs-lookup"><span data-stu-id="fd60a-108">Retail product properties were *global*.</span></span> <span data-ttu-id="fd60a-109">Toisin sanoen tietyn tuoteominaisuuden arvot jaettiin kaikkiin yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="fd60a-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="fd60a-110">Tuotteen perusominaisuudet olivat *yrityskohtaisia*.</span><span class="sxs-lookup"><span data-stu-id="fd60a-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="fd60a-111">Toisin sanoen tuoteominaisuus voi vaihdella yritysten välillä yrityskohtaisista liiketoiminnan tarpeista riippuen.</span><span class="sxs-lookup"><span data-stu-id="fd60a-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="fd60a-112">Näissä parannuksissa vähittäismyynnin tuoteluokan ominaisuuksiin säilytetään kenttien erottelu niiden soveltuvuuden perusteella ryhmässä, jotta ne vastaavat vapautettujen tuotetietojen lomakerakennetta.</span><span class="sxs-lookup"><span data-stu-id="fd60a-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="fd60a-113">Ominaisuuksien hallinnan yrityskohtaisille ominaisuuksille voi vaihtaa yleisestä yrityskohtaiseksi.</span><span class="sxs-lookup"><span data-stu-id="fd60a-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="fd60a-114">Valitse vain **Näytä/Muokkaa kaikissa yrityksissä** tai **Näytä/Muokkaa tietyssä yrityksessä** tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="fd60a-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="fd60a-115">Myynninedistämispäälliköt voivat myös määrittää oletusarvot lisäjoukolle tuoteominaisuuksia yksittäisen luokan tasolla.</span><span class="sxs-lookup"><span data-stu-id="fd60a-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="fd60a-116">Tuotteet perivät nämä ominaisuuden arvot niiden luonninaikaiseen luokkaliitokseen perustuen.</span><span class="sxs-lookup"><span data-stu-id="fd60a-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="fd60a-117">Valitse ominaisuudet, jotka päivitetään tuotteille vähittäismyynnin tuoteluokkalomakkeessa</span><span class="sxs-lookup"><span data-stu-id="fd60a-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="fd60a-118">Loogisten ryhmittelyominaisuuksien avulla voit valita, mitkä päivitetyt tuoteominaisuudet päivitetään liitettyihin tuotteisiin.</span><span class="sxs-lookup"><span data-stu-id="fd60a-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="fd60a-119">Myynninedistämispäälliköt voivat muokata näitä perittyjä tuoteominaisuuksia tuotekohtaisesti täyttääkseen yksittäisiä liiketoiminnan vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="fd60a-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

