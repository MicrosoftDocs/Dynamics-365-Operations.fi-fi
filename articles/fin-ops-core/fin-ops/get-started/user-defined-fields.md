---
title: Mukautettujen kenttien luominen ja käsitteleminen
description: Tässä ohjeaiheessa käsitellään sitä, miten mukautettuja kenttiä luodaan käyttöliittymässä sovelluksen muokkaamiseksi yrityksen tarpeita vastaaviksi.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: f689bb3ec844459d1dd6e199804a30f3e0cb38bc
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112333"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="d3538-103">Mukautettujen kenttien luominen ja käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="d3538-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3538-104">Vaikka käytettävissä on useita valmiita kenttiä monenlaisten liiketoimintaprosessien hallintaa varten, joskus yritysten on seurattava myös muita tietoja järjestelmässä.</span><span class="sxs-lookup"><span data-stu-id="d3538-104">While there is an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="d3538-105">Ohjelmoijia voidaan käyttää näiden kenttien lisäämisessä laajennuksina kehittäjän työkaluihin. Mukautettujen kenttien toiminnon avulla kentät voidaan lisätä suoraan käyttöliittymästä. Näin käyttäjä voi räätälöidä sovellusta liiketoiminnan vaatimusten mukaan selaimessa.</span><span class="sxs-lookup"><span data-stu-id="d3538-105">While programmers can be used to add those fields as extensions in the developer tools, the custom fields feature allows fields to be added directly from the user interface, thereby allowing you to tailor the application to fit your business using your web browser.</span></span>

<span data-ttu-id="d3538-106">Mukautettujen kenttien lisääminen on mahdollista päivityksestä 13 eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="d3538-106">The ability to add custom fields is available in platform update 13 and later.</span></span> <span data-ttu-id="d3538-107">Vain käyttäjät, joilla on erityiset käyttöoikeudet, voivat käyttää tätä ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="d3538-107">Only users with special permissions have access to this feature.</span></span>

