---
title: Tilinhallintasivujen yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tilinhallintasivujen yleiskatsaus.
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
ms.openlocfilehash: d0e066428e8c4717b5a50144f63e59b87089d286
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412079"
---
# <a name="account-management-pages-overview"></a><span data-ttu-id="61775-103">Tilinhallintasivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="61775-103">Account management pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="61775-104">Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen tilinhallintasivujen yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="61775-104">This topic provides an overview of account management pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="61775-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="61775-105">Overview</span></span>

<span data-ttu-id="61775-106">Tilinhallintasivujen avulla asiakkaat voivat tarkastella tietoja, jotka liittyvät heidän tiliinsä ja tilauksiin.</span><span class="sxs-lookup"><span data-stu-id="61775-106">Account management pages let customers view information that is related to their account and orders.</span></span> <span data-ttu-id="61775-107">Tilinhallinnan sivut sisältävät tilinhallinnan saapumissivun, käyttäjäprofiilisivun, osoitteiden sivun, tilaushistoriasivun, tilaustietojen sivun, kanta-asiakaspisteiden sivun ja toivomusluettelosivun.</span><span class="sxs-lookup"><span data-stu-id="61775-107">Account management pages include the account management landing page, and pages for the user's profile, addresses, order history, order details, loyalty points, and wish list.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="61775-108">Tilinhallinnan saapumissivu</span><span class="sxs-lookup"><span data-stu-id="61775-108">Account management landing page</span></span>

<span data-ttu-id="61775-109">Kun asiakas kirjautuu sisään ja valitsee **Oma tili**, tilinhallinnan saapumissivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="61775-109">When a customer signs in and selects **My Account**, the account management landing page is opened.</span></span> <span data-ttu-id="61775-110">Tällä sivulla on kaikkien tiliin liittyvien tietojen lyhyt yhteenveto. Tietoja ovat esimerkiksi käyttäjäprofiili, tilaukset, toivomuslista, osoitteet ja kanta-asiakkuuspisteet.</span><span class="sxs-lookup"><span data-stu-id="61775-110">This page provides a quick summary of all account-related information, such as the user's profile, orders, wish list, addresses, loyalty points.</span></span> <span data-ttu-id="61775-111">Tältä sivulta asiakas voi tutkia kunkin alueen lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="61775-111">From this page, the customer can access more details for each area.</span></span>

<span data-ttu-id="61775-112">Seuraavassa kuvassa on esimerkki tilinhallinnan saapumissivusta.</span><span class="sxs-lookup"><span data-stu-id="61775-112">The following illustration shows an example of the account management landing page.</span></span>

![Esimerkki tilinhallinnan saapumissivusta](./media/Account-Management.PNG)

### <a name="my-profile-page"></a><span data-ttu-id="61775-114">Oma profiili -sivu</span><span class="sxs-lookup"><span data-stu-id="61775-114">My profile page</span></span>

<span data-ttu-id="61775-115">**Oma profiili** -sivulla on asiakkaan tilitiedot, kuten nimi ja puhelinnumero.</span><span class="sxs-lookup"><span data-stu-id="61775-115">The **My profile** page shows customer's account information, such as his or her name and phone number.</span></span> <span data-ttu-id="61775-116">Asiakas voi päivittää profiilitietojaan tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="61775-116">The customer can update his or her profile information on this page.</span></span> <span data-ttu-id="61775-117">Tätä sivua voidaan mukauttaa siten, että se sisältää asiakkaan tilin lisämäärityksiä, kuten markkinointisähköpostiviestien hyväksyntävaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="61775-117">This page can be customized so that it includes additional customer account preferences, such as an option for opting in to marketing email.</span></span>

<span data-ttu-id="61775-118">Seuraavassa kuvassa on esimerkki **Oma profiili** -sivusta, joka on luotu moduulikirjaston avulla.</span><span class="sxs-lookup"><span data-stu-id="61775-118">The following illustration shows an example of a **My profile** page that was built by using the module library.</span></span>

![Esimerkki Oma profiili -sivusta](./media/Account-Management-MyProfile.PNG)

### <a name="addresses-page"></a><span data-ttu-id="61775-120">Osoitteet-sivu</span><span class="sxs-lookup"><span data-stu-id="61775-120">Addresses page</span></span>

<span data-ttu-id="61775-121">**Osoitteet**-sivulla asiakas voi lisätä osoitteita omalle tililleen.</span><span class="sxs-lookup"><span data-stu-id="61775-121">The **Addresses** page lets the customer add addresses to his or her account.</span></span> <span data-ttu-id="61775-122">Sivulla on myös niiden osoitteiden luettelo, joita asiakas on aiemmin lisännyt tai tallentanut tilille.</span><span class="sxs-lookup"><span data-stu-id="61775-122">It also shows the list of addresses that the customer has previously added or saved to the account.</span></span> <span data-ttu-id="61775-123">Nämä osoitteet ovat osoitteita, jotka asiakas on syöttänyt joko tälle sivulle tai tilauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="61775-123">These addresses are addresses that the customer entered either on this page or while placing an order.</span></span>

<span data-ttu-id="61775-124">Seuraavassa kuvassa on esimerkki **Osoitteet**-sivusta.</span><span class="sxs-lookup"><span data-stu-id="61775-124">The following illustration shows an example of the **Addresses** page.</span></span>

![Esimerkki Osoitteet-sivusta](./media/Account-Management-Address.png)

