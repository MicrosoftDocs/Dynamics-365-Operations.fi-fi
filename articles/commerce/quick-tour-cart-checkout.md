---
title: Ostoskorin ja maksusivun yleiskatsaus
description: Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen ostoskori- ja kassasivun yleiskatsaus.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d0b5a74a9880a5cabfdbc124f557998540c94a4d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792240"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="f9522-103">Ostoskorin ja maksusivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f9522-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f9522-104">Tässä ohjeaiheessa on Microsoft Dynamics 365 Commercen ostoskori- ja kassasivun yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="f9522-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f9522-105">Sähköisen kaupankäynnin sivuston ostoskorisivulla näkyvät kaikki nimikkeet, jotka asiakas on lisännyt koriin.</span><span class="sxs-lookup"><span data-stu-id="f9522-105">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="f9522-106">Ostoskorisivu luodaan ostoskorimoduulin avulla.</span><span class="sxs-lookup"><span data-stu-id="f9522-106">The cart page is built by using the cart module.</span></span> <span data-ttu-id="f9522-107">Ostoskorimoduuli on säilö, joka isännöi kaikkia niitä moduuleja, joita tarvitaan näytettäessä ostoskorin nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="f9522-107">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="f9522-108">Ostoskorimoduuli voi käyttää myös muita moduuleja tilauksen yhteenvedon ja mahdollisten asiakastilausta koskevien tarjouskoodien näyttämisessä.</span><span class="sxs-lookup"><span data-stu-id="f9522-108">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="f9522-109">Sähköisen kaupankäynnin sivuston kassasivulla on vaiheittainen työnkulku, jota asiakkaat seuraavat syöttäessään tilauksen tekemisessä vaadittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="f9522-109">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="f9522-110">Kassamoduuli voi sisältää moduuleja, jotka käsittelevät toimitusosoitetta, toimitusmenetelmiä, laskutustietoja, tilauksen yhteenvetoa ja muita asiakastilauksiin liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="f9522-110">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="f9522-111">Ostoskorisivu</span><span class="sxs-lookup"><span data-stu-id="f9522-111">Cart page</span></span>

<span data-ttu-id="f9522-112">Ostoskorisivu toimii ostoskassina. Se sisältää kaikki ostoskoriin lisätyt nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="f9522-112">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="f9522-113">Seuraavassa kuvassa on esimerkki ostoskorisivusta, joka on luotu verkon moduulikirjaston ja Fabrikam-teeman avulla.</span><span class="sxs-lookup"><span data-stu-id="f9522-113">The following illustration show an example of a cart page that was built by using the module library and the "Fabrikam" theme.</span></span>

![Esimerkki ostoskorisivusta](./media/cart2.PNG)

