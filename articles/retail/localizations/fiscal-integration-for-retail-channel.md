---
title: "Vähittäismyyntikanavan kirjanpidon integrointi"
description: "Tässä ohjeaiheessa on yleiskuvaus Retail POS:n kirjanpidon integroinnista."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: fi-fi
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="4a359-103">Vähittäismyyntikanavan kirjanpidon integrointi</span><span class="sxs-lookup"><span data-stu-id="4a359-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a359-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 for Retailin kirjanpidon integrointitoiminnosta.</span><span class="sxs-lookup"><span data-stu-id="4a359-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="4a359-105">Kirjanpidon integrointitoiminto on kehikko, joka on suunniteltu tukemaan paikallista kirjanpitolainsäädäntöä. Sen avulla on tarkoitus estää petoksia vähittäismyyntialalla.</span><span class="sxs-lookup"><span data-stu-id="4a359-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="4a359-106">Kirjanpidon integraatiota käyttäviä tyypillisiä skenaarioita ovat esimerkiksi seuraavat:</span><span class="sxs-lookup"><span data-stu-id="4a359-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="4a359-107">Verokuitin tulostaminen ja sen antaminen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="4a359-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="4a359-108">Myyntipisteessä suoritettuun myyntiin ja palautuksiin liittyvien tietojen lähettämisen turvaaminen viranomaisen ilmoittamaan ulkoiseen palveluun.</span><span class="sxs-lookup"><span data-stu-id="4a359-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="4a359-109">Tietojen suojaaminen käyttämällä viranomaisen hyväksymää digitaalista allekirjoitusta.</span><span class="sxs-lookup"><span data-stu-id="4a359-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="4a359-110">Tässä ohjeaiheessa on ohjeet kirjanpidon integraation määrittämiseen siten, että käyttäjät voivat suorittaa seuraavat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="4a359-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="4a359-111">Määritä kirjanpidon yhdistimet, jotka ovat laskentavälineitä tai -palveluja. Niitä käytetään kirjanpidon rekisteröinnissä, kuten kirjanpitotietojen tallentaminen, digitaalinen allekirjoittaminen ja turvallinen lähettäminen.</span><span class="sxs-lookup"><span data-stu-id="4a359-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="4a359-112">Määritä asiakirjan toimittaja, joka määrittää tulostusmenetelmän ja kirjanpitoasiakirjan muodostusalgoritmin.</span><span class="sxs-lookup"><span data-stu-id="4a359-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="4a359-113">Määritä kirjanpidon rekisteröintiprosessi, joka määrittää vaiheiden järjestyksen ja kussakin vaiheessa käytetyn yhdistinryhmän.</span><span class="sxs-lookup"><span data-stu-id="4a359-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="4a359-114">Määritä kirjanpidon rekisteröintiprosessin myyntipisteen toimintaprofiileihin.</span><span class="sxs-lookup"><span data-stu-id="4a359-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="4a359-115">Määrittää yhdistimen tekniset profiilit joko laitteistoprofiileihin (paikallisille kirjanpidon yhdistimille) tai myyntipisteen toimintaprofiileihin (muille kirjanpidon yhdistintyypeille).</span><span class="sxs-lookup"><span data-stu-id="4a359-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="4a359-116">Kirjanpidon integroinnin suorittamisen työnkulku</span><span class="sxs-lookup"><span data-stu-id="4a359-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="4a359-117">Seuraavassa skenaariossa esitellään yleinen kirjanpidon integroinnin suorittamisen työnkulku.</span><span class="sxs-lookup"><span data-stu-id="4a359-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="4a359-118">Kirjanpidon rekisteröintiprosessin alustaminen.</span><span class="sxs-lookup"><span data-stu-id="4a359-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="4a359-119">Sen jälkeen kun on suoritettu joitakin toimintoja, joissa tarvitaan kirjanpidon rekisteröintiä, kuten vähittäismyyntitapahtuman päättämisen jälkeen, kirjanpidon rekisteröintiprosessi liitetään nykyiseen myyntipisteen toimintoprofiiliin.</span><span class="sxs-lookup"><span data-stu-id="4a359-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="4a359-120">Kirjanpidon yhdistimen haku.</span><span class="sxs-lookup"><span data-stu-id="4a359-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="4a359-121">Järjestelmä vertaa kirjanpidon yhdistinluetteloa jokaiseen kirjanpidon rekisteröintiprosessiin sisältyvään kirjanpidon rekisteröintivaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="4a359-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="4a359-122">Näillä yhdistimillä on toimintaprofiili, joka sisältyy määritettyyn yhdistinryhmään sekä yhdistinluettelo, joiden tekninen profiili on liitetty nykyiseen laitteistoprofiiliin (kun yhdistintyyppi on sama kuin vain **Paikallinen**) tai nykyiseen myyntipisteen toimintoprofiiliin (muille yhdistintyypeille).</span><span class="sxs-lookup"><span data-stu-id="4a359-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="4a359-123">Kirjanpidon integroinnin suorittaminen.</span><span class="sxs-lookup"><span data-stu-id="4a359-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="4a359-124">Järjestelmä suorittaa kaikki tarvittavat löydettyyn yhdistimeen linkitetyn kokoonpanon määrittämät toiminnot.</span><span class="sxs-lookup"><span data-stu-id="4a359-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="4a359-125">Se tehdään kyseisen yhdistimen edellisessä vaiheessa löydetyn toimintaprofiilin ja teknisen profiilin asetusten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="4a359-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="4a359-126">Kirjanpidon integroinnin käyttöä edeltävät asetukset</span><span class="sxs-lookup"><span data-stu-id="4a359-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="4a359-127">Määritä seuraavat asetukset ennen kirjanpidon integrointitoiminnon käyttämistä:</span><span class="sxs-lookup"><span data-stu-id="4a359-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="4a359-128">Määritä kirjanpidon toimintaprofiilin numeron numerosarjan **Vähittäismyynnin parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4a359-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="4a359-129">Määritä seuraavien viitteiden numerosarjat **Vähittäismyynnin yhteiset parametrit** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="4a359-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="4a359-130">Kirjanpidon teknisen profiilin numero</span><span class="sxs-lookup"><span data-stu-id="4a359-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="4a359-131">Kirjanpidon yhdistinryhmän numero</span><span class="sxs-lookup"><span data-stu-id="4a359-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="4a359-132">Rekisteröintiprosessin numero</span><span class="sxs-lookup"><span data-stu-id="4a359-132">Registration process number</span></span>

