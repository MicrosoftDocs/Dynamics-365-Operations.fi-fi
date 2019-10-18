---
title: RCS:n ja ER:n sovelluskohtaisten metatietojen valmisteleminen
description: Tässä ohjeaiheessa käsitellään Regulatory Configuration Servicen (RCS) ja sähköisen raportoinnin (ER) sovelluskohtaisten metatietojen valmistelua.
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c036eab38845db8427c447b27cce0be8048669fd
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248651"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a><span data-ttu-id="10c0c-103">RCS:n sovelluskohtaisten metatietojen valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="10c0c-103">Prepare application-specific metadata for RCS</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="10c0c-104">Tässä ohjeaiheessa on käytännön esimerkkejä seuraavista tehtävistä:</span><span class="sxs-lookup"><span data-stu-id="10c0c-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="10c0c-105">RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="10c0c-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="10c0c-106">Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla</span><span class="sxs-lookup"><span data-stu-id="10c0c-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="10c0c-107">Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla</span><span class="sxs-lookup"><span data-stu-id="10c0c-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="10c0c-108">RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="10c0c-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="10c0c-109">Seuraavassa menettelyssä osoitetaan, miten käyttäjä, jolla on **Järjestelmänvalvoja**- tai **Sähköisen raportoinnin kehittäjä** -rooli, voi luoda sähköisen raportoinnin ER-konfiguraation, jossa on sovelluksen metatietoja ja jolla suunnitellaan ER-mallin yhdistämismääritykset Regulatory Configuration Servicessä (RCS).</span><span class="sxs-lookup"><span data-stu-id="10c0c-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="10c0c-110">Tässä esimerkissä luodulla ER-näytemallin yhdistämismäärityksellä voidaan käyttää ulkomaankauppatapahtumia.</span><span class="sxs-lookup"><span data-stu-id="10c0c-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="10c0c-111">Tässä merkissä käytetään RCS:ää suunnittelemaan sellainen sovelluksen ER-ratkaisu, jolla luodaan ulkomaankaupan liiketoimintatoimialueen tietoja sisältäviä sähköisiä asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="10c0c-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="10c0c-112">Jos haluat määrittää ER-tietomallin ja tarvittavien tietojen lähteiden välisen määrityksen, sinulla on oltava sovelluksen metatietojen käyttöoikeus RCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="10c0c-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="10c0c-113">Tämän vuoksi ER-ratkaisun suunnittelun osana on määritettävä uusi ER-metatietokonfiguraatio, joka sisältää kaikki valitun liiketoimintatoimialueen ER-raporttien luontiin tällä hetkellä tarvittavat metatiedot.</span><span class="sxs-lookup"><span data-stu-id="10c0c-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="10c0c-114">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa missä tahansa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="10c0c-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="10c0c-115">Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="10c0c-116">Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="10c0c-117">Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) -menettely.</span><span class="sxs-lookup"><span data-stu-id="10c0c-117">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="10c0c-118">Valitse **Metatietojen konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="10c0c-119">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="10c0c-120">Anna avattavan luettelon **Nimi**-kentässä nimi.</span><span class="sxs-lookup"><span data-stu-id="10c0c-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="10c0c-121">Kirjoita tässä esimerkissä **Ulkomaankaupan metatiedot**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="10c0c-122">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="10c0c-123">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-123">Select **Designer**.</span></span>
8. <span data-ttu-id="10c0c-124">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10c0c-125">Voit valita joko koko sovelluksen tai valittujen mallien tai moduulien kaikki metatiedot.</span><span class="sxs-lookup"><span data-stu-id="10c0c-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="10c0c-126">Muista kummassakin tapauksessa, että seuraavat metatiedot lisätään automaattisesti: tietue-, luettelo- ja laajennetut tietotyyppi (EDT) -taulut.</span><span class="sxs-lookup"><span data-stu-id="10c0c-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="10c0c-127">Jos muita metatietoja tarvitaan, ne on lisättävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="10c0c-127">When additional types of metadata are required, they must be manually added.</span></span>

<span data-ttu-id="10c0c-128">Ulkomaankauppatapahtumiin liittyvät metatiedot on lisättävä ja metatietonimikkeen on valittava manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="10c0c-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="10c0c-129">Valitse **Lisää tietolähde \> Taulukkotietueet**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="10c0c-130">Suodata **Nimi**-kentän **Intrastat**-arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="10c0c-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="10c0c-131">Valitse **Intrastat**-taulukkotietue.</span><span class="sxs-lookup"><span data-stu-id="10c0c-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="10c0c-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-132">Select **OK**.</span></span>

