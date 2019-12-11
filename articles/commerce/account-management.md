---
title: Tilinhallinnan sivut ja moduulit
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen tilienhallintasivuista ja -moduuleista.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785375"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="d672c-103">Tilinhallinnan sivut ja moduulit</span><span class="sxs-lookup"><span data-stu-id="d672c-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d672c-104">Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen tilienhallintasivuista ja -moduuleista.</span><span class="sxs-lookup"><span data-stu-id="d672c-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d672c-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d672c-105">Overview</span></span>

<span data-ttu-id="d672c-106">Tilien hallinta viittaa sivuryhmään, jota käytetään Dynamics 365 Commercen käyttäjän tileihin liittyvien tietojen hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="d672c-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="d672c-107">Tilinhallinnan sivut sisältävät tilinhallinnan saapumissivun, käyttäjäprofiilisivun, käyttäjän osoitteen sivun, tilaushistoriasivun, tilaustietojen sivun, kanta-asiakkuussivun ja toivomusluettelosivun.</span><span class="sxs-lookup"><span data-stu-id="d672c-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="d672c-108">Tilinhallinnan saapumissivu</span><span class="sxs-lookup"><span data-stu-id="d672c-108">Account management landing page</span></span>

<span data-ttu-id="d672c-109">Tilihallinnan saapumissivulla käytetään seuraavia moduuleja:</span><span class="sxs-lookup"><span data-stu-id="d672c-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="d672c-110">**Sisällönsijoittelu** – Tämä moduuli on säilömoduuli, joka sisältää kaikki moduulit tilinhallinnan saapumissivulla.</span><span class="sxs-lookup"><span data-stu-id="d672c-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="d672c-111">**Tilin tervetulonimike** – Tämä moduuli sisältää tervetulosanoman tilinhallinnan sivulla.</span><span class="sxs-lookup"><span data-stu-id="d672c-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="d672c-112">Se sisältää ylätunnisteen ja ruudun koon ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="d672c-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="d672c-113">**Ruudun koko** -ominaisuus määrittää moduulin leveyden sisällönsijoittelumoduulissa.</span><span class="sxs-lookup"><span data-stu-id="d672c-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="d672c-114">Arvot vaihtelevat välillä **1**–**12**, jossa **12** edustaa sisällönsijoitussäilön täyttä leveyttä.</span><span class="sxs-lookup"><span data-stu-id="d672c-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="d672c-115">**Tilin tilauksen sijoittelunimike** – Tämän moduulin avulla voit määrittää yhteenvedon käyttäjätilin tekemistä tilauksista.</span><span class="sxs-lookup"><span data-stu-id="d672c-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="d672c-116">Se sisältää ylätunnisteen ja ruudun koon ominaisuudet sekä näkymän tietojen linkin.</span><span class="sxs-lookup"><span data-stu-id="d672c-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="d672c-117">Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen tilaushistoriasivulle.</span><span class="sxs-lookup"><span data-stu-id="d672c-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="d672c-118">**Tiliprofiilin sijoittelunimike** – Tätä moduulia käytetään käyttäjäprofiilin yhteenvedon määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="d672c-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="d672c-119">Se sisältää ylätunnisteen ja ruudun koon ominaisuudet sekä näkymän tietojen linkin.</span><span class="sxs-lookup"><span data-stu-id="d672c-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="d672c-120">Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen käyttäjäprofiilisivulle.</span><span class="sxs-lookup"><span data-stu-id="d672c-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="d672c-121">**Toivomuslistan nimike** – Tämän moduulin avulla määritetään asiakkaan toivomuslistan nimikkeiden yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="d672c-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="d672c-122">Se voi esimerkiksi ilmoittaa, että toivomuslistassa on 10 nimikettä.</span><span class="sxs-lookup"><span data-stu-id="d672c-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="d672c-123">Se sisältää ylätunnisteen ja ruudun koon ominaisuudet sekä näkymän tietojen linkin.</span><span class="sxs-lookup"><span data-stu-id="d672c-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="d672c-124">Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen toivomuslistasivulle.</span><span class="sxs-lookup"><span data-stu-id="d672c-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="d672c-125">**Tilin osoitteen nimike** – Tätä moduulia käytetään käyttäjän osoitteiden yhteenvedon määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="d672c-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="d672c-126">Siinä voi lukea esimerkiksi seuraava teksti: Tilillesi on lisätty 2 osoitetta.</span><span class="sxs-lookup"><span data-stu-id="d672c-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="d672c-127">Se sisältää ylätunnisteen ja ruudun koon ominaisuudet sekä näkymän tietojen linkin.</span><span class="sxs-lookup"><span data-stu-id="d672c-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="d672c-128">Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen käyttäjän osoitteen sivulle.</span><span class="sxs-lookup"><span data-stu-id="d672c-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="d672c-129">**Tilin kanta-asiakasnimike** – Tämän moduulin avulla näytetään ja linkitetään kanta-asiakasohjelman tiedot.</span><span class="sxs-lookup"><span data-stu-id="d672c-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="d672c-130">Se sisältää ylätunnisteen ja ruudun koon ominaisuudet, näkymän tietojen linkin ja Liity jäseneksi -linkin.</span><span class="sxs-lookup"><span data-stu-id="d672c-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="d672c-131">Näkymän tietojen linkki on määritettävä niin, että se ohjaa uudelleen kanta-asiakkuussivulle.</span><span class="sxs-lookup"><span data-stu-id="d672c-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="d672c-132">Liity jäseneksi -linkki on määritettävä niin, että se ohjaa sivulle, jossa käyttäjät voivat liittyä kanta-asiakasohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="d672c-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="d672c-133">Tilaushistoriasivu</span><span class="sxs-lookup"><span data-stu-id="d672c-133">Order history page</span></span>

