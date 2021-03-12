---
title: Ostoskorin ja maksusivun yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen ostoskori- ja kassasivun yleiskatsaus.
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
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a9b7fe1722c366eb504882c61a337a95500c92ab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000506"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="a1f2b-103">Ostoskorin ja maksusivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a1f2b-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a1f2b-104">Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen ostoskori- ja kassasivun yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a1f2b-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a1f2b-105">Overview</span></span>

<span data-ttu-id="a1f2b-106">Sähköisen kaupankäynnin sivuston ostoskorisivulla näkyvät kaikki nimikkeet, jotka asiakas on lisännyt koriin.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="a1f2b-107">Ostoskorisivu luodaan ostoskorimoduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="a1f2b-108">Ostoskorimoduuli on säilö, joka isännöi kaikkia niitä moduuleja, joita tarvitaan näytettäessä ostoskorin nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="a1f2b-109">Ostoskorimoduuli voi käyttää myös muita moduuleja tilauksen yhteenvedon ja mahdollisten asiakastilausta koskevien tarjouskoodien näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="a1f2b-110">Sähköisen kaupankäynnin sivuston kassasivulla on vaiheittainen työnkulku, jota asiakkaat seuraavat syöttäessään tilauksen tekemisessä vaadittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="a1f2b-111">Kassamoduuli voi sisältää moduuleja, jotka käsittelevät toimitusosoitetta, toimitusmenetelmiä, laskutustietoja, tilauksen yhteenvetoa ja muita asiakastilauksiin liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="a1f2b-112">Ostoskorisivu</span><span class="sxs-lookup"><span data-stu-id="a1f2b-112">Cart page</span></span>

<span data-ttu-id="a1f2b-113">Ostoskorisivu toimii ostoskassina. Se sisältää kaikki ostoskoriin lisätyt nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="a1f2b-114">Seuraavassa kuvassa on esimerkki ostoskorisivusta, joka on luotu verkon moduulikirjaston ja Fabrikam-teeman avulla.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-114">The following illustration show an example of a cart page that was built by using the module library and the "Fabrikam" theme.</span></span>

![Esimerkki ostoskorisivusta](./media/cart2.PNG)

<span data-ttu-id="a1f2b-116">Ostoskorisivun päätekstiosassa näkyvät kaikki nimikkeet, jotka asiakas on lisännyt koriin.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="a1f2b-117">Kaikki käytettävissä olevat alennukset ovat esillä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="a1f2b-118">Nämä alennukset sisältävät monimutkaisia alennuksia.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-118">These discounts include complex discounts.</span></span> <span data-ttu-id="a1f2b-119">Esimerkkejä ovat Osta 3 nimikettä ja saat 10 % alennusta tai Osta pullo ja reppu ja saat 10 % alennusta.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="a1f2b-120">Tilauksen yhteenvedon moduulissa on esimerkiksi alennusten, toimituksen ja verojen jälkeen maksettavaksi jäävä summa.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="a1f2b-121">Tarjouskoodimoduulin avulla asiakas voi käyttää tarjouskoodeja tai poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="a1f2b-122">Asiakas voi tehdä ostoksia anonyymisti tai kirjautuneena käyttäjänä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="a1f2b-123">Jos asiakas on kirjautunut sisään, ostoskorin nimikkeet säilytetään istuntojen välillä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="a1f2b-124">Näin asiakas voi jatkaa ostonsa tekemistä useista laitteista.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="a1f2b-125">Ostoskorista asiakas voi jatkaa kassalle.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="a1f2b-126">Asiakas voi aloittaa kassalle siirtymisen vieraana tai kirjautuneena käyttäjänä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="a1f2b-127">Lisätietoja ostoskorisivun muokkaamisesta on kohdassa [Ostoskorimoduulin lisääminen sivulle](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="a1f2b-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="a1f2b-128">Kassasivu</span><span class="sxs-lookup"><span data-stu-id="a1f2b-128">Checkout page</span></span>

