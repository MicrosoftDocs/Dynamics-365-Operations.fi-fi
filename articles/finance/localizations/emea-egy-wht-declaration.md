---
title: Egyptin ennakonpidätysilmoitus
description: Tässä aiheessa kerrotaan, miten Egyptin ennakonpidätysilmoitus konfiguroidaan ja muodostetaan.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8c9aaa3868167806ce3189d724621991ec7e53eb
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022808"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="95f2a-103">Egyptin ennakonpidätysilmoitus (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="95f2a-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="95f2a-104">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="95f2a-104">Overview</span></span>
<span data-ttu-id="95f2a-105">Tässä ohjeaiheessa on tietoja ennakonpidätysilmoituksen ja ennakonpidätysilmoituksen lomakkeiden 41 ja 11 määrittämisestä ja luomisesta yrityksille Egyptissä</span><span class="sxs-lookup"><span data-stu-id="95f2a-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="95f2a-106">Kaikkien egyptiläisten yritysten on valmisteltava lomake 41, joka sisältää yhteenvedon kaikista paikallisilta toimittajilta ja palveluntuottajilta pidätetyistä veroista.</span><span class="sxs-lookup"><span data-stu-id="95f2a-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="95f2a-107">Lomakkeen 41 lisäksi on muodostettava lomake 11, jotta voidaan eritellään kaikki ulkomaisilta toimittajilta pidätetyt verot.</span><span class="sxs-lookup"><span data-stu-id="95f2a-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="95f2a-108">Dynamics 365 Financen **Ennakonpidätysilmoitus**-raportti sisältää seuraavat raportit:</span><span class="sxs-lookup"><span data-stu-id="95f2a-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="95f2a-109">Ilmoituslomake nro</span><span class="sxs-lookup"><span data-stu-id="95f2a-109">Declaration form No.</span></span> <span data-ttu-id="95f2a-110">41</span><span class="sxs-lookup"><span data-stu-id="95f2a-110">41</span></span>
- <span data-ttu-id="95f2a-111">Ilmoituslomake nro</span><span class="sxs-lookup"><span data-stu-id="95f2a-111">Declaration form No.</span></span> <span data-ttu-id="95f2a-112">11</span><span class="sxs-lookup"><span data-stu-id="95f2a-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="95f2a-113">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="95f2a-113">Prerequisites</span></span>
<span data-ttu-id="95f2a-114">Yrityksen ensisijainen osoite on on oltava Egyptissä.</span><span class="sxs-lookup"><span data-stu-id="95f2a-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="95f2a-115">**Ominaisuuksien hallinta** -työtilassa on otettava käyttöön seuraava ominaisuus:</span><span class="sxs-lookup"><span data-stu-id="95f2a-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="95f2a-116">**Yleinen ennakonpidätys**</span><span class="sxs-lookup"><span data-stu-id="95f2a-116">**Global withholding tax**</span></span>

