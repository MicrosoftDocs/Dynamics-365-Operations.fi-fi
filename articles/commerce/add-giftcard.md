---
title: Lahjakorttimoduuli
description: Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a8428963e105e422dcd048863c17df0926a409ac
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411109"
---
# <a name="gift-card-module"></a><span data-ttu-id="fe066-103">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="fe066-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe066-104">Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="fe066-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fe066-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="fe066-105">Overview</span></span>

<span data-ttu-id="fe066-106">Lahjakortit ovat yleinen maksutapa, ja lahjakorttimoduulia voidaan käyttää kassamoduulissa hyväksymään lahjakortteja.</span><span class="sxs-lookup"><span data-stu-id="fe066-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="fe066-107">Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja.</span><span class="sxs-lookup"><span data-stu-id="fe066-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="fe066-108">SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta.</span><span class="sxs-lookup"><span data-stu-id="fe066-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="fe066-109">Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="fe066-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

<span data-ttu-id="fe066-110">Seuraavassa kuvassa on esimerkki lahjakorttimoduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="fe066-110">The following image shows an example of a gift card module on a checkout page.</span></span>

![Esimerkki lahjakorttimoduulista](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="fe066-112">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="fe066-112">Module properties</span></span>

- <span data-ttu-id="fe066-113">**Näytä lisäkentät** - Tämä ominaisuus määrittää, mitkä lahjakorttien kentät näytetään aina oletusarvoisesti näytettävän lahjakortin numeron lisäksi.</span><span class="sxs-lookup"><span data-stu-id="fe066-113">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="fe066-114">Esimerkiksi jotkin lahjakortit tukevat henkilökohtaista tunnuslukua (PIN), ja toiset tukevat PIN-koodin ja vanhentumispäivämäärän näyttämistä.</span><span class="sxs-lookup"><span data-stu-id="fe066-114">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="fe066-115">Vaihtoehtoisesti tämän ominaisuuden arvoksi voi määrittää "Ei mitään", jolloin näytetään vain lahjakortin numero eikä muita kenttiä näy.</span><span class="sxs-lookup"><span data-stu-id="fe066-115">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="fe066-116">Tuetut arvot:</span><span class="sxs-lookup"><span data-stu-id="fe066-116">Supported values:</span></span>
-   <span data-ttu-id="fe066-117">PIN-koodi</span><span class="sxs-lookup"><span data-stu-id="fe066-117">PIN</span></span>
-   <span data-ttu-id="fe066-118">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="fe066-118">Expiration date</span></span>
-   <span data-ttu-id="fe066-119">PIN-koodi ja vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="fe066-119">PIN and expiration date</span></span> 
-   <span data-ttu-id="fe066-120">None</span><span class="sxs-lookup"><span data-stu-id="fe066-120">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="fe066-121">Lahjakorttimoduulien toimipaikan asetukset</span><span class="sxs-lookup"><span data-stu-id="fe066-121">Site settings for gift card modules</span></span>

<span data-ttu-id="fe066-122">Kauppapaikan luomistyökalussa **Sivuston asetukset \> -laajennukset** -kohdassa on lahjakorttimoduulin asetus nimeltä **Tuettu lahjakorttityyppi**.</span><span class="sxs-lookup"><span data-stu-id="fe066-122">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="fe066-123">Tämä asetus tukee kolmea arvoa:</span><span class="sxs-lookup"><span data-stu-id="fe066-123">This setting supports three values:</span></span>
- <span data-ttu-id="fe066-124">**Dynamics 365 -lahjakortti** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365 -lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="fe066-124">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="fe066-125">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="fe066-125">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="fe066-126">**SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="fe066-126">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="fe066-127">Tätä asetusta tuetaan kirjautuneiden ja anonyymien käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="fe066-127">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="fe066-128">**Dynamics 365-, SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365-, SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="fe066-128">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="fe066-129">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="fe066-129">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="fe066-130">Lahjakorttimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="fe066-130">Add a gift card module to a page</span></span>

<span data-ttu-id="fe066-131">Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="fe066-131">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe066-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fe066-132">Additional resources</span></span>

[<span data-ttu-id="fe066-133">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fe066-133">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fe066-134">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="fe066-134">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fe066-135">Ulkoisten lahjakorttien tuki</span><span class="sxs-lookup"><span data-stu-id="fe066-135">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
