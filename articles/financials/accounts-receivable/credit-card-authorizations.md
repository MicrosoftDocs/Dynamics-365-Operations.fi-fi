---
title: "Luottokorttien määritys, varmennus ja sieppaaminen"
description: "Tässä artikkelissa on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin tehtävän luottokortin varmennuksen yleiskatsaus. Artikkeli sisältää tietoja maksupalvelun määrittämisestä, luottokortin lisäämisestä myyntitilaukseen ja varmennuksen mitätöinnistä."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations, Core, Retail
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 40d636cac477871f094286d29edc32cd5616ad44
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="1baa1-104">Luottokorttien määritys, varmennus ja sieppaaminen</span><span class="sxs-lookup"><span data-stu-id="1baa1-104">Credit card setup, authorization, and capture</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


<span data-ttu-id="1baa1-105">Tässä artikkelissa on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin tehtävän luottokortin varmennuksen yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="1baa1-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="1baa1-106">Artikkeli sisältää tietoja maksupalvelun määrittämisestä, luottokortin lisäämisestä myyntitilaukseen ja varmennuksen mitätöinnistä.</span><span class="sxs-lookup"><span data-stu-id="1baa1-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="1baa1-107">Luottokorttien maksupalvelun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1baa1-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="1baa1-108">Jos haluat käyttää luottokortteja, sinun on määritettävä ja aktivoitava maksupalvelu Maksupalvelut-sivulla.</span><span class="sxs-lookup"><span data-stu-id="1baa1-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="1baa1-109">Maksupalvelu toimii välittäjänä yrityksesi ja asiakkaan korttimaksut käsittelevän pankin välillä.</span><span class="sxs-lookup"><span data-stu-id="1baa1-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="1baa1-110">Sinun on käytettävä luottokorttimaksun tarjoajaa, joka on saatavilla Maksuyhdistin-kentässä ja määrittää tili kyseiselle palveluntarjoajalle.</span><span class="sxs-lookup"><span data-stu-id="1baa1-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="1baa1-111">Sinun on sitten määritettävä muut asetukset Maksupalvelut-sivulla, määritettävä luottokorttityypit American Express, Discover, MasterCard ja Visa -korteille Luottokorttityypit-sivulla ja aktivoitava palveluntarjoaja oletuspalveluntarjoajaksi.</span><span class="sxs-lookup"><span data-stu-id="1baa1-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="1baa1-112">Sinun on myös noudatettava seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="1baa1-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="1baa1-113">Määritä luottokortin varmennuksessa käytettävät parametrit Myyntireskontran parametrit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1baa1-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="1baa1-114">Määritä luottokorttien maksuehdot Maksuehdot-sivulla.</span><span class="sxs-lookup"><span data-stu-id="1baa1-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="1baa1-115">Valitse Luottokortti Maksutyyppi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1baa1-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="1baa1-116">Syötä asiakkaan luottokorttitiedot Asiakkaan luottokortit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="1baa1-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="1baa1-117">Uuden luottokortin lisääminen</span><span class="sxs-lookup"><span data-stu-id="1baa1-117">Adding a new credit card</span></span>
<span data-ttu-id="1baa1-118">Voit luoda uudet luottokorttitietueet Asiakkaat-sivulla kohdasta Asiakas > Määritä > Luottokortti.</span><span class="sxs-lookup"><span data-stu-id="1baa1-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="1baa1-119">Voit myös luoda luottokorttitietueita kirjatessasi myyntitilauksia Myyntitilaus-sivulla kohdasta Hallinta > Asiakas > Luottokortti > Rekisteröi.</span><span class="sxs-lookup"><span data-stu-id="1baa1-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>
<span data-ttu-id="1baa1-120">Luottokortin lisääminen myyntitilaukseen</span><span class="sxs-lookup"><span data-stu-id="1baa1-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="1baa1-121">Voit lisätä luottokortin myyntitilaukseen valitsemalla luottokortin Myyntitilaus-sivun Hinnat ja alennukset -pikavälilehden luottokorttihausta.</span><span class="sxs-lookup"><span data-stu-id="1baa1-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="1baa1-122">Varmennusprosessin voit aloittaa valitsemalla toimintoruudun Hallinta-välilehdestä kohdan Luottokortti ja Varmenna.</span><span class="sxs-lookup"><span data-stu-id="1baa1-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>
<span data-ttu-id="1baa1-123">Luottokortin varmennus</span><span class="sxs-lookup"><span data-stu-id="1baa1-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="1baa1-124">Kun luottokortti varmennetaan, kortin numero ja kortin haltijan henkilöllisyys varmennetaan ja käytettävissä oleva luottosaldo tarkistetaan.</span><span class="sxs-lookup"><span data-stu-id="1baa1-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="1baa1-125">Voit myös tarkistaa kortin tarkistusnumeron ja kortinhaltijan osoitteen.</span><span class="sxs-lookup"><span data-stu-id="1baa1-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="1baa1-126">Laskun summa vähennetään tämän jälkeen asiakkaan käytettävissä olevasta luottosaldosta.</span><span class="sxs-lookup"><span data-stu-id="1baa1-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="1baa1-127">Maksupalvelu lähettää tiedon luottokortin hyväksymisestä tai hylkäämisestä.</span><span class="sxs-lookup"><span data-stu-id="1baa1-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="1baa1-128">Kun myyntitilaus laskutetaan, laskun summa veloitetaan (siepataan) luottokortilta.</span><span class="sxs-lookup"><span data-stu-id="1baa1-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="1baa1-129">Kortin tarkistusnumero</span><span class="sxs-lookup"><span data-stu-id="1baa1-129">Card verification value</span></span>

