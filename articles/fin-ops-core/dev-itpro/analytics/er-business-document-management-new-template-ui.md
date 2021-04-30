---
title: Microsoft Office -tyylin käyttöliittymä liiketoiminta-asiakirjan hallinnassa
description: Tässä ohjeaiheessa kerrotaan, kuinka uutta käyttöliittymää käytetään sähköisen raportoinnin (ER) kehyksen yritysasiakirjojen hallintatoiminnossa.
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881033"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="2c6d4-103">Microsoft Office -tyylin käyttöliittymä liiketoiminta-asiakirjan hallinnassa</span><span class="sxs-lookup"><span data-stu-id="2c6d4-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c6d4-104">Liiketoiminta-asiakirjojen hallinnan avulla yrityskäyttäjät voivat muokata liiketoiminta-asiakirjamalleja Microsoft 365 -palvelun tai asianmukaisen Microsoft Office -työpöytäsovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="2c6d4-105">Muokkauksia voivat olla esimerkiksi suunnittelumuutoksia tai uusia käyttöönottoja. Käyttäjät voivat myös lisätä paikkamerkkejä tietojen lisäämiseksi ilman lähdekoodin muuttamista.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="2c6d4-106">Lisätietoja liiketoiminta-asiakirjojen hallinnan käyttämisestä on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="2c6d4-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="2c6d4-107">Uusi käyttöliittymä on selkeämpi ja mukavampi käyttää.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="2c6d4-108">**Liiketoiminta asiakirja** -alueella näkyvät vain ne mallit, jotka ovat käytettävissä kulloisenkin toimittajan osalta.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="2c6d4-109">Edellisessä käyttöliittymässä **Malli**-välilehdessä luetellaan kaikki mallit, jotka olivat kaikkien palveluntarjoajien käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="2c6d4-110">Lisäksi se on näyttänyt kaikki kaikkien niiden käyttäjien luomat ja muokatut mallit, joilla on sama rooli.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="2c6d4-111">Voit käyttää **Uusi asiakirja** -painiketta luodaksesi ja muokataksesi mallia sähköisen raportoinnin (ER) muotomäärityksessä, joka on peräisin toiselta toimittajalta.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="2c6d4-112">Tämän ohjeaiheen esimerkissä toimittaja on Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="2c6d4-113">Vaihtoehtoisesti voit luoda mallin lataamalla oman mallisi Excel-muodossa.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="2c6d4-114">[Luo uusi liiketoiminta-asiakirja käyttämällä edellä kuvattua Liiketoimintatiedostojen hallinta](https://youtu.be/gAIYl-mM_pw) -videoa (näkyy yllä) on lisätty [Finance and Operations -soittolistalle](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavilla YouTubessa.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="2c6d4-115">Uuden liiketoiminta-asiakirjojen hallinnan asiakirjojen käyttöliittymän käyttöön tarjoaminen</span><span class="sxs-lookup"><span data-stu-id="2c6d4-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="2c6d4-116">Aloittaaksesi uuden asiakirjojen käyttöliittymän käyttämisen liiketoiminta-asiakirjojen hallinnassa sinun on otettava **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -toiminto käyttöön **Ominaisuuksien hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="2c6d4-117">Noudata seuraavia ohjeita ottaaksesi tämän ominaisuuden käyttöön kaikille yrityksille.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="2c6d4-118">Valitse **Ominaisuuksien hallinta** -työtila **Kaikki** -välilehden luettelosta **Officea muistuttava käyttöliittymäkokemus liiketoiminta-asiakirjojen hallintaan** -ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="2c6d4-119">Ota valittu toiminto käyttöön valitsemalla **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="2c6d4-120">Voit avata uuden toiminnon päivittämällä sivun.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="2c6d4-121">Muokkaa muiden toimittajien omistamia malleja</span><span class="sxs-lookup"><span data-stu-id="2c6d4-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="2c6d4-122">Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![Liiketoiminta-asiakirjojen hallinnan työtila](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="2c6d4-124">Valitse **Valitse**-valintaruudussa mallina käytettävä asiakirja ja sitten **Luo tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![Liiketoiminta-asiakirjojen valintaruutu](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="2c6d4-126">Vaihda otsikkoa uuden valintaruudun **Otsikko**-kentässä tarpeesi mukaan.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="2c6d4-127">Otsikkotekstin avulla voit nimetä automaattisesti luotavan uuden ER-muotomäärityksen.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="2c6d4-128">Huomaa, että tämän määrityksen luonnosta (**Asiakkaan FTI-raportti (GER) Copy**), joka sisältää muokatun mallin, käytetään suorittamaan tämä ER-muoto nykyiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="2c6d4-129">ER-perusmuotomäärityksen alkuperäistä mallia käytetään tämän ER-muodon suorittamiseen kaikille muille käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="2c6d4-130">Vaihda **Nimi** -kenttään automaattisesti luotavan muokattavan mallin ensimmäisen version nimi.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="2c6d4-131">Päivitä huomautukset **Kommentti**-kenttään automaattisesti luotavan muokattavan mallin uuden version huomautukset.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="2c6d4-132">Vahvista muokkausprosessin aloittaminen valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![Tiedoston luonnin valintaruutu](./media/BDM_overview_new_template3.png)

<span data-ttu-id="2c6d4-134">**Uusi asiakirja** -painiketta käytetään luomaan ja muokkaamaan mallia toisen toimittajan toimittamassa ER-muotomäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="2c6d4-135">Tässä esimerkissä toimittajana on Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="2c6d4-136">Kun valitset **Uusi tiedosto**, näet kaikki nykyisen toimittajan tai muiden toimittajien omistamat mallit.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="2c6d4-137">Kun olet valinnut mallin, se avautuu muokattavaksi.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="2c6d4-138">Muokattu malli tallennetaan sen jälkeen uuteen ER-muotokonfiguraatioon, joka luodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="2c6d4-139">Aiemmin luotua Excel-muotoa käyttävän mallin lataaminen</span><span class="sxs-lookup"><span data-stu-id="2c6d4-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="2c6d4-140">Noudata näitä ohjeita, kun haluat antaa tarvittavat tiedot ennen mallin lataamista.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="2c6d4-141">Valitse **Liiketoiminta-asiakirjan hallinta** -työtilassa **Uusi asiakirja**.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![Liiketoiminta-asiakirjojen hallinnan työtila](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="2c6d4-143">Valitse **Luo uusi malli** -sivun **Palvelimeen lataaminen** -välilehden **Malli**-välilehdestä **Etsi selaamalla** ja valitse malliksi käytettävä Excel-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="2c6d4-144">**Malli**-osan **Otsikko**- ja **Kuvaus**-kentät täytetään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="2c6d4-145">Ne määrittävät uuden automaattisesti luotavan ER-muotokonfiguraation nimen ja kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="2c6d4-146">Voit muokata näitä kenttiä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="2c6d4-147">Määritä **Tiedostotyyppi**-osan **Nimi**-kenttään liiketoimintatiedoston tyyppi.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="2c6d4-148">Tätä arvoa käytetään oikean tietolähteen haussa (ER-mallin konfiguraatiossa).</span><span class="sxs-lookup"><span data-stu-id="2c6d4-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![Mallivälilehti](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="2c6d4-150">Valitse **Tietolähde**-välilehden **Suodatin**-pikavälilehdestä **Käytä suodatinta**.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="2c6d4-151">**Tietolähde**-osassa **Nimi**-kenttä täytetään automaattisesti. Voit myös valita arvon manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="2c6d4-152">Voit etsiä tietolähteen nimeä nimen, kuvauksen, maa-/aluekoodin ja liiketoimintatiedostotyypin perusteella suodattimen avulla.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![Tietolähde-välilehti](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="2c6d4-154">**Suodatin**-pikavälilehteä käytetään oikean tietolähteen haussa (ER-mallin konfiguraatiossa).</span><span class="sxs-lookup"><span data-stu-id="2c6d4-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="2c6d4-155">Voit etsiä lataatavalle tiedostolle sopivimman tietolähteen muokkaamalla kaikkia suodatinkenttiä.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="2c6d4-156">**Suodata**-pikavälilehden ehtoja käytetään **TAI**-ehtona.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="2c6d4-157">Valitse **Yhdistämismääritys**-välilehdessä **Automaattinen havainnointi**.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="2c6d4-158">**Juurimääritys**-kenttä täytetään automaattisesti. Voit myös valita arvon manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="2c6d4-159">Tässä välilehdessä näytetään mallin ja mallin elementtien lopetusmääritys.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![Määritys-välilehti](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="2c6d4-161">**Mallirakenne**-osan määrityksessä käytetään täysin tietolähteen otsikoita tai kuvauksia käyttäjän kielellä ja mallin matkapuhelinnimessä.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="2c6d4-162">Valitse **Luo tiedosto**, kun haluat vahvistaa, että haluat luoda mallin, ja aloittaa muokkausprosessin.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="2c6d4-163">Lisätietoja on kohdassa [Liiketoiminta-asiakirjojen hallinta – yleiskatsaus](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="2c6d4-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="2c6d4-164">Jos sähköisessä raportoinnissa ei ole toimittajaa, voit luoda sen.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="2c6d4-165">Jos aktiivista palveluntarjoajaa ei ole, voit aktivoida sen.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="2c6d4-166">Jos haluat luoda tarjoajan, muuta tarjoajan nimi **Nimi**-kentässä, päivitä uuden tarjoajan **Internet-osoite** kenttään ja vahvista valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![Uuden tarjoajan luominen BDM:ssä](./media/bdm_create_provider.png)
    
- <span data-ttu-id="2c6d4-168">Voit aktivoida aiemmin luodun tarjoajan valitsemalla **Konfigurointipalvelu**-kentästä tarjoajan nimen ja valitsemalla **OK**, jos haluat määrittää tarjoajan aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![Tarjoajan aktivoiminen BDM:ssä](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="2c6d4-170">Kunkin BDM-malli viittaa palveluntarjoajaan kokoonpanon tekijänä.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="2c6d4-171">Siksi mallissa tarvitaan aktiivista toimittajaa.</span><span class="sxs-lookup"><span data-stu-id="2c6d4-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
