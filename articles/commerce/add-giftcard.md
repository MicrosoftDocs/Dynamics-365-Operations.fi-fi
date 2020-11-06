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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b7d28e041b8adc828a2447ab09a0c1d28cc2aec0
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022002"
---
# <a name="gift-card-module"></a><span data-ttu-id="cbefb-103">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="cbefb-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cbefb-104">Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="cbefb-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cbefb-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="cbefb-105">Overview</span></span>

<span data-ttu-id="cbefb-106">Lahjakorttimoduuleja voi käyttää kassamoduuleissa lahjakorttien hyväksynnässä. Se on yleinen maksumuoto, jota käytetään sähköisen kaupankäynnin tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="cbefb-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="cbefb-107">Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja.</span><span class="sxs-lookup"><span data-stu-id="cbefb-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="cbefb-108">SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta.</span><span class="sxs-lookup"><span data-stu-id="cbefb-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="cbefb-109">Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta, on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="cbefb-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="cbefb-110">Tuki SVS- ja Givex-lahjakorttien lunastamiselle kassatyönkulussa on käytettävissä Dynamics 365 Commercen versiossa 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="cbefb-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="cbefb-111">Käytettävissä on seuraavat kaksi lahjakorttimoduulia:</span><span class="sxs-lookup"><span data-stu-id="cbefb-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="cbefb-112">**Lahjakortti** - Tätä moduulia voi käyttää kassasivulla lunastettaessa lahjakortti maksuvälineenä.</span><span class="sxs-lookup"><span data-stu-id="cbefb-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="cbefb-113">**Lahjakortin saldon tarkistus** - Tätä moduulia voi käyttää millä tahansa sivulla, kun halutaan tarkistaa lahjakortin saldo.</span><span class="sxs-lookup"><span data-stu-id="cbefb-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="cbefb-114">Tämä moduuli on käytettävissä Commercen versiossa 10.0.14 ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="cbefb-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="cbefb-115">Lahjakortin saldontarkistusmoduulin tuki on saatavilla Dynamics 365 Commercen versiossa 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="cbefb-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="cbefb-116">Seuraavassa kuvassa on esimerkki lahjakorttimoduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="cbefb-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Esimerkki lahjakorttimoduulista](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="cbefb-118">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="cbefb-118">Module properties</span></span>

- <span data-ttu-id="cbefb-119">**Näytä lisäkentät** - Tämä ominaisuus määrittää, mitkä lahjakorttien kentät näytetään aina oletusarvoisesti näytettävän lahjakortin numeron lisäksi.</span><span class="sxs-lookup"><span data-stu-id="cbefb-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="cbefb-120">Esimerkiksi jotkin lahjakortit tukevat henkilökohtaista tunnuslukua (PIN), ja toiset tukevat PIN-koodin ja vanhentumispäivämäärän näyttämistä.</span><span class="sxs-lookup"><span data-stu-id="cbefb-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="cbefb-121">Vaihtoehtoisesti tämän ominaisuuden arvoksi voi määrittää "Ei mitään", jolloin näytetään vain lahjakortin numero eikä muita kenttiä näy.</span><span class="sxs-lookup"><span data-stu-id="cbefb-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="cbefb-122">Tuetut arvot:</span><span class="sxs-lookup"><span data-stu-id="cbefb-122">Supported values:</span></span>
-   <span data-ttu-id="cbefb-123">PIN-koodi</span><span class="sxs-lookup"><span data-stu-id="cbefb-123">PIN</span></span>
-   <span data-ttu-id="cbefb-124">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="cbefb-124">Expiration date</span></span>
-   <span data-ttu-id="cbefb-125">PIN-koodi ja vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="cbefb-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="cbefb-126">None</span><span class="sxs-lookup"><span data-stu-id="cbefb-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="cbefb-127">Lahjakorttimoduulien toimipaikan asetukset</span><span class="sxs-lookup"><span data-stu-id="cbefb-127">Site settings for gift card modules</span></span>

<span data-ttu-id="cbefb-128">Kauppapaikan luomistyökalussa **Sivuston asetukset \> -laajennukset** -kohdassa on lahjakorttimoduulin asetus nimeltä **Tuettu lahjakorttityyppi**.</span><span class="sxs-lookup"><span data-stu-id="cbefb-128">In Commerce site builder under **Site Settings \> Extensions** , there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="cbefb-129">Tämä asetus tukee kolmea arvoa:</span><span class="sxs-lookup"><span data-stu-id="cbefb-129">This setting supports three values:</span></span>
- <span data-ttu-id="cbefb-130">**Dynamics 365 -lahjakortti** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365 -lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="cbefb-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="cbefb-131">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="cbefb-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="cbefb-132">**SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="cbefb-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="cbefb-133">Tätä asetusta tuetaan kirjautuneiden ja anonyymien käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="cbefb-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="cbefb-134">**Dynamics 365-, SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365-, SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="cbefb-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="cbefb-135">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="cbefb-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cbefb-136">Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.11-versiossa, ja niitä tarvitaan vain, jos tarvitset tukea SVS- tai Givex-lahjakorteille.</span><span class="sxs-lookup"><span data-stu-id="cbefb-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="cbefb-137">Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="cbefb-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="cbefb-138">Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="cbefb-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="cbefb-139">Lahjakorttimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="cbefb-139">Add a gift card module to a page</span></span>

<span data-ttu-id="cbefb-140">Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="cbefb-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cbefb-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="cbefb-141">Additional resources</span></span>

[<span data-ttu-id="cbefb-142">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="cbefb-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cbefb-143">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="cbefb-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="cbefb-144">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="cbefb-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="cbefb-145">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="cbefb-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="cbefb-146">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="cbefb-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="cbefb-147">Toimitusvaihtoehtomoduuli</span><span class="sxs-lookup"><span data-stu-id="cbefb-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="cbefb-148">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="cbefb-148">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="cbefb-149">Ulkoisten lahjakorttien tuki</span><span class="sxs-lookup"><span data-stu-id="cbefb-149">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="cbefb-150">SDK:n ja moduulikirjaston päivitykset</span><span class="sxs-lookup"><span data-stu-id="cbefb-150">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
