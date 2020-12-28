---
title: Myyntipisteen Peruuta tilaus -toiminto
description: Tässä ohjeaiheessa käsitellään myyntipisteen parannetulla tilausten peruutussivuilla olevia ominaisuuksia.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42b11ff16757d633b868dfdf248341193a44378f
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665295"
---
# <a name="recall-order-operation-in-pos"></a><span data-ttu-id="e56e4-103">Myyntipisteen Peruuta tilaus -toiminto</span><span class="sxs-lookup"><span data-stu-id="e56e4-103">Recall order operation in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e56e4-104">Commercen myyntipisteen **Peruuta tilaus** -toiminnossa on päivitetyt tilauksen haku- ja suodatusominaisuudet ja tilauskohtaiset tiedot.</span><span class="sxs-lookup"><span data-stu-id="e56e4-104">The **Recall order** operation in the Commerce point of sale (POS) provides updated order search and filtering features and order-specific information.</span></span> <span data-ttu-id="e56e4-105">Tämä ominaisuus on käytettävissä Commercen versiossa 10.0.15 ja sitä uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="e56e4-105">This feature is available in Commerce versions 10.0.15 and later.</span></span>

<span data-ttu-id="e56e4-106">Ota tämä toiminto käyttöön ottamalla **Parannettu tilauksen peruutustoiminto myyntipisteessä** -ominaisuus käyttöön Commercen pääkonttorin **Ominaisuuksien hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="e56e4-106">To enable this functionality, turn the **Improved Recall order operation in POS** feature on in **Feature management** workspace in Commerce headquarters.</span></span> <span data-ttu-id="e56e4-107">Kun ominaisuus on otettu käyttöön, harkitse myyntipisteen [näytön asettelujen](pos-screen-layouts.md) päivittämistä, jotta voit käyttää muutettuja ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="e56e4-107">After you enable the feature, consider updating your [screen layouts](pos-screen-layouts.md) in POS to take advantage of some of the changed  capabilities.</span></span>

<span data-ttu-id="e56e4-108">**Peruuta tilaus** -toimintopainikkeen määritys antaa organisaatioille mahdollisuuden ottaa toiminnon käyttöön siten, että näyttö määritetty valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="e56e4-108">The configuration of the **Recall order** operation button allows organizations to deploy the operation with a pre-defined display.</span></span>

![Painikeruudukon määritykset](media/recallorderbuttongrid.png)

<span data-ttu-id="e56e4-110">Näyttöasetukset:</span><span class="sxs-lookup"><span data-stu-id="e56e4-110">The display options are as follows.</span></span>
- <span data-ttu-id="e56e4-111">**Ei mitään** – Tällä asetuksella toiminto otetaan käyttöön ilman tiettyä näyttöä.</span><span class="sxs-lookup"><span data-stu-id="e56e4-111">**None** – This option deploys the operation with no specific display.</span></span> <span data-ttu-id="e56e4-112">Kun käyttäjä avaa toiminnon tällä määrityksellä, häntä pyydetään hakemaan tilaukset tai tekemään valinnan esimääritetystä tilaussuodattimesta.</span><span class="sxs-lookup"><span data-stu-id="e56e4-112">When a user opens the operation with this configuration, they will be prompted to search and find orders or choose from a pre-defined order filter.</span></span>
- <span data-ttu-id="e56e4-113">**Täytettävät tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka myymälän on täytettävä.</span><span class="sxs-lookup"><span data-stu-id="e56e4-113">**Orders to fulfill** – When a user launches the operation, a query will run automatically to search and display a list of orders that are to be fulfilled by the store.</span></span> <span data-ttu-id="e56e4-114">Nämä tilaukset määritetään myymälästä noudatettavaksi tai lähetettäväksi eikä näiden tilausten rivejä ole vielä poimittu tai pakattu.</span><span class="sxs-lookup"><span data-stu-id="e56e4-114">These orders are configured for in-store pickup or store shipment and the lines of these orders have not yet been picked or packed.</span></span>
- <span data-ttu-id="e56e4-115">**Poimittavat tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka on määritetty myymälästä poimittavaksi käyttäjän nykyisestä myymälästä.</span><span class="sxs-lookup"><span data-stu-id="e56e4-115">**Orders to pick up** – When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for in-store pickup at the user's current store.</span></span>
- <span data-ttu-id="e56e4-116">**Lähetettävät tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka on määritetty lähetettäväksi käyttäjän nykyisestä myymälästä.</span><span class="sxs-lookup"><span data-stu-id="e56e4-116">**Orders to ship** - When a user launches the operation, a query will run automatically to search and display a list of orders that are configured for shipment from the user's current store.</span></span>

