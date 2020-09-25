---
title: Lahjakorttimoduuli
description: Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4cc947b9d6f3cfa51bce2155170c49e9529d0f7d
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761078"
---
# <a name="gift-card-module"></a><span data-ttu-id="d9858-103">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="d9858-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d9858-104">Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="d9858-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d9858-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="d9858-105">Overview</span></span>

<span data-ttu-id="d9858-106">Lahjakorttimoduuleja voi käyttää kassamoduuleissa lahjakorttien hyväksynnässä. Se on yleinen maksumuoto, jota käytetään sähköisen kaupankäynnin tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="d9858-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="d9858-107">Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja.</span><span class="sxs-lookup"><span data-stu-id="d9858-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="d9858-108">SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta.</span><span class="sxs-lookup"><span data-stu-id="d9858-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="d9858-109">Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta, on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="d9858-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

<span data-ttu-id="d9858-110">Käytettävissä on seuraavat kaksi lahjakorttimoduulia:</span><span class="sxs-lookup"><span data-stu-id="d9858-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="d9858-111">**Lahjakortti** - Tätä moduulia voi käyttää kassasivulla lunastettaessa lahjakortti maksuvälineenä.</span><span class="sxs-lookup"><span data-stu-id="d9858-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="d9858-112">**Lahjakortin saldon tarkistus** - Tätä moduulia voi käyttää millä tahansa sivulla, kun halutaan tarkistaa lahjakortin saldo.</span><span class="sxs-lookup"><span data-stu-id="d9858-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="d9858-113">Tämä moduuli on käytettävissä Commercen versiossa 10.0.14 ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="d9858-113">This module is available in Commerce release 10.0.14 and later.</span></span>

<span data-ttu-id="d9858-114">Seuraavassa kuvassa on esimerkki lahjakorttimoduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="d9858-114">The following image shows an example of a gift card module on a checkout page.</span></span>

![Esimerkki lahjakorttimoduulista](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="d9858-116">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="d9858-116">Module properties</span></span>

- <span data-ttu-id="d9858-117">**Näytä lisäkentät** - Tämä ominaisuus määrittää, mitkä lahjakorttien kentät näytetään aina oletusarvoisesti näytettävän lahjakortin numeron lisäksi.</span><span class="sxs-lookup"><span data-stu-id="d9858-117">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="d9858-118">Esimerkiksi jotkin lahjakortit tukevat henkilökohtaista tunnuslukua (PIN), ja toiset tukevat PIN-koodin ja vanhentumispäivämäärän näyttämistä.</span><span class="sxs-lookup"><span data-stu-id="d9858-118">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="d9858-119">Vaihtoehtoisesti tämän ominaisuuden arvoksi voi määrittää "Ei mitään", jolloin näytetään vain lahjakortin numero eikä muita kenttiä näy.</span><span class="sxs-lookup"><span data-stu-id="d9858-119">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="d9858-120">Tuetut arvot:</span><span class="sxs-lookup"><span data-stu-id="d9858-120">Supported values:</span></span>
-   <span data-ttu-id="d9858-121">PIN-koodi</span><span class="sxs-lookup"><span data-stu-id="d9858-121">PIN</span></span>
-   <span data-ttu-id="d9858-122">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="d9858-122">Expiration date</span></span>
-   <span data-ttu-id="d9858-123">PIN-koodi ja vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="d9858-123">PIN and expiration date</span></span> 
-   <span data-ttu-id="d9858-124">None</span><span class="sxs-lookup"><span data-stu-id="d9858-124">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="d9858-125">Lahjakorttimoduulien toimipaikan asetukset</span><span class="sxs-lookup"><span data-stu-id="d9858-125">Site settings for gift card modules</span></span>

<span data-ttu-id="d9858-126">Kauppapaikan luomistyökalussa **Sivuston asetukset \> -laajennukset** -kohdassa on lahjakorttimoduulin asetus nimeltä **Tuettu lahjakorttityyppi**.</span><span class="sxs-lookup"><span data-stu-id="d9858-126">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="d9858-127">Tämä asetus tukee kolmea arvoa:</span><span class="sxs-lookup"><span data-stu-id="d9858-127">This setting supports three values:</span></span>
- <span data-ttu-id="d9858-128">**Dynamics 365 -lahjakortti** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365 -lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="d9858-128">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="d9858-129">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="d9858-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="d9858-130">**SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="d9858-130">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="d9858-131">Tätä asetusta tuetaan kirjautuneiden ja anonyymien käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="d9858-131">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="d9858-132">**Dynamics 365-, SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365-, SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="d9858-132">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="d9858-133">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="d9858-133">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="d9858-134">Lahjakorttimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="d9858-134">Add a gift card module to a page</span></span>

<span data-ttu-id="d9858-135">Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="d9858-135">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9858-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d9858-136">Additional resources</span></span>

[<span data-ttu-id="d9858-137">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="d9858-137">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d9858-138">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="d9858-138">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d9858-139">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="d9858-139">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d9858-140">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="d9858-140">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d9858-141">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="d9858-141">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="d9858-142">Toimitusvaihtoehdot -moduuli</span><span class="sxs-lookup"><span data-stu-id="d9858-142">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d9858-143">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="d9858-143">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d9858-144">Ulkoisten lahjakorttien tuki</span><span class="sxs-lookup"><span data-stu-id="d9858-144">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
