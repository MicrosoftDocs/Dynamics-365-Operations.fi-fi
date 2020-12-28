---
title: BOPIS:n määrittäminen Dynamics 365 Commerce -arviointiympäristössä
description: Tässä ohjeaiheessa selitetään, miten BOPIS (osta verkosta, nouda myymälästä) määritetään Microsoft Dynamics 365 Commerce -arviointiympäristössä, kun se on valmisteltu.
author: rubendel
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 62dabaa2610341cc8ad8e85812a317ac3123fcb1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411868"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="54b4e-103">BOPIS:n määrittäminen Dynamics 365 Commerce -arviointiympäristössä</span><span class="sxs-lookup"><span data-stu-id="54b4e-103">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="54b4e-104">Tässä ohjeaiheessa selitetään, miten BOPIS (osta verkosta, nouda myymälästä) määritetään Microsoft Dynamics 365 Commerce -arviointiympäristössä, kun ympäristö on valmisteltu.</span><span class="sxs-lookup"><span data-stu-id="54b4e-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce evaluation environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="54b4e-105">Edellytys</span><span class="sxs-lookup"><span data-stu-id="54b4e-105">Prerequisite</span></span>

<span data-ttu-id="54b4e-106">Suorita tämän ohjeaiheen toimet vasta, kun Commercen arviointiympäristö on valmisteltu ja määritetty.</span><span class="sxs-lookup"><span data-stu-id="54b4e-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned and configured.</span></span> <span data-ttu-id="54b4e-107">Lisätietoja ympäristön valmistelusta ja määrittämisestä on kohdissa [Dynamics 365 Commerce -arviointiympäristön valmisteleminen](provisioning-guide.md) ja [Dynamics 365 Commerce -arviointiympäristön määrittäminen](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="54b4e-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce evaluation environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce evaluation environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="54b4e-108">Kun Commerce-ympäristö on valmisteltu ja määritetty päättyneeksi, voit ottaa käyttöön BOPIS-skenaariot tämän ohjeaiheen avulla.</span><span class="sxs-lookup"><span data-stu-id="54b4e-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="54b4e-109">Määritä POS</span><span class="sxs-lookup"><span data-stu-id="54b4e-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="54b4e-110">Modern POS:in määrittäminen</span><span class="sxs-lookup"><span data-stu-id="54b4e-110">Configure Modern POS</span></span>