<span data-ttu-id="d672c-134">Tilaushistoriasivulla näkyvät kaikki käyttäjän asettamat viimeaikaiset tilaukset tilaushistoriamoduulissa.</span><span class="sxs-lookup"><span data-stu-id="d672c-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="d672c-135">Tilauksen tietojen sivu</span><span class="sxs-lookup"><span data-stu-id="d672c-135">Order details page</span></span>

<span data-ttu-id="d672c-136">Tilaustietojen sivulla on eriteltyjä tietoja jokaisesta tilauksesta. Sitä voi käyttää tilaushistoriasivulta.</span><span class="sxs-lookup"><span data-stu-id="d672c-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="d672c-137">Se käyttää tilaustietojen moduulia, jossa edellytetään myynnin tai tapahtuman tunnusta tilaustietojen noutamiseksi.</span><span class="sxs-lookup"><span data-stu-id="d672c-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="d672c-138">Käyttäjäprofiilisivu</span><span class="sxs-lookup"><span data-stu-id="d672c-138">User profile page</span></span>

<span data-ttu-id="d672c-139">Käyttäjäprofiilisivulla näkyvät käyttäjätilin tiedot, kuten käyttäjän nimi ja sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="d672c-139">The user profile page shows user account details, such as user's name and email address.</span></span> <span data-ttu-id="d672c-140">Se käyttää käyttäjäprofiilimoduulia.</span><span class="sxs-lookup"><span data-stu-id="d672c-140">It uses the user profile module.</span></span> <span data-ttu-id="d672c-141">Vaikka sähköpostiosoitetta ei voi poistaa, sitä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="d672c-141">Although the email address can't be removed, it can be edited.</span></span>

### <a name="user-address-page"></a><span data-ttu-id="d672c-142">Käyttäjän osoitteen sivu</span><span class="sxs-lookup"><span data-stu-id="d672c-142">User address page</span></span>

<span data-ttu-id="d672c-143">Käyttäjän osoitteen sivulla on niiden osoitteiden luettelo, jotka on liitetty käyttäjätiliin.</span><span class="sxs-lookup"><span data-stu-id="d672c-143">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="d672c-144">Käyttäjä on antanut nämä osoitteet kassatoiminnon aikana tai lisännyt ne suoraan tälle sivulle.</span><span class="sxs-lookup"><span data-stu-id="d672c-144">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="d672c-145">Käyttäjän osoitteen moduulia käytetään osoitteiden lisäämiseen ja muokkaamiseen, ensisijaisen osoitteen määrittämiseen ja sivun olemassa olevien osoitteiden hahmontamiseen.</span><span class="sxs-lookup"><span data-stu-id="d672c-145">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="d672c-146">Toivomuslistasivu</span><span class="sxs-lookup"><span data-stu-id="d672c-146">Wish list page</span></span>

<span data-ttu-id="d672c-147">Toivomuslistasivulla ovat nimikkeet, jotka on lisätty asiakkaan toivomuslistaan.</span><span class="sxs-lookup"><span data-stu-id="d672c-147">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="d672c-148">Se käyttää toivomuslistamoduulia toivomuslistan nimikkeiden hahmontamiseen.</span><span class="sxs-lookup"><span data-stu-id="d672c-148">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="d672c-149">Kanta-asiakassivu</span><span class="sxs-lookup"><span data-stu-id="d672c-149">Loyalty page</span></span>

<span data-ttu-id="d672c-150">Kanta-asiakkuussivulla asiakkaat voivat liittyä kanta-asiakasohjelmaan. Jos he ovat jo kanta-asiakasohjelman jäseniä, he voivat katsella omia tietojaan.</span><span class="sxs-lookup"><span data-stu-id="d672c-150">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="d672c-151">He voivat myös tarkastella pisteitä, jotka he ovat ansainneet ja lunastaneet edellisten tapahtumien aikana.</span><span class="sxs-lookup"><span data-stu-id="d672c-151">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d672c-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d672c-152">Additional resources</span></span>

[<span data-ttu-id="d672c-153">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d672c-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d672c-154">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="d672c-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d672c-155">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="d672c-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="d672c-156">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="d672c-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d672c-157">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="d672c-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d672c-158">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="d672c-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d672c-159">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="d672c-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="d672c-160">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="d672c-160">Footer module</span></span>](author-footer-module.md)