<span data-ttu-id="e56e4-117">Jos **Peruuta tilaus** -toiminto käynnistetään myyntipisteessä ja jos näytön määrityksenä on **Ei mitään**, käyttäjä voi hakea ja noutaa tilauksia jollakin seuraavista tavoista.</span><span class="sxs-lookup"><span data-stu-id="e56e4-117">When launching the **Recall order** operation from POS, if the display is configured to **None**, a user will be able to search and retrieve orders in one of the following ways.</span></span>
- <span data-ttu-id="e56e4-118">Skannaa tilauksen viivakoodit.</span><span class="sxs-lookup"><span data-stu-id="e56e4-118">Scan order barcodes.</span></span> <span data-ttu-id="e56e4-119">Tällä tavoin haetaan vastaavuuksien tilauksen numeron, kanavaviitteen ja vastaanottotunnuksen kentät.</span><span class="sxs-lookup"><span data-stu-id="e56e4-119">This will search order number, channel reference, and receipt ID fields for matches.</span></span>
- <span data-ttu-id="e56e4-120">Valitse sovelluspalkissa **Hae tilaukset**- tai **Hae ja suodata** -kuvake. Tällä tavoin voit käyttää suodatusmekanismia suodatusehtoja vastaavien tilausten paikantamiseen.</span><span class="sxs-lookup"><span data-stu-id="e56e4-120">Select **Search orders** or **Search and filter** icon on the AppBar to use the filtering mechanism to locate orders that meet the filter criteria.</span></span>
- <span data-ttu-id="e56e4-121">Valitse jokin esimääritetty suodatin avattavassa **Näytä tilaukset** -valikossa (täytettävät tilaukset, poimittavat tilaukset tai lähetettävät tilaukset).</span><span class="sxs-lookup"><span data-stu-id="e56e4-121">Choose from a pre-defined filter from the **Show Orders** drop-down menu (orders to fulfill, orders to pick up, or orders to ship).</span></span>

![RecallOrderMainMenu](media/recallordermain.png)

<span data-ttu-id="e56e4-123">Kun ehtojen mukainen haku on tehty, sovellus näyttää vastaavien myyntitilausten luettelon.</span><span class="sxs-lookup"><span data-stu-id="e56e4-123">After search criteria are applied, the application will display a list of matching sales orders.</span></span>

![RecallOrderDetail](media/orderrecalldetail.png)

<span data-ttu-id="e56e4-125">Käyttäjä voi valita luettelossa tilauksen ja katsoa lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="e56e4-125">A user can select an order on the list to view additional details.</span></span> <span data-ttu-id="e56e4-126">Näytön oikealla puolella on tietopaneeli, jossa on tietoja valitusta tilauksesta, kuten tilausrivin tiedot, toimituksen tiedot ja täyttämistiedot.</span><span class="sxs-lookup"><span data-stu-id="e56e4-126">The information panel on the right side of the screen displays specifics on the selected order, including order line details, delivery details, and fulfillment details.</span></span>

<span data-ttu-id="e56e4-127">Valitse toiminto sovelluspalkissa.</span><span class="sxs-lookup"><span data-stu-id="e56e4-127">From the AppBar, a user can select an operation.</span></span> <span data-ttu-id="e56e4-128">Tilauksen tilan mukaan määräytyy, voidaanko tietyt toiminnot ottaa käyttää.</span><span class="sxs-lookup"><span data-stu-id="e56e4-128">Depending on the status of the order, certain operations may not be enabled.</span></span>

- <span data-ttu-id="e56e4-129">**Palautus** – palauttaa vähintään yhden valittuun myyntilaskuun liittyvän laskun.</span><span class="sxs-lookup"><span data-stu-id="e56e4-129">**Return** – Executes a return for one or more invoices related to the selected customer order.</span></span>

- <span data-ttu-id="e56e4-130">**Peruuta** – myöntää valitun myyntitilauksen täyden peruutuksen.</span><span class="sxs-lookup"><span data-stu-id="e56e4-130">**Cancel** – Issue a full cancellation of the selected sales order.</span></span>

- <span data-ttu-id="e56e4-131">**Täytä** – Siirtää käyttäjän tilauksen täyttämissivulle, joka esisuodatetaan valittuun tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="e56e4-131">**Fulfill** – Transfers the user to the order fulfillment page, which will be pre-filtered for the selected order.</span></span> <span data-ttu-id="e56e4-132">Näkyvissä on vain ne valitun tilauksen tilausrivit, jotka ovat avoimia täytettäväksi käyttäjän myymälässä.</span><span class="sxs-lookup"><span data-stu-id="e56e4-132">Only order lines that are open for fulfillment by the user's store for the selected order will be displayed.</span></span>

- <span data-ttu-id="e56e4-133">**Muokkaa** – käyttäjät saavat tehdä muutoksia valittuun asiakastilaukseen.</span><span class="sxs-lookup"><span data-stu-id="e56e4-133">**Edit** – Allows users to make changes to the selected customer order.</span></span>

- <span data-ttu-id="e56e4-134">**Keräile** – käynnistää keräilytyönkulun, jossa käyttäjä voi valita kerättävät tuotteet ja joka luo myynnin keräilytapahtuman.</span><span class="sxs-lookup"><span data-stu-id="e56e4-134">**Pick up** – Launches the pickup flow, which allows the user to choose the products to be picked up and creates the pickup sales transaction.</span></span>
