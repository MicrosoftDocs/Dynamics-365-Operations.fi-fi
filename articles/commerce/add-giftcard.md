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
ms.openlocfilehash: d9626f33ced0433bc96ed58429e95d4f75af6508
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980379"
---
# <a name="gift-card-module"></a><span data-ttu-id="1523e-103">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="1523e-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1523e-104">Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="1523e-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1523e-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="1523e-105">Overview</span></span>

<span data-ttu-id="1523e-106">Lahjakorttimoduuleja voi käyttää kassamoduuleissa lahjakorttien hyväksynnässä. Se on yleinen maksumuoto, jota käytetään sähköisen kaupankäynnin tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="1523e-106">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="1523e-107">Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja.</span><span class="sxs-lookup"><span data-stu-id="1523e-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="1523e-108">SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta.</span><span class="sxs-lookup"><span data-stu-id="1523e-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="1523e-109">Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta, on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="1523e-109">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1523e-110">Tuki SVS- ja Givex-lahjakorttien lunastamiselle kassatyönkulussa on käytettävissä Dynamics 365 Commercen versiossa 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="1523e-110">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="1523e-111">Käytettävissä on seuraavat kaksi lahjakorttimoduulia:</span><span class="sxs-lookup"><span data-stu-id="1523e-111">There are two gift card modules available:</span></span>

- <span data-ttu-id="1523e-112">**Lahjakortti** - Tätä moduulia voi käyttää kassasivulla lunastettaessa lahjakortti maksuvälineenä.</span><span class="sxs-lookup"><span data-stu-id="1523e-112">**Gift card** - This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="1523e-113">**Lahjakortin saldon tarkistus** - Tätä moduulia voi käyttää millä tahansa sivulla, kun halutaan tarkistaa lahjakortin saldo.</span><span class="sxs-lookup"><span data-stu-id="1523e-113">**Gift card balance check** - This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="1523e-114">Tämä moduuli on käytettävissä Commercen versiossa 10.0.14 ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="1523e-114">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="1523e-115">Lahjakortin saldontarkistusmoduulin tuki on saatavilla Dynamics 365 Commercen versiossa 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="1523e-115">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="1523e-116">Seuraavassa kuvassa on esimerkki lahjakorttimoduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="1523e-116">The following image shows an example of a gift card module on a checkout page.</span></span>

![Esimerkki lahjakorttimoduulista](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="1523e-118">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="1523e-118">Module properties</span></span>

- <span data-ttu-id="1523e-119">**Näytä lisäkentät** - Tämä ominaisuus määrittää, mitkä lahjakorttien kentät näytetään aina oletusarvoisesti näytettävän lahjakortin numeron lisäksi.</span><span class="sxs-lookup"><span data-stu-id="1523e-119">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="1523e-120">Esimerkiksi jotkin lahjakortit tukevat henkilökohtaista tunnuslukua (PIN), ja toiset tukevat PIN-koodin ja vanhentumispäivämäärän näyttämistä.</span><span class="sxs-lookup"><span data-stu-id="1523e-120">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="1523e-121">Vaihtoehtoisesti tämän ominaisuuden arvoksi voi määrittää "Ei mitään", jolloin näytetään vain lahjakortin numero eikä muita kenttiä näy.</span><span class="sxs-lookup"><span data-stu-id="1523e-121">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="1523e-122">Tuetut arvot:</span><span class="sxs-lookup"><span data-stu-id="1523e-122">Supported values:</span></span>
-   <span data-ttu-id="1523e-123">PIN-koodi</span><span class="sxs-lookup"><span data-stu-id="1523e-123">PIN</span></span>
-   <span data-ttu-id="1523e-124">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="1523e-124">Expiration date</span></span>
-   <span data-ttu-id="1523e-125">PIN-koodi ja vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="1523e-125">PIN and expiration date</span></span> 
-   <span data-ttu-id="1523e-126">None</span><span class="sxs-lookup"><span data-stu-id="1523e-126">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="1523e-127">Lahjakorttimoduulien toimipaikan asetukset</span><span class="sxs-lookup"><span data-stu-id="1523e-127">Site settings for gift card modules</span></span>

<span data-ttu-id="1523e-128">Kauppapaikan luomistyökalussa **Sivuston asetukset \> -laajennukset** -kohdassa on lahjakorttimoduulin asetus nimeltä **Tuettu lahjakorttityyppi**.</span><span class="sxs-lookup"><span data-stu-id="1523e-128">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="1523e-129">Tämä asetus tukee kolmea arvoa:</span><span class="sxs-lookup"><span data-stu-id="1523e-129">This setting supports three values:</span></span>
- <span data-ttu-id="1523e-130">**Dynamics 365 -lahjakortti** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365 -lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="1523e-130">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="1523e-131">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="1523e-131">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="1523e-132">**SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="1523e-132">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="1523e-133">Tätä asetusta tuetaan kirjautuneiden ja anonyymien käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="1523e-133">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="1523e-134">**Dynamics 365-, SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365-, SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="1523e-134">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="1523e-135">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="1523e-135">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1523e-136">Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.11-versiossa, ja niitä tarvitaan vain, jos tarvitset tukea SVS- tai Givex-lahjakorteille.</span><span class="sxs-lookup"><span data-stu-id="1523e-136">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="1523e-137">Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="1523e-137">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="1523e-138">Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="1523e-138">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="1523e-139">Lahjakorttimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="1523e-139">Add a gift card module to a page</span></span>

<span data-ttu-id="1523e-140">Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="1523e-140">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1523e-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1523e-141">Additional resources</span></span>

[<span data-ttu-id="1523e-142">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="1523e-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1523e-143">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="1523e-143">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="1523e-144">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="1523e-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1523e-145">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="1523e-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="1523e-146">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="1523e-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="1523e-147">Toimitusvaihtoehtomoduuli</span><span class="sxs-lookup"><span data-stu-id="1523e-147">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="1523e-148">Noudon tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="1523e-148">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="1523e-149">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="1523e-149">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1523e-150">Ulkoisten lahjakorttien tuki</span><span class="sxs-lookup"><span data-stu-id="1523e-150">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="1523e-151">SDK:n ja moduulikirjaston päivitykset</span><span class="sxs-lookup"><span data-stu-id="1523e-151">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
