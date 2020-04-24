---
title: Lahjakorttimoduuli
description: Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 70047376cec44523cc9cfe4df792bde23c776d8c
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261565"
---
# <a name="gift-card-module"></a><span data-ttu-id="fac96-103">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="fac96-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fac96-104">Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="fac96-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fac96-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="fac96-105">Overview</span></span>

<span data-ttu-id="fac96-106">Lahjakortit ovat yleinen maksutapa, ja lahjakorttimoduulia voidaan käyttää kassamoduulissa hyväksymään lahjakortteja.</span><span class="sxs-lookup"><span data-stu-id="fac96-106">Gift cards are a common form of payment, and the gift card module can be used in a checkout module to accept gift cards.</span></span> <span data-ttu-id="fac96-107">Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja.</span><span class="sxs-lookup"><span data-stu-id="fac96-107">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="fac96-108">SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta.</span><span class="sxs-lookup"><span data-stu-id="fac96-108">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span>

<span data-ttu-id="fac96-109">Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md)</span><span class="sxs-lookup"><span data-stu-id="fac96-109">For more information on support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md)</span></span>

## <a name="module-properties"></a><span data-ttu-id="fac96-110">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="fac96-110">Module properties</span></span>

- <span data-ttu-id="fac96-111">**Näytä lisäkentät** - Tämä ominaisuus määrittää, mitkä lahjakorttien kentät näytetään aina oletusarvoisesti näytettävän lahjakortin numeron lisäksi.</span><span class="sxs-lookup"><span data-stu-id="fac96-111">**Show additional fields** - This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="fac96-112">Esimerkiksi jotkin lahjakortit tukevat henkilökohtaista tunnuslukua (PIN), ja toiset tukevat PIN-koodin ja vanhentumispäivämäärän näyttämistä.</span><span class="sxs-lookup"><span data-stu-id="fac96-112">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="fac96-113">Vaihtoehtoisesti tämän ominaisuuden arvoksi voi määrittää "Ei mitään", jolloin näytetään vain lahjakortin numero eikä muita kenttiä näy.</span><span class="sxs-lookup"><span data-stu-id="fac96-113">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="fac96-114">Tuetut arvot:</span><span class="sxs-lookup"><span data-stu-id="fac96-114">Supported values:</span></span>
-   <span data-ttu-id="fac96-115">PIN-koodi</span><span class="sxs-lookup"><span data-stu-id="fac96-115">PIN</span></span>
-   <span data-ttu-id="fac96-116">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="fac96-116">Expiration date</span></span>
-   <span data-ttu-id="fac96-117">PIN-koodi ja vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="fac96-117">PIN and expiration date</span></span> 
-   <span data-ttu-id="fac96-118">None</span><span class="sxs-lookup"><span data-stu-id="fac96-118">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="fac96-119">Lahjakorttimoduulien toimipaikan asetukset</span><span class="sxs-lookup"><span data-stu-id="fac96-119">Site settings for gift card modules</span></span>

<span data-ttu-id="fac96-120">Kauppapaikan luomistyökalussa **Sivuston asetukset \> -laajennukset** -kohdassa on lahjakorttimoduulin asetus nimeltä **Tuettu lahjakorttityyppi**.</span><span class="sxs-lookup"><span data-stu-id="fac96-120">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="fac96-121">Tämä asetus tukee kolmea arvoa:</span><span class="sxs-lookup"><span data-stu-id="fac96-121">This setting supports three values:</span></span>
- <span data-ttu-id="fac96-122">**Dynamics 365 -lahjakortti** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365 -lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="fac96-122">**Dynamics 365 gift card** - When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="fac96-123">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="fac96-123">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="fac96-124">**SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="fac96-124">**SVS and Givex gift cards** - When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="fac96-125">Tätä asetusta tuetaan kirjautuneiden ja anonyymien käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="fac96-125">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="fac96-126">**Dynamics 365-, SVS- ja Givex-lahjakortit** - Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365-, SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="fac96-126">**Dynamics 365, SVS, and Givex gift cards** - When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="fac96-127">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="fac96-127">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="fac96-128">Lahjakorttimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="fac96-128">Add a gift card module to a page</span></span>

<span data-ttu-id="fac96-129">Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="fac96-129">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fac96-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fac96-130">Additional resources</span></span>

[<span data-ttu-id="fac96-131">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fac96-131">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fac96-132">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="fac96-132">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="fac96-133">Ulkoisten lahjakorttien tuki</span><span class="sxs-lookup"><span data-stu-id="fac96-133">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)