<span data-ttu-id="a1f2b-129">Kassasivulla asiakkaat syöttävät tilauksen tekemisessä vaadittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="a1f2b-130">Seuraavassa kuvassa on esimerkki kassasivusta, joka on luotu moduulikirjaston avulla.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-130">The following illustration show an example of a checkout page that was built by using the module library.</span></span>

![Esimerkki kassasivusta](./media/Checkout.PNG)

<span data-ttu-id="a1f2b-132">Kassasivun päätekstiosa kerää tilauksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="a1f2b-133">Näitä tietoja ovat toimitusosoite, toimitusvaihtoehdot ja maksutiedot.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="a1f2b-134">Kassalle siirtyminen on vaiheittainen työnkulku, koska tiedot on syötettävä tietyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="a1f2b-135">Esimerkiksi toimitusosoite on syötettävä ennen toimituskustannusten laskemista ja maksun hyväksymistä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="a1f2b-136">Toimitusosoite</span><span class="sxs-lookup"><span data-stu-id="a1f2b-136">Shipping address</span></span>

<span data-ttu-id="a1f2b-137">Toimitusosoite on pakollinen, jos nimikkeet on toimitettava.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="a1f2b-138">Kunkin alueen toimitusosoitteiden muoto voidaan määrittää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="a1f2b-139">Jos nimikkeet toimitetaan esimerkiksi Yhdysvaltoihin, toimitusosoitteessa on oltava katuosoite, osavaltio ja postinumero.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="a1f2b-140">Toimitusosoitekentille tehdään joitakin perussyötteiden tarkistuksia, kuten aakkosnumeeristen merkkien, enimmäispituuden ja numeroiden tarkistus.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="a1f2b-141">Vaikka osoitteen oikeellisuutta ei sinänsä tarkisteta, tämä tarkistus voidaan tehdä käyttämällä mukautettuja kolmannen osapuolen palveluita.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="a1f2b-142">Toimitusosoitetta käytetään kaikissa ostoskorin nimikkeissä, joille on valittu toimitusvaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="a1f2b-143">Jos käytössä on kassatyönkulku, joka sisältyy moduulikirjastoon, yksittäisiä ostoskorin nimikkeitä ei voi toimittaa eri osoitteisiin.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-143">If you use the checkout flow that is provided in the module library, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="a1f2b-144">Jos tarvitset tätä ominaisuutta, se voidaan ottaa käyttöön kassamoduulien mukauttamisen avulla.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="a1f2b-145">Kun toimitusosoite on annettu, Dynamics 365 Commerce -verkkokaupassa käytettävissä olevat toimitustavat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="a1f2b-146">Toimitustavat ja niitä tukevat osoitteet voidaan määrittää Commerce-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-146">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="a1f2b-147">Maksu</span><span class="sxs-lookup"><span data-stu-id="a1f2b-147">Payment</span></span>

<span data-ttu-id="a1f2b-148">Kassatyönkulun seuraava vaihe on maksu.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="a1f2b-149">Sähköisessä kaupankäynnissä voidaan käyttää useita maksutapoja, kuten luottokortteja, lahjakortteja ja kanta-asiakkuuspisteitä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="a1f2b-150">Myös näiden toimitustapojen yhdistelmää voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="a1f2b-151">Käytettävissä olevien toimitustapojen mukaan voidaan tarvita lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="a1f2b-152">Esimerkiksi luottokorttimaksu edellyttää laskutusosoitetta.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="a1f2b-153">Luottokorttimaksut käsitellään Adyen-maksuyhdistimen avulla.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="a1f2b-154">Kanta-asiakkuuspisteet</span><span class="sxs-lookup"><span data-stu-id="a1f2b-154">Loyalty points</span></span>

