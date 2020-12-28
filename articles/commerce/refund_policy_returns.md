---
title: Kanavan palautus- ja hyvityskäytännön luominen ja päivittäminen
description: Tässä ohjeaiheessa kerrotaan, miten kanavan palautus- ja hyvityskäytäntö määritetään.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: c2a9325f09ffe43c3436b7e0ca2ab511e1f57f83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412071"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a><span data-ttu-id="e7a03-103">Kanavan palautus- ja hyvityskäytännön luominen ja päivittäminen</span><span class="sxs-lookup"><span data-stu-id="e7a03-103">Create and update a returns and refunds policy for a channel</span></span>

[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="e7a03-104">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e7a03-104">Overview</span></span>

<span data-ttu-id="e7a03-105">Kanavan palautuskäytännön avulla jälleenmyyjät voivat määrittää Dynamics 365 Commercessa, mitkä maksutarjoukset voidaan sallia myyntipisteen (POS) palautuksen käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="e7a03-105">The channel return policy in Dynamics 365 Commerce enables retailers to set enforcements on which payment tenders can be allowed for processing a return on a point of sale (POS) device.</span></span>  

<span data-ttu-id="e7a03-106">Tässä ohjeaiheessa kuvataan, miten kanavan palautus- ja hyvityskäytäntö määritetään.</span><span class="sxs-lookup"><span data-stu-id="e7a03-106">This topic describes the steps to set up a returns and refunds policy for a channel.</span></span>

<span data-ttu-id="e7a03-107">Tämän käytännön soveltamisala rajoittuu tällä hetkellä siihen, että voidaan määrittää kanaville sallitut maksutarjoukset.</span><span class="sxs-lookup"><span data-stu-id="e7a03-107">The scope of the policy is currently limited to setting the payment tenders that can be allowed for a channel.</span></span> <span data-ttu-id="e7a03-108">Sallittu-luettelo perustuu oston tekemiseen käytettyihin maksutapoihin.</span><span class="sxs-lookup"><span data-stu-id="e7a03-108">The "allowed" list is based on the payment methods used to make the purchase.</span></span> <span data-ttu-id="e7a03-109">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="e7a03-109">For example:</span></span>

- <span data-ttu-id="e7a03-110">Jos osto on tehty käyttämällä lahjakorttia, myymäläkäytännöllä on tarkoitus käsitellä palautuksia vain uuteen lahjakorttiin tai tallentaa myymäläluottoa.</span><span class="sxs-lookup"><span data-stu-id="e7a03-110">If a purchase was made using a gift card, the store policy is to process refunds only to a new gift card or to give store credit.</span></span> 
- <span data-ttu-id="e7a03-111">Jos myynti tehdään käteisellä, hyvityksen sallitut vaihtoehdot ovat käteinen, lahjakortti ja asiakastili, mutta ei luottokorttia.</span><span class="sxs-lookup"><span data-stu-id="e7a03-111">If a sale is made using cash, the options allowed for refund are cash, gift card, and customer account, but not credit card.</span></span> 


## <a name="enable-return-policy"></a><span data-ttu-id="e7a03-112">Ota käyttöön palautuskäytäntö</span><span class="sxs-lookup"><span data-stu-id="e7a03-112">Enable return policy</span></span>

<span data-ttu-id="e7a03-113">Voit ottaa kanavan palautuksen käytäntötoiminnon käyttöön seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e7a03-113">To enable the channel return policy functionality, do the following:</span></span>

1. <span data-ttu-id="e7a03-114">Avaa **Ominaisuuksien hallinta** -työtilaan Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="e7a03-114">Go to the **Feature Management** workspace in Dynamics 365 Commerce.</span></span>
2. <span data-ttu-id="e7a03-115">Etsi ominaisuuksien nimien luettelosta **Ota käyttöön kanavan palautuksen käytännöt** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="e7a03-115">Search for the **Enable channel return policies** feature in the list of feature names.</span></span>
3. <span data-ttu-id="e7a03-116">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="e7a03-116">Select **Enable now**.</span></span> 

## <a name="configure-return-policy"></a><span data-ttu-id="e7a03-117">Määritä palautuskäytäntö</span><span class="sxs-lookup"><span data-stu-id="e7a03-117">Configure return policy</span></span>

<span data-ttu-id="e7a03-118">Noudattamalla näitä ohjeita voit määrittää jälleenmyyntimyymälän tai online-vähittäismyyntikanavan palautuksen.</span><span class="sxs-lookup"><span data-stu-id="e7a03-118">Follow these steps to configure a return policy for a retail store or online retail channel.</span></span>

1. <span data-ttu-id="e7a03-119">Siirry kohtaan **Retail ja Commerce** \> **Kanava-asetukset** \> **Palautukset** \> **Kanavan palautuskäytäntö**.</span><span class="sxs-lookup"><span data-stu-id="e7a03-119">Go to **Retail and Commerce** \> **Channel Setup** \> **Returns** \> **Channel return policy**.</span></span>

2. <span data-ttu-id="e7a03-120">Valitse **Uusi** luodaksesi uuden palautuskäytännön mallin.</span><span class="sxs-lookup"><span data-stu-id="e7a03-120">Select **New** to create a new return policy template.</span></span> <span data-ttu-id="e7a03-121">Jos haluat käyttää aiemmin luotua mallia, valitse malli vasemmanpuoleisesta ruudusta.</span><span class="sxs-lookup"><span data-stu-id="e7a03-121">To use an existing template, select the template in the left pane.</span></span> <span data-ttu-id="e7a03-122">Lisää uusille malleille nimi ja kuvaus, joiden avulla voit tunnistaa käytännön, kun sitä käytetään kanavassa.</span><span class="sxs-lookup"><span data-stu-id="e7a03-122">For new templates, add a name and description that will help you identify the policy when it is being applied to the channel.</span></span>

   <span data-ttu-id="e7a03-123">![Uuden palautuskäytännön lisääminen](media/Return-policy-page1.png "Uuden palautuskäytännön lisääminen")</span><span class="sxs-lookup"><span data-stu-id="e7a03-123">![Add new return policy](media/Return-policy-page1.png "Add new return rolicy")</span></span>
     
   
3. <span data-ttu-id="e7a03-124">Määritä **Sallittu palautuksen maksutapa** -osassa **Sallitut** palautusmaksutarjoukset, jotka koskevat kutakin maksutapaa.</span><span class="sxs-lookup"><span data-stu-id="e7a03-124">In the **Allowed refund payment methods** section, define **Allowed** return payment tenders that are specific to each payment method.</span></span>
   <span data-ttu-id="e7a03-125">![Lisää maksutavat](media/Return-policy-page2.PNG "Määritä sallitut toimitustavat maksutyypeittäin")</span><span class="sxs-lookup"><span data-stu-id="e7a03-125">![Add payment methods](media/Return-policy-page2.PNG "Set allowed payment methods per payment type")</span></span>
   
    > [!IMPORTANT]
    > - <span data-ttu-id="e7a03-126">Maksut johdetaan organisaatiolle määritetyistä toimitustavoista.</span><span class="sxs-lookup"><span data-stu-id="e7a03-126">The payment methods are derived from the payment methods set for the organization.</span></span>
    > - <span data-ttu-id="e7a03-127">Kun lisäät sallitun palautusmaksuvälinetyypin jokaiselle luetellulle maksutavalle, voit varmistaa, että palautusmaksuvälinetyyppiin voidaan tehdä palautus.</span><span class="sxs-lookup"><span data-stu-id="e7a03-127">Adding an allowed return tender type for each listed payment method will ensure that returns can be made to the allowed return tender type.</span></span>
    
4. <span data-ttu-id="e7a03-128">Liitä palautuskäytäntömalli myymälöihin, joissa sitä käytetään.</span><span class="sxs-lookup"><span data-stu-id="e7a03-128">Associate the return policy template with the stores where it will be used.</span></span> <span data-ttu-id="e7a03-129">Valitse **Lisää** **vähittäismyyntikanavat** -välilehdestä ja liitä käytettävissä olevat kanavat.</span><span class="sxs-lookup"><span data-stu-id="e7a03-129">Select **Add** in the **Retail Channels** tab and associate the available channels.</span></span> 

    - <span data-ttu-id="e7a03-130">Valitse **Valitse organisaatiosolmut** -valintaikkunassa ne myymälät, alueet ja organisaatiot, joihin malli liitetään.</span><span class="sxs-lookup"><span data-stu-id="e7a03-130">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>
    - <span data-ttu-id="e7a03-131">Kuhunkin myymälään voidaan liittää vain yksi myymälän palautuskäytäntömalli.</span><span class="sxs-lookup"><span data-stu-id="e7a03-131">Only one return policy template can be associated with each store.</span></span>
    - <span data-ttu-id="e7a03-132">Valitse myymälät, alueet tai organisaatiot nuolipainikkeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="e7a03-132">Use the arrow buttons to select stores, regions, or organizations.</span></span>
    - <span data-ttu-id="e7a03-133">Käytännön voimaan tulopäivämäärä on aika, jolloin käytäntöjä käytetään kanavissa, ja kanavatyöt suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="e7a03-133">The effective date on the policy will be the date on which the policies are applied to the channels and the channel jobs are run.</span></span> 

    <span data-ttu-id="e7a03-134">![Valitse organisaatiosolmujen valintaikkuna](media/Return-policy-page3.PNG "Valitse organisaatiosolmujen valintaikkuna")</span><span class="sxs-lookup"><span data-stu-id="e7a03-134">![Choose organization nodes dialog box](media/Return-policy-page3.PNG "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="e7a03-135">Suorita **1070**-työ **Jakeluaikataulu**-sivulla, jotta kanavan palautuskäytäntö tulisi käytettäväksi POS:issa.</span><span class="sxs-lookup"><span data-stu-id="e7a03-135">On the **Distribution schedule** page, run the **1070** job to make the channel return policy available to the POS.</span></span>

## <a name="preview-the-channel-return-policy-in-the-pos"></a><span data-ttu-id="e7a03-136">Kanavien palauttamisen käytännön esikatselu POS-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="e7a03-136">Preview the channel return policy in the POS</span></span>

<span data-ttu-id="e7a03-137">Voit tarkastella myyntipisteen sallittuja palautuksen maksuvälinetyyppejä noudattamalla jommankumman seuraavan esimerkin ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e7a03-137">Follow the steps in either of the following examples to view the allowed return tender types in POS.</span></span>

1. <span data-ttu-id="e7a03-138">Kirjaudu POS-sovellukseen kassaksi tai projektipäälliköksi.</span><span class="sxs-lookup"><span data-stu-id="e7a03-138">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="e7a03-139">Valitse **Vaihto ja laatikko** -kohdasta **Näytä kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="e7a03-139">Under **Shift and Drawer**, select **Show journal**.</span></span>
3. <span data-ttu-id="e7a03-140">Valitse tapahtuma, joka on osa palautusta.</span><span class="sxs-lookup"><span data-stu-id="e7a03-140">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="e7a03-141">Valitse palautettavat nimikkeet ja valitse maksutapa.</span><span class="sxs-lookup"><span data-stu-id="e7a03-141">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="e7a03-142">Jos valittu maksuväline on palautusmaksuvälinetyyppien sallittu-luettelossa, kassanhoitaja voi suorittaa tapahtuman loppuun.</span><span class="sxs-lookup"><span data-stu-id="e7a03-142">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="e7a03-143">Jos valittu maksuväline ei ole sallittu, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="e7a03-143">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="e7a03-144">Valitse **Maksettava summa**, joka näyttää kaikkien sallittujen palautusten maksuvälinetyyppien luettelon.</span><span class="sxs-lookup"><span data-stu-id="e7a03-144">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="e7a03-145">-tai-</span><span class="sxs-lookup"><span data-stu-id="e7a03-145">-or-</span></span>

1. <span data-ttu-id="e7a03-146">Kirjaudu POS-sovellukseen kassaksi tai projektipäälliköksi.</span><span class="sxs-lookup"><span data-stu-id="e7a03-146">Sign in to the POS as a cashier or manager.</span></span>
2. <span data-ttu-id="e7a03-147">Valitse **Palauta tapahtuma** ja syötä kuitin tunnus viivakoodin tarkistuksen tai manuaalisen merkinnän avulla.</span><span class="sxs-lookup"><span data-stu-id="e7a03-147">Select **Return Transaction** and enter the receipt ID using a barcode scan or by manual entry.</span></span> 
3. <span data-ttu-id="e7a03-148">Valitse tapahtuma, joka on osa palautusta.</span><span class="sxs-lookup"><span data-stu-id="e7a03-148">Select the transaction that is part of the return.</span></span> 
4. <span data-ttu-id="e7a03-149">Valitse palautettavat nimikkeet ja valitse maksutapa.</span><span class="sxs-lookup"><span data-stu-id="e7a03-149">Select the items to refund, and choose the payment method.</span></span>  
- <span data-ttu-id="e7a03-150">Jos valittu maksuväline on palautusmaksuvälinetyyppien sallittu-luettelossa, kassanhoitaja voi suorittaa tapahtuman loppuun.</span><span class="sxs-lookup"><span data-stu-id="e7a03-150">If the payment tender selected is in the allowed list of return tender types, the cashier can complete the transaction.</span></span>
- <span data-ttu-id="e7a03-151">Jos valittu maksuväline ei ole sallittu, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="e7a03-151">If the payment tender selected is not allowed, an error message is displayed.</span></span>
- <span data-ttu-id="e7a03-152">Valitse **Maksettava summa**, joka näyttää kaikkien sallittujen palautusten maksuvälinetyyppien luettelon.</span><span class="sxs-lookup"><span data-stu-id="e7a03-152">Select **Amount Due** to display a list of all the allowed return tender types.</span></span>

<span data-ttu-id="e7a03-153">![Palautus ei sallittu](media/Return-policy-page6.png "Palautustyyppi ei sallittu")</span><span class="sxs-lookup"><span data-stu-id="e7a03-153">![Refund not allowed](media/Return-policy-page6.png "Refund type not allowed")</span></span>



<span data-ttu-id="e7a03-154">![Maksutapaluettelo](media/Return-policy-page5.PNG "Palautustyypit eivät ole sallittuja")</span><span class="sxs-lookup"><span data-stu-id="e7a03-154">![List of payment methods](media/Return-policy-page5.PNG "Refund types allowed")</span></span>