<span data-ttu-id="10c0c-133">Intrastat-taulukkotietueen metatiedot on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="10c0c-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="10c0c-134">Valitse puussa **Taulukkotietueet Intrastat \> \>Suhteet\> IntrastatCommodity (Taulukkotietueet EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="10c0c-135">Valitse **Lisää metatiedot**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10c0c-136">Valitun taulukkotietueen pakollisten suhteiden metatiedot on lisättävä manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="10c0c-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="10c0c-137">Valitse **Lisää tietolähde**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="10c0c-138">Valitse **Luettelointi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="10c0c-139">Suodata **Nimi**-kentän **IntrastatDirection**-arvon mukaan.</span><span class="sxs-lookup"><span data-stu-id="10c0c-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="10c0c-140">Valitse **IntrastatDirection**-luettelointitietue.</span><span class="sxs-lookup"><span data-stu-id="10c0c-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="10c0c-141">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-141">Select **OK**.</span></span>
20. <span data-ttu-id="10c0c-142">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-142">Select **Save**.</span></span>
21. <span data-ttu-id="10c0c-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="10c0c-143">Close the page.</span></span>
22. <span data-ttu-id="10c0c-144">Viimeistele metatietokonfiguraation luonnosversio:</span><span class="sxs-lookup"><span data-stu-id="10c0c-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="10c0c-145">Valitse **Muutoksen tila \> Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="10c0c-146">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-146">Select **OK**.</span></span>
    3. <span data-ttu-id="10c0c-147">Valitse valmis versio 1.</span><span class="sxs-lookup"><span data-stu-id="10c0c-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="10c0c-148">Vie metatietokonfiguraation valmis versio sovelluksesta XML-tiedostona:</span><span class="sxs-lookup"><span data-stu-id="10c0c-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="10c0c-149">Valitse **Vaihto \> Vie XML-tiedostona**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="10c0c-150">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-150">Select **OK**.</span></span>

<span data-ttu-id="10c0c-151">Luotu ER-metatietokonfiguraatio tallennetaan **Ulkomaankaupan metatiedot.xml** -tiedostona.</span><span class="sxs-lookup"><span data-stu-id="10c0c-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="10c0c-152">Voit nyt tuoda sen RCS:ään käytettäväksi ulkomaankaupan liiketoimintatoimialueen metatietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="10c0c-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="10c0c-153">Voit määrittää näiden tietojen perusteella sovelluksen metatietojen ja ER-tietomallin välisen yhdistämismäärityksen.</span><span class="sxs-lookup"><span data-stu-id="10c0c-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="10c0c-154">Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla</span><span class="sxs-lookup"><span data-stu-id="10c0c-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="10c0c-155">Seuraava menettely näyttää, miten RCS-käyttäjä, jolla on **Järjestelmänvalvoja**- tai **Sähköisen raportoinnin kehittäjä** -rooli, voi suunnitella uuden ER-mallin yhdistämismäärityksen käyttämällä sovelluksen metatietoja.</span><span class="sxs-lookup"><span data-stu-id="10c0c-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="10c0c-156">Sovelluksen metatietoja käytetään ER-metatietokonfiguraatiolla, joka sisältää ulkomaankauppatapahtumien käyttöön tarkoitetun metatietojen näytejoukon.</span><span class="sxs-lookup"><span data-stu-id="10c0c-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="10c0c-157">Ennen kuin suoritat tämän menettelyn, seuraava menettely on viimeisteltävä ensin.</span><span class="sxs-lookup"><span data-stu-id="10c0c-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="10c0c-158">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi</span><span class="sxs-lookup"><span data-stu-id="10c0c-158">Create a configuration provider and mark it as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="10c0c-159">RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen</span><span class="sxs-lookup"><span data-stu-id="10c0c-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="10c0c-160">Valitse **Kaikki työtilat \> Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="10c0c-161">Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="10c0c-162">Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) -menettely.</span><span class="sxs-lookup"><span data-stu-id="10c0c-162">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="10c0c-163">Tuo metatiedot sisältävä sovelluksen ER-metatietokonfiguraatio, joka on määritetty luomaan sähköisiä ulkomaankaupan liiketoimintatoimialueen asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="10c0c-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="10c0c-164">Loit tämän ER-metatietokonfiguraation ja veit sen XML-tiedostona [RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen](#prepare-application-metadata-that-can-be-used-in-rcs) -menettelynä aiemmin tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="10c0c-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="10c0c-165">Valitse **Metatietojen konfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="10c0c-166">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="10c0c-167">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="10c0c-168">Selaa **Ulkomaankaupan metatiedot.xml** -tiedostoon ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="10c0c-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="10c0c-169">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-169">Select **OK**.</span></span>
    6. <span data-ttu-id="10c0c-170">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="10c0c-170">Close the page.</span></span>

