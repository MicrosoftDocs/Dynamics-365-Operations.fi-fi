---
title: Hinnanoikaisut ja alennukset
description: Tässä artikkelissa on tietoja Dynamics 365 Commercen hinnanoikaisuista ja alennuksista.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240939"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="7393d-103">Hinnanoikaisut ja alennukset</span><span class="sxs-lookup"><span data-stu-id="7393d-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7393d-104">Tässä artikkelissa on tietoja Dynamics 365 Commercen hinnanoikaisuista ja alennuksista.</span><span class="sxs-lookup"><span data-stu-id="7393d-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7393d-105">Voit tehdä Commercessa tuotteiden hinnanoikaisuja ja myös määrittää alennuksia, joita käytetään nimikkeeseen tai tapahtumaan myyntipisteessä, puhelinkeskuksen myyntitilauksessa tai verkkotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="7393d-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="7393d-106">Sekä hinnanoikaisut että alennukset voidaan linkittää hintaryhmiin.</span><span class="sxs-lookup"><span data-stu-id="7393d-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="7393d-107">Hinnanoikaisuille ja alennuksille voidaan määrittää yksi aloitus- ja päättymispäivämäärä tai toistuva jakso, alennuskoodi ja joitakin muita määritteitä.</span><span class="sxs-lookup"><span data-stu-id="7393d-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="7393d-108">Hinnanoikaisuja ja alennuksia voidaan käyttää tuotteissa, varianteissa tai kategorioissa.</span><span class="sxs-lookup"><span data-stu-id="7393d-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="7393d-109">Jos tuotteelle on useita alennuksia, asiakas voi saada minkä tahansa alennuksen tai alennusten yhdistelmän alennuksen määritysten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="7393d-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="7393d-110">Commerce käyttää automaattisesti alennusta tai alennusten yhdistelmää, joka takaa asiakkaalle parhaan hinnan.</span><span class="sxs-lookup"><span data-stu-id="7393d-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="7393d-111">Kun määrität hinnanoikaisua tai alennusta, muista vahvistaa, että hintaryhmät on liitetty oikeisiin kanaviin, luetteloihin, liitoksiin tai kanta-asiakasohjelmiin, joissa haluat käyttää alennusta.</span><span class="sxs-lookup"><span data-stu-id="7393d-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="7393d-112">Lisäksi jos haluat luoda alennustunnuksen automaattisesti, määritä numerosarjat **Commercen parametrit** -sivulla, ennen kuin määrität uuden hinnanoikaisun tai alennuksen.</span><span class="sxs-lookup"><span data-stu-id="7393d-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="7393d-113">Voit poistaa hinnanoikaisun tai alennuksen.</span><span class="sxs-lookup"><span data-stu-id="7393d-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="7393d-114">Tällöin tilastotiedot kuitenkin häviävät.</span><span class="sxs-lookup"><span data-stu-id="7393d-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="7393d-115">Alennusten tyypit</span><span class="sxs-lookup"><span data-stu-id="7393d-115">Types of discounts</span></span>

<span data-ttu-id="7393d-116">Alennuksia on useita tyyppejä:</span><span class="sxs-lookup"><span data-stu-id="7393d-116">There are many types of discounts:</span></span>

- <span data-ttu-id="7393d-117">**Yksinkertainen alennus** – Yksi prosenttiosuus tai määrä.</span><span class="sxs-lookup"><span data-stu-id="7393d-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="7393d-118">**Määräalennus** – alennus, jota käytetään, kun tuotteita ostetaan vähintään kaksi.</span><span class="sxs-lookup"><span data-stu-id="7393d-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="7393d-119">**Yhdistelmäalennus** – alennus, jota käytetään, kun ostetaan tietty tuoteyhdistelmä.</span><span class="sxs-lookup"><span data-stu-id="7393d-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="7393d-120">**Raja-arvon alennus** – alennus, jota käytetään, kun tapahtuman kokonaissumma ylittää tietyn summan.</span><span class="sxs-lookup"><span data-stu-id="7393d-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="7393d-121">**Maksuvälinepohjainen alennus** – Alennus, jota käytetään, kun tapahtuman kokonaissumma on määritettyä summaa suurempi ja tiettyä maksutyyppiä (esimerkiksi käteinen, luottokortti tai pankkikortti) on käytetty maksussa.</span><span class="sxs-lookup"><span data-stu-id="7393d-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="7393d-122">**Lähetysalennus** – Alennus, jota käytetään, kun tapahtuman kokonaissumma on enemmän kuin määritetty summa ja jos tilauksessa on käytössä tietty toimitustapa (esimerkiksi kahden päivän toimitus tai toimitus yön aikana).</span><span class="sxs-lookup"><span data-stu-id="7393d-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="7393d-123">Sekä hinnanoikaisut että alennukset voidaan yhdistää hintaryhmiin.</span><span class="sxs-lookup"><span data-stu-id="7393d-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="7393d-124">Hintaryhmät voidaan tämän jälkeen liittää kanaviin, luetteloihin, liitoksiin ja kanta-asiakasohjelmiin.</span><span class="sxs-lookup"><span data-stu-id="7393d-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="7393d-125">Yhdistelmäalennus ja raja-alennus sisältävät ominaisuudet nimeltään "Laske ei-alennuskelpoiset tuotteet" ja "Laske ei-alennuskelpoiset tuotteet raja-arvon suhteen".</span><span class="sxs-lookup"><span data-stu-id="7393d-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="7393d-126">Jos nämä ominaisuudet ovat käytössä, nimike, joka ei ole oikeutettu mihinkään alennukseen, voi silti auttaa hyväksymään alennustapahtuman, mutta nimike, jolle ei ole oikeutta, ei saa alennusta.</span><span class="sxs-lookup"><span data-stu-id="7393d-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="7393d-127">Jos esimerkiksi luot yhdistelmäalennuksen, jossa on kaksi riviä A ja B, jossa asiakkaan tulee saada 10 %:n alennus molemmista nimikkeistä, mutta nimikkeen A konfiguraatiossa on "Estä kaikki alennukset" -valintaruutu, tämä yleensä lopettaisi nimikkeen A sisällyttämisen alennukseen.</span><span class="sxs-lookup"><span data-stu-id="7393d-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="7393d-128">Jos kuitenkin Laske ei-alennuskelpoiset tuotteet -ominaisuus on käytössä, nimikettä A voidaan käyttää yhdistelmäalennuksen hyväksymiseen, mutta 10 %:n alennus koskee vain nimikettä B. Vastaava logiikka koskee raja-alennusta.</span><span class="sxs-lookup"><span data-stu-id="7393d-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="7393d-129">"Laske ei-alennuskelpoiset tuotteet raja-arvon suhteen" -ominaisuudessa on kuitenkin lisätoiminto verrattuna yhdistelmäalennusten "Laske ei-alennuskelpoiset tuotteet" -ominaisuuteen.</span><span class="sxs-lookup"><span data-stu-id="7393d-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="7393d-130">Jos raja-alennus on käytössä ja jos jollain nimikkeellä on voimassa oleva alennus, joka estää nimikettä muista alennuksista, nimikkeelle maksettava hinta täyttää raja-arvon, mutta tämä nimike ei saa lisäalennusta.</span><span class="sxs-lookup"><span data-stu-id="7393d-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