<span data-ttu-id="f9522-115">Ostoskorisivun päätekstiosassa näkyvät kaikki nimikkeet, jotka asiakas on lisännyt koriin.</span><span class="sxs-lookup"><span data-stu-id="f9522-115">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="f9522-116">Kaikki käytettävissä olevat alennukset ovat esillä.</span><span class="sxs-lookup"><span data-stu-id="f9522-116">All applicable discounts are showcased.</span></span> <span data-ttu-id="f9522-117">Nämä alennukset sisältävät monimutkaisia alennuksia.</span><span class="sxs-lookup"><span data-stu-id="f9522-117">These discounts include complex discounts.</span></span> <span data-ttu-id="f9522-118">Esimerkkejä ovat Osta 3 nimikettä ja saat 10 % alennusta tai Osta pullo ja reppu ja saat 10 % alennusta.</span><span class="sxs-lookup"><span data-stu-id="f9522-118">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="f9522-119">Tilauksen yhteenvedon moduulissa on esimerkiksi alennusten, toimituksen ja verojen jälkeen maksettavaksi jäävä summa.</span><span class="sxs-lookup"><span data-stu-id="f9522-119">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="f9522-120">Tarjouskoodimoduulin avulla asiakas voi käyttää tarjouskoodeja tai poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="f9522-120">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="f9522-121">Asiakas voi tehdä ostoksia anonyymisti tai kirjautuneena käyttäjänä.</span><span class="sxs-lookup"><span data-stu-id="f9522-121">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="f9522-122">Jos asiakas on kirjautunut sisään, ostoskorin nimikkeet säilytetään istuntojen välillä.</span><span class="sxs-lookup"><span data-stu-id="f9522-122">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="f9522-123">Näin asiakas voi jatkaa ostonsa tekemistä useista laitteista.</span><span class="sxs-lookup"><span data-stu-id="f9522-123">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="f9522-124">Ostoskorista asiakas voi jatkaa kassalle.</span><span class="sxs-lookup"><span data-stu-id="f9522-124">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="f9522-125">Asiakas voi aloittaa kassalle siirtymisen vieraana tai kirjautuneena käyttäjänä.</span><span class="sxs-lookup"><span data-stu-id="f9522-125">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="f9522-126">Lisätietoja ostoskorisivun muokkaamisesta on kohdassa [Ostoskorimoduulin lisääminen sivulle](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="f9522-126">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="f9522-127">Kassasivu</span><span class="sxs-lookup"><span data-stu-id="f9522-127">Checkout page</span></span>

<span data-ttu-id="f9522-128">Kassasivulla asiakkaat syöttävät tilauksen tekemisessä vaadittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="f9522-128">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="f9522-129">Seuraavassa kuvassa on esimerkki kassasivusta, joka on luotu moduulikirjaston avulla.</span><span class="sxs-lookup"><span data-stu-id="f9522-129">The following illustration show an example of a checkout page that was built by using the module library.</span></span>

![Esimerkki kassasivusta](./media/Checkout.PNG)

<span data-ttu-id="f9522-131">Kassasivun päätekstiosa kerää tilauksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="f9522-131">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="f9522-132">Näitä tietoja ovat toimitusosoite, toimitusvaihtoehdot ja maksutiedot.</span><span class="sxs-lookup"><span data-stu-id="f9522-132">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="f9522-133">Kassalle siirtyminen on vaiheittainen työnkulku, koska tiedot on syötettävä tietyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="f9522-133">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="f9522-134">Esimerkiksi toimitusosoite on syötettävä ennen toimituskustannusten laskemista ja maksun hyväksymistä.</span><span class="sxs-lookup"><span data-stu-id="f9522-134">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="f9522-135">Toimitusosoite</span><span class="sxs-lookup"><span data-stu-id="f9522-135">Shipping address</span></span>

<span data-ttu-id="f9522-136">Toimitusosoite on pakollinen, jos nimikkeet on toimitettava.</span><span class="sxs-lookup"><span data-stu-id="f9522-136">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="f9522-137">Kunkin alueen toimitusosoitteiden muoto voidaan määrittää Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f9522-137">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f9522-138">Jos nimikkeet toimitetaan esimerkiksi Yhdysvaltoihin, toimitusosoitteessa on oltava katuosoite, osavaltio ja postinumero.</span><span class="sxs-lookup"><span data-stu-id="f9522-138">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="f9522-139">Toimitusosoitekentille tehdään joitakin perussyötteiden tarkistuksia, kuten aakkosnumeeristen merkkien, enimmäispituuden ja numeroiden tarkistus.</span><span class="sxs-lookup"><span data-stu-id="f9522-139">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="f9522-140">Vaikka osoitteen oikeellisuutta ei sinänsä tarkisteta, tämä tarkistus voidaan tehdä käyttämällä mukautettuja kolmannen osapuolen palveluita.</span><span class="sxs-lookup"><span data-stu-id="f9522-140">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="f9522-141">Toimitusosoitetta käytetään kaikissa ostoskorin nimikkeissä, joille on valittu toimitusvaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="f9522-141">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="f9522-142">Jos käytössä on kassatyönkulku, joka sisältyy moduulikirjastoon, yksittäisiä ostoskorin nimikkeitä ei voi toimittaa eri osoitteisiin.</span><span class="sxs-lookup"><span data-stu-id="f9522-142">If you use the checkout flow that is provided in the module library, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="f9522-143">Jos tarvitset tätä ominaisuutta, se voidaan ottaa käyttöön kassamoduulien mukauttamisen avulla.</span><span class="sxs-lookup"><span data-stu-id="f9522-143">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="f9522-144">Kun toimitusosoite on annettu, Dynamics 365 Commerce -verkkokaupassa käytettävissä olevat toimitustavat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="f9522-144">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="f9522-145">Toimitustavat ja niitä tukevat osoitteet voidaan määrittää Commerce-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="f9522-145">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="f9522-146">Maksu</span><span class="sxs-lookup"><span data-stu-id="f9522-146">Payment</span></span>

<span data-ttu-id="f9522-147">Kassatyönkulun seuraava vaihe on maksu.</span><span class="sxs-lookup"><span data-stu-id="f9522-147">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="f9522-148">Sähköisessä kaupankäynnissä voidaan käyttää useita maksutapoja, kuten luottokortteja, lahjakortteja ja kanta-asiakkuuspisteitä.</span><span class="sxs-lookup"><span data-stu-id="f9522-148">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="f9522-149">Myös näiden toimitustapojen yhdistelmää voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="f9522-149">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="f9522-150">Käytettävissä olevien toimitustapojen mukaan voidaan tarvita lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="f9522-150">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="f9522-151">Esimerkiksi luottokorttimaksu edellyttää laskutusosoitetta.</span><span class="sxs-lookup"><span data-stu-id="f9522-151">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="f9522-152">Luottokorttimaksut käsitellään Adyen-maksuyhdistimen avulla.</span><span class="sxs-lookup"><span data-stu-id="f9522-152">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="f9522-153">Kanta-asiakkuuspisteet</span><span class="sxs-lookup"><span data-stu-id="f9522-153">Loyalty points</span></span>

<span data-ttu-id="f9522-154">Kassatyönkulun aikana asiakas, joka on kanta-asiakkuusohjelman jäsen ja joka on kerännyt kanta-asiakkuuspisteitä, voi lunastaa pisteet tilausta varten.</span><span class="sxs-lookup"><span data-stu-id="f9522-154">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="f9522-155">Kanta-asiakkuuspisteiden moduuli näkyy vain, jos asiakas on kanta-asiakasohjelman jäsen.</span><span class="sxs-lookup"><span data-stu-id="f9522-155">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="f9522-156">Tämä moduuli ei näy käyttäjille, jotka eivät ole jäseniä, eikä vierailijoille.</span><span class="sxs-lookup"><span data-stu-id="f9522-156">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="f9522-157">Lahjakortit</span><span class="sxs-lookup"><span data-stu-id="f9522-157">Gift cards</span></span>

<span data-ttu-id="f9522-158">Moduulikirjaston avulla voi lunastaa sisäiset lahjakortit tilausta varten.</span><span class="sxs-lookup"><span data-stu-id="f9522-158">The module library lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="f9522-159">Asiakkaan on kirjauduttava sisään, jotta hän voi käyttää sisäistä lahjakorttia.</span><span class="sxs-lookup"><span data-stu-id="f9522-159">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="f9522-160">Lisäsuojausta varten on suositeltavaa mukauttaa työnkulku käyttämällä sisäisissä lahjakorteissa henkilökohtaista tunnuslukua (PIN).</span><span class="sxs-lookup"><span data-stu-id="f9522-160">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="f9522-161">Kirjautuneet käyttäjät ja vierailijat</span><span class="sxs-lookup"><span data-stu-id="f9522-161">Signed-in and guest users</span></span>

<span data-ttu-id="f9522-162">Asiakas voi suorittaa kassaprosessin valmiiksi vierailijana tai kirjautuneena käyttäjänä.</span><span class="sxs-lookup"><span data-stu-id="f9522-162">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="f9522-163">Jos asiakas kirjautuu sisään, tilin tiedot, kuten tallennetut toimitusosoitteet ja tallennetun luottokortin tiedot, haetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="f9522-163">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="f9522-164">Tilauksen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="f9522-164">Order summary</span></span>

<span data-ttu-id="f9522-165">Kassaprosessi näyttää ostoskorin rivinimikkeiden yhteenvedon. Asiakas voi tarkistaa tilauksen ennen sen tekemistä.</span><span class="sxs-lookup"><span data-stu-id="f9522-165">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="f9522-166">Rivinimikkeitä ei voi muokata kassatyönkulun aikana.</span><span class="sxs-lookup"><span data-stu-id="f9522-166">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="f9522-167">Näkyvissä on kuitenkin linkki ostoskoriin siltä varalta, että asiakas haluaa siirtyä takaisin ja muokata rivinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="f9522-167">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="f9522-168">Kun asiakas antaa toimitus- ja laskutustiedot, tilauksen yhteenvetoon päivittyy summa kanta-asiakkuuspisteiden, lahjakorttien ja muiden maksutapojen huomioimisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="f9522-168">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="f9522-169">Tilausvahvistus ja sähköposti</span><span class="sxs-lookup"><span data-stu-id="f9522-169">Order confirmation and email</span></span>

<span data-ttu-id="f9522-170">Kun asiakas tekee tilauksen, hänelle annetaan vahvistusnumero.</span><span class="sxs-lookup"><span data-stu-id="f9522-170">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="f9522-171">Tässä vaiheessa maksu on hyväksytty, mutta sitä ei ole veloitettu.</span><span class="sxs-lookup"><span data-stu-id="f9522-171">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="f9522-172">Maksu veloitetaan vasta, kun tilaus on täytetty (eli kun se on joko lähetetty tai noudettu).</span><span class="sxs-lookup"><span data-stu-id="f9522-172">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="f9522-173">Tilauksen luomisen jälkeen asiakkaalle lähetetään tilausvahvistussähköpostiviesti.</span><span class="sxs-lookup"><span data-stu-id="f9522-173">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="f9522-174">Lisätietoja kassasivun muokkaamisesta on kohdassa [Kassamoduulin lisääminen sivulle](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="f9522-174">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9522-175">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f9522-175">Additional resources</span></span>

[<span data-ttu-id="f9522-176">Aloitussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f9522-176">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="f9522-177">Tuotetietosivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f9522-177">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="f9522-178">Tilinhallintasivujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f9522-178">Account management pages overview</span></span>](quick-tour-account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