4. <span data-ttu-id="10c0c-171">Luo tietomallin konfiguraatio:</span><span class="sxs-lookup"><span data-stu-id="10c0c-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="10c0c-172">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="10c0c-173">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="10c0c-174">Kirjoita avattavan luettelon **Nimi**-kenttään **Ulkomaankauppamalli**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="10c0c-175">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="10c0c-176">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="10c0c-177">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="10c0c-178">Kirjoita **Nimi**-kenttään **Juuri**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="10c0c-179">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="10c0c-180">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="10c0c-181">Kirjoita **Nimi**-kenttään **Tapahtuma**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="10c0c-182">Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="10c0c-183">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="10c0c-184">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="10c0c-185">Kirjoita **Nimi**-kenttään **Kauppatavarakoodi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="10c0c-186">Valitse **Nimiketyyppi**-kentässä **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="10c0c-187">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-187">Select **Add**.</span></span>

    9. <span data-ttu-id="10c0c-188">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="10c0c-189">Kirjoita Nimi-kenttään **Laskutettu summa**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="10c0c-190">Valitse **Nimiketyyppi**-kentässä **Reaaliluku**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="10c0c-191">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-191">Select **Add**.</span></span>

    10. <span data-ttu-id="10c0c-192">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="10c0c-193">Kirjoita **Nimi**-kenttään **Päivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="10c0c-194">Valitse **Nimiketyyppi**-kentässä **Päivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="10c0c-195">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="10c0c-196">Valitse **Lisää \> Juuriviite**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="10c0c-197">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-197">Select **OK**.</span></span>
    13. <span data-ttu-id="10c0c-198">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-198">Select **Save**.</span></span>
    14. <span data-ttu-id="10c0c-199">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="10c0c-199">Close the page.</span></span>
    15. <span data-ttu-id="10c0c-200">Valitse **Muutoksen tila \> Viimeistele**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="10c0c-201">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-201">Select **OK**.</span></span>

5. <span data-ttu-id="10c0c-202">Luo mallin yhdistämismääritys:</span><span class="sxs-lookup"><span data-stu-id="10c0c-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="10c0c-203">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="10c0c-204">Kirjoita avattavan luettelon **Nimi**-kenttään **Mallin yhdistämismääritys perustuu tietomallin ulkomaankauppamalliin**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="10c0c-205">Kirjoita **Nimi**-kenttään **Ulkomaankaupan yhdistäminen**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="10c0c-206">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="10c0c-207">Valitse **Edellytykset**-pikavälilehdessä **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="10c0c-208">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-208">Select **New**.</span></span>
    7. <span data-ttu-id="10c0c-209">Valitse **Edellytysosan tyyppi** -kentässä **Konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="10c0c-210">Valitse **Ulkomaankaupan metatiedot** -määritys.</span><span class="sxs-lookup"><span data-stu-id="10c0c-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="10c0c-211">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-211">Select **Save**.</span></span> <span data-ttu-id="10c0c-212">Huomautus viitteen lisäämisestä **Ulkomaankaupan metatiedot** -määrityksen versioon 1.</span><span class="sxs-lookup"><span data-stu-id="10c0c-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="10c0c-213">Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan.</span><span class="sxs-lookup"><span data-stu-id="10c0c-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="10c0c-214">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="10c0c-214">Close the page.</span></span>
    11. <span data-ttu-id="10c0c-215">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="10c0c-216">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="10c0c-217">Valitse puussa **Dynamics 365 for Operations \> Taulukkotietueet**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="10c0c-218">Valitse **Lisää pääkansio**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="10c0c-219">Kirjoita **Nimi**-kenttään **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="10c0c-220">Valitse **Intrastat**-taulukkotietueet.</span><span class="sxs-lookup"><span data-stu-id="10c0c-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="10c0c-221">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="10c0c-222">Valittavana on vain kaksi taulukkoa, sillä tällä hetkellä käytössä olevaan metatietosarjaan lisättiin vain kaksi taulukkoa.</span><span class="sxs-lookup"><span data-stu-id="10c0c-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="10c0c-223">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="10c0c-224">Valitse puussa **Intrastat \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="10c0c-225">Valitse puussa **Tapahtuma = Intrastat \> Laskutettu summa**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="10c0c-226">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="10c0c-227">Valitse puussa **Intrastat \> TransDate**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="10c0c-228">Valitse puussa **Tapahtuma = Intrastat \> Date**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="10c0c-229">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="10c0c-230">Valitse puussa **Intrastat \> \>Suhteet \> IntrastatCommodity \> Koodi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="10c0c-231">Valitse puussa **Tapahtuma = Intrastat \> Kauppatavarakoodi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="10c0c-232">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="10c0c-233">Valitse **Tarkista**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="10c0c-234">Kun tarkistus on valmis, tietomallin elementtien ja kuvattujen nimikkeiden tietolähteiden sitominen onnistui käyttämällä sovelluksen tietoja viitatuista ER-metatietokonfiguraatiosta.</span><span class="sxs-lookup"><span data-stu-id="10c0c-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="10c0c-235">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-235">Select **Save**.</span></span>