<span data-ttu-id="d3538-108">Tässä videossa näytetään, miten helppoa mukautetun kentän lisääminen sivulle on: [Mukautettujen kenttien lisääminen](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="d3538-108">This video shows how easy it is to add a custom field to a page: [Adding custom fields](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="d3538-109">Mukautettujen kenttien luominen</span><span class="sxs-lookup"><span data-stu-id="d3538-109">Creating custom fields</span></span>

<span data-ttu-id="d3538-110">Kun olet tunnistanut tiedot, joita haluat seurata sovelluksessa, voit luoda mukautetun kentän soveltuvaan tauluun ja tuoda kyseisen uuden kentän näkyviin sivulle.</span><span class="sxs-lookup"><span data-stu-id="d3538-110">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="d3538-111">Seuraavissa ohjeissa käsitellään mukautetun kentän luontiprosessi ja kyseisen kentän sijoittaminen lomakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="d3538-111">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="d3538-112">Siirry lomakkeessa kohtaan, jossa uutta kenttää tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="d3538-112">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="d3538-113">Koska varsinaisena tavoitteena on tuoda mukautettu kenttä näkyviin lomakkeessa, mukautettujen kenttien luonnin aloituskohta on mukautuskokemuksessa.</span><span class="sxs-lookup"><span data-stu-id="d3538-113">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="d3538-114">Avaa mukauttamisen työkalurivi valitsemalla ensin **Asetukset** ja sitten **Mukauta tämä lomake**.</span><span class="sxs-lookup"><span data-stu-id="d3538-114">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="d3538-115">Valitse ensin **Lisää** ja sitten **Kenttä**.</span><span class="sxs-lookup"><span data-stu-id="d3538-115">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="d3538-116">Valitse lomakkeessa alue, jossa haluat uuden kentän näkyvän.</span><span class="sxs-lookup"><span data-stu-id="d3538-116">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="d3538-117">Valinnan jälkeen **Lisää kenttiä** -valintaikkunassa on luettelo aiemmin luoduista kentistä, jotka voidaan lisätä valitulle lomake-alueelle.</span><span class="sxs-lookup"><span data-stu-id="d3538-117">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="d3538-118">Varmista, että haluamasi kenttä ei ole jo luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d3538-118">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="d3538-119">Jos löydät sen, sinun tarvitsee vain valita ensin kenttä luettelossa ja valita sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="d3538-119">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="d3538-120">Käynnistä mukautetun kentän luontiprosessi valitsemalla luettelon yläpuolella **Luo uusi kenttä**.</span><span class="sxs-lookup"><span data-stu-id="d3538-120">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="d3538-121">**Luo uusi kenttä** -valintaikkuna avautuu.</span><span class="sxs-lookup"><span data-stu-id="d3538-121">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="d3538-122">Jos **Luo uusi kenttä** -painike ei ole näkyvissä, sinulla ei ole ominaisuuden käyttöön tarvittavia käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="d3538-122">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="d3538-123">Anna seuraavat tiedot **Luo uusi kenttä** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="d3538-123">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="d3538-124">Valitse tietokantataulu, johon tämä kenttä lisätään.</span><span class="sxs-lookup"><span data-stu-id="d3538-124">Select the database table where this field should be added.</span></span> <span data-ttu-id="d3538-125">Huomaa, että vain mukautettuja kenttiä tukevat taulut näkyvät avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d3538-125">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="d3538-126">Jäljempänä on tuettujen taulujen tekniset tiedot.</span><span class="sxs-lookup"><span data-stu-id="d3538-126">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="d3538-127">Valitse uuden kentän tietotyyppi.</span><span class="sxs-lookup"><span data-stu-id="d3538-127">Select the data type for the new field.</span></span> <span data-ttu-id="d3538-128">Valittavana on seuraavat tietotyypit: valintaruutu, päivämäärä, päivämäärä ja aika, desimaali, luku, valintaluettelo ja teksti.</span><span class="sxs-lookup"><span data-stu-id="d3538-128">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="d3538-129">Jos tietotyypiksi tekstin, voit määrittää myös kenttään annettavan tekstin enimmäispituuden.</span><span class="sxs-lookup"><span data-stu-id="d3538-129">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="d3538-130">Jos valitset tietotyypiksi valintaluettelon, voit valita myös arvot, joita kentässä saa käyttää.</span><span class="sxs-lookup"><span data-stu-id="d3538-130">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="d3538-131">Anna kentälle nimi, otsikko ja ohjeteksti.</span><span class="sxs-lookup"><span data-stu-id="d3538-131">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="d3538-132">Nimi vastaa tietokannan fyysistä kenttänimeä, kun taas otsikko ja ohjeteksti ovat kentän käyttöliittymässä käytettäviä tekstejä.</span><span class="sxs-lookup"><span data-stu-id="d3538-132">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="d3538-133">Jos tämä on ainoa tähän lomakkeeseen luotava kenttä, valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="d3538-133">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="d3538-134">Jos kenttiä on luotava lisää, valitse **Tallenna ja uusi** ja palaa vaiheeseen 7.</span><span class="sxs-lookup"><span data-stu-id="d3538-134">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="d3538-135">Huomaa, että tällä hetkellä **taulussa saa olla enintään 20 mukautettua kenttää**.</span><span class="sxs-lookup"><span data-stu-id="d3538-135">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="d3538-136">Kun poistut **Luo uusi kenttä** -valintaikkunassa, palaat **Lisää kenttiä** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="d3538-136">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="d3538-137">Juuri lisätyt mukautetut kentät merkitään kenttäluettelossa automaattisesti lomakkeeseen lisättäviksi.</span><span class="sxs-lookup"><span data-stu-id="d3538-137">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="d3538-138">Lisää merkityt kentät valitulle lomakealueelle valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="d3538-138">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="d3538-139">**Valinnainen:** Ota **Siirrä**-tila käyttöön mukauttamisen työkalurivillä, jos haluat siirtää uudet kentät paikalleen valitulle alueelle.</span><span class="sxs-lookup"><span data-stu-id="d3538-139">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="d3538-140">Kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md) on lisätietoja, miten erilaisten mukauttamistoimintojen avulla lomakkeen voi optimoida omaa käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="d3538-140">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="d3538-141">Mukautettujen kenttien jakaminen muiden käyttäjien kanssa</span><span class="sxs-lookup"><span data-stu-id="d3538-141">Sharing custom fields with other users</span></span>

<span data-ttu-id="d3538-142">Kun olet luonut mukautetun kentän ja se näkyy lomakkeessa, haluat ehkä tuoda uuden kentän sisältävän päivitetyn sivunäkymän muiden järjestelmän käyttäjien saataville.</span><span class="sxs-lookup"><span data-stu-id="d3538-142">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="d3538-143">Sen voi tehdä kahdella tavalla käyttämällä tuotteen mukauttamisominaisuuksia:</span><span class="sxs-lookup"><span data-stu-id="d3538-143">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="d3538-144">Suosituksena on pyytää järjestelmänvalvojaa toimittamaan mukautus kaikille käyttäjille tai osalle käyttäjiä.</span><span class="sxs-lookup"><span data-stu-id="d3538-144">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="d3538-145">Lisätietoja on kohdassa [Käyttäjäkokemuksen mukauttaminen](personalize-user-experience.md).</span><span class="sxs-lookup"><span data-stu-id="d3538-145">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="d3538-146">Vaihtoehtoisesti voit viedä muutokset (eli *mukautukset*), lähettää ne yhdelle tai usealle käyttäjälle ja pyytää heitä jokaista tuomaan muutokset.</span><span class="sxs-lookup"><span data-stu-id="d3538-146">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="d3538-147">Voit viedä ja tuoda mukautuksia mukauttamisen työkalurivin **Hallinta**-asetuksella.</span><span class="sxs-lookup"><span data-stu-id="d3538-147">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="d3538-148">Mukautettujen kenttien hallinta</span><span class="sxs-lookup"><span data-stu-id="d3538-148">Managing custom fields</span></span>

<span data-ttu-id="d3538-149">Järjestelmän kaikkia mukautettuja kenttiä voi hallita järjestelmänhallintamoduulin **Mukautetut kentät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d3538-149">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="d3538-150">Tällä sivulla käyttäjät voivat käyttää monia toimintoja, kuten</span><span class="sxs-lookup"><span data-stu-id="d3538-150">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="d3538-151">tarkastella luetteloa kaikista järjestelmän mukautetuista kentistä</span><span class="sxs-lookup"><span data-stu-id="d3538-151">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="d3538-152">aiemmin luotujen mukautettujen kenttien rajallinen muokkaus</span><span class="sxs-lookup"><span data-stu-id="d3538-152">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="d3538-153">mukautettujen kenttien poistaminen</span><span class="sxs-lookup"><span data-stu-id="d3538-153">Deleting custom fields.</span></span>
- <span data-ttu-id="d3538-154">mukautettujen kenttien tuominen tietoyksiköiden nähtäville</span><span class="sxs-lookup"><span data-stu-id="d3538-154">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="d3538-155">mukautettujen kenttien otsikoiden ja ohjetekstien kääntäminen.</span><span class="sxs-lookup"><span data-stu-id="d3538-155">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="d3538-156">Kaikkien mukautettujen kenttien tarkastelu</span><span class="sxs-lookup"><span data-stu-id="d3538-156">Viewing all custom fields</span></span>

<span data-ttu-id="d3538-157">Kaikki järjestelmässä määritetyt mukautetut kentät ovat näkyvissä **Mukautetut kentät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d3538-157">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="d3538-158">Valitse vain sopiva taulu ja päivittyvällä sivulla on luettelo kyseiseen tauluun liitetyistä mukautetuista kentistä.</span><span class="sxs-lookup"><span data-stu-id="d3538-158">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="d3538-159">Voit tarkastella kaikkia kentän tietoja valitsemalla mukautetun kentän luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d3538-159">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="d3538-160">Mukautettujen kenttien muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="d3538-160">Editing custom fields</span></span>

<span data-ttu-id="d3538-161">Kentän luonnin jälkeen vain tiettyjä mukautetun kentän tietoja voi muokata **Mukautetut kentät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d3538-161">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="d3538-162">*Voit* muokata seuraavia määritteitä:</span><span class="sxs-lookup"><span data-stu-id="d3538-162">You *can* modify these attributes:</span></span>

- <span data-ttu-id="d3538-163">Nimiö</span><span class="sxs-lookup"><span data-stu-id="d3538-163">Label</span></span>
- <span data-ttu-id="d3538-164">Ohjeteksti</span><span class="sxs-lookup"><span data-stu-id="d3538-164">Help text</span></span>
- <span data-ttu-id="d3538-165">Pituus (tekstikentissä)</span><span class="sxs-lookup"><span data-stu-id="d3538-165">Length, for Text fields</span></span>

<span data-ttu-id="d3538-166">*ET* voi muokata seuraavia määritteitä:</span><span class="sxs-lookup"><span data-stu-id="d3538-166">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="d3538-167">Kentän nimi</span><span class="sxs-lookup"><span data-stu-id="d3538-167">Field name</span></span>
- <span data-ttu-id="d3538-168">Tietotyyppi</span><span class="sxs-lookup"><span data-stu-id="d3538-168">Data type</span></span>

<span data-ttu-id="d3538-169">Lisäksi mukautetuista kentistä valintaluettelokenttien arvojoukon järjestystä voi muokata ja uusia arvoja voi lisätä. Valintaluettelokentässä olevia arvoja ei kuitenkaan saa poistaa.</span><span class="sxs-lookup"><span data-stu-id="d3538-169">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="d3538-170">Muista tallentaa muutokset valitsemalla **Ota muutokset käyttöön**, kun lopetat tietyn taulun kenttien muokkaamisen.</span><span class="sxs-lookup"><span data-stu-id="d3538-170">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="d3538-171">Mukautettujen kenttien tuominen tietoyksiköiden nähtäville</span><span class="sxs-lookup"><span data-stu-id="d3538-171">Exposing custom fields on data entities</span></span>

<span data-ttu-id="d3538-172">On myös tärkeää, että tietoyksiköt voivat havaita mukautetut kentät.</span><span class="sxs-lookup"><span data-stu-id="d3538-172">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="d3538-173">Tietoyksiköitä käytetään [Office-integroinnin yleiskatsaus](../../dev-itpro/office-integration/office-integration.md) -toiminnossa sekä tietojen tuonti- ja vientiskenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="d3538-173">Data entities are utilized in the [Office integration overview](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="d3538-174">Voit tuoda mukautetun kentän tietoyksikön nähtäville seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d3538-174">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="d3538-175">Valitse mukautettu kenttä **Mukautetut kentät** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="d3538-175">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="d3538-176">Tuo soveltuvat yksiköt näkyviin laajentamalla **Yksiköt**-osa.</span><span class="sxs-lookup"><span data-stu-id="d3538-176">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="d3538-177">Napsauta **Muokkaa**-painiketta.</span><span class="sxs-lookup"><span data-stu-id="d3538-177">Click the **Edit** button.</span></span>
4. <span data-ttu-id="d3538-178">Muokkaa kullekin yksikölle valittavaa **Käytössä**-kenttää, jonka on tuotava tämä kenttä näkyviin.</span><span class="sxs-lookup"><span data-stu-id="d3538-178">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="d3538-179">Tallenna valinnat valitsemalla **Ota muutokset käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="d3538-179">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="d3538-180">Mukautettujen kenttien näyttämisen salliminen muilla kielillä</span><span class="sxs-lookup"><span data-stu-id="d3538-180">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="d3538-181">Koska eri kieltä käyttävien käyttäjien on ehkä voitava käyttää mukautettuja kenttiä, **Mukautetut kentät** -sivulla on mekanismi, jolla mukautetun kentän otsikko ja ohjeteksti voidaan kääntää muille kielille.</span><span class="sxs-lookup"><span data-stu-id="d3538-181">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="d3538-182">Mukautetut kentät voidaan kääntää muille kielille seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d3538-182">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="d3538-183">Valitse mukautettu kenttä **Mukautetut kentät** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d3538-183">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="d3538-184">Valitse toimintoruudussa **Käännökset**-painike.</span><span class="sxs-lookup"><span data-stu-id="d3538-184">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="d3538-185">Kentän aiemmat käännökset sisältävä avattava valikko avautuu.</span><span class="sxs-lookup"><span data-stu-id="d3538-185">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="d3538-186">Avattavassa **Kieli**-luettelossa on kielet, joille on jo tehty käännöksiä.</span><span class="sxs-lookup"><span data-stu-id="d3538-186">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="d3538-187">Jos haluat muokata valmista käännöstä, valitse valikossa kieli ja muokkaa otsikon ja ohjetekstin arvoja.</span><span class="sxs-lookup"><span data-stu-id="d3538-187">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="d3538-188">Napsauta muussa tapauksessa **Lisää kieli** -painiketta, valitse valikossa kieli ja anna otsikon ja ohjetekstin käännetyt arvot.</span><span class="sxs-lookup"><span data-stu-id="d3538-188">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="d3538-189">Valitse **OK**, kun olet valmis.</span><span class="sxs-lookup"><span data-stu-id="d3538-189">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="d3538-190">Mukautettujen kenttien poistaminen</span><span class="sxs-lookup"><span data-stu-id="d3538-190">Deleting custom fields</span></span>

<span data-ttu-id="d3538-191">Joskus harvoin voi käydä niin, että mukautettua kenttää ei enää tarvita.</span><span class="sxs-lookup"><span data-stu-id="d3538-191">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="d3538-192">Järjestelmänvalvoja voi päättää silloin poistaa kentän **Mukautetut kentät** -sivulta.</span><span class="sxs-lookup"><span data-stu-id="d3538-192">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="d3538-193">Varmista siinä tapauksessa, että oikea kenttä on valittu. Valitse sitten **Poista** ja vahvista poista valitsemalla **Kyllä**. Valitse lopuksi **Ota muutokset käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="d3538-193">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="d3538-194">Tätä toimintoa ei voi peruuttaa. Lisäksi kenttään liitetyt tiedot poistetaan pysyvästi tietokannasta.</span><span class="sxs-lookup"><span data-stu-id="d3538-194">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="d3538-195">Liite</span><span class="sxs-lookup"><span data-stu-id="d3538-195">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="d3538-196">Kenellä on oikeus luoda mukautettuja kenttiä?</span><span class="sxs-lookup"><span data-stu-id="d3538-196">Who can create custom fields?</span></span>

<span data-ttu-id="d3538-197">Järjestelmän suojaamiseksi vain järjestelmänvalvojat voivat oletusarvoisesti luoda mukautettuja kenttiä.</span><span class="sxs-lookup"><span data-stu-id="d3538-197">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="d3538-198">Organisaatio voi kuitenkin antaa tarvittaessa sopiville tehokäyttäjille mukautettujen kenttien luontioikeudet. Järjestelmänvalvojat voivat tehdä sen käyttämällä **Suorituksenaikainen mukautuksen tehokäyttäjä** -käyttöoikeusroolia.</span><span class="sxs-lookup"><span data-stu-id="d3538-198">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="d3538-199">Vaikka käyttäjät, joilla ei ole tätä käyttöoikeusroolia, eivät voi luoda mukautettuja kenttiä, he voivat kuitenkin nähdä ja käyttää muiden järjestelmän käyttäjien lisäämiä mukautettuja kenttiä.</span><span class="sxs-lookup"><span data-stu-id="d3538-199">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="d3538-200">Mitkä taulukot tukevat mukautettuja kenttiä?</span><span class="sxs-lookup"><span data-stu-id="d3538-200">What tables support custom fields?</span></span>

<span data-ttu-id="d3538-201">Suorituskyvyn ja teknisten syiden vuoksi vain seuraavat ehdot täyttävät taulut sallivat tällä hetkellä mukautettujen kenttien lisäämisen.</span><span class="sxs-lookup"><span data-stu-id="d3538-201">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="d3538-202">Taulun on luotava merkitty joksikin seuraavista ryhmistä:</span><span class="sxs-lookup"><span data-stu-id="d3538-202">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="d3538-203">Ryhmä</span><span class="sxs-lookup"><span data-stu-id="d3538-203">Group</span></span>
    - <span data-ttu-id="d3538-204">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="d3538-204">WorksheetHeader</span></span>
    - <span data-ttu-id="d3538-205">Otsikko</span><span class="sxs-lookup"><span data-stu-id="d3538-205">Main</span></span>
    - <span data-ttu-id="d3538-206">Muut</span><span class="sxs-lookup"><span data-stu-id="d3538-206">Miscellaneous</span></span>
    - <span data-ttu-id="d3538-207">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3538-207">Parameter</span></span>
    - <span data-ttu-id="d3538-208">Viite</span><span class="sxs-lookup"><span data-stu-id="d3538-208">Reference</span></span>
    - <span data-ttu-id="d3538-209">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="d3538-209">TransactionHeader</span></span>

- <span data-ttu-id="d3538-210">Taulu ei voi laajentaa toista taulua.</span><span class="sxs-lookup"><span data-stu-id="d3538-210">The table cannot extend another table.</span></span>
- <span data-ttu-id="d3538-211">Taulua ei voi merkitä järjestelmätauluksi.</span><span class="sxs-lookup"><span data-stu-id="d3538-211">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="d3538-212">Taulu ei voi olla väliaikainen taulu.</span><span class="sxs-lookup"><span data-stu-id="d3538-212">The table cannot be a temporary table.</span></span>

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a><span data-ttu-id="d3538-213">Voinko viitata mukautettuihin kenttiin kehittäjän työkaluissa?</span><span class="sxs-lookup"><span data-stu-id="d3538-213">Can I reference custom fields from the developer tools?</span></span>  

<span data-ttu-id="d3538-214">Mukautettuja kenttiä voi hallinnoida vain käyttöliittymässä. Niihin ei voi viitata koodilla.</span><span class="sxs-lookup"><span data-stu-id="d3538-214">Custom fields can only be managed through the user interface and cannot be referenced by code.</span></span> 
