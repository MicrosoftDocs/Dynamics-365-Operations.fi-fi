---
title: Asiakkaan sisäänkuittausilmoitusten ottaminen käyttöön myyntipisteessä
description: Tässä aiheessa kuvataan, kuinka asiakkaan sisäänkuittausilmoitukset otetaan käyttöön Microsoft Dynamics 365 Commerce -myyntipisteessä (POS).
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271422"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="12337-103">Asiakkaan sisäänkuittausilmoitusten ottaminen käyttöön myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="12337-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="12337-104">Tässä aiheessa kuvataan, kuinka asiakkaan sisäänkuittausilmoitukset otetaan käyttöön Microsoft Dynamics 365 Commerce -myyntipisteessä (POS).</span><span class="sxs-lookup"><span data-stu-id="12337-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="12337-105">Organisaatiot voivat lähettää sähköpostien "Tilaus valmis noudettavaksi" -sähköpostiviestissä linkin tai painikkeen, jonka avulla asiakkaat ilmoittavat myymälälle, että he ovat paikan päällä ja odottavat paketin tuontia.</span><span class="sxs-lookup"><span data-stu-id="12337-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="12337-106">Tämän jälkeen asiakkaat saavat sisäänkuittausvahvistuksen, ja myymälä saa ilmoituksen tehtävänä myyntipistesovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="12337-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="12337-107">Tämä tehtävä toimii kehotteena myyntiedustajalle toimittaa tilaus asiakkaan ajoneuvoon.</span><span class="sxs-lookup"><span data-stu-id="12337-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="12337-108">Asiakkaan ei siis tarvitse mennä sisään myymälään.</span><span class="sxs-lookup"><span data-stu-id="12337-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="12337-109">Asiakkaan sisäänkuittaustyönkulun voi myös konfiguroida keräämään asiakkailta lisätietoja, kuten pysäköintipaikan numeron, ajoneuvon mallin ja värin sekä toimitusohjeet.</span><span class="sxs-lookup"><span data-stu-id="12337-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="12337-110">Vähittäismyymälän myyjä voi helpottaa tilausten täyttämistä näiden tietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="12337-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="12337-111">Asiakkaan sisäänkuittauksen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="12337-111">Enable customer check-in</span></span>

<span data-ttu-id="12337-112">Kun asiakkaan sisään sisäänkuittaustoiminto on käytössä, Commerce luo tilausvahvistuksen tunnuksen (tunnetaan myös kanavan viitetunnuksena).</span><span class="sxs-lookup"><span data-stu-id="12337-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="12337-113">Se luo myös tilausvahvistustunnukset tilauksille, jotka on luotu myyntipisteen (POS) tai puhelinkeskuskanavien kautta.</span><span class="sxs-lookup"><span data-stu-id="12337-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="12337-114">Ota asiakkaan sisäänkuittausominaisuus käyttöön Commercen pääkonttorisovelluksessa seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="12337-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="12337-115">Valitse **Työtilat \> Ominaisuuden hallinta**.</span><span class="sxs-lookup"><span data-stu-id="12337-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="12337-116">Etsi **Yhdenmukaisen kanavan viitetunnuksen muodon muodostaminen eri kanavissa** -ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="12337-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="12337-117">Valitse ominaisuus ja valitse sitten ominaisuusruudusta **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="12337-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="12337-118">Sisäänkuittaussivun luominen</span><span class="sxs-lookup"><span data-stu-id="12337-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="12337-119">Sähköisen kaupankäynnin sivustossa luo uusi sivu, jota käytetään sisäänkuittauksessa.</span><span class="sxs-lookup"><span data-stu-id="12337-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="12337-120">Lisäkonfiguraation avulla sivu voi myös sisältää lomakkeen, joka kerää asiakkailta lisätietoja tilausten täyttämistä varten.</span><span class="sxs-lookup"><span data-stu-id="12337-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="12337-121">Lisätietoja sivun ja moduulin määrittämisestä on kohdassa [Asiakkaan sisäänkuittausmoduuli](check-in-pickup-module.md).</span><span class="sxs-lookup"><span data-stu-id="12337-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="12337-122">Tapahtumasähköpostimallin konfiguroiminen</span><span class="sxs-lookup"><span data-stu-id="12337-122">Configure the transactional email template</span></span>

<span data-ttu-id="12337-123">Lisää tapahtumasähköpostimalliin **Olen paikalla** -linkki tai -painike, jonka asiakkaat saavat, kun heidän tilauksensa on valmis noudettavaksi.</span><span class="sxs-lookup"><span data-stu-id="12337-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="12337-124">Tämän linkin tai painikkeen avulla asiakkaat voivat ilmoittaa myymälälle, että he ovat saapuneet noutamaan tilauksen.</span><span class="sxs-lookup"><span data-stu-id="12337-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="12337-125">Lisää linkki tai painike malliin, joka on yhdistetty **Pakkaus valmis** -ilmoituksen tyyppiin ja toimitustapaan, jota käytät tien vierestä noudettavan tilauksen täyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="12337-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="12337-126">Luo mallissa HTML-linkki tai -painike, joka osoittaa luomasi sisäänkuittaussivun URL-osoitteeseen.</span><span class="sxs-lookup"><span data-stu-id="12337-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="12337-127">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="12337-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="12337-128">Lisätietoja sähköpostimallien määrittämisestä on kohdassa [Tapahtumasähköpostien mukauttaminen toimitustilan mukaan](customize-email-delivery-mode.md).</span><span class="sxs-lookup"><span data-stu-id="12337-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="12337-129">Sisäänkuittaustehtävä luodaan myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="12337-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="12337-130">Kun asiakas ilmoittaa myymälälle, että hän on paikalla noutoa varten, hän saa kuittausvahvistusilmoituksen ja tehtävä luodaan myyntipisteen tehtäväluetteloon myymälälle, josta asiakas noutaa tilauksen.</span><span class="sxs-lookup"><span data-stu-id="12337-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="12337-131">Tehtävä sisältää kaikki tilauksen täyttämisen edellyttämät asiakas- ja tilaustiedot.</span><span class="sxs-lookup"><span data-stu-id="12337-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="12337-132">Tehtävän ohjeet-kentässä näkyvät kaikki asiakkaalta lisätietolomakkeella kerätyt tiedot.</span><span class="sxs-lookup"><span data-stu-id="12337-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="12337-133">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="12337-133">Additional resources</span></span>

[<span data-ttu-id="12337-134">Noutomoduulin sisäänkuittaus</span><span class="sxs-lookup"><span data-stu-id="12337-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
