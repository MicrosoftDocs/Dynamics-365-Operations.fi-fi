---
title: Automaattisten veloitusten käyttöönotto ja määritys kanavan mukaan
description: Tässä ohjeaiheessa kerrotaan, kuinka automaattiset veloitukset otetaan käyttöön ja määritetään Microsoft Dynamics 365 Commerce -kanavalla.
author: gvrmohanreddy
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 1be07c754e563298d82f6ca54f09ae3aa9118602
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411949"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="3db06-103">Automaattisten veloitusten käyttöönotto ja määritys kanavan mukaan</span><span class="sxs-lookup"><span data-stu-id="3db06-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="3db06-104">Tässä ohjeaiheessa kerrotaan, kuinka automaattiset veloitukset (auto charges) otetaan käyttöön ja määritetään Microsoft Dynamics 365 Commerce -kanavalla.</span><span class="sxs-lookup"><span data-stu-id="3db06-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3db06-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="3db06-105">Overview</span></span>

<span data-ttu-id="3db06-106">Sinulla voi olla tilanteita, joissa kierrätysmaksuja tai muita maksuja on sovellettava tuoteryhmään, joka myydään tietyn osavaltion kaikissa tai joissakin myymälöissä (esimerkiksi Kaliforniassa).</span><span class="sxs-lookup"><span data-stu-id="3db06-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="3db06-107">**Ota käyttöön automaattiset veloitukset kanavakohtaisesti** -ominaisuuden avulla voit määrittää automaattiset maksut kanavan mukaan (esimerkiksi tietty myyntipaikka).</span><span class="sxs-lookup"><span data-stu-id="3db06-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="3db06-108">Ominaisuutta on saatavilla Dynamics 365 Commercen versiossa 10.0.10 ja sitä uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="3db06-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="3db06-109">Jos haluat ottaa käyttöön ja määrittää automaattiset veloitukset kanavakohtaisesti, sinun on suoritettava seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="3db06-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="3db06-110">Ota käyttöön **Suodata automaattiset kulut kanavan mukaan** -toiminto.</span><span class="sxs-lookup"><span data-stu-id="3db06-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="3db06-111">Määritä organisaatiohierarkian tarkoitukset.</span><span class="sxs-lookup"><span data-stu-id="3db06-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="3db06-112">Määritä automaattiset veloitukset kanavan mukaan.</span><span class="sxs-lookup"><span data-stu-id="3db06-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="3db06-113">**Ota suodattimien automaattiset veloitukset käyttöön** -toiminto toimii vain, jos myös automaattiset lisämaksut -toiminto on käytössä.</span><span class="sxs-lookup"><span data-stu-id="3db06-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="3db06-114">Lisätietoja automaattisten lisämaksujen lisäasetusten ottamisesta käyttöön on kohdassa [Monikanavaiset edistyneet automaattiset veloitukset](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="3db06-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="3db06-115">Ota käyttöön Suodata automaattiset kulut kanavan mukaan -toiminto</span><span class="sxs-lookup"><span data-stu-id="3db06-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="3db06-116">Jos haluat ottaa käyttöön automaattiset veloitukset kanavassa, noudata seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="3db06-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3db06-117">Valitse **Järjestelmänvalvoja \> Työtilat \> Ominaisuuksien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="3db06-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="3db06-118">Valitse **Ei käytössä** -välilehdessä **Ominaisuuden nimi** -luettelosta **Ota suodattimen automaattiset veloitukset käyttöön kanavalla**.</span><span class="sxs-lookup"><span data-stu-id="3db06-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="3db06-119">Valitse oikeasta alakulmasta **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="3db06-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="3db06-120">Kun ominaisuus on otettu käyttöön, se näkyy **Kaikki**-välilehden luettelossa.</span><span class="sxs-lookup"><span data-stu-id="3db06-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="3db06-121">Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="3db06-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="3db06-122">Etsi ja valitse vasemmanpuoleisesta ruudusta **1110** (**Yleinen konfigurointi**) -tehtävä.</span><span class="sxs-lookup"><span data-stu-id="3db06-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="3db06-123">Jos haluat levittää konfigurointimuutoksia, valitse toimintoruudussa **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="3db06-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="3db06-124">Jos poistat **Ota suodattimen automaattiset veloitukset käyttöön kanavan mukaan** -toiminnon käytöstä sen jälkeen, kun olet jo käyttänyt sitä, **Automaattiset kulut** -kohdan **Vähittäismyyntikanavan suhde** -kenttä ei enää tule näkyviin ja menetät kaikki olemassa olevat määritykset.</span><span class="sxs-lookup"><span data-stu-id="3db06-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="3db06-125">Jos **Vähittäismyyntikanavan suhde** -kokoonpanojen poistaminen aiheuttaa automaattisen kulujen sääntöjen monistumisen, toiminto ei onnistu.</span><span class="sxs-lookup"><span data-stu-id="3db06-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="3db06-126">Tarkista kaikki automaattiset veloitukset ja tee tarvittavat muutokset, ennen kuin poistat toiminnon käytöstä.</span><span class="sxs-lookup"><span data-stu-id="3db06-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="3db06-127">Määritä organisaatiohierarkian tarkoitukset</span><span class="sxs-lookup"><span data-stu-id="3db06-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="3db06-128">Uusi organisaatiohierarkian tarkoitus, jonka nimi on **Vähittäismyynnin automaattinen veloitus**, on luotu, jotta voidaan hallita kanavan automaattisia veloituksia.</span><span class="sxs-lookup"><span data-stu-id="3db06-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="3db06-129">Voit määrittää organisaation hierarkian käyttötarkoituksen oletushierarkian noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="3db06-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="3db06-130">Siirry kohtaan **Organisaation hallinto \> Organisaatiot \> Organisaatiohierarkian käyttötarkoitukset**.</span><span class="sxs-lookup"><span data-stu-id="3db06-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="3db06-131">Valitse vasemmasta ruudusta **Vähittäismyynnin automaattinen veloitus**.</span><span class="sxs-lookup"><span data-stu-id="3db06-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="3db06-132">Valitse **Määritetyt hierarkiat** -kohdasta **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="3db06-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="3db06-133">Valitse **Organisaation hierarkiat**-valintaikkunassa organisaatiohierarkia (esimerkiksi **Vähittäismyymälät alueittain**) ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="3db06-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="3db06-134">Valitse **Määritetyt hierarkiat** -kohdasta **Aseta oletukseksi**.</span><span class="sxs-lookup"><span data-stu-id="3db06-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="3db06-135">Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="3db06-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="3db06-136">Etsi ja valitse vasemmanpuoleisesta ruudusta **1040** (**Tuotteet**) -tehtävä.</span><span class="sxs-lookup"><span data-stu-id="3db06-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="3db06-137">Valitse toimintoruudussa **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="3db06-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="3db06-138">Suorita **1070** (**Kanavan määritys**)- ja **1110** (**Yleinen määritys**) -työt toistamalla edelliset kaksi vaihetta.</span><span class="sxs-lookup"><span data-stu-id="3db06-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![Vähittäismyynnin automaattisen latauksen organisaatiohierarkian tarkoituksen määrittäminen](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="3db06-140">Määritä automaattiset veloitukset kanavan mukaan</span><span class="sxs-lookup"><span data-stu-id="3db06-140">Define auto charges by channel</span></span>

<span data-ttu-id="3db06-141">Kun olet ottanut käyttöön **Suodata automaattiset kulut kanavan mukaan** -ominaisuuden ja määrittänyt **Vähittäismyynnin automaattisen veloituksen** -organisaatiohierarkian tarkoituksen, automaattiset veloitukset voidaan määrittää joko tilauksen otsikkotasolla tai tilausrivin tasolla.</span><span class="sxs-lookup"><span data-stu-id="3db06-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="3db06-142">Jos haluat määritellä automaattiset veloitukset kanavassa, noudata seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="3db06-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3db06-143">Valitse  **Myyntireskontra \> Kulujen määritys \> Automaattiset kulut**.</span><span class="sxs-lookup"><span data-stu-id="3db06-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="3db06-144">Valitse vasemman ruudun **Taso**-kentästä liiketoiminnan tarpeista riippuen joko **Otsikko** tai **Rivi**.</span><span class="sxs-lookup"><span data-stu-id="3db06-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="3db06-145">Valitse kanavan koodi **Vähittäismyyntikanavan koodi** -kentässä (esimerkiksi **Taulu** tai **Ryhmä**).</span><span class="sxs-lookup"><span data-stu-id="3db06-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="3db06-146">Jos oletusasetus on **Kaikki**, veloitussääntöjä käytetään kaikissa kanavissa.</span><span class="sxs-lookup"><span data-stu-id="3db06-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="3db06-147">Jos valitset **Ryhmä**-vaihtoehdon, varmista, että kanavaveloitusryhmä luodaan kohdassa **Vähittäismyynti ja kauppa \> Kanava-asetus \> Veloitus \> Vähittäismyyntikanavien veloitusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="3db06-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="3db06-148">Jos valitset **Taulu**-vaihtoehdon, voit valita tietyn kanavan (esimerkiksi **San Francisco**) **Vähittäismyynnin kanava suhteessa** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="3db06-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="3db06-149">Mene kohtaan **Retail ja Commerce \> Retail ja Commerce IT \> Jakeluaikataulu**.</span><span class="sxs-lookup"><span data-stu-id="3db06-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="3db06-150">Etsi ja valitse vasemmanpuoleisesta ruudusta **1040** (**Tuotteet**) -tehtävä.</span><span class="sxs-lookup"><span data-stu-id="3db06-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="3db06-151">Valitse toimintoruudussa **Suorita nyt**.</span><span class="sxs-lookup"><span data-stu-id="3db06-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="3db06-152">Suorita **1070** (**Kanavan määritys**)- ja **1110** (**Yleinen määritys**) -työt toistamalla edelliset kaksi vaihetta.</span><span class="sxs-lookup"><span data-stu-id="3db06-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![Kanavan mukaan määritetyt automaattiset veloitukset](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="3db06-154">Esimerkkiskenaario</span><span class="sxs-lookup"><span data-stu-id="3db06-154">Example scenario</span></span>

<span data-ttu-id="3db06-155">Seuraavassa esimerkissä kuvataan vaiheet, jotka tarvitaan tuotteen määrittämisessä, jotta kierrätysmaksuja veloitetaan, kun tuote myydään San Franciscon kivijalkakaupan kautta.</span><span class="sxs-lookup"><span data-stu-id="3db06-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="3db06-156">Esimerkissä näytetään myös, miten automaattiset veloitukset näkyvät kaupan myyntipiste (POS)-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="3db06-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="3db06-157">Organisaatio määrittää kulujen koodin, joka on nimeltään **KIERRÄTÄ**, kuten seuraavasta kuvasta näkyy.</span><span class="sxs-lookup"><span data-stu-id="3db06-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![KIERRÄTÄ kulujen koodi](media/Auto-charges-charge-code.png)

<span data-ttu-id="3db06-159">Automaattinen veloitus luodaan rivitasolla.</span><span class="sxs-lookup"><span data-stu-id="3db06-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="3db06-160">Sillä on seuraavat määritykset:</span><span class="sxs-lookup"><span data-stu-id="3db06-160">It has the following configuration:</span></span>

- <span data-ttu-id="3db06-161">**Tilikoodi**-kentän arvoksi määritetään **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="3db06-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="3db06-162">**Nimekekoodi**-kentän arvoksi määritetään **Taulu**.</span><span class="sxs-lookup"><span data-stu-id="3db06-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="3db06-163">**Nimikkeen suhde** -kentän arvoksi määritetään tuotetunnus **91001**.</span><span class="sxs-lookup"><span data-stu-id="3db06-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="3db06-164">**Toimitustapakoodi** -kentän arvoksi määritetään **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="3db06-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="3db06-165">**Vähittäiskaupan koodi** -kentän arvoksi määritetään **Taulu**.</span><span class="sxs-lookup"><span data-stu-id="3db06-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="3db06-166">**Vähittäiskaupan kanava suhteessa** -kentän arvoksi määritetään myymälä **San Francisco** ssa.</span><span class="sxs-lookup"><span data-stu-id="3db06-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="3db06-167">Järjestelmä luo automaattisen kulujen rivin.</span><span class="sxs-lookup"><span data-stu-id="3db06-167">An auto charges line is created.</span></span> <span data-ttu-id="3db06-168">Sillä on seuraavat määritykset:</span><span class="sxs-lookup"><span data-stu-id="3db06-168">It has the following configuration:</span></span>

- <span data-ttu-id="3db06-169">**Valuutta**-kentän tilaksi määritetään **USD**.</span><span class="sxs-lookup"><span data-stu-id="3db06-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="3db06-170">**Veloituskoodi**-kentän arvoksi määritetään **KIERRÄTÄ**.</span><span class="sxs-lookup"><span data-stu-id="3db06-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="3db06-171">**Luokkaa**-kentän tilaksi määritetään **Korjattu**.</span><span class="sxs-lookup"><span data-stu-id="3db06-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="3db06-172">**Veloitukset**-kentän tilaksi on määritetään **$6,25**.</span><span class="sxs-lookup"><span data-stu-id="3db06-172">The **Charges** field is set to **$6.25**.</span></span>

![Rivitason automaattisen latauksen määritys ja automaattisten kulujen rivi](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="3db06-174">Myyntitilaus luodaan POS-sovelluksessa **San Francisco**-myymäläkanavalla.</span><span class="sxs-lookup"><span data-stu-id="3db06-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="3db06-175">**Veloitukset**-rivillä näkyy kierrätysmaksu **$6,25**.</span><span class="sxs-lookup"><span data-stu-id="3db06-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="3db06-176">Valitsemalla **Tapahtumavaihtoehdot \> Veloitukset \> Hallitse veloituksia** POS-sovelluksessa, voit tarkastella kierrätysmaksun kulukoodia ja kuvausta.</span><span class="sxs-lookup"><span data-stu-id="3db06-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![Kierrätysmaksu POS-sovelluksessa](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="3db06-178">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3db06-178">Additional resources</span></span>

[<span data-ttu-id="3db06-179">Omnikanavan automaattiset etukäteisveloitukset</span><span class="sxs-lookup"><span data-stu-id="3db06-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="3db06-180">Otsikon kulujen suhteellinen jakaminen vastaaville myyntiriveille</span><span class="sxs-lookup"><span data-stu-id="3db06-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)
