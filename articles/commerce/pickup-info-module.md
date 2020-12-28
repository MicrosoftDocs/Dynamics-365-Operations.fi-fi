---
title: Noudon tiedot -moduuli
description: Tässä ohjeaiheessa käsitellään noutotietojen moduulia ja sen lisäämistä kassasivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
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
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 61b97d72b6a397737c10476cd6c02764e60f10b1
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665345"
---
# <a name="pickup-information-module"></a><span data-ttu-id="045b1-103">Noudon tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="045b1-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="045b1-104">Tässä ohjeaiheessa käsitellään noutotietojen moduulia ja sen lisäämistä kassasivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="045b1-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="045b1-105">Noutotietomoduulia voidaan käyttää kassamoduulissa tilauksen noutotietojen näyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="045b1-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="045b1-106">Asiakkaat voivat tarkastella käytettävissä olevia noutopäivämääriä ja aikavälejä ja valita sitten tilauksen noutoa varten sopivan ajan.</span><span class="sxs-lookup"><span data-stu-id="045b1-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="045b1-107">Esimerkiksi asiakas voi halutessaan noutaa tilauksen 21.3. klo 15.00 San Franciscon myymälästä.</span><span class="sxs-lookup"><span data-stu-id="045b1-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="045b1-108">Soveltuvien myymälöiden noutoajat on konfiguroitava Commerce-pääkonttorisovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="045b1-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="045b1-109">Lisätietoja: [Asiakasnoudon ajankohtien luominen ja päivittäminen](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="045b1-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="045b1-110">Jos noutotietomoduuli luodaan kassasivulla, mutta valitulle noutomyymälälle ei ole määritetty aikavälejä, moduulissa näytetään tiedot, mutta käyttäjä ei voi valita aikavälejä.</span><span class="sxs-lookup"><span data-stu-id="045b1-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="045b1-111">Aikavälit ovat valinnaisia, eikä tilauksen tekeminen edellytä niitä.</span><span class="sxs-lookup"><span data-stu-id="045b1-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="045b1-112">Jos useista myymälöistä noutoa varten on valittu useita nimikkeitä, noudon tiedot -moduulin avulla käyttäjä voi valita kullekin myymälälle aikavälin, jos käytettävissä on aikavälejä.</span><span class="sxs-lookup"><span data-stu-id="045b1-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="045b1-113">Aikavälien ja kassasivun noutotietomoduulin tuki on saatavana Dynamics 365 Commerce -versiossa 10.0.15 ja sitä uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="045b1-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="045b1-114">Seuraavassa kuvassa on esimerkki aikavälin valinnasta kassasivun noutotietomoduulin kautta.</span><span class="sxs-lookup"><span data-stu-id="045b1-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Esimerkki noutotietomoduulista kassasivulla](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="045b1-116">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="045b1-116">Module properties</span></span>

- <span data-ttu-id="045b1-117">**Otsikko** – Anna moduuliin otsikko.</span><span class="sxs-lookup"><span data-stu-id="045b1-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="045b1-118">Aikavälin tietojen näyttäminen tilauksen tekemisen jälkeen</span><span class="sxs-lookup"><span data-stu-id="045b1-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="045b1-119">Kun tilaus on tehty, valittua aika paikkaa koskevia tietoja voi tarkastella [tilausvahvistusmoduulissa](order-confirmation-module.md) ja [tilaustiedot-moduulissa](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="045b1-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="045b1-120">Molemmissa moduuleissa on **Näytä aikavälin tiedot** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="045b1-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="045b1-121">Ennen kuin ne voivat näyttää valitun aikavälin tilausprosessin aikana, tämän ominaisuuden arvoksi on asetettava **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="045b1-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="045b1-122">Lisää kassan noutotietomoduuli sivulle</span><span class="sxs-lookup"><span data-stu-id="045b1-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="045b1-123">Lisätietoja noutotietomoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="045b1-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="045b1-124">Seuraavassa kuvassa on esimerkki sähköisen kaupankäynnin kassasivusta, joka sisältää aikavälit noudettaville rivinimikkeille.</span><span class="sxs-lookup"><span data-stu-id="045b1-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Esimerkki sähköisen kaupankäynnin kassasivusta, joka sisältää aikavälit noudettaville rivinimikkeille](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="045b1-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="045b1-126">Additional resources</span></span>

[<span data-ttu-id="045b1-127">Asiakasnoudon ajankohtien luominen ja päivittäminen</span><span class="sxs-lookup"><span data-stu-id="045b1-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="045b1-128">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="045b1-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="045b1-129">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="045b1-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="045b1-130">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="045b1-130">Order details module</span></span>](account-management.md)
