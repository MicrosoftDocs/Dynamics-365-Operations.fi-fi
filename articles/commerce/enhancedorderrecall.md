---
title: Myyntipisteen Peruuta tilaus -toiminto
description: Tässä ohjeaiheessa käsitellään myyntipisteen parannetulla tilausten peruutussivuilla olevia ominaisuuksia.
author: hhainesms
manager: annbe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 174821fce4baf81e4298da4b066f855bfec98ca5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585127"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="a00af-103">Myyntipisteen Peruuta tilaus -toiminto</span><span class="sxs-lookup"><span data-stu-id="a00af-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a00af-104">Commercen myyntipisteen **Peruuta tilaus** -toiminnossa on päivitetyt tilauksen haku- ja suodatusominaisuudet ja tilauskohtaiset tiedot.</span><span class="sxs-lookup"><span data-stu-id="a00af-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="a00af-105">Tämä ominaisuus on käytettävissä Commercen versiossa 10.0.15 ja sitä uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="a00af-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="a00af-106">Ota tämä toiminto käyttöön ottamalla **Parannettu tilauksen peruutustoiminto myyntipisteessä** -ominaisuus käyttöön Commercen pääkonttorin **Ominaisuuksien hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="a00af-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="a00af-107">Kun ominaisuus on otettu käyttöön, harkitse myyntipisteen [näytön asettelujen](pos-screen-layouts.md) päivittämistä, jotta voit käyttää muutettuja ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="a00af-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="a00af-108">**Peruuta tilaus** -toimintopainikkeen määritys antaa organisaatioille mahdollisuuden ottaa toiminnon käyttöön siten, että näyttö määritetty valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="a00af-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Painikeruudukon määritykset](media/recallorderbuttongrid.png)

<span data-ttu-id="a00af-110">Näyttöasetukset:</span><span class="sxs-lookup"><span data-stu-id="a00af-110">The display options are as follows.</span></span>
- <span data-ttu-id="a00af-111">**Ei mitään** – Tällä asetuksella toiminto otetaan käyttöön ilman tiettyä näyttöä.</span><span class="sxs-lookup"><span data-stu-id="a00af-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="a00af-112">Kun käyttäjä avaa toiminnon tällä määrityksellä, häntä pyydetään hakemaan tilaukset tai tekemään valinnan esimääritetystä tilaussuodattimesta.</span><span class="sxs-lookup"><span data-stu-id="a00af-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="a00af-113">**Täytettävät tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka käyttäjän nykyisen myymälän on täytettävä.</span><span class="sxs-lookup"><span data-stu-id="a00af-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the user's current store.</span></span> <span data-ttu-id="a00af-114">Nämä tilaukset määritetään myymälästä noudatettavaksi tai lähetettäväksi eikä näiden tilausten rivejä ole vielä poimittu tai pakattu.</span><span class="sxs-lookup"><span data-stu-id="a00af-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="a00af-115">**Poimittavat tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka on määritetty myymälästä poimittavaksi käyttäjän nykyisestä myymälästä.</span><span class="sxs-lookup"><span data-stu-id="a00af-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="a00af-116">**Lähetettävät tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka on määritetty lähetettäväksi käyttäjän nykyisestä myymälästä.</span><span class="sxs-lookup"><span data-stu-id="a00af-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="a00af-117">Jos **Peruuta tilaus** -toiminto käynnistetään myyntipisteessä ja jos näytön määrityksenä on **Ei mitään**, käyttäjä voi hakea ja noutaa tilauksia jollakin seuraavista tavoista.</span><span class="sxs-lookup"><span data-stu-id="a00af-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="a00af-118">Skannaa tilauksen viivakoodit.</span><span class="sxs-lookup"><span data-stu-id="a00af-118">Scan order barcodes.</span></span> <span data-ttu-id="a00af-119">Tällä tavoin haetaan vastaavuuksien tilauksen numeron, kanavaviitteen ja vastaanottotunnuksen kentät.</span><span class="sxs-lookup"><span data-stu-id="a00af-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="a00af-120">Valitse sovelluspalkissa **Hae tilaukset**- tai **Hae ja suodata** -kuvake. Tällä tavoin voit käyttää suodatusmekanismia suodatusehtoja vastaavien tilausten paikantamiseen.</span><span class="sxs-lookup"><span data-stu-id="a00af-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="a00af-121">Valitse jokin esimääritetty suodatin avattavassa **Näytä tilaukset** -valikossa (täytettävät tilaukset, poimittavat tilaukset tai lähetettävät tilaukset).</span><span class="sxs-lookup"><span data-stu-id="a00af-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="a00af-123">Kun ehtojen mukainen haku on tehty, sovellus näyttää vastaavien myyntitilausten luettelon.</span><span class="sxs-lookup"><span data-stu-id="a00af-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span> <span data-ttu-id="a00af-124">Haku- tai suodatusasetuksia käytettäessä on tärkeää muistaa, että haettujen tilausten ei tarvitse olla käyttäjän nykyiseen myymälään linkitettyjä tilauksia.</span><span class="sxs-lookup"><span data-stu-id="a00af-124">It's important to note that when using the search/filter options, the orders retrieved do not have to be orders linked to the user's current store.</span></span> <span data-ttu-id="a00af-125">Tämä hakuprosessi hakee ja näyttää kaikki hakuehtoja vastaavat asiakastilaukset, vaikka tilaus olisi luotu tai määritetty toisen myymälän/kanavan tai varaston sijainnin avulla.</span><span class="sxs-lookup"><span data-stu-id="a00af-125">This search process will retrieve and display any customer order that matches the search criteria, even if the order was created or set to be fulfilled by another store/channel or warehouse location.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="a00af-127">Käyttäjä voi valita luettelossa tilauksen ja katsoa lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="a00af-127">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="a00af-128">Näytön oikealla puolella on tietopaneeli, jossa on tietoja valitusta tilauksesta, kuten tilausrivin tiedot, toimituksen tiedot ja täyttämistiedot.</span><span class="sxs-lookup"><span data-stu-id="a00af-128">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="a00af-129">Valitse toiminto sovelluspalkissa.</span><span class="sxs-lookup"><span data-stu-id="a00af-129">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="a00af-130">Tilauksen tilan mukaan määräytyy, voidaanko tietyt toiminnot ottaa käyttää.</span><span class="sxs-lookup"><span data-stu-id="a00af-130">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="a00af-131">**Palauta** – Aloittaa prosessin, joka luo palautuksen valitun asiakastilauksen laskutetuille tuotteille.</span><span class="sxs-lookup"><span data-stu-id="a00af-131">**Return** – Initiates the process of creating a return for any of the invoiced products on the selected customer order.</span></span>