<span data-ttu-id="95f2a-117">Lisätietoja uusien ominaisuuksien käyttöönotosta on kohdassa [ominaisuuksien hallinnan yleiskuvaus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="95f2a-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="95f2a-118">Siirry kohtaan **Vero** >  **Asetukset** > **Parametrit** > **Kirjanpitoparametrit** ja määritä **Ennakonpidätys**-välilehden **Ota yleinen ennakonpidätys käyttöön** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="95f2a-119">Tuo **Sähköinen raportointi** -työtilassa seuraavat sähköiset raportointimuodot tietovarastosta:</span><span class="sxs-lookup"><span data-stu-id="95f2a-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="95f2a-120">Ennakonpidätysilmoitus, Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="95f2a-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="95f2a-121">Edellä esitetty muoto perustuu **veroilmoituksen malliin** ja käyttää **veroilmoituksen mallimääritystä**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="95f2a-122">Tämä lisäkonfiguraatio tuodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="95f2a-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="95f2a-123">Lisätietoja sähköisen raportoinnin konfiguraatioiden tuomisesta on kohdassa [Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Services  -palveluista](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="95f2a-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="95f2a-124">Sähköisen raportoinnin konfiguraatioiden lataaminen</span><span class="sxs-lookup"><span data-stu-id="95f2a-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="95f2a-125">Egyptin ennakonpidätysilmoituslomakkeiden toteutus, joka perustuu sähköisen raportoinnin konfiguraatioihin.</span><span class="sxs-lookup"><span data-stu-id="95f2a-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="95f2a-126">Lisätietoja konfiguroitavan raportoinnin ominaisuuksista ja käsitteistä on kohdassa [Sähköinen raportointi](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="95f2a-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="95f2a-127">Tuotanto- ja käyttäjähyväksyntätestausympäristöille on ohjeet aiheessa [Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Services -palveluista](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="95f2a-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="95f2a-128">Jos haluat luoda ennakonpidätysilmoitukset egyptiläisessä yrityksessä, sinun on ladattava palvelimeen seuraavat konfiguraatiot:</span><span class="sxs-lookup"><span data-stu-id="95f2a-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="95f2a-129">Veroilmoitus model.version.82.xml tai myöhempi versio</span><span class="sxs-lookup"><span data-stu-id="95f2a-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="95f2a-130">Veroilmoituksen mallin mapping.version.82.133.xml tai myöhempi versio</span><span class="sxs-lookup"><span data-stu-id="95f2a-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="95f2a-131">Ennakonpidätysilmoituksen Excel (EG).version.82.21 tai myöhempi versio</span><span class="sxs-lookup"><span data-stu-id="95f2a-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="95f2a-132">Kun olet ladanut ER-konfiguraatiot Lifecycle Services (LCS) -palvelusta tai yleisestä tietovarastosta, tee seuraavat toimet.</span><span class="sxs-lookup"><span data-stu-id="95f2a-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="95f2a-133">Valitse **Sähköisen raportoinnin** työtilassa **Raportointimääritykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="95f2a-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="95f2a-134">Valitse toimintoruudun **Konfiguroinnit**-välilehdessä **Vaihda > Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="95f2a-135">Lataa kaikki tiedostot sen mukaan, missä järjestyksessä ne on lueteltu edellisessä luettelossa.</span><span class="sxs-lookup"><span data-stu-id="95f2a-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="95f2a-136">Kun kaikki konfiguraatiot on ladattu palvelimeen, konfiguraatiopuun pitäisi näkyä Financessa.</span><span class="sxs-lookup"><span data-stu-id="95f2a-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="95f2a-137">Sovelluskohtaisten parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="95f2a-137">Set up application-specific parameters</span></span>

<span data-ttu-id="95f2a-138">Sovelluskohtaisien parametrien vaihtoehdon avulla käyttäjät voivat määrittää kriteerit, joiden mukaan verotapahtumat luokitellaan ja lasketaan kullakin luodun raportin rivillä sen mukaan, miten **ennakonpidätysnimikeryhmä** tai muu ehto on määritetty hakumäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="95f2a-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="95f2a-139">Ennakonpidätyslomake 41 sisältää erityissarakkeen, jossa ennakonpidätystapahtuma on luokiteltava veroviranomaisen **Alennuskoodityyppi**-nimisen luokituksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="95f2a-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="95f2a-140">Sen sijaan, että nämä uudet luokittelut sisällytettäisiin uuden viennin tietoina tapahtumien kirjaamisen yhteydessä, luokittelut määritetään kohdassa **Määritykset** > **Määritä sovelluskohtaiset parametrit** > **Määritys** esiteltyjen eri hakujen mukaan, jotta täytetään Egyptin ennakonpidätysraporttien vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="95f2a-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="95f2a-141">Seuraavan konfiguraation avulla voidaan luokitella tapahtumat ennakonpidätyslomakkeen 41 raportissa:</span><span class="sxs-lookup"><span data-stu-id="95f2a-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="95f2a-142">**DiscountTaxTypeLookup**-> Sarake nro 18</span><span class="sxs-lookup"><span data-stu-id="95f2a-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="95f2a-143">Seuraavia ohjeita noudattamalla voit määrittää eri hakuja, joita käytetään ennakonpidätysilmoituksen ja siihen liittyvien kirjojen raporttien luomisessa.</span><span class="sxs-lookup"><span data-stu-id="95f2a-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="95f2a-144">Valitse **Sähköinen raportointi** -työtilassa **Määritykset** > **Määritys**, kun haluat määrittää säännöt, jotka määrittävät, miten tapahtumat luokitellaan ennakonpidätysilmoitusraportissa.</span><span class="sxs-lookup"><span data-stu-id="95f2a-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="95f2a-145">Valitse nykyinen versio ja valitse hakunimi **Haut**-pikavälilehdistä.</span><span class="sxs-lookup"><span data-stu-id="95f2a-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="95f2a-146">Esimerkiksi **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="95f2a-147">Tämä haku määrittää veroviranomaisen edellyttämän alennustyyppien luettelon.</span><span class="sxs-lookup"><span data-stu-id="95f2a-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="95f2a-148">Valitse **Ehdot**-pikavälilehdessä **Lisää** ja valitse uuden rivin **Hakutulos**-sarakkeessa liittyvä rivi, joka vastaa **sarakkeen 18** luokittelua.</span><span class="sxs-lookup"><span data-stu-id="95f2a-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="95f2a-149">Valitse **Ennakonpidätysnimikeryhmä**-sarakkeesta liittyvä koodi, jota käytetään luokituksen tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="95f2a-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="95f2a-150">Esimerkiksi **Sallittu alennus**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="95f2a-151">Toista vaiheet 3 ja 4 kaikille käytettävissä oleville hauille.</span><span class="sxs-lookup"><span data-stu-id="95f2a-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="95f2a-152">Valitse uudelleen **Lisää**, jos haluat sisällyttää lopullisen tietuerivin. Valitse sitten **Hakutulos**-sarakkeesta **Ei sovellettavissa**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="95f2a-153">Valitse jäljellä olevissa sarakkeissa **Ei tyhjä**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="95f2a-154">Kirjanpidon parametrien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="95f2a-154">Set up General ledger parameters</span></span>

<span data-ttu-id="95f2a-155">Voit luoda ennakonpidätysilmoituslomakkeen raportit Microsoft Excelissä, kun määrität ER-muodon **Kirjanpitoparametrit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="95f2a-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="95f2a-156">Siirry kohtaan **Vero** > **Asetukset** > **Kirjanpitoparametrit**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="95f2a-157">Valitse **Ennakonpidätys**-välilehden **Ennakonpidätysilmoituksen muodon määritys** -kentästä **Ennakonpidätysilmoitus, Excel (EG)**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="95f2a-158">Jos jätät tämän kentän tyhjäksi, arvonlisäveron vakioraportti luodaan SSRS-muodossa.</span><span class="sxs-lookup"><span data-stu-id="95f2a-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Ilmoituslomake](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="95f2a-160">Ennakonpidätysilmoituslomakkeiden muodostaminen</span><span class="sxs-lookup"><span data-stu-id="95f2a-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="95f2a-161">Tietyn kauden ennakonpidätyslomakkeen valmistelu- ja lähetysprosessi perustuu Tilitä ja kirjaa maksun vero -työn aikana kirjattuihin ennakonpidätystapahtumiin.</span><span class="sxs-lookup"><span data-stu-id="95f2a-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="95f2a-162">Lisätietoja yleisistä ennakonpidätyksistä on kohdassa [Yleinen ennakonpidätys](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="95f2a-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="95f2a-163">Luo veroilmoitusraportti noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="95f2a-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="95f2a-164">Siirry kohtaan **Vero** > **Ilmoitus** > **Ennakonpidätys** > \**Ennakonpidätysmaksu*.</span><span class="sxs-lookup"><span data-stu-id="95f2a-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="95f2a-165">Valitse tilityskausi ja valitse sitten raportin aloituspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="95f2a-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="95f2a-166">Syötä tapahtuman päivämäärä ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="95f2a-167">Valitse näyttöön tulevassa valintaikkunassa yksi tai useampi lomaketyypeistä **Form nro 41**, **Form nro 11** tai **Ei mikään**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="95f2a-168">Jos valitset **Ei mikään**, luodaan vakioraportti.</span><span class="sxs-lookup"><span data-stu-id="95f2a-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="95f2a-169">Valitse kieli.</span><span class="sxs-lookup"><span data-stu-id="95f2a-169">Select the language.</span></span> <span data-ttu-id="95f2a-170">Kaikki raportit käänetään kielille **en-us** ja **ar-eg**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="95f2a-171">Syötä sen pankin sivuliike ja nimi, josta veromaksu maksetaan.</span><span class="sxs-lookup"><span data-stu-id="95f2a-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="95f2a-172">Valitse yrityksen tyyppi ja kirjoita sitten tarkistus- ja asiakirjanumerot.</span><span class="sxs-lookup"><span data-stu-id="95f2a-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="95f2a-173">Anna yksikön tyyppi.</span><span class="sxs-lookup"><span data-stu-id="95f2a-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="95f2a-174">Kirjoita sen henkilön nimi, joka on rekisteröity määrittämään lomake, ja vahvista raportin luonti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="95f2a-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
