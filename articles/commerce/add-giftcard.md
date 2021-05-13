---
title: Lahjakorttimoduuli
description: Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.
author: anupamar-ms
ms.date: 04/29/2021
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
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962760"
---
# <a name="gift-card-module"></a><span data-ttu-id="7e9a8-103">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="7e9a8-103">Gift card module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7e9a8-104">Tässä ohjeaiheessa on tietoja lahjakorttimoduuleista ja niiden lisäämisestä Microsoft Dynamics 365 Commercen sivuston sivuille.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-104">This topic covers gift card modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7e9a8-105">Lahjakorttimoduuleja voi käyttää kassamoduuleissa lahjakorttien hyväksynnässä. Se on yleinen maksumuoto, jota käytetään sähköisen kaupankäynnin tapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-105">Gift card modules can be used in checkout modules to accept gift cards, a common form of payment used for e-Commerce transactions.</span></span> <span data-ttu-id="7e9a8-106">Lahjakorttimoduuli tukee Dynamics 365-, SVS- ja Givex-lahjakortteja.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-106">The gift card module supports Dynamics 365, SVS, and Givex gift cards.</span></span> <span data-ttu-id="7e9a8-107">SVS- ja Givex-lahjakortit lunastetaan Adyen-maksupalveluntarjoajan kautta.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-107">SVS and Givex gift cards are redeemed via the Adyen payment provider.</span></span> <span data-ttu-id="7e9a8-108">Lisätietoja ulkoisten lahjakorttien, kuten SVS:n ja Givexin tuesta, on ohjeaiheessa [Ulkoisten lahjakorttien tuki](./dev-itpro/gift-card.md).</span><span class="sxs-lookup"><span data-stu-id="7e9a8-108">For more information about support for external gift cards such as SVS and Givex, see [Support for external gift cards](./dev-itpro/gift-card.md).</span></span>

> [!NOTE]
> <span data-ttu-id="7e9a8-109">Tuki SVS- ja Givex-lahjakorttien lunastamiselle kassatyönkulussa on käytettävissä Dynamics 365 Commercen versiossa 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-109">Support for redeeming SVS and Givex gift cards during checkout flow is available in the Dynamics 365 Commerce 10.0.11 release.</span></span> 

<span data-ttu-id="7e9a8-110">Käytettävissä on seuraavat kaksi lahjakorttimoduulia:</span><span class="sxs-lookup"><span data-stu-id="7e9a8-110">There are two gift card modules available:</span></span>

- <span data-ttu-id="7e9a8-111">**Lahjakortti** – Tätä moduulia voi käyttää kassasivulla lunastettaessa lahjakortti maksuvälineenä.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-111">**Gift card** – This module can be used on a checkout page to redeem a gift card as tender.</span></span> 
- <span data-ttu-id="7e9a8-112">**Lahjakortin saldon tarkistus** – Tätä moduulia voi käyttää millä tahansa sivulla, kun halutaan tarkistaa lahjakortin saldo.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-112">**Gift card balance check** – This module can be used on any page to check the balance on a gift card.</span></span> <span data-ttu-id="7e9a8-113">Tämä moduuli on käytettävissä Commercen versiossa 10.0.14 ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-113">This module is available in Commerce release 10.0.14 and later.</span></span>

> [!NOTE]
> <span data-ttu-id="7e9a8-114">Lahjakortin saldontarkistusmoduulin tuki on saatavilla Dynamics 365 Commercen versiossa 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-114">Support for the gift card balance check module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="7e9a8-115">Seuraavassa kuvassa on esimerkki lahjakorttimoduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-115">The following image shows an example of a gift card module on a checkout page.</span></span>

