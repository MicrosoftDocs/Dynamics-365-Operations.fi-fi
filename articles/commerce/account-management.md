---
title: Tilinhallinnan sivut ja moduulit
description: Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen tilienhallintasivuista ja -moduuleista.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: b0f963bcf65ae622522fe52fd59996c6ec0ecf17
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817155"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="c6789-103">Tilinhallinnan sivut ja moduulit</span><span class="sxs-lookup"><span data-stu-id="c6789-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6789-104">Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 Commercen tilienhallintasivuista ja -moduuleista.</span><span class="sxs-lookup"><span data-stu-id="c6789-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c6789-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c6789-105">Overview</span></span>

<span data-ttu-id="c6789-106">Tilien hallinta viittaa sivuryhmään, jota käytetään Dynamics 365 Commercen käyttäjän tileihin liittyvien tietojen hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="c6789-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c6789-107">Tilinhallinnan sivut sisältävät tilinhallinnan saapumissivun, käyttäjäprofiilisivun, käyttäjän osoitteen sivun, tilaushistoriasivun, tilaustietojen sivun, kanta-asiakkuussivun ja toivomusluettelosivun.</span><span class="sxs-lookup"><span data-stu-id="c6789-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="c6789-108">Tilinhallinnan saapumissivu</span><span class="sxs-lookup"><span data-stu-id="c6789-108">Account management landing page</span></span>

<span data-ttu-id="c6789-109">Tilihallinnan saapumissivulla käytetään seuraavia moduuleja:</span><span class="sxs-lookup"><span data-stu-id="c6789-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="c6789-110">**Säilö** – kaikki tilinhallinnan saapumissivumoduulit on sijoitettava säilöön.</span><span class="sxs-lookup"><span data-stu-id="c6789-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="c6789-111">**Tilin tervetuloruutu** – Tämä moduuli sisältää tervetulosanoman tilinhallinnan sivulla.</span><span class="sxs-lookup"><span data-stu-id="c6789-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="c6789-112">Se sisältää otsikon ominaisuudet.</span><span class="sxs-lookup"><span data-stu-id="c6789-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="c6789-113">**Tilin yleinen ruutu** – Tämän moduulin avulla saadaan otsikot ja linkit tilinhallintasivuille, kuten Tilaushistoria- ja Oma profiili -sivuille.</span><span class="sxs-lookup"><span data-stu-id="c6789-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="c6789-114">Yleinen ruutumoduulin avulla voidaan määrittää minkä tahansa sivun ruutu.</span><span class="sxs-lookup"><span data-stu-id="c6789-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="c6789-115">Fabrikamissa tätä moduulia käytetään Tilaushistoria- ja Oma profiili -sivulinkeissä tilinhallinnan saapumissivulla.</span><span class="sxs-lookup"><span data-stu-id="c6789-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="c6789-116">**Toivelistaruutu** – Tämän moduulin avulla määritetään asiakkaan toivelistan nimikkeiden yhteenveto.</span><span class="sxs-lookup"><span data-stu-id="c6789-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="c6789-117">Se voi esimerkiksi ilmoittaa, että toivomuslistassa on 10 nimikettä.</span><span class="sxs-lookup"><span data-stu-id="c6789-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="c6789-118">Se sisältää otsikon ja Näytä tiedot -linkin.</span><span class="sxs-lookup"><span data-stu-id="c6789-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="c6789-119">Näytä tiedot -linkki on määritettävä niin, että se ohjaa uudelleen toivelistasivulle.</span><span class="sxs-lookup"><span data-stu-id="c6789-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="c6789-120">**Tilin osoiteruutu** – Tätä moduulia käytetään käyttäjän osoitteiden yhteenvedon määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="c6789-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="c6789-121">Siinä voi lukea esimerkiksi seuraava teksti: Tilillesi on lisätty 2 osoitetta.</span><span class="sxs-lookup"><span data-stu-id="c6789-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="c6789-122">Se sisältää otsikon ja Näytä tiedot -linkin.</span><span class="sxs-lookup"><span data-stu-id="c6789-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="c6789-123">Näytä tietojen -linkki on määritettävä niin, että se ohjaa uudelleen käyttäjän osoitesivulle.</span><span class="sxs-lookup"><span data-stu-id="c6789-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="c6789-124">**Tilin kanta-asiakasruutu** – Tämän moduulin avulla näytetään ja linkitetään kanta-asiakasohjelman tiedot.</span><span class="sxs-lookup"><span data-stu-id="c6789-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="c6789-125">Tässä ruudussa on kakis tilaa: toinen tila näyttää linkin kanta-asiakasohjelmaan liittymiseen, jos käyttäjä ei ole vielä jäsen.</span><span class="sxs-lookup"><span data-stu-id="c6789-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="c6789-126">Toinen tila näyttää linkit kanta-asiakastietojen sivulle, kun käyttäjä on jo jäsen.</span><span class="sxs-lookup"><span data-stu-id="c6789-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="c6789-127">Ominaisuuksia ovat otsikko, Rekisteröidy-linkki ja Näytä kanta-asiakkuus -linkki.</span><span class="sxs-lookup"><span data-stu-id="c6789-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="c6789-128">Näytä kanta-asiakkuus -linkki on määritettävä niin, että se ohjaa uudelleen kanta-asiakkuussivulle.</span><span class="sxs-lookup"><span data-stu-id="c6789-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="c6789-129">Rekisteröidy-linkki on määritettävä niin, että se ohjaa sivulle, jossa käyttäjät voivat liittyä kanta-asiakasohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="c6789-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="c6789-130">Tilaushistoriasivu</span><span class="sxs-lookup"><span data-stu-id="c6789-130">Order history page</span></span>