### <a name="order-history-and-order-details-pages"></a><span data-ttu-id="61775-126">Tilaushistoria- ja Tilaustiedot-sivut</span><span class="sxs-lookup"><span data-stu-id="61775-126">Order history and Order details pages</span></span>

<span data-ttu-id="61775-127">**Tilaushistoria**-sivulla näkyy yhteenveto kaikista tilauksista, jotka asiakas on lähettänyt tilin avulla.</span><span class="sxs-lookup"><span data-stu-id="61775-127">The **Order history** page shows a summary of all orders that the customer has submitted by using his or her account.</span></span> <span data-ttu-id="61775-128">Sen avulla saa nopeasti yhteenvedon tilatuista nimikkeistä, vahvistusnumerosta, myynnin tunnuksesta, seurannan tiedoista ja muista tiedoista.</span><span class="sxs-lookup"><span data-stu-id="61775-128">It gives a quick summary of the items that were ordered, the confirmation number, sales ID, tracking information, and other information.</span></span> <span data-ttu-id="61775-129">Kunkin tilauksen yksityiskohtaisempaa erittelyä voi tarkastella **Tilaustiedot**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="61775-129">If the customer wants to view a more detailed breakdown of each order, there is an **Order details** page.</span></span> <span data-ttu-id="61775-130">Tällä sivulla on tietoja, kuten toimitusosoite, maksutiedot, alennukset, verot ja tilauksen toimituskulut.</span><span class="sxs-lookup"><span data-stu-id="61775-130">This page includes information such as the shipping address, payment information, discounts, taxes, and shipping costs for the order.</span></span>

<span data-ttu-id="61775-131">Seuraavassa kuvassa on esimerkki **Tilaushistoria**-sivusta.</span><span class="sxs-lookup"><span data-stu-id="61775-131">The following illustration shows an example of the **Order history** page.</span></span>

![Esimerkki Tilaushistoria-sivusta](./media/Account-Management-OrderHistory.PNG)

<span data-ttu-id="61775-133">Seuraavassa kuvassa on esimerkki **Tilauksen tiedot** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="61775-133">The following illustration shows an example of the **Order details** page.</span></span>

![Esimerkki Tilauksen tiedot -sivusta](./media/Account-Management-OrderDetails.PNG)

### <a name="loyalty-program-page"></a><span data-ttu-id="61775-135">Kanta-asiakasohjelma-sivu</span><span class="sxs-lookup"><span data-stu-id="61775-135">Loyalty program page</span></span>

<span data-ttu-id="61775-136">**Kanta-asiakasohjelma**-sivulla asiakas voi liittyä kanta-asiakasohjelman jäseneksi.</span><span class="sxs-lookup"><span data-stu-id="61775-136">The **Loyalty program** page lets the customer become a member of a loyalty program.</span></span> <span data-ttu-id="61775-137">Kun asiakas on rekisteröitynyt kanta asiakasohjelmaan, sen **Kanta-asiakasohjelma**-sivulle lisätään tiedot, kuten ansaittujen pisteiden ja lunastettujen pisteiden määrä.</span><span class="sxs-lookup"><span data-stu-id="61775-137">After a customer has signed up for a loyalty program, the **Loyalty program** page include details such as the number of points that have been earned and the number of points that have been redeemed.</span></span>

<span data-ttu-id="61775-138">Seuraavassa kuvassa on **Kanta-asiakasohjelma** -sivun esimerkki.</span><span class="sxs-lookup"><span data-stu-id="61775-138">The following illustration shows an example of a **Loyalty program** page.</span></span>

![Esimerkki Kanta-asiakasohjelma-sivusta](./media/Account-Management-Loyalty.PNG)

### <a name="wishlist-page"></a><span data-ttu-id="61775-140">Toivelistasivu</span><span class="sxs-lookup"><span data-stu-id="61775-140">Wishlist page</span></span>

<span data-ttu-id="61775-141">**Toivomuslista**-sivulla on niiden nimikkeiden luettelo, jotka asiakas on lisännyt toivomuslistaansa.</span><span class="sxs-lookup"><span data-stu-id="61775-141">The **Wishlist** page shows a list of the items that the customer has added to his or her wish list.</span></span> <span data-ttu-id="61775-142">Sekä tuotteet että tuotevariantit voidaan lisätä toivomuslistaan.</span><span class="sxs-lookup"><span data-stu-id="61775-142">Both products and product variants can be added to the wish list.</span></span> <span data-ttu-id="61775-143">Tällä sivulla asiakas voi poistaa nimikkeen toivomuslistasta tai lisätä nimikkeen suoraan ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="61775-143">From this page, the customer can remove an item from the wish list or add an item directly to the cart.</span></span>

<span data-ttu-id="61775-144">Seuraavassa kuvassa on **Toivomuslista**-sivun esimerkki.</span><span class="sxs-lookup"><span data-stu-id="61775-144">The following illustration shows an example of a **Wishlist** page.</span></span>

![Esimerkki Toivomuslista-sivusta](./media/Account-Management-Wishlist.PNG)

<span data-ttu-id="61775-146">Lisätietoja tilienhallintamoduuleista ja niiden muokkaamisesta on kohdassa [Tilinhallinta](account-management.md).</span><span class="sxs-lookup"><span data-stu-id="61775-146">For more information about account management modules and how to author them, see [Account Management](account-management.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61775-147">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="61775-147">Additional resources</span></span>

[<span data-ttu-id="61775-148">Aloitussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="61775-148">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="61775-149">Tuotetietosivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="61775-149">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="61775-150">Ostoskorin ja maksusivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="61775-150">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