- <span data-ttu-id="a00af-132">**Peruuta** – myöntää valitun myyntitilauksen täyden peruutuksen.</span><span class="sxs-lookup"><span data-stu-id="a00af-132">**Cancel** – Issue a full cancellation of the selected sales order.</span></span> <span data-ttu-id="a00af-133">Tämä vaihtoehto ei ole käytettävissä puhelinkeskuksen kanavan kautta käynnistettaville tilauksille, eikä sitä voi käyttää tilauksen osittaista peruuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="a00af-133">This option will not be available for orders initiated through a call center channel and cannot be used to partially cancel an order.</span></span>

- <span data-ttu-id="a00af-134">**Täytä** – Siirtää käyttäjän tilauksen täyttämissivulle, joka esisuodatetaan valittuun tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="a00af-134">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="a00af-135">Näkyvissä on vain ne valitun tilauksen tilausrivit, jotka ovat avoimia täytettäväksi käyttäjän myymälässä.</span><span class="sxs-lookup"><span data-stu-id="a00af-135">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="a00af-136">**Muokkaa** – käyttäjät saavat tehdä muutoksia valittuun asiakastilaukseen.</span><span class="sxs-lookup"><span data-stu-id="a00af-136">**Edit** – Allows users to make changes to the selected customer order.</span></span> <span data-ttu-id="a00af-137">Tilauksia voi muokata vain [tietyissä tilanteissa](customer-orders-overview.md#edit-an-existing-customer-order).</span><span class="sxs-lookup"><span data-stu-id="a00af-137">Orders are only editable in [certain scenarios](customer-orders-overview.md#edit-an-existing-customer-order).</span></span>

- <span data-ttu-id="a00af-138">**Nouto** – Tämä vaihtoehto on käytettävissä, jos tilauksessa on vähintään yksi rivi, joka on määritetty noudettavaksi käyttäjän nykyisessä myymälässä.</span><span class="sxs-lookup"><span data-stu-id="a00af-138">**Pick up** – This option will be available if the order has one or more lines designated for pickup at the user's current store.</span></span> <span data-ttu-id="a00af-139">Tämä toiminto käynnistää keräilytyönkulun, jossa käyttäjä voi valita kerättävät tuotteet ja joka luo myynnin keräilytapahtuman.</span><span class="sxs-lookup"><span data-stu-id="a00af-139">This operation launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>

## <a name="add-notifications-to-the-recall-order-operation"></a><span data-ttu-id="a00af-140">Ilmoitusten lisääminen palautustilauksen toimintoon</span><span class="sxs-lookup"><span data-stu-id="a00af-140">Add notifications to the recall order operation</span></span>

<span data-ttu-id="a00af-141">Versiossa 10.0.18 ja sitä myöhemmässä versiossa voit tarvittaessa määrittää **Tilauksen palautus** -toiminnolle myyntipisteilmoitukset ja live- ruutuhälytykset.</span><span class="sxs-lookup"><span data-stu-id="a00af-141">In version 10.0.18 and later, you can configure POS notifications and live tile alerts for the **Order Recall** operation if desired.</span></span> <span data-ttu-id="a00af-142">Lisätietoja on kohdassa [Tilausilmoitusten näyttäminen myyntipisteessä](notifications-pos.md).</span><span class="sxs-lookup"><span data-stu-id="a00af-142">For more information, see [Show order notifications in the point of sale (POS)](notifications-pos.md).</span></span>  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