<span data-ttu-id="a1f2b-155">Kassatyönkulun aikana asiakas, joka on kanta-asiakkuusohjelman jäsen ja joka on kerännyt kanta-asiakkuuspisteitä, voi lunastaa pisteet tilausta varten.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="a1f2b-156">Kanta-asiakkuuspisteiden moduuli näkyy vain, jos asiakas on kanta-asiakasohjelman jäsen.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="a1f2b-157">Tämä moduuli ei näy käyttäjille, jotka eivät ole jäseniä, eikä vierailijoille.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="a1f2b-158">Lahjakortit</span><span class="sxs-lookup"><span data-stu-id="a1f2b-158">Gift cards</span></span>

<span data-ttu-id="a1f2b-159">Moduulikirjaston avulla voi lunastaa sisäiset lahjakortit tilausta varten.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-159">The module library lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="a1f2b-160">Asiakkaan on kirjauduttava sisään, jotta hän voi käyttää sisäistä lahjakorttia.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="a1f2b-161">Lisäsuojausta varten on suositeltavaa mukauttaa työnkulku käyttämällä sisäisissä lahjakorteissa henkilökohtaista tunnuslukua (PIN).</span><span class="sxs-lookup"><span data-stu-id="a1f2b-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="a1f2b-162">Kirjautuneet käyttäjät ja vierailijat</span><span class="sxs-lookup"><span data-stu-id="a1f2b-162">Signed-in and guest users</span></span>

<span data-ttu-id="a1f2b-163">Asiakas voi suorittaa kassaprosessin valmiiksi vierailijana tai kirjautuneena käyttäjänä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="a1f2b-164">Jos asiakas kirjautuu sisään, tilin tiedot, kuten tallennetut toimitusosoitteet ja tallennetun luottokortin tiedot, haetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="a1f2b-165">Tilauksen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="a1f2b-165">Order summary</span></span>

<span data-ttu-id="a1f2b-166">Kassaprosessi näyttää ostoskorin rivinimikkeiden yhteenvedon. Asiakas voi tarkistaa tilauksen ennen sen tekemistä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="a1f2b-167">Rivinimikkeitä ei voi muokata kassatyönkulun aikana.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="a1f2b-168">Näkyvissä on kuitenkin linkki ostoskoriin siltä varalta, että asiakas haluaa siirtyä takaisin ja muokata rivinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="a1f2b-169">Kun asiakas antaa toimitus- ja laskutustiedot, tilauksen yhteenvetoon päivittyy summa kanta-asiakkuuspisteiden, lahjakorttien ja muiden maksutapojen huomioimisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="a1f2b-170">Tilausvahvistus ja sähköposti</span><span class="sxs-lookup"><span data-stu-id="a1f2b-170">Order confirmation and email</span></span>

<span data-ttu-id="a1f2b-171">Kun asiakas tekee tilauksen, hänelle annetaan vahvistusnumero.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="a1f2b-172">Tässä vaiheessa maksu on hyväksytty, mutta sitä ei ole veloitettu.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="a1f2b-173">Maksu veloitetaan vasta, kun tilaus on täytetty (eli kun se on joko lähetetty tai noudettu).</span><span class="sxs-lookup"><span data-stu-id="a1f2b-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="a1f2b-174">Tilauksen luomisen jälkeen asiakkaalle lähetetään tilausvahvistussähköpostiviesti.</span><span class="sxs-lookup"><span data-stu-id="a1f2b-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="a1f2b-175">Lisätietoja kassasivun muokkaamisesta on kohdassa [Kassamoduulin lisääminen sivulle](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="a1f2b-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1f2b-176">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a1f2b-176">Additional resources</span></span>

[<span data-ttu-id="a1f2b-177">Aloitussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a1f2b-177">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="a1f2b-178">Tuotetietosivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a1f2b-178">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="a1f2b-179">Tilinhallintasivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a1f2b-179">Account management pages overview</span></span>](quick-tour-account-management.md)