![Esimerkki lahjakorttimoduulista](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a><span data-ttu-id="7e9a8-117">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="7e9a8-117">Module properties</span></span>

- <span data-ttu-id="7e9a8-118">**Näytä lisäkentät** – Tämä ominaisuus määrittää, mitkä lahjakorttien kentät näytetään aina oletusarvoisesti näytettävän lahjakortin numeron lisäksi.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-118">**Show additional fields** – This property defines what fields should be displayed for gift cards in addition to the gift card number, which is always displayed by default.</span></span> <span data-ttu-id="7e9a8-119">Esimerkiksi jotkin lahjakortit tukevat henkilökohtaista tunnuslukua (PIN), ja toiset tukevat PIN-koodin ja vanhentumispäivämäärän näyttämistä.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-119">For example, some gift cards support displaying a personal identification number (PIN), and others support displaying a PIN and expiration date.</span></span> <span data-ttu-id="7e9a8-120">Vaihtoehtoisesti tämän ominaisuuden arvoksi voi määrittää "Ei mitään", jolloin näytetään vain lahjakortin numero eikä muita kenttiä näy.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-120">Alternatively, this property could be set to "None", which would only display the gift card number and no additional fields.</span></span>

<span data-ttu-id="7e9a8-121">Tuetut arvot:</span><span class="sxs-lookup"><span data-stu-id="7e9a8-121">Supported values:</span></span>
-   <span data-ttu-id="7e9a8-122">PIN-koodi</span><span class="sxs-lookup"><span data-stu-id="7e9a8-122">PIN</span></span>
-   <span data-ttu-id="7e9a8-123">Vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="7e9a8-123">Expiration date</span></span>
-   <span data-ttu-id="7e9a8-124">PIN-koodi ja vanhentumispäivä</span><span class="sxs-lookup"><span data-stu-id="7e9a8-124">PIN and expiration date</span></span> 
-   <span data-ttu-id="7e9a8-125">None</span><span class="sxs-lookup"><span data-stu-id="7e9a8-125">None</span></span>

## <a name="site-settings-for-gift-card-modules"></a><span data-ttu-id="7e9a8-126">Lahjakorttimoduulien toimipaikan asetukset</span><span class="sxs-lookup"><span data-stu-id="7e9a8-126">Site settings for gift card modules</span></span>

<span data-ttu-id="7e9a8-127">Kauppapaikan luomistyökalussa **Sivuston asetukset \> -laajennukset** -kohdassa on lahjakorttimoduulin asetus nimeltä **Tuettu lahjakorttityyppi**.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-127">In Commerce site builder under **Site Settings \> Extensions**, there is a gift card module setting called **Supported gift card type**.</span></span> <span data-ttu-id="7e9a8-128">Tämä asetus tukee kolmea arvoa:</span><span class="sxs-lookup"><span data-stu-id="7e9a8-128">This setting supports three values:</span></span>
- <span data-ttu-id="7e9a8-129">**Dynamics 365 -lahjakortti** – Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365 -lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-129">**Dynamics 365 gift card** – When this setting is applied, the gift card module only allows the redemption of Dynamics 365 gift cards.</span></span> <span data-ttu-id="7e9a8-130">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-130">This setting is only supported for signed-in users on the e-Commerce site.</span></span>
- <span data-ttu-id="7e9a8-131">**SVS- ja Givex-lahjakortit** – Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-131">**SVS and Givex gift cards** – When this setting is applied, the gift card module only allows the redemption of Givex and SVS gift cards.</span></span> <span data-ttu-id="7e9a8-132">Tätä asetusta tuetaan kirjautuneiden ja anonyymien käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-132">This setting is supported for signed-in and anonymous users on the e-Commerce site.</span></span>
- <span data-ttu-id="7e9a8-133">**Dynamics 365-, SVS- ja Givex-lahjakortit** – Kun tämä asetus on käytössä, lahjakorttimoduuli sallii vain Dynamics 365-, SVS- ja Givex-lahjakorttien lunastamisen.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-133">**Dynamics 365, SVS, and Givex gift cards** – When this setting is applied, the gift card module allows the redemption of Dynamics 365, Givex, and SVS gift cards.</span></span> <span data-ttu-id="7e9a8-134">Tätä asetusta tuetaan vain kirjautuneiden käyttäjien verkkokauppasivustossa.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-134">This setting is only supported for signed-in users on the e-Commerce site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e9a8-135">Nämä asetukset ovat käytettävissä Dynamics 365 Commercen versiossa 10.0.11-versiossa, ja niitä tarvitaan vain, jos tarvitset tukea SVS- tai Givex-lahjakorteille.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-135">These settings are available in the Dynamics 365 Commerce 10.0.11 release and are required only if you need support for SVS or Givex gift cards.</span></span> <span data-ttu-id="7e9a8-136">Jos päivität vanhemmasta Dynamics 365 Commerce -versiosta, sinun on päivitettävä appsettings.json-tiedosto manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-136">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="7e9a8-137">Ohjeet appsettings.json-tiedoston päivittämiseen: [SDK:n ja moduuliskirjaston päivitykset](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="7e9a8-137">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span> 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a><span data-ttu-id="7e9a8-138">Sisäisten lahjakorttien laajennus sähköisen kaupankäynnin verkkokauppoihin</span><span class="sxs-lookup"><span data-stu-id="7e9a8-138">Extend internal gift cards for use in e-commerce storefronts</span></span>

<span data-ttu-id="7e9a8-139">Sisäiset lahjakortit eivät ole oletusarvoisesti optimoituja sähköisen kaupankäynnin verkkokauppoja varten.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-139">By default, internal gift cards aren't optimized for use in e-commerce storefronts.</span></span> <span data-ttu-id="7e9a8-140">Siksi ennen kuin sallit sisäisillä lahjakorteilla maksamisen, ne on määritettävä laajennuksilla, jotta ne ovat suojatumpia.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-140">Therefore, before you allow internal gift cards to be used for payment, you should configure them with extensions that help make them more secure.</span></span> <span data-ttu-id="7e9a8-141">Ennen sisäisten lahjakorttien käyttöä tuotannossa on hyvä laajentaa seuraavia lahjakorttialueita:</span><span class="sxs-lookup"><span data-stu-id="7e9a8-141">Here are the gift card areas that you should extend before you allow internal gift cards to be used in production:</span></span>

- <span data-ttu-id="7e9a8-142">**Lahjakortin numero** – Numerosarjojen avulla luodaan lahjakorttien numerot sisäisille lahjakorteille.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-142">**Gift card number** – Number sequences are used to generate gift card numbers for internal gift cards.</span></span> <span data-ttu-id="7e9a8-143">Koska numerosarjoja voidaan helposti ennakoida, lahjakorttien numeroiden luontia tulisi laajentaa siten, että myönnettyjen lahjakorttien numeroissa käytetään satunnaisia, kryptografisesti suojattuja merkkijonoja.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-143">Because number sequences can easily be predicted, you should extend the generation of gift card numbers so that random, cryptographically secure strings are used for the gift card numbers that are issued.</span></span>
- <span data-ttu-id="7e9a8-144">**GetBalance** – **GetBalance**-ohjelmointirajapintaa käytetään lahjakorttien saldojen etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-144">**GetBalance** – The **GetBalance** API is used to look up gift card balances.</span></span> <span data-ttu-id="7e9a8-145">Oletusarvon mukaan tämä ohjelmointirajapinta on julkinen.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-145">By default, this API public.</span></span> <span data-ttu-id="7e9a8-146">Jos PIN-koodia ei tarvita lahjakorttien saldojen etsimiseen, on mahdollista, että väsytyshyökkäykset saattavat käyttää **GetBalance**-ohjelmointirajapintaa etsiäkseen niiden lahjakorttien numeroita, joissa on saldoa.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-146">If a PIN isn't required to look up gift card balances, there is a risk that brute force attacks could use the **GetBalance** API to try to look up gift card numbers that have balances.</span></span> <span data-ttu-id="7e9a8-147">Kun otat käyttöön molemmat sisäisten lahjakorttien ja ohjelmointirajapinnan rajoittamisen PIN-vaatimukset käyttöön, voit pienentää riskiä.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-147">By implementing both PIN requirements for internal gift cards and API throttling, you can help mitigate the risk.</span></span>
- <span data-ttu-id="7e9a8-148">**PIN** – Sisäiset lahjakortit eivät oletusarvoisesti tue PIN-koodia.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-148">**PIN** – By default, internal gift cards don't support PINs.</span></span> <span data-ttu-id="7e9a8-149">Laajenna sisäiset lahjakortit niin, että saldojen etsimiseen tarvitaan PIN-koodi.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-149">You should extend internal gift cards so that a PIN is required to look up balances.</span></span> <span data-ttu-id="7e9a8-150">Näitä toimintoja voidaan käyttää myös lahjakorttien lukitsemaan sen jälkeen, kun PIN-koodia on yritetty kirjoittaa virheellisesti monta kertaa peräkkäin.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-150">This functionality can also be used to lock gift cards after consecutive incorrect attempts to enter the PIN.</span></span>

## <a name="enable-gift-card-payments-for-guest-checkout"></a><span data-ttu-id="7e9a8-151">Lahjakorttimaksujen käyttöönotto vieraan uloskuittausta varten</span><span class="sxs-lookup"><span data-stu-id="7e9a8-151">Enable gift card payments for guest checkout</span></span>

<span data-ttu-id="7e9a8-152">Oletusarvon mukaan lahjakorttimaksut eivät ole käytössä vieraan (anonyymi) uloskuittauksessa.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-152">By default, gift card payments aren't enabled for guest (anonymous) checkout.</span></span> <span data-ttu-id="7e9a8-153">Ne otetaan käyttöön seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-153">To enable them, follow these steps.</span></span>

1. <span data-ttu-id="7e9a8-154">Siirry Commerce headquartersissa kohtaan **Retail ja Commerce \> Kanavan asetukset \> Myyntipisteen asetukset \> Myyntipiste \> Myyntipistetoiminnot**.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-154">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> POS Operations**.</span></span>
1. <span data-ttu-id="7e9a8-155">Valitse ja pidä valittuna (tai valitse hiiren kakkospainikkeella) ruudukon otsikko ja valitse sitten **Lisää sarakkeita**.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-155">Select and hold (or right-click) the header of the grid, and then select **Insert columns**.</span></span>
1. <span data-ttu-id="7e9a8-156">Valitse **Lisää sarakkeita** -valintaikkunassa **AllowAnonymousAccess**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-156">In the **Insert columns** dialog box, select the **AllowAnonymousAccess** check box.</span></span>
1. <span data-ttu-id="7e9a8-157">Valitse **Päivitä**.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-157">Select **Update**.</span></span>
1. <span data-ttu-id="7e9a8-158">Toiminnoille **520** (lahjakortin saldo) ja **214**, määritä **AllowAnonymousAccess**-arvoksi **1**.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-158">For operations **520** (Gift card balance) and **214**, set the **AllowAnonymousAccess** value to **1**.</span></span>
1. <span data-ttu-id="7e9a8-159">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-159">Select **Save**.</span></span>
1. <span data-ttu-id="7e9a8-160">Suorita **1090**-ajoitustoiminto, kun synkronoit muutokset kanavatietokannan kanssa.</span><span class="sxs-lookup"><span data-stu-id="7e9a8-160">Run the **1090** scheduler job to sync changes to the channel database.</span></span> 

## <a name="add-a-gift-card-module-to-a-page"></a><span data-ttu-id="7e9a8-161">Lahjakorttimoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="7e9a8-161">Add a gift card module to a page</span></span>

<span data-ttu-id="7e9a8-162">Lisätietoja lahjakorttimoduulin lisäämisestä kassasivulle ja tarvittavien ominaisuuksien määrittämisestä on kohdassa [Kassamoduuli.](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="7e9a8-162">For instructions on how to add a gift card module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e9a8-163">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7e9a8-163">Additional resources</span></span>

[<span data-ttu-id="7e9a8-164">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="7e9a8-164">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7e9a8-165">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="7e9a8-165">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7e9a8-166">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="7e9a8-166">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7e9a8-167">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="7e9a8-167">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="7e9a8-168">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="7e9a8-168">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="7e9a8-169">Toimitusvaihtoehtomoduuli</span><span class="sxs-lookup"><span data-stu-id="7e9a8-169">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="7e9a8-170">Noudon tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="7e9a8-170">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="7e9a8-171">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="7e9a8-171">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7e9a8-172">Ulkoisten lahjakorttien tuki</span><span class="sxs-lookup"><span data-stu-id="7e9a8-172">Support for external gift cards</span></span>](./dev-itpro/gift-card.md)

[<span data-ttu-id="7e9a8-173">SDK:n ja moduulikirjaston päivitykset</span><span class="sxs-lookup"><span data-stu-id="7e9a8-173">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