<span data-ttu-id="10c0c-236">Voit tarvittaessa laajentaa aiemmin luotua metatietojoukkoa sovelluksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="10c0c-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="10c0c-237">Voit sitten viedä uuden täydellisen ER-metatietokonfiguraation version, tuoda sen RCS:een ja päivittää tuodun metatietokonfiguraation uuteen versioon viittaavan määritetyn mallin yhdistämiskonfiguraation edellytykset.</span><span class="sxs-lookup"><span data-stu-id="10c0c-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="10c0c-238">Tietojen hankkiminen sovelluksen metatiedoista tällä tavoin on käytettävissä vain paikallisesti käyttöönotetuissa sovelluksissa (kun liiketoimintatietojen paikallista \[LBD\] käyttöönottomallia käytetään sovelluksessa).</span><span class="sxs-lookup"><span data-stu-id="10c0c-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="10c0c-239">Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla</span><span class="sxs-lookup"><span data-stu-id="10c0c-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="10c0c-240">Seuraava menettely näyttää, miten RCS-käyttäjä, jolla on **Järjestelmänvalvoja**- tai **Sähköisen raportoinnin kehittäjä** -rooli, voi suunnitella uuden ER-mallin yhdistämismäärityksen käyttämällä sovelluksen metatietoja.</span><span class="sxs-lookup"><span data-stu-id="10c0c-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="10c0c-241">Sovelluksen metatietoja käytetään verkossa RCS:n yhdistetyllä sovelluksella.</span><span class="sxs-lookup"><span data-stu-id="10c0c-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="10c0c-242">ER-näytemallin yhdistäminen määritetään käyttämään ulkomaankauppatapahtumia.</span><span class="sxs-lookup"><span data-stu-id="10c0c-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="10c0c-243">[Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet on suoritettava ennen tämän menettelyn suorittamista RCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="10c0c-243">To complete this procedure, you must first complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="10c0c-244">Jos et ole vielä viimeistellyt [Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla](#access-application-metadata-by-using-an-er-configuration) -menettelyä aiemmin tässä ohjeaiheessa, siirry [Dynamics 365 for Finance and Operations 8.1:n sähköisen raportoinnin tehtäväoppaat](https://go.microsoft.com/fwlink/?linkid=2082739) -sivulle ja lataa seuraavat ER-konfiguraatiotiedostot etukäteen ja tallenna ne paikallisesti: **Ulkomaankaupan metatiedot.xml**, **Ulkomaankauppamalli.xml** ja **Ulkomaankaupan yhdistäminen.xml**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="10c0c-245">Tarvittavien ER-konfiguraatioiden hankkiminen</span><span class="sxs-lookup"><span data-stu-id="10c0c-245">Get required ER configurations</span></span>

