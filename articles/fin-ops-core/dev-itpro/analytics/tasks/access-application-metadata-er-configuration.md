---
title: Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla
description: Tämän aiheessa käsitellään, miten Regulatory Configuration Servicen käyttäjä voi suunnitella uuden sähköisen raportoinnin mallin käyttämällä metatietoja.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c50047781fdc21c9157ceb634822c6cfb5a075
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559648"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="73f9c-103">Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla</span><span class="sxs-lookup"><span data-stu-id="73f9c-103">Access application metadata by using ER configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="73f9c-104">Seuraavissa vaiheissa selitetään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava Regulatory Configuration Service (RCS) -käyttäjä voi suunnitella uuden sähköisen raportoinnin ER-mallin yhdistämisen sovelluksen metatietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="73f9c-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="73f9c-105">Sovelluksen metatietoja käytetään ER-metatietokonfiguraatiolla, joka sisältää ulkomaankauppatapahtumien käyttöön tarkoitetun metatietojen näytejoukon.</span><span class="sxs-lookup"><span data-stu-id="73f9c-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="73f9c-106">Näitä varten RCS-sovelluksessa on ensin suoritettava aiheessa [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="73f9c-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="73f9c-107">Seuraavaksi on suoritettava vaiheet, jotka on käsitelty aiheessa [RCS:ssä käytettävien sovelluksen metatietojen valmistelu](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="73f9c-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="73f9c-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="73f9c-108">Prerequisites</span></span>
1. <span data-ttu-id="73f9c-109">Valitse **Kaikki työtilat** > **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="73f9c-110">Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="73f9c-111">Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="73f9c-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="73f9c-112">Metatietokonfiguraation tuominen</span><span class="sxs-lookup"><span data-stu-id="73f9c-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="73f9c-113">Valitse **metatietojen konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="73f9c-114">Tuo metatiedot sisältävä ER-metatietokonfiguraatio, joka on määritetty luomaan sähköisiä ulkomaankaupan asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="73f9c-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="73f9c-115">Tämä ER-metatietokonfiguraatio on viety XML-tiedostona samalla, kun toimenpiteen [Sovelluksen metatietojen valmisteleminen RCS:ssä käytettäviksi](prepare-application-metadata-rcs.md) vaiheita suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="73f9c-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="73f9c-116">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="73f9c-117">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="73f9c-118">Valitse ensin **Selaa** ja sitten Ulkomaankaupan metatiedot.xml-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="73f9c-118">Click **Browse** and select the 'Foreign trade metadata.xml' file.</span></span> 
6. <span data-ttu-id="73f9c-119">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-119">Click **OK**.</span></span> 
7. <span data-ttu-id="73f9c-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="73f9c-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="73f9c-121">Tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="73f9c-121">Create data model configuration</span></span>
1. <span data-ttu-id="73f9c-122">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="73f9c-123">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="73f9c-124">Kirjoita **Nimi**-kenttään Ulkomaankauppamalli.</span><span class="sxs-lookup"><span data-stu-id="73f9c-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="73f9c-125">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="73f9c-126">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="73f9c-127">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="73f9c-128">Kirjoita **Nimi**-kenttään Juuri.</span><span class="sxs-lookup"><span data-stu-id="73f9c-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="73f9c-129">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-129">Click **Add**.</span></span> 
9. <span data-ttu-id="73f9c-130">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-130">Click **New** to open the drop dialog.</span></span> 
10.    <span data-ttu-id="73f9c-131">Kirjoita **Nimi**-kenttään Tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="73f9c-131">In the **Name** field, type 'Transaction'.</span></span> 
11.    <span data-ttu-id="73f9c-132">Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-132">In the **Item type** field, select **Record list**.</span></span> 
12.    <span data-ttu-id="73f9c-133">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-133">Click **Add**.</span></span> 
13.    <span data-ttu-id="73f9c-134">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-134">Click **New** to open the drop dialog.</span></span> 
14.    <span data-ttu-id="73f9c-135">Kirjoita **Nimi**-kenttään Kauppatavarakoodi.</span><span class="sxs-lookup"><span data-stu-id="73f9c-135">In the **Name** field, type 'Commodity code'.</span></span> 
15.    <span data-ttu-id="73f9c-136">Valitse **Nimiketyyppi**-kentässä **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-136">In the **Item type** field, select **String**.</span></span> 
16.    <span data-ttu-id="73f9c-137">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-137">Click **Add**.</span></span> 
17.    <span data-ttu-id="73f9c-138">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-138">Click **New** to open the drop dialog.</span></span> 
18.    <span data-ttu-id="73f9c-139">Kirjoita **Nimi**-kenttään Laskutettu summa.</span><span class="sxs-lookup"><span data-stu-id="73f9c-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19.    <span data-ttu-id="73f9c-140">Valitse **Nimiketyyppi**-kentässä **Reaaliluku**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-140">In the **Item type** field, select **Real**.</span></span> 
20.    <span data-ttu-id="73f9c-141">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-141">Click **Add**.</span></span> 
21.    <span data-ttu-id="73f9c-142">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-142">Click **New** to open the drop dialog.</span></span> 
22.    <span data-ttu-id="73f9c-143">Kirjoita **Nimi**-kenttään Päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="73f9c-143">In the **Name** field, type 'Date'.</span></span> 
23.    <span data-ttu-id="73f9c-144">Valitse **Nimiketyyppi**-kentässä **Päivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-144">In the **Item type** field, select **Date**.</span></span> 
24.    <span data-ttu-id="73f9c-145">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-145">Click **Add**.</span></span> 
25.    <span data-ttu-id="73f9c-146">Valitse **Juuriviite**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-146">Click **Root reference**.</span></span> 
26.    <span data-ttu-id="73f9c-147">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-147">Click **OK**.</span></span> 
27.    <span data-ttu-id="73f9c-148">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-148">Click **Save**.</span></span> 
28.    <span data-ttu-id="73f9c-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="73f9c-149">Close the page.</span></span> 
29.    <span data-ttu-id="73f9c-150">Valitse **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-150">Click **Change status**.</span></span> 
30.    <span data-ttu-id="73f9c-151">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-151">Click **Complete**.</span></span> 
31.    <span data-ttu-id="73f9c-152">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="73f9c-153">Mallin yhdistämismäärityksen luominen</span><span class="sxs-lookup"><span data-stu-id="73f9c-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="73f9c-154">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="73f9c-155">Anna **Uusi**-kenttään Mallin yhdistämismääritys perustuu tietomallin ulkomaankauppamalliin.</span><span class="sxs-lookup"><span data-stu-id="73f9c-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="73f9c-156">Kirjoita **Nimi**-kenttään Ulkomaankaupan yhdistäminen.</span><span class="sxs-lookup"><span data-stu-id="73f9c-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="73f9c-157">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="73f9c-158">Laajenna **Edellytykset**-osa.</span><span class="sxs-lookup"><span data-stu-id="73f9c-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="73f9c-159">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="73f9c-160">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-160">Click **New**.</span></span> 
8. <span data-ttu-id="73f9c-161">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="73f9c-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="73f9c-162">Valitse **Edellytysosan tyyppi** -kentässä **Konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10.    <span data-ttu-id="73f9c-163">Valitse **Ulkomaankaupan metatiedot** -määritys.</span><span class="sxs-lookup"><span data-stu-id="73f9c-163">Select **Foreign trade metadata** configuration.</span></span> 
11.    <span data-ttu-id="73f9c-164">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-164">Click **Save**.</span></span> 
12.    <span data-ttu-id="73f9c-165">Ulkomaankaupan metatiedot -määrityksen versioon 1 lisättiin viite.</span><span class="sxs-lookup"><span data-stu-id="73f9c-165">We added the reference to the version 1 of the 'Foreign trade metadata' configuration.</span></span> <span data-ttu-id="73f9c-166">Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan.</span><span class="sxs-lookup"><span data-stu-id="73f9c-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13.    <span data-ttu-id="73f9c-167">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="73f9c-167">Close the page.</span></span> 
14.    <span data-ttu-id="73f9c-168">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-168">Click **Designer**.</span></span> 
15.    <span data-ttu-id="73f9c-169">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-169">Click **Designer**.</span></span> 
16.    <span data-ttu-id="73f9c-170">Valitse puussa **Dynamics 365 for Operations\Taulukon tietueet**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17.    <span data-ttu-id="73f9c-171">Valitse **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-171">Click **Add root**.</span></span> 
18.    <span data-ttu-id="73f9c-172">Kirjoita **Nimi**-kenttään Intrastat.</span><span class="sxs-lookup"><span data-stu-id="73f9c-172">In the **Name** field, type 'Intrastat'.</span></span> 
19.    <span data-ttu-id="73f9c-173">Valitse **Intrastat**-taulukkotietueet.</span><span class="sxs-lookup"><span data-stu-id="73f9c-173">Select **Intrastat** table records.</span></span> 
20.    <span data-ttu-id="73f9c-174">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="73f9c-175">Valittavana on vain kaksi taulukkoa, sillä tällä hetkellä käytössä olevaan metatietosarjaan lisättiin vain kaksi taulukkoa.</span><span class="sxs-lookup"><span data-stu-id="73f9c-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21.    <span data-ttu-id="73f9c-176">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-176">Click **Bind**.</span></span> 
22.    <span data-ttu-id="73f9c-177">Laajenna puussa **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-177">In the tree, expand **Intrastat**.</span></span> 
23.    <span data-ttu-id="73f9c-178">Valitse puussa **Intrastat\AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24.    <span data-ttu-id="73f9c-179">Laajenna puussa **Tapahtuma = Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25.    <span data-ttu-id="73f9c-180">Valitse puussa **Tapahtuma = Intrastat\Laskutettu summa**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26.    <span data-ttu-id="73f9c-181">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-181">Click **Bind**.</span></span> 
27.    <span data-ttu-id="73f9c-182">Valitse puussa **Intrastat\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28.    <span data-ttu-id="73f9c-183">Valitse puussa **Tapahtuma = Intrastat\Date**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29.    <span data-ttu-id="73f9c-184">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-184">Click **Bind**.</span></span> 
30.    <span data-ttu-id="73f9c-185">Laajenna puussa **Intrastat\>Suhteet**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31.    <span data-ttu-id="73f9c-186">Laajenna puussa **Intrastat\>Relations\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32.    <span data-ttu-id="73f9c-187">Valitse puussa **Intrastat\>Relations\IntrastatCommodity\Code**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33.    <span data-ttu-id="73f9c-188">Valitse puussa **Tapahtuma = Intrastat\Kauppatavarakoodi**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34.    <span data-ttu-id="73f9c-189">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-189">Click **Bind**.</span></span> 
35.    <span data-ttu-id="73f9c-190">Valitse **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="73f9c-191">Tietomallin elementtien ja kuvattujen nimikkeiden tietolähteiden sitominen onnistui käyttämällä sovelluksen tietoja viitatuista ER-metatietokonfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="73f9c-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36.    <span data-ttu-id="73f9c-192">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="73f9c-192">Click **Save**.</span></span> 
37.    <span data-ttu-id="73f9c-193">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="73f9c-193">Close the page.</span></span> 
38.    <span data-ttu-id="73f9c-194">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="73f9c-194">Close the page.</span></span> 
39.    <span data-ttu-id="73f9c-195">Laajenna aiemmin luotu metatietojoukko tarvittaessa ja vie sitten uusi ER-metatietomäärityksen valmis versio.</span><span class="sxs-lookup"><span data-stu-id="73f9c-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="73f9c-196">Voit sitten tuoda sen RCS:hen ja päivittää sellaisen määritetyn mallin yhdistämäärityksen edellytykset, jotka viittaavat tuodun metatietomäärityksen uuteen versioon.</span><span class="sxs-lookup"><span data-stu-id="73f9c-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="73f9c-197">Tietojen hankkiminen sovelluksen metatiedoista tällä tavoin on käytettävissä vain paikallisesti käyttöönotetuissa sovelluksissa (kun liiketoimintatietojen paikallista (LBD) käyttöönottomallia käytetään).</span><span class="sxs-lookup"><span data-stu-id="73f9c-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]