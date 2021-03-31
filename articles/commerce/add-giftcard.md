---
title: Lahjakorttimoduuli
description: Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c024cc1b16ca60b2277eba2d7045020c2e67c3a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206292"
---
# <a name="gift-card-module"></a><span data-ttu-id="b5dfc-103">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="b5dfc-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b5dfc-104">Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b5dfc-105">Lahjakorttimoduuleja voi käyttää kassamoduuleissa lahjakorttien hyväksynnässä. Se on yleinen maksumuoto, jota käytetään sähköisen kaupankäynnin tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="b5dfc-106">Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="b5dfc-107">SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="b5dfc-108">Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta, on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="b5dfc-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b5dfc-109">Tuki SVS- ja Givex-lahjakorttien lunastamiselle kassatyönkulussa on käytettävissä Dynamics 365 Commercen versiossa 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="b5dfc-110">Käytettävissä on seuraavat kaksi lahjakorttimoduulia:</span><span class="sxs-lookup"><span data-stu-id="b5dfc-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="b5dfc-111">**Lahjakortti** - Tätä moduulia voi käyttää kassasivulla lunastettaessa lahjakortti maksuvälineenä.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-111">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="b5dfc-112">**Lahjakortin saldon tarkistus** - Tätä moduulia voi käyttää millä tahansa sivulla, kun halutaan tarkistaa lahjakortin saldo.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-112">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="b5dfc-113">Tämä moduuli on käytettävissä Commercen versiossa 10.0.14 ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="b5dfc-114">Lahjakortin saldontarkistusmoduulin tuki on saatavilla Dynamics 365 Commercen versiossa 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="b5dfc-115">Seuraavassa kuvassa on esimerkki lahjakorttimoduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Esimerkki lahjakorttimoduulista](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="b5dfc-117">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b5dfc-117">Module properties</span></span>

- <span data-ttu-id="b5dfc-118">**Näytä lisäkentät** - Tämä ominaisuus määrittää, mitkä lahjakorttien kentät näytetään aina oletusarvoisesti näytettävän lahjakortin numeron lisäksi.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-118">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="b5dfc-119">Esimerkiksi jotkin lahjakortit tukevat henkilökohtaista tunnuslukua (PIN), ja toiset tukevat PIN-koodin ja vanhentumispäivämäärän näyttämistä.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="b5dfc-120">Vaihtoehtoisesti tämän ominaisuuden arvoksi voi määrittää "Ei mitään", jolloin näytetään vain lahjakortin numero eikä muita kenttiä näy.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="b5dfc-121">Tuetut arvot:</span><span class="sxs-lookup"><span data-stu-id="b5dfc-121">Supported values:</span></span>
-   <span data-ttu-id="b5dfc-122">PIN-koodi</span><span class="sxs-lookup"><span data-stu-id="b5dfc-122">PIN</span></span>
-   <span data-ttu-id="b5dfc-123">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="b5dfc-123">Expiration date</span></span>
-   <span data-ttu-id="b5dfc-124">PIN-koodi ja vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="b5dfc-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="b5dfc-125">None</span><span class="sxs-lookup"><span data-stu-id="b5dfc-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="b5dfc-126">Lahjakorttimoduulien toimipaikan asetukset</span><span class="sxs-lookup"><span data-stu-id="b5dfc-126">Site settings for gift card modules</span></span>

<span data-ttu-id="b5dfc-127">Kauppapaikan luomistyökalussa **Sivuston asetukset \> -laajennukset** -kohdassa on lahjakorttimoduulin asetus nimeltä **Tuettu lahjakorttityyppi**.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="b5dfc-128">Tämä asetus tukee kolmea arvoa:</span><span class="sxs-lookup"><span data-stu-id="b5dfc-128">This setting supports three values:</span></span>
- <span data-ttu-id="b5dfc-129">**Dynamics 365 -lahjakortti** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365 -lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-129">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="b5dfc-130">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="b5dfc-131">**SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-131">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="b5dfc-132">Tätä asetusta tuetaan kirjautuneiden ja anonyymien käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="b5dfc-133">**Dynamics 365-, SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365-, SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-133">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="b5dfc-134">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5dfc-135">Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.11-versiossa, ja niitä tarvitaan vain, jos tarvitset tukea SVS- tai Givex-lahjakorteille.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="b5dfc-136">Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="b5dfc-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="b5dfc-137">Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="b5dfc-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="b5dfc-138">Lahjakorttimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="b5dfc-138">Add a gift card module to a page</span></span>

<span data-ttu-id="b5dfc-139">Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b5dfc-139">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5dfc-140">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b5dfc-140">Additional resources</span></span>

[<span data-ttu-id="b5dfc-141">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="b5dfc-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b5dfc-142">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="b5dfc-142">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b5dfc-143">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="b5dfc-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b5dfc-144">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="b5dfc-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b5dfc-145">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="b5dfc-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b5dfc-146">Toimitusvaihtoehtomoduuli</span><span class="sxs-lookup"><span data-stu-id="b5dfc-146">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b5dfc-147">Noudon tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="b5dfc-147">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b5dfc-148">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="b5dfc-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b5dfc-149">Ulkoisten lahjakorttien tuki</span><span class="sxs-lookup"><span data-stu-id="b5dfc-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="b5dfc-150">SDK:n ja moduulikirjaston päivitykset</span><span class="sxs-lookup"><span data-stu-id="b5dfc-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]