- <span data-ttu-id="4a359-133">Luo **kirjanpidon yhdistin** jokaiselle laitteelle tai palvelulle, jota aiot käyttää kirjanpidon integroinnissa, valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi > Kirjanpidon yhdistimet**.</span><span class="sxs-lookup"><span data-stu-id="4a359-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="4a359-134">Luo **Kirjainpitoasiakirjan toimittajat** kaikille kirjanpidon yhdistimille valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi > Kirjainpitoasiakirjan toimittajat**.</span><span class="sxs-lookup"><span data-stu-id="4a359-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="4a359-135">Tietojen yhdistämisen katsotaan olevan osa kirjainpitoasiakirjan toimittajaa.</span><span class="sxs-lookup"><span data-stu-id="4a359-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="4a359-136">Jos haluat määrittää samalle yhdistimelle erilaisia tietojen yhdistämisiä (kuten osavaltiokohtaisia säädöksiä), sinun on luotava erillisiä kirjainpitoasiakirjan toimittajia.</span><span class="sxs-lookup"><span data-stu-id="4a359-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="4a359-137">Luo **Yhdistimen toiminnallinen profiili** kullekin kirjanpitoasiakirjan toimittajalle valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi >Yhdistimen toiminnallinen profiili**.</span><span class="sxs-lookup"><span data-stu-id="4a359-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="4a359-138">Valitse yhdistimen nimi.</span><span class="sxs-lookup"><span data-stu-id="4a359-138">Select a connector name.</span></span>
  - <span data-ttu-id="4a359-139">Valitse asiakirjan toimittaja.</span><span class="sxs-lookup"><span data-stu-id="4a359-139">Select a document provider.</span></span>
  - <span data-ttu-id="4a359-140">Määritä ALV-prosenttiasetukset **Palvelun asetukset** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4a359-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="4a359-141">Määritä ALV-koodien yhdistäminen ja maksuvälinetyyppien yhdistäminen **Tietojen yhdistäminen** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4a359-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="4a359-142">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="4a359-142">Examples</span></span> 

  |  | <span data-ttu-id="4a359-143">Muoto</span><span class="sxs-lookup"><span data-stu-id="4a359-143">Format</span></span> | <span data-ttu-id="4a359-144">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="4a359-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="4a359-145">ALV-prosenttiasetukset</span><span class="sxs-lookup"><span data-stu-id="4a359-145">VAT rates settings</span></span> | <span data-ttu-id="4a359-146">arvo: VATrate</span><span class="sxs-lookup"><span data-stu-id="4a359-146">value : VATrate</span></span> | <span data-ttu-id="4a359-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="4a359-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="4a359-148">ALV-koodien yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="4a359-148">VAT codes mapping</span></span> | <span data-ttu-id="4a359-149">VATcode : arvo</span><span class="sxs-lookup"><span data-stu-id="4a359-149">VATcode : value</span></span> | <span data-ttu-id="4a359-150">vat20 : 1, vat18 : 2</span><span class="sxs-lookup"><span data-stu-id="4a359-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="4a359-151">Maksuvälinetyyppien yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="4a359-151">Tender types mapping</span></span> | <span data-ttu-id="4a359-152">TenderTyp : arvo</span><span class="sxs-lookup"><span data-stu-id="4a359-152">TenderTyp : value</span></span> | <span data-ttu-id="4a359-153">Käteinen : 1, Kortti : 2</span><span class="sxs-lookup"><span data-stu-id="4a359-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="4a359-154">Luo **Kirjanpidon yhdistinryhmät** valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi > Kirjanpidon yhdistinryhmät**.</span><span class="sxs-lookup"><span data-stu-id="4a359-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="4a359-155">Yhdistinryhmä on niiden toiminnallisten profiilien alajoukko, joka on linkitetty samoja toimintoja suorittaviin kirjanpidon yhdistimiin ja joita käytetään samassa kirjanpidon rekisteröintiprosessin vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="4a359-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="4a359-156">Lisää toiminnalliset profiilit yhdistinryhmään.</span><span class="sxs-lookup"><span data-stu-id="4a359-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="4a359-157">Valitse ensin **Lisää** **Toiminnalliset profiilit** -sivulla ja sitten profiilin numero.</span><span class="sxs-lookup"><span data-stu-id="4a359-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="4a359-158">Jos haluat keskeyttää toiminnallisen profiilin käytön, valitse **Poista käytöstä** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="4a359-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="4a359-159">Muutos koskee vain nykyistä yhdistinryhmää.</span><span class="sxs-lookup"><span data-stu-id="4a359-159">This change affects the current connector group only.</span></span> <span data-ttu-id="4a359-160">Voit jatkaa saman toiminnallisen profiilin käyttöä muissa yhdistinryhmissä.</span><span class="sxs-lookup"><span data-stu-id="4a359-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="4a359-161">Kullakin kirjanpidon yhdistimellä voi olla yhdistinryhmässä vain yksi toiminnallinen profiili.</span><span class="sxs-lookup"><span data-stu-id="4a359-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="4a359-162">Luo **Yhdistimen tekninen profiili** kullekin kirjanpidon yhdistimelle valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi >Yhdistimen tekninen profiili**.</span><span class="sxs-lookup"><span data-stu-id="4a359-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="4a359-163">Valitse yhdistimen nimi.</span><span class="sxs-lookup"><span data-stu-id="4a359-163">Select a connector name.</span></span>
  - <span data-ttu-id="4a359-164">Valitse yhdistimen tyyppi:</span><span class="sxs-lookup"><span data-stu-id="4a359-164">Select a connector type:</span></span> 
      - <span data-ttu-id="4a359-165">**Paikallinen** – määritä tämä tyyppi paikalliseen koneeseen asennetuille fyysisille laitteille tai sovelluksille.</span><span class="sxs-lookup"><span data-stu-id="4a359-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="4a359-166">**Sisäinen** – määritä tämä tyyppi Retail Serveriin yhdistetyille kirjanpidon laitteille ja palveluille.</span><span class="sxs-lookup"><span data-stu-id="4a359-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="4a359-167">**Ulkoinen** – ulkoisille kirjanpidon palveluille, kuten veroviranomaisten verkkoportaalille.</span><span class="sxs-lookup"><span data-stu-id="4a359-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="4a359-168">Määritä asetukset **Yhteys**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4a359-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="4a359-169">Aiemmin ladatun määrityksen päivitetty versio ladataan sekä toiminnalliselle että tekniselle profiilille.</span><span class="sxs-lookup"><span data-stu-id="4a359-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="4a359-170">Jos soveltuva yhdistin asiakirjan toimittaja on jo käytössä, saat siitä ilmoituksen.</span><span class="sxs-lookup"><span data-stu-id="4a359-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="4a359-171">Oletusarvoisesti kaikki toiminnalliseen ja tekniseen profiiliin manuaalisesti tehdyt muutokset tallennetaan.</span><span class="sxs-lookup"><span data-stu-id="4a359-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="4a359-172">Voit korvata nämä profiilit määrityksen oletusparametrijoukolla valitsemalla **Päivitä** **Yhdistimen toiminnalliset profiilit** -sivulla ja **Yhdistimen tekniset profiilit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4a359-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="4a359-173">Luo **Kirjanpidon rekisteröintiprosessi** kirjanpidon integroinnin jokaiselle yksilölliselle prosessille valitsemalla **Vähittäismyynti > Kanavan asetukset > Kirjanpidon integrointi > Kirjanpidon rekisteröintiprosessi**.</span><span class="sxs-lookup"><span data-stu-id="4a359-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="4a359-174">Rekisteröintivaiheiden järjestys ja kussakin vaiheessa käytetty yhdistinryhmä määrittävät rekisteröintiprosessin.</span><span class="sxs-lookup"><span data-stu-id="4a359-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="4a359-175">Lisää rekisteröintivaiheet prosessiin:</span><span class="sxs-lookup"><span data-stu-id="4a359-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="4a359-176">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="4a359-176">Click **Add**.</span></span>
      - <span data-ttu-id="4a359-177">Valitse yhdistimen tyyppi.</span><span class="sxs-lookup"><span data-stu-id="4a359-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="4a359-178">Tämä kenttä määrittää, mistä järjestelmä etsii yhdistintä teknisessä profiilissa. Jos yhdistimen tyyppi on **Paikallinen**, haku tehdään laitteistoprofiileissa, kun taas muita kirjanpidon yhdistintyyppejä haetaan myyntipisteen toiminnallisista profiileista.</span><span class="sxs-lookup"><span data-stu-id="4a359-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="4a359-179">Valitse yhdistinryhmä.</span><span class="sxs-lookup"><span data-stu-id="4a359-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="4a359-180">Tarkista rekisteröintiprosessin rakenteen yhtenäisyys valitsemalla **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="4a359-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="4a359-181">Tarkistusten suorittamista suositellaan seuraavissa tapauksissa:</span><span class="sxs-lookup"><span data-stu-id="4a359-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="4a359-182">Uudessa rekisteröintiprosessissa sen jälkeen, kun kaikki asetukset ovat valmiita. Tämä koskee myös sidontaa myyntipisteen toiminnallisiin profiileihin ja laitteistoprofiileihin.</span><span class="sxs-lookup"><span data-stu-id="4a359-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="4a359-183">Aiemmin luodun rekisteröintiprosessin päivittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="4a359-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="4a359-184">Sido kirjanpidon rekisteröintiprosessit myyntipisteen toiminnallisiin profiileihin valitsemalla **Vähittäismyynti > Kanavan asetukset > POS-asetukset > POS-profiilit > Toiminnalliset profiilit**.</span><span class="sxs-lookup"><span data-stu-id="4a359-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="4a359-185">Valitse ensin **Muokkaa** ja sitten **Prosessin numero** **Kirjanpidon rekisteröintiprosessi** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4a359-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="4a359-186">Sido yhdistimen tekniset profiilit laiteprofiileihin valitsemalla **Vähittäismyynti > Kanavan asetukset > POS-asetukset > POS-profiilit > Laiteprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="4a359-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="4a359-187">Valitse ensin **Muokkaa** ja sitten **Uusi** **Kirjanpidon tekninen profiili** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="4a359-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="4a359-188">Valitse yhdistimen tekninen profiili **Profiilin numero** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4a359-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="4a359-189">Voit lisätä useita teknisiä profiileja laiteprofiiliin.</span><span class="sxs-lookup"><span data-stu-id="4a359-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="4a359-190">Tätä ei kuitenkaan tueta, jos laiteprofiilissa on useampi kuin yksi leikkauskohta jonkin yhdistinryhmän kanssa.</span><span class="sxs-lookup"><span data-stu-id="4a359-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="4a359-191">Voit estää virheelliset asetukset, jos tarkistat rekisteröintiprosessin suositusten mukaisesti kaikkien laiteprofiilien päivittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="4a359-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