<span data-ttu-id="54b4e-111">BOPIS-skenaariot, joihin liittyy luottokorttimaksu, edellyttävät laitteistoasemaa.</span><span class="sxs-lookup"><span data-stu-id="54b4e-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="54b4e-112">Laiteasema muodostetaan Windowsin Modern POS:iin Windowsille ja Androidille.</span><span class="sxs-lookup"><span data-stu-id="54b4e-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="54b4e-113">Jos käytät iOS POS-tai Modern POS-sovellusta iOS:lle, myyntipisteasiakasohjelman on muodostettava laitepari jaetun laiteaseman kanssa.</span><span class="sxs-lookup"><span data-stu-id="54b4e-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="54b4e-114">Tässä ohjeaiheessa selitetään, kuinka BOPIS määritetään Windows- ja Android-asiakkaita varten.</span><span class="sxs-lookup"><span data-stu-id="54b4e-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="54b4e-115">Lisätietoja jaetun laiteaseman asentamisesta on kohdassa [Retail Hardware Stationin määrittäminen ja asentaminen](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="54b4e-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="54b4e-116">Siirry kohtaan **Vähittäismyynti ja kauppa \> Kanavan asetukset \> POS-asetukset \> Kassakoneet**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="54b4e-117">Valitse rekisteröi **SANFRAN-5** ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="54b4e-118">Muuta **laitteistoprofiili**-kentän arvo **HW002**-arvosta **HW001**-arvoon ja valitse sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="54b4e-119">Synkronoidaksesi muutokset, siirry kohtaan **Retail ja Commerce \> Retail ja Commercen IT \> Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="54b4e-120">Valitse jakeluaikataulu **1090** ja valitse sitten toimintoruudusta **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="54b4e-121">Valitse **Kyllä** ja aloita tietojen synkronointi valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="54b4e-122">Asenna Modern POS</span><span class="sxs-lookup"><span data-stu-id="54b4e-122">Install Modern POS</span></span>

1. <span data-ttu-id="54b4e-123">Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> POS-asetukset \> Laitteet**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="54b4e-124">Valitse laite **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="54b4e-125">Valitse toimintoruudussa **Lataa** ja valitse sitten **määritystiedosto**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="54b4e-126">Valitse **Lataa** ja valitse sitten **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="54b4e-127">Kun **ModernPOSSetup.exe**-tiedoston lataus on päättynyt, valitse **Avaa tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Avaa tiedosto](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="54b4e-129">Valitse **Seuraava**, jos haluat käydä läpi asennusprosessin.</span><span class="sxs-lookup"><span data-stu-id="54b4e-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="54b4e-130">Kun asennus on päättynyt, valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="54b4e-131">Modern POS -toiminnon aktivoiminen</span><span class="sxs-lookup"><span data-stu-id="54b4e-131">Activate Modern POS</span></span>

1. <span data-ttu-id="54b4e-132">Valitse Windowsin työpöydällä **Käynnistä**-painike ja syötä **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="54b4e-133">Valitse **Retail Modern POS** -sovellus, jonka aktivointi aloitetaan.</span><span class="sxs-lookup"><span data-stu-id="54b4e-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="54b4e-134">Valitse **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-134">Select **Next**.</span></span> <span data-ttu-id="54b4e-135">**Palvelimen URL-osoite**, **laitetunnus** ja **rekisterinumero**-kentät on määritettävä valmiiksi käyttämällä edellisessä kohdassa lataamaasi määritystiedoston tietoja.</span><span class="sxs-lookup"><span data-stu-id="54b4e-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="54b4e-136">Valitse **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-136">Select **Activate**.</span></span>
5. <span data-ttu-id="54b4e-137">Näyttöön tulee todennusvalintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="54b4e-137">An authentication dialog box appears.</span></span> <span data-ttu-id="54b4e-138">Valitse tili, joka käyttää sähköpostiosoitetta, joka yhdistettiin aiemmin työntekijään **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="54b4e-139">Jos et ole vielä liittänyt työntekijää henkilöllisyytesi, aktivointi epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="54b4e-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="54b4e-140">Noudata tässä tapauksessa Liitä työntekijä henkilöllisyyteesi -kohdan ohjeita ohjeaiheessa [Määritä Dynamics 365 Commerce -arviointiympäristö](cpe-post-provisioning.md#associate-a-worker-with-your-identity).</span><span class="sxs-lookup"><span data-stu-id="54b4e-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce evaluation environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="54b4e-141">Kun sinua kehotetaan antamaan organisaatiosi hallita laitetta, valitse **Vain tämä sovellus**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="54b4e-142">Kun aktivointi on tehty, valitse **Aloita**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="54b4e-143">Ota käyttöön BOPIS Modern POS:issa</span><span class="sxs-lookup"><span data-stu-id="54b4e-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="54b4e-144">Kirjaudu sisään Modern POS-sovellukseen käyttämällä **000713** -operaattoritunnusta ja **123**-salasanaa.</span><span class="sxs-lookup"><span data-stu-id="54b4e-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="54b4e-145">Kun videota toistetaan, valitse kaksi valintaruutua valintaikkunan vasemmassa alakulmassa ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="54b4e-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="54b4e-146">Jos sinua ei kehoteta sulkemaan vaihtonäppäintä, siirry **Aloitus**-sivulla oikealle, valitse **Sulje vaihto** ja kirjaudu sitten takaisin POS-sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="54b4e-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="54b4e-147">Kun olet kirjautunut sisään, valitse **Suorita muu kuin kassatoiminto**, kun sinua kehotetaan tekemään niin.</span><span class="sxs-lookup"><span data-stu-id="54b4e-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="54b4e-148">Siirry **Aloitus**-sivulla oikealle ja valitse **Valitse laiteasema** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="54b4e-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="54b4e-149">Valitse **Hallitse**, määritä **Käytä laiteasemaa** -asetukseksi **Käytössä** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="54b4e-150">Kirjaudu ulos myyntipisteestä ja kirjaudu takaisin sisään.</span><span class="sxs-lookup"><span data-stu-id="54b4e-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="54b4e-151">Kun olet kirjautunut sisään, valitse **Avaa uusi vaihto** ja valitse sitten **Kassa**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="54b4e-152">Suorita BOPIS-skenaario loppuun</span><span class="sxs-lookup"><span data-stu-id="54b4e-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="54b4e-153">Luo myymälätilaus noutomyymälälle</span><span class="sxs-lookup"><span data-stu-id="54b4e-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="54b4e-154">Siirry sen URL-osoitteen kohdalle, jonka määritit [Alusta e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) -vaiheessa ympäristön määrityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="54b4e-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="54b4e-155">Valitse nimike ja valitse **Lisää ostoskoriin**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="54b4e-156">Valitse ostoskassisivulla juuri lisäämäsi tilausrivin **Nouto**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="54b4e-157">Kirjoita **Valitse myymälä** -valintaikkunaan **San Francisco** ja valitse sitten **Haku**-painike.</span><span class="sxs-lookup"><span data-stu-id="54b4e-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="54b4e-158">Etsi tulosluettelosta San Franciscon liike ja valitse **nouto tästä**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="54b4e-159">Valitse ostoskassisivulta **Kassalle vieraana**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="54b4e-160">Jos haluat jatkaa kassalle, sinun on hyväksyttävä evästeilmoitus.</span><span class="sxs-lookup"><span data-stu-id="54b4e-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="54b4e-161">Tämä ilmoitus näkyy bannerissa Kassa-sivun yläosassa.</span><span class="sxs-lookup"><span data-stu-id="54b4e-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="54b4e-162">Kirjoita luottokortin maksutapakenttään seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="54b4e-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="54b4e-163">**Kortinhaltijan nimi:** Syötä mikä tahansa nimi.</span><span class="sxs-lookup"><span data-stu-id="54b4e-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="54b4e-164">**Kortin numero:** Syötä **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="54b4e-165">**Vanhentumispäivä:** Syötä **10/20**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="54b4e-166">**Kortin tarkistusnumero (CVV) -koodi:** Syötä **737**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="54b4e-167">Älä milloinkaan, missään tapauksessa yritä käyttää testisivustossa todellisia luottokortin tietoja.</span><span class="sxs-lookup"><span data-stu-id="54b4e-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="54b4e-168">Jatka kassalle syöttämällä laskutusosoitteen tiedot ja valitse sitten **Tallenna ja jatka**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="54b4e-169">Kun tilaus on valmis lähetettäväksi, valitse **Kassa**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="54b4e-170">Online-tilausten synkronoiminen taustajärjestelmään</span><span class="sxs-lookup"><span data-stu-id="54b4e-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="54b4e-171">Tietoja online-tilausten synkronoimista on kohdassa [Online-myynnin ja -maksujen kirjaaminen](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="54b4e-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="54b4e-172">Nouda tilaus myymälästä</span><span class="sxs-lookup"><span data-stu-id="54b4e-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="54b4e-173">Kirjaudu myyntipisteeseen.</span><span class="sxs-lookup"><span data-stu-id="54b4e-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="54b4e-174">Valitse **Aloitus**-näytössä **Tilauksen täyttäminen**</span><span class="sxs-lookup"><span data-stu-id="54b4e-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="54b4e-175">Valitse noudettavien nimikkeiden luettelosta rivi, joka on sijoitettu online-tilassa olevaan tilaukseen.</span><span class="sxs-lookup"><span data-stu-id="54b4e-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="54b4e-176">Kun tilausrivi on valittuna, valitse **Nouda**.</span><span class="sxs-lookup"><span data-stu-id="54b4e-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="54b4e-177">Rivinimike lisätään transaktionäyttöön ja **$0,00** näkyy erääntyvänä saldona.</span><span class="sxs-lookup"><span data-stu-id="54b4e-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="54b4e-178">Valitse saldo, jonka määrä on **$0,00**, tai valitse mikä tahansa maksutapa transaktion tekemistä varten.</span><span class="sxs-lookup"><span data-stu-id="54b4e-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="54b4e-179">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="54b4e-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="54b4e-180">POS:ista noudettavien online-tilausten saldo ei ole nolla</span><span class="sxs-lookup"><span data-stu-id="54b4e-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="54b4e-181">Jos erääntyvä saldo ei ole 0 (nolla), kun tilaus haetaan myymälässä tapahtuvaa noutoa varten, varmista, että käytössä on Modern POS ja että laitteistoasema on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="54b4e-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="54b4e-182">Jos käytössä on Cloud POS tai iOS:n Modern POS, varmista, että jaettu laiteasema on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="54b4e-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="54b4e-183">Online-tilassa suoritettavien maksujen noutamiseen tarvitaan jonkinlaista aktiivista laiteasemaa.</span><span class="sxs-lookup"><span data-stu-id="54b4e-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="54b4e-184">Maksun tarkistukseen liittyvät yleiset ongelmat</span><span class="sxs-lookup"><span data-stu-id="54b4e-184">General issues with payment capture</span></span>

<span data-ttu-id="54b4e-185">Kaikkien yleisten ongelmien varalta kannattaa aina tutustua Modern POS- tai Internet Information Services (IIS) -laiteasemien tapahtumalokeihin.</span><span class="sxs-lookup"><span data-stu-id="54b4e-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="54b4e-186">Nämä lokit löytyvät Windowsin tapahtumalokin seuraavista solmuista:</span><span class="sxs-lookup"><span data-stu-id="54b4e-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="54b4e-187">Sovellus- ja palvelulokit \> Microsoft \> Dynamics \> Commerce-ModernPOS</span><span class="sxs-lookup"><span data-stu-id="54b4e-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="54b4e-188">Sovellus- ja palvelulokit \> Microsoft \> Dynamics \> Commerce-laiteasema</span><span class="sxs-lookup"><span data-stu-id="54b4e-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54b4e-189">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="54b4e-189">Additional resources</span></span>

[<span data-ttu-id="54b4e-190">Dynamics 365 Commerce -arviointiympäristön yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="54b4e-190">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="54b4e-191">Dynamics 365 Commerce -arviointiympäristön valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="54b4e-191">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="54b4e-192">Dynamics 365 Commerce -arviointiympäristön valinnaisten ominaisuuksien määritykset</span><span class="sxs-lookup"><span data-stu-id="54b4e-192">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="54b4e-193">Dynamics 365 Commerce -arviointiympäristön usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="54b4e-193">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="54b4e-194">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="54b4e-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="54b4e-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="54b4e-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="54b4e-196">Microsoft Azure -portaali</span><span class="sxs-lookup"><span data-stu-id="54b4e-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="54b4e-197">Dynamics 365 Commerce -sivusto</span><span class="sxs-lookup"><span data-stu-id="54b4e-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="54b4e-198">Adyen-maksuyhdistin</span><span class="sxs-lookup"><span data-stu-id="54b4e-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="54b4e-199">Online-maksuvälineiden tallentaminen Adyen-yhdistimen avulla</span><span class="sxs-lookup"><span data-stu-id="54b4e-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="54b4e-200">Omnikanavamaksujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="54b4e-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