<span data-ttu-id="1baa1-130">Voit vaatia kortin tarkistusarvon käyttöä, jota kutsutaan toisinaan myös turvakoodiksi.</span><span class="sxs-lookup"><span data-stu-id="1baa1-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="1baa1-131">American Express -korteilla tämä luku on nelinumeroinen.</span><span class="sxs-lookup"><span data-stu-id="1baa1-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="1baa1-132">Discover, MasterCard ja Visa -korteilla luku on kolminumeroinen.</span><span class="sxs-lookup"><span data-stu-id="1baa1-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="1baa1-133">Osoitteen tarkistus</span><span class="sxs-lookup"><span data-stu-id="1baa1-133">Address verification</span></span>

<span data-ttu-id="1baa1-134">Osoitteen varmennustiedot lähetetään aina maksupalvelulle.</span><span class="sxs-lookup"><span data-stu-id="1baa1-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="1baa1-135">Voit päättää, kuinka paljon tietoja tarvitaan tapahtuman hyväksymiseksi.</span><span class="sxs-lookup"><span data-stu-id="1baa1-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="1baa1-136">Muista varmistaa palveluntarjoajaltasi, voiko se hyväksyä näitä tietoja.</span><span class="sxs-lookup"><span data-stu-id="1baa1-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="1baa1-137">Nämä ovat osoitetietojen varmennuksen vaihtoehdot:</span><span class="sxs-lookup"><span data-stu-id="1baa1-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="1baa1-138">**Hyväksy tapahtuma aina** – Hyväksy tapahtuma riippumatta osoitteen tarkistustuloksista.</span><span class="sxs-lookup"><span data-stu-id="1baa1-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="1baa1-139">**Tilin omistaja** – Vertaa kortinhaltijan nimeä tapahtumasta luottokorttiyhtiön tietoihin.</span><span class="sxs-lookup"><span data-stu-id="1baa1-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="1baa1-140">**Laskutusosoite** – Vertaa kortinhaltijan nimeä ja laskutusosoitetta tapahtumasta luottokorttiyhtiön tietoihin.</span><span class="sxs-lookup"><span data-stu-id="1baa1-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="1baa1-141">**Laskutusosoitteen postinumero** – Vertaa kortinhaltijan nimeä, laskutusosoitetta ja postinumeroa tapahtumasta luottokorttiyhtiön tietoihin.</span><span class="sxs-lookup"><span data-stu-id="1baa1-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="1baa1-142">Tietotuki</span><span class="sxs-lookup"><span data-stu-id="1baa1-142">Data support</span></span>
<span data-ttu-id="1baa1-143">Voit määrittää kullekin tukemallesi luottokorttityypille tuetun tiedon tason.</span><span class="sxs-lookup"><span data-stu-id="1baa1-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="1baa1-144">Taso määrittää, kuinka paljon tietoja tapahtumasta siirretään maksupalvelulle.</span><span class="sxs-lookup"><span data-stu-id="1baa1-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="1baa1-145">Muista varmistaa palveluntarjoajaltasi, voiko se tarjota näitä tietoja.</span><span class="sxs-lookup"><span data-stu-id="1baa1-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="1baa1-146">Nämä ovat tietotuen tasoasetukset:</span><span class="sxs-lookup"><span data-stu-id="1baa1-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="1baa1-147">**Taso 1** – Siirrä tapahtuman päivämäärä, summa ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="1baa1-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="1baa1-148">**Taso 2** – Siirrä kaikki tason 1 tiedot sekä toimitusosoite, myyjän osoite ja verotiedot.</span><span class="sxs-lookup"><span data-stu-id="1baa1-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="1baa1-149">**Taso 3** – Siirrä kaikki tason 2 tiedot sekä tilausrivin tiedot.</span><span class="sxs-lookup"><span data-stu-id="1baa1-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="1baa1-150">Osamaksut</span><span class="sxs-lookup"><span data-stu-id="1baa1-150">Partial payments</span></span>
<span data-ttu-id="1baa1-151">Jos toimitat vain osan tilauksesta, osatilauksen määrä siepataan ja koko tilauksen määrälle tarkoitettu varmennus suljetaan.</span><span class="sxs-lookup"><span data-stu-id="1baa1-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="1baa1-152">Toimittamattomalle tilausmäärälle luodaan sitten uusi varmennus.</span><span class="sxs-lookup"><span data-stu-id="1baa1-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="1baa1-153">Varmennuksen mitätöinti </span><span class="sxs-lookup"><span data-stu-id="1baa1-153">Voiding an authorization</span></span>
<span data-ttu-id="1baa1-154">Luottokortin varmennuksen voit mitätöidä vaihtamalla maksutavan sellaiseksi, jolla ei ole Luottokortti-tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="1baa1-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>