<span data-ttu-id="10c0c-246">Jos olet jo suorittanut [Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla](#access-application-metadata-by-using-an-er-configuration) -menettelyn aiemmin tässä vaiheessa, sinulla on jo tarvittavat nykyisen RCS-esiintymän ER-määritykset (ulkomaankaupan metatietojen, mallin ja yhdistämisen määritykset).</span><span class="sxs-lookup"><span data-stu-id="10c0c-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="10c0c-247">Voit siinä tapauksessa ohittaa tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="10c0c-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="10c0c-248">Valitse **Kaikki työtilat \> Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="10c0c-249">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="10c0c-250">Lataa **Ulkomaankaupan metatiedot.xml**-, **Ulkomaankauppamalli.xml**- ja **Ulkomaankaupan yhdistäminen.xml** -määritystiedostot toistamalla seuraavat peräkkäiset vaiheet kunkin kohdalla:</span><span class="sxs-lookup"><span data-stu-id="10c0c-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="10c0c-251">Valitse **Vaihto**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="10c0c-252">Valitse **Lataa XML-tiedostosta**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="10c0c-253">Valitse ensin **Selaa** ja sitten tiedosto.</span><span class="sxs-lookup"><span data-stu-id="10c0c-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="10c0c-254">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="10c0c-255">Rekisteröi yhteys sovellukseen</span><span class="sxs-lookup"><span data-stu-id="10c0c-255">Register the connection with the application</span></span>

1. <span data-ttu-id="10c0c-256">Valitse **Kaikki työtilat \> Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="10c0c-257">Valitse **Yhdistetyt sovellukset**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="10c0c-258">Varmista, että määritetty sovellus perustuu Microsoft Azureen ja että se on yleisesti RCS-käyttäjien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="10c0c-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="10c0c-259">Nykyisellä RCS-käyttäjällä on oltava valitun sovelluksen käyttöoikeus ja hänen on oltava rekisteröitynyt sovelluksen käyttäjäksi roolilla, jolla voi käyttää sovelluksen metatietoja.</span><span class="sxs-lookup"><span data-stu-id="10c0c-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="10c0c-260">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-260">Select **New**.</span></span>
5. <span data-ttu-id="10c0c-261">Kirjoita **Nimi**-kenttään **MyConnectedApp** yhdistetyn sovelluksen nimeksi.</span><span class="sxs-lookup"><span data-stu-id="10c0c-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="10c0c-262">Määritä sovelluksen URL-osoite **Sovellus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="10c0c-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="10c0c-263">Määritä sovelluksen toimittaja **Vuokraaja**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="10c0c-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="10c0c-264">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-264">Select **Save**.</span></span> 
9. <span data-ttu-id="10c0c-265">Voit tarkistaa yhteyden määritettyyn sovellukseen valitsemalla **Yhdistä etäsovellukseen** -sivulla **Muodosta yhteys etäsovellukseen valitsemalla tämä** -linkki.</span><span class="sxs-lookup"><span data-stu-id="10c0c-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="10c0c-266">Tarkista määritetyn sovelluksen käyttöoikeus valitsemalla **Tarkista yhteys**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="10c0c-267">Valitse **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-267">Select **Close**.</span></span>

<span data-ttu-id="10c0c-268">Kun olet suorittanut tämän menettelyn ja yhteyden tarkistus onnistuu, nykyisen ruudukon määritetyn sovelluksen version ja vuokraajan tiedot päivitetään.</span><span class="sxs-lookup"><span data-stu-id="10c0c-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="10c0c-269">Aiemmin määritetyn mallin yhdistämismäärityksen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="10c0c-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="10c0c-270">Valitse **Kaikki työtilat \> Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="10c0c-271">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="10c0c-272">Valitse puussa **Ulkomaankauppamalli \> Ulkomaankaupan yhdistäminen**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="10c0c-273">Valitse **Edellytykset**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="10c0c-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10c0c-274">Tällä hetkellä yhdistämismääritys viittaa metatietomääritykseen.</span><span class="sxs-lookup"><span data-stu-id="10c0c-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="10c0c-275">Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan.</span><span class="sxs-lookup"><span data-stu-id="10c0c-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="10c0c-276">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-276">Select **Designer**.</span></span>
5. <span data-ttu-id="10c0c-277">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-277">Select **Designer**.</span></span>
6. <span data-ttu-id="10c0c-278">Valitse puussa **Dynamics 365 for Operations \> Taulukkotietueet**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="10c0c-279">Valitse **Lisää pääkansio**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-279">Select **Add root**.</span></span>
8. <span data-ttu-id="10c0c-280">Anna tai valitse **Taulu**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="10c0c-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10c0c-281">Tällä hetkellä yhdistämismääritys viittaa metatietomääritykseen.</span><span class="sxs-lookup"><span data-stu-id="10c0c-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="10c0c-282">Tämän konfiguraation sovelluksen metatiedot ovat käytettävissä, kun mallin yhdistämistä suunnitellaan.</span><span class="sxs-lookup"><span data-stu-id="10c0c-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="10c0c-283">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="10c0c-284">Yhdistetyn sovelluksen määrittäminen mallin yhdistämiseen</span><span class="sxs-lookup"><span data-stu-id="10c0c-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="10c0c-285">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-285">Select **Edit**.</span></span>
2. <span data-ttu-id="10c0c-286">Valitse **Yhdistetty sovellus** -kentässä **MyConnectedApp**-sovellus.</span><span class="sxs-lookup"><span data-stu-id="10c0c-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10c0c-287">Tämä yhdistämismääritys viittaa valitun yhdistetyn sovelluksen metatietoihin.</span><span class="sxs-lookup"><span data-stu-id="10c0c-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="10c0c-288">Jos yhdistämismääritys viittaa samanaikaisesti metatietojen määritykseen ja yhdistettyyn sovellukseen, yhdistetyn sovelluksen metatietoja käytetään.</span><span class="sxs-lookup"><span data-stu-id="10c0c-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="10c0c-289">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-289">Select **Designer**.</span></span>
4. <span data-ttu-id="10c0c-290">Valitse **Suunnittelu**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-290">Select **Designer**.</span></span>
5. <span data-ttu-id="10c0c-291">Valitse puussa **Dynamics 365 for Operations \> Taulukkotietueet**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="10c0c-292">Valitse **Lisää pääkansio**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-292">Select **Add root**.</span></span>
7. <span data-ttu-id="10c0c-293">Anna tai valitse **Taulu**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="10c0c-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="10c0c-294">Tällä hetkellä valittavana on nyt enemmän kuin kaksi sovellustaulukkoa, sillä tämä yhdistämismääritys käyttää siihen määritetyn yhdistetyn sovelluksen kaikkia metatietoja.</span><span class="sxs-lookup"><span data-stu-id="10c0c-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="10c0c-295">Valitse **Peruuta**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="10c0c-296">Valitse **Tarkista**.</span><span class="sxs-lookup"><span data-stu-id="10c0c-296">Select **Validate**.</span></span>

<span data-ttu-id="10c0c-297">Tietomallin elementtien ja kuvattujen nimikkeiden tietolähteiden sitominen onnistui käyttämällä tähän yhdistämismääritykseen määritetyn yhdistetyn sovelluksen metatietoja.</span><span class="sxs-lookup"><span data-stu-id="10c0c-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="10c0c-298">Kun tämä malli on arvioitava käyttämällä toisen version sovelluksen metatietoja, rekisteröi toinen yhdistetty sovellus, määritä se tähän mallin yhdistämismääritykseen ja vahvista se käyttämällä uusia metatietoja.</span><span class="sxs-lookup"><span data-stu-id="10c0c-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10c0c-299">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="10c0c-299">Additional resources</span></span>

<span data-ttu-id="10c0c-300">Vaihtoehtoisesti voit toistaa **RSC:ssä käytettävien sovelluksen metatietojen valmisteleminen** -tehtäväoppaan sovelluksessa sekä **Sovelluksen metatietojen käyttäminen ER-konfiguraation avulla**- ja **Sovelluksen metatietojen käyttäminen yhdistetyillä sovelluksilla** -tehtäväoppaat RCS:ssä.</span><span class="sxs-lookup"><span data-stu-id="10c0c-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="10c0c-301">Tehtäväoppaat voidaan ladata [Dynamics 365 for Finance and Operations 8.1:n sähköisen raportoinnin tehtäväoppaat](https://go.microsoft.com/fwlink/?linkid=2082739) -sivulla.</span><span class="sxs-lookup"><span data-stu-id="10c0c-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