<span data-ttu-id="c6789-131">Tilaushistoriasivulla näkyvät kaikki käyttäjän asettamat viimeaikaiset tilaukset tilaushistoriamoduulissa.</span><span class="sxs-lookup"><span data-stu-id="c6789-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="c6789-132">Tilauksen tietojen sivu</span><span class="sxs-lookup"><span data-stu-id="c6789-132">Order details page</span></span>

<span data-ttu-id="c6789-133">Tilaustietojen sivulla on eriteltyjä tietoja jokaisesta tilauksesta. Sitä voi käyttää tilaushistoriasivulta.</span><span class="sxs-lookup"><span data-stu-id="c6789-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="c6789-134">Se käyttää tilaustietojen moduulia, jossa edellytetään myynnin tai tapahtuman tunnusta tilaustietojen noutamiseksi.</span><span class="sxs-lookup"><span data-stu-id="c6789-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="c6789-135">Käyttäjäprofiilisivu</span><span class="sxs-lookup"><span data-stu-id="c6789-135">User profile page</span></span>

<span data-ttu-id="c6789-136">Käyttäjäprofiilisivulla näkyvät käyttäjätilin tiedot, kuten käyttäjän nimi ja sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="c6789-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="c6789-137">Se käyttää käyttäjäprofiilin tieto- ja muokkausmoduuleja.</span><span class="sxs-lookup"><span data-stu-id="c6789-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="c6789-138">Vaikka sähköpostiosoitetta ei voi poistaa, sitä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="c6789-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="c6789-139">Käyttäjäprofiilisivulla näkyvät myös käyttäjäasetukset, joiden avulla käyttäjä voi halutessaan valita tiettyjä ominaisuuksia, kuten suositusluetteloiden mukauttamisen, tai poistaa ne käytöstä.</span><span class="sxs-lookup"><span data-stu-id="c6789-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="c6789-140">Käyttäjän osoitteen sivu</span><span class="sxs-lookup"><span data-stu-id="c6789-140">User address page</span></span>

<span data-ttu-id="c6789-141">Käyttäjän osoitteen sivulla on niiden osoitteiden luettelo, jotka on liitetty käyttäjätiliin.</span><span class="sxs-lookup"><span data-stu-id="c6789-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="c6789-142">Käyttäjä on antanut nämä osoitteet kassatoiminnon aikana tai lisännyt ne suoraan tälle sivulle.</span><span class="sxs-lookup"><span data-stu-id="c6789-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="c6789-143">Käyttäjän osoitteen moduulia käytetään osoitteiden lisäämiseen ja muokkaamiseen, ensisijaisen osoitteen määrittämiseen ja sivun olemassa olevien osoitteiden hahmontamiseen.</span><span class="sxs-lookup"><span data-stu-id="c6789-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="c6789-144">Toivomuslistasivu</span><span class="sxs-lookup"><span data-stu-id="c6789-144">Wish list page</span></span>

<span data-ttu-id="c6789-145">Toivomuslistasivulla ovat nimikkeet, jotka on lisätty asiakkaan toivomuslistaan.</span><span class="sxs-lookup"><span data-stu-id="c6789-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="c6789-146">Se käyttää toivomuslistamoduulia toivomuslistan nimikkeiden hahmontamiseen.</span><span class="sxs-lookup"><span data-stu-id="c6789-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="c6789-147">Kanta-asiakassivu</span><span class="sxs-lookup"><span data-stu-id="c6789-147">Loyalty page</span></span>

<span data-ttu-id="c6789-148">Kanta-asiakkuussivulla asiakkaat voivat tarkastella omia kanta-asiakastietojaan, jos he ovat jo kanta-asiakasohjelman jäseniä.</span><span class="sxs-lookup"><span data-stu-id="c6789-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="c6789-149">He voivat myös tarkastella pisteitä, jotka he ovat ansainneet ja lunastaneet edellisten tapahtumien aikana.</span><span class="sxs-lookup"><span data-stu-id="c6789-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="c6789-150">Sivu käyttää kanta-asiakastietomoduulia näyttämään kanta-asiakastiedot.</span><span class="sxs-lookup"><span data-stu-id="c6789-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="c6789-151">Kanta-asiakasohjelmaan liittymistä varten voidaan luoda markkinointisivu, jossa on kanta-asiakkaiden rekisteröitymisen ja kanta-asiakkuuden ehtojen moduulit.</span><span class="sxs-lookup"><span data-stu-id="c6789-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="c6789-152">Jos käyttäjä ei ole kanta-asiakasohjelman jäsen, käyttäjä voi rekisteröityä näiden moduulien avulla.</span><span class="sxs-lookup"><span data-stu-id="c6789-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6789-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c6789-153">Additional resources</span></span>

[<span data-ttu-id="c6789-154">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c6789-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c6789-155">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="c6789-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c6789-156">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="c6789-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c6789-157">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="c6789-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c6789-158">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="c6789-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c6789-159">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="c6789-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c6789-160">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="c6789-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c6789-161">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="c6789-161">Footer module</span></span>](author-footer-module.md)
