---
title: Regulatory Configuration Services (RCS) – globalisointiominaisuudet
description: Tässä ohjeaiheessa käsitellään Microsoft Regulatory Configuration Servicesin (RCS) ja yleisen säilön käyttöä globalisointitoiminnon luontiin ja käyttöön.
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: d5d42bd076ca77c5d2906593d44ae420d954a0b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218851"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="bdcfb-103">Regulatory Configuration Services (RCS) – globalisointiominaisuudet</span><span class="sxs-lookup"><span data-stu-id="bdcfb-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdcfb-104">Microsoft Regulatory Configuration Servicesin (RCS) avulla voit luoda globalisointitoiminnon, jota voidaan käyttää esimerkiksi verkkolaskupalveluissa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="bdcfb-105">RCS-toiminnon avulla voit suorittaa seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="bdcfb-106">Määritä ominaisuuden liittyvät komponentit.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-106">Define related components of a feature.</span></span>
- <span data-ttu-id="bdcfb-107">Hallitse ominaisuuden elinkaarta toiminnon tilan avulla.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="bdcfb-108">Määritä ominaisuus käytettäviksi määritetyille ympäristöille.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="bdcfb-109">Jaa ominaisuus muiden organisaatioiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="bdcfb-110">Seuraavissa ohjeissa selitetään, kuinka RCS-käyttäjä voi lisätä globalisaatiotoiminnon ja siihen liittyvät komponentit, päivittää toiminnon tilan ja määrittää toiminnon käytettäväksi, jotta sitä voidaan käyttää globalisointipalveluissa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="bdcfb-111">Ennen kuin suoritat toimenpiteet, sinun on suoritettava seuraaviin tehtäviin liittyvät vaiheet:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="bdcfb-112">Pääsy RCS-esiintymään.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="bdcfb-113">Konfigurointipalvelun luominen ja aktivoiminen.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="bdcfb-114">Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="bdcfb-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="bdcfb-115">Noudata seuraavia ohjeita Finance and Operations -sovellusesiintymässä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="bdcfb-116">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="bdcfb-117">Jos yritykseen ei ole valmisteltu RCS-ympäristöä, valitse **Regulatory Services – määritys** -linkki ja valmistele sellainen ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="bdcfb-118">Jos yritykseen on valmisteltu RCS-ympäristö, siirry ympäristöön sivun URL-osoitteen avulla valitsemalla kirjautumisvaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="bdcfb-119">Globalisaatio-ominaisuuksien ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="bdcfb-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="bdcfb-120">Valitse RCS-esiintymässä **Ominaisuuksien hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="bdcfb-121">**Valitse ominaisuuksien hallinta** -työtilassa luettelosta **globalisaation ominaisuudet** ja valitse sitten **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![Globalisaatio-ominaisuudet ominaisuuksien hallinnassa](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="bdcfb-123">Globalisaatio-ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="bdcfb-123">Globalization features</span></span>

<span data-ttu-id="bdcfb-124">Jos haluat käyttää globalisointiominaisuutta, sinun on ensin tuotava se yleisestä tietovarastosta ja luotava sen oma versio.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="bdcfb-125">Voit lisätä globalisaatiotoimintoja kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="bdcfb-126">Lisää johdettu ominaisuus, joka perustuu aiemmin julkaistuun tai jaettuun toimintoon.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="bdcfb-127">Lisää uusi luomasi ominaisuus tyhjästä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="bdcfb-128">Globalisaatio-ominaisuuksien käyttäminen</span><span class="sxs-lookup"><span data-stu-id="bdcfb-128">Access Globalization features</span></span>

1. <span data-ttu-id="bdcfb-129">Varmista, että **globalisointitoiminnot** -toiminto on otettu käyttöön ominaisuuksien hallinnassa aiemmin tässä ohjeaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="bdcfb-130">Avaa uusi **globalisointitoiminnot** -työtila ja valitse sitten **Ominaisuudet**-kohdan **sähköinen laskutus** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![Yleiset ominaisuudet -työtila](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="bdcfb-132">**Sähköisen laskutuksen ominaisuudet** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-132">The **e-Invoicing Features** page is opened.</span></span>

    ![Sähköisen laskutuksen ominaisuudet -sivu](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="bdcfb-134">Johdetun globalisaatiotoiminnon lisääminen</span><span class="sxs-lookup"><span data-stu-id="bdcfb-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="bdcfb-135">Voit lisätä uuden globalisaatiotoiminnon määrittämällä sen aiemmin julkaistusta tai jaetusta toiminnosta.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="bdcfb-136">Valitse **Tuo** avataksesi **Tuo toiminto yleisestä tietovarastosta**-sivun.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![Tuo toiminto yleiseltä tietovarastosivulta](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="bdcfb-138">Saat uusimmat ominaisuudet valitsemalla **Synkronoi**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="bdcfb-139">Synkronoidussa luettelossa on toimintoja, jotka ovat käytettävissä joko sen vuoksi, että Microsoft on julkaissut ne tai että toinen konfiguraatiotoimittaja on jakanut ne.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![Synkronoitu ominaisuuksien luettelo](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="bdcfb-141">Valitse tuotavat ominaisuudet luettelosta ja valitse sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="bdcfb-142">Näyttöön tulee sanoma, kun valittujen toimintojen tuominen onnistui.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![Sanoma onnistuneesta tuonnista](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="bdcfb-144">Valitse **Lisää** ja valitse sitten avattavasta valintaikkunasta **Aiemmin luodun version perusteella** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="bdcfb-145">Kirjoita ominaisuuden nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="bdcfb-146">Valitse käytettävissä olevien ominaisuuksien luettelosta ominaisuuden perusversio ja valitse sitten **Luo ominaisuus**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![Johdetun ominaisuuden lisääminen](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="bdcfb-148">Lisäämäsi ominaisuus luodaan, ja sen tila on **Luonnos**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![Johdettu toiminto, jonka tila on luonnos](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="bdcfb-150">Tarkista ominaisuuksien osista, tarvitaanko päivityksiä:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="bdcfb-151">Tarkista konfiguraatiot, jos sinun on mukautettava sähköisen raportoinnin muotoja ja niiden sidontaa ominaisuusversion muotokartoituksilla.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="bdcfb-152">Tarkista asetukset, jos sinun on mukautettava **Toiminnot**-välilehteä, **Soveltuvuussäännöt**-välilehteä tai ominaisuusversion **Muuttujat**-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="bdcfb-153">Valitse **Versiot**-välilehdessä **Voimassa olon alkamispäivämäärä** ja kirjoita kuvaus, jos **Kuvaus**-kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="bdcfb-154">Viimeistele toiminto valitsemalla **Muuta tilaa**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="bdcfb-155">Valmiit toiminnot ovat käytettävissä tietyssä ympäristössä, jotta niitä voidaan käyttää globalisointipalveluissa tai ne voidaan julkaista yleiseen tietovarastoon.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="bdcfb-156">Ominaisuudet, joiden **Ominaisuusversion tilan** arvo on **julkaistu**, voidaan jakaa ulkoisten organisaatioiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="bdcfb-157">Uuden globalisaatiotoiminnon lisääminen</span><span class="sxs-lookup"><span data-stu-id="bdcfb-157">Add a new Globalization feature</span></span>

<span data-ttu-id="bdcfb-158">Voit lisätä uuden globalisaatiotoiminnon luomalla sen alusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="bdcfb-159">Valitse **Tuo toiminto yleisestä tietovarastosta** -sivulta **Lisää** ja valitse sitten avattavasta valintaikkunasta **Uusi ominaisuus** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="bdcfb-160">Kirjoita ominaisuuden nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="bdcfb-161">Valitse **Luo ominaisuus**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-161">Select **Create feature**.</span></span>

    ![Uuden ominaisuuden lisääminen](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="bdcfb-163">Valitse **Versiot**-välilehdestä **Voimaantulo**-päivämäärä ja suorita sitten toiminto valitsemalla **Muuta tilaa**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="bdcfb-164">Valmiit toiminnot ovat käytettävissä tietyssä ympäristössä, jotta niitä voidaan käyttää globalisointipalveluissa tai ne voidaan julkaista yleiseen tietovarastoon.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="bdcfb-165">Ominaisuudet, joiden **Ominaisuusversion tilan** arvo on **julkaistu**, voidaan jakaa ulkoisten organisaatioiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="bdcfb-166">Ominaisuuksien komponenttien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bdcfb-166">Feature component overview</span></span>

<span data-ttu-id="bdcfb-167">Globalisaatio-ominaisuuksilla on useita komponentteja:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-167">Globalization features have several components:</span></span>

- <span data-ttu-id="bdcfb-168">**Versio** – Tämä komponentti tukee ominaisuuksien elinkaaren hallintaa, ja sen avulla käyttäjät voivat hallita toiminnon eri versioiden tilaa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="bdcfb-169">**Kokoonpanot** – Tämän komponentin avulla käyttäjät voivat hallita, tarkastella ja muokata toisiinsa liittyviä ER-muotoja ja muotomäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="bdcfb-170">**Asetukset** – Tämän osan avulla voit hallita järjestelmän palveluiden, kuten sähköisen laskutuspalvelun käyttäjien hallintatoimintoja.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="bdcfb-171">Näin ollen se tukee viestintä- ja vastaussääntöjen joustavaa rakentamista.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="bdcfb-172">**Ympäristö** – Tämän komponentin avulla voit käyttää globalisointipalveluja, kuten sähköistä laskutuspalvelua, hallita ympäristöä, jossa toiminnon version asetuksia käytetään, ja myöntää käyttöoikeuden käyttäjille, joilla on oikeus käyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="bdcfb-173">**Organisaatiot** – Tämän osan avulla käyttäjät voivat jakaa ominaisuuden ulkoisten organisaatioiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="bdcfb-174">Ominaisuuskomponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="bdcfb-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="bdcfb-175">Versio ja tila</span><span class="sxs-lookup"><span data-stu-id="bdcfb-175">Version and status</span></span>

<span data-ttu-id="bdcfb-176">Version avulla hallitaan globalisointitoiminnon elinkaarta.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="bdcfb-177">Tilaa voi muuttaa **Versio**-välilehden **Tila**-kentässä. Käytettävissä ovat seuraavat tilat:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="bdcfb-178">**Vedos** – Ominaisuutta voi muokata vain, jos se on tässä tilassa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="bdcfb-179">**Valmis** – Toiminto ja kaikki siihen liittyvät komponentit on viimeistelty (valmis), eikä niitä voi muokata.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="bdcfb-180">**Julkaistu** – Ominaisuus ja kaikki siihen liittyvät komponentit on julkaistu yleisessä tietovarastossa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="bdcfb-181">**Jaettu** – Toiminto ja kaikki siihen liittyvät komponentit on jaettu ulkoisten organisaatioiden kanssa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="bdcfb-182">**Käytössä** – Ominaisuus ja kaikki siihen liittyvät komponentit on otettu käyttöön globalisointipalvelussa, kuten sähköisen laskutuksen palvelussa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="bdcfb-183">Toimintojen on siirryttävä peräkkäin joihinkin näistä tiloista.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="bdcfb-184">Näin ollen kaikki tilat eivät välttämättä ole käytettävissä kaikissa elinkaarivaiheissa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="bdcfb-185">Konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="bdcfb-185">Configurations</span></span>

<span data-ttu-id="bdcfb-186">Konfiguroinneissa ovat käytettävissä seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="bdcfb-187">**Näytä** – Tarkastele pohjana olevia ominaisuuskonfiguraatioita, jotka eivät vaadi päivitystä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="bdcfb-188">**Muokkaa** – Luo valitusta konfiguraatiosta luonnosversio, jotta voit muokata muotoa tai muotomääritystä muodon suunnittelijassa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="bdcfb-189">**Poista** – Poista valittu konfiguraatio ominaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="bdcfb-190">**Uudelleenkäytä** – Ominaisuuden uudelleenkäyttäminen.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="bdcfb-191">Lisätietoja on jäljempänä tämän ohjeaiheen kohdassa [Uudelleenkäytä johdettuja globalisointiominaisuuksia](#rebase).</span><span class="sxs-lookup"><span data-stu-id="bdcfb-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="bdcfb-192">Asetukset</span><span class="sxs-lookup"><span data-stu-id="bdcfb-192">Setups</span></span>

<span data-ttu-id="bdcfb-193">Ominaisuuksien asennuksissa ovat käytettävissä seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="bdcfb-194">**Lisää** – Luo uusi ominaisuusasetus.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="bdcfb-195">Tämä ominaisuusmääritys voidaan määrittää aiemmin luodusta toimintomäärityksestä tai siitä, että se luodaan tyhjästä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="bdcfb-196">**Poista** – Poista valitut ominaisuusmääritykset.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="bdcfb-197">**Näytä** – Tarkastele perusominaisuuksien asetuksia, jotka eivät edellytä muutoksia.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="bdcfb-198">**Muokkaa** – Luo, poista tai muokkaa ominaisuuksien asetusten kolmen pääkomponentin määritteitä:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="bdcfb-199">Toimenpiteet ja niiden parametrit</span><span class="sxs-lookup"><span data-stu-id="bdcfb-199">Actions and their parameters</span></span>
    - <span data-ttu-id="bdcfb-200">Soveltuvuussäännöt</span><span class="sxs-lookup"><span data-stu-id="bdcfb-200">Applicability rules</span></span>
    - <span data-ttu-id="bdcfb-201">Muuttujat</span><span class="sxs-lookup"><span data-stu-id="bdcfb-201">Variables</span></span>

![Ominaisuusversion asetussivu](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="bdcfb-203">Ympäristöt</span><span class="sxs-lookup"><span data-stu-id="bdcfb-203">Environments</span></span>

<span data-ttu-id="bdcfb-204">Ympäristöissä ovat käytettävissä seuraavat toiminnot:</span><span class="sxs-lookup"><span data-stu-id="bdcfb-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="bdcfb-205">**Ota käyttöön** – Jos kyseessä on valittu toimintoversio, valitse julkaistu ympäristö ja valitse **voimassa olon alkamispäivämäärä**, kun se on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="bdcfb-206">Lisätietoja on jäljempänä tämän ohjeaiheen kohdassa [Määritä ympäristöjä aktivointia varten](#configureenvironment).</span><span class="sxs-lookup"><span data-stu-id="bdcfb-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="bdcfb-207">**Peruuta** – Poista ominaisuusasetusten ympäristö.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="bdcfb-208">Organisaatiot</span><span class="sxs-lookup"><span data-stu-id="bdcfb-208">Organizations</span></span>

<span data-ttu-id="bdcfb-209">Voit jakaa globalisaatiotoiminnon ulkoisen organisaation kanssa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="bdcfb-210">**Valitse sähköisen laskutuksen ominaisuudet** -sivulla toiminto ja jaettava ominaisuusversio.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="bdcfb-211">Valitse **Organisaatiot**-välilehdestä **Jaa seuraavan kanssa** -vaihtoehto ja kirjoita sitten avattavaan valintaikkunaan organisaation toimialueen nimi.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="bdcfb-212">Valitse **Jaa**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-212">Select **Share**.</span></span>

    ![Ominaisuuden jakaminen organisaation kanssa.](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="bdcfb-214">Ominaisuus jaetaan valitun organisaation kanssa, ja se on kyseisen organisaation käytettävissä yleisessä säilössä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="bdcfb-215">Tällöin toiminto voidaan tuoda organisaation RCS-esiintymään tai Dynamics 365 Financeen niin, että sitä voidaan käyttää.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="bdcfb-216">Johdettujen globalisaatiotoimintojen pohjustaminen</span><span class="sxs-lookup"><span data-stu-id="bdcfb-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="bdcfb-217">Voit määrittää uudelleen johdetun globalisaatiotoiminnon uuteen tai päivitettyyn perustoiminnon versioon.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="bdcfb-218">Näin perusversiossa tapahtuneet muutokset voidaan päivittää automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="bdcfb-219">Alkuperäinen konfigurointipalvelu luo päivitetyn perusominaisuuden version, jonka jälkeen se julkaistaan tai jaetaan.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![Päivitetty perustoiminnon versio](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="bdcfb-221">Jos esimerkiksi haluat määrittää uudelleen luomasi ominaisuuden johdetun version, saat ensin toiminnon uusimman version tuomalla sen yleisestä tietovarastosta.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="bdcfb-222">Valitse **sähköisen laskutuksen ominaisuudet** -sivulla **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="bdcfb-223">Saat uusimmat ominaisuudet valitsemalla **Synkronoi**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="bdcfb-224">Valitse ominaisuusluettelosta tuotavat ominaisuudet ja valitse sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![Toiminnon uusimman version tuominen](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="bdcfb-226">Valitse ominaisuuksien luettelosta uudelleenperustoiminto.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="bdcfb-227">Luo luonnosversio valitsemalla **Versio**-välilehdestä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![Uusi luonnosversio on laadittu](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="bdcfb-229">Valitse **Pohjusta**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="bdcfb-230">Valitse **Pohjusta**-valintaikkunassa sen toiminnon uusin versio, johon haluat pohjustaa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![Pohjusta-valintaikkuna](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="bdcfb-232">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-232">Select **OK**.</span></span>
9. <span data-ttu-id="bdcfb-233">Tarkista ominaisuuden komponentit ja tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="bdcfb-234">Viimeistele pohjustettu toiminto valitsemalla **Muuta tilaa**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="bdcfb-235">Kun pohjustus on saatu valmiiksi, voit suorittaa lisätoimenpiteitä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="bdcfb-236">Voit esimerkiksi julkaista ominaisuuden ja määrittää sen käytettäviksi globalisointipalveluissa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![Toiminnon tila päivitetty valmiiksi](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="bdcfb-238">Ympäristöjen määrittäminen globalisaation ominaisuuksille</span><span class="sxs-lookup"><span data-stu-id="bdcfb-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="bdcfb-239">Globalisointipalveluiden käyttäjät voivat hallita ympäristöä niin, että ne määrittävät globalisointiominaisuuden ja myöntävät valtuutuksen muille käyttäjille, joilla on oikeus käyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="bdcfb-240">Valitse **globalisointitoiminnot**-työtila ja **Ympäristöt**-kohdan **sähköinen laskutus** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![Globalisointiominaisuudet -työtila](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="bdcfb-242">Valitse **Avainsäilöparametrit** ja luo Azure avainsäilön salaisuus valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="bdcfb-243">Kirjoita avainsäilön nimi ja kuvaus ja kirjoita sitten **Avainsäilön URI** -kenttään URL-osoite, joka yksilöi avainsäilöresurssin Azure-tietokannassa.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="bdcfb-244">Lisää sertifikaatti valitsemalla **sertifikaatit**-pikavälilehdessä **Lisää** ja kirjoita kunkin sertifikaatin nimi ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![Sertifikaatti lisätty](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="bdcfb-246">Luo uusi ympäristö valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="bdcfb-247">Kirjoita nimi, kuvaus ja jaetun käyttöoikeuden allekirjoituksen tunnussanoma, jota tallennus edellyttää.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="bdcfb-248">Lisää käyttäjä, jolla on oikeus käyttää tätä ympäristöä, valitsemalla **Käyttäjät**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="bdcfb-249">Kirjoita käyttäjän käyttäjätunnus ja sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="bdcfb-250">Voit lisätä muita käyttäjiä tekemällä kohtien 7 ja 8 toimet uudelleen.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="bdcfb-251">Julkaise ympäristö valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="bdcfb-251">Select **Publish** to publish the environment.</span></span>

    ![Julkaistu ympäristö](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]