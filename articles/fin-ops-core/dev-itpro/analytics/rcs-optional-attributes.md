---
title: Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä
description: Tässä ohjeaiheessa on tietoja sellaisten ER-muotojen suunnittelemisesta, joissa määritetään XML-määritteet jäsentämään saapuvat sähköiset asiakirjat XML-muodossa.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 399f19197a729c11eaff94d708c837caef0d366d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562949"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="a160a-103">Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä</span><span class="sxs-lookup"><span data-stu-id="a160a-103">Import files in XML format with optional attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a160a-104">Voit suunnitella sähköisen raportoinnin (ER) muodot jäsentämään saapuvat sähköiset asiakirjat XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="a160a-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="a160a-105">Tietyt XML-elementtien määritteet voidaan määrittää suunnitellussa ER-muodossa valinnaisina.</span><span class="sxs-lookup"><span data-stu-id="a160a-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="a160a-106">Sen avulla voit käsitellä saapuvia tiedostoja asianmukaisesti riippumatta siitä, onko siinä kyseiset määritteet vai ei.</span><span class="sxs-lookup"><span data-stu-id="a160a-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="a160a-107">Sitten voit käyttää näiden tiedostojen sisältöä sovelluksen tietojen päivittämiseen.</span><span class="sxs-lookup"><span data-stu-id="a160a-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="a160a-108">Saat lisätietoja tästä ominaisuudesta suorittamalla ohjeaiheen [(RCS) Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä](tasks/import-files-xml-format-optional-attributes.md) vaiheet. Se on osa 7.5.4.3 IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen (10677) -liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="a160a-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="a160a-109">Voit ladata kyseisen tehtäväoppaan ja liitetyt mallitiedostot [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="a160a-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="a160a-110">Sisällön kuvaus</span><span class="sxs-lookup"><span data-stu-id="a160a-110">Content description</span></span>       | <span data-ttu-id="a160a-111">Tiedosto</span><span class="sxs-lookup"><span data-stu-id="a160a-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="a160a-112">XML-muotoinen mallitiedosto</span><span class="sxs-lookup"><span data-stu-id="a160a-112">Sample file in XML format</span></span> | <span data-ttu-id="a160a-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="a160a-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="a160a-114">Tehtävän ohjaus</span><span class="sxs-lookup"><span data-stu-id="a160a-114">Task guide</span></span>                | <span data-ttu-id="a160a-115">RCS Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä.axtr</span><span class="sxs-lookup"><span data-stu-id="a160a-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="a160a-116">Seuraavissa vaiheissa käsitellään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi suunnitella ER-muotomäärityksen tuomaan valinnaisia määritteitä sisältävän XML-muotoisia tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="a160a-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="a160a-117">Näitä vaiheita varten on ensin suoritettava menettelyssä [Konfiguraation lähteiden luominen ja merkitseminen aktiivisiksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) käsitellyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="a160a-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="a160a-118">Ennen kuin aloitat, lataa ja tallenna IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-tiedosto paikallisesti Microsoft Download Centeristä (https://go.microsoft.com/fwlink/?linkid=874684 ).</span><span class="sxs-lookup"><span data-stu-id="a160a-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="a160a-119">Valitse **Organisaation hallinto** > **Työtilat** > **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="a160a-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="a160a-120">Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="a160a-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="a160a-121">Jos konfiguraation lähde ei ole näkyvissä, suorita ohjeaiheen [Konfiguraation lähteiden luominen ja merkitseminen aktiivisiksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheet.</span><span class="sxs-lookup"><span data-stu-id="a160a-121">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="a160a-122">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="a160a-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="a160a-123">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="a160a-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="a160a-124">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="a160a-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="a160a-125">Kirjoita **Nimi**-kenttään Xml-tiedoston tuontimalli.</span><span class="sxs-lookup"><span data-stu-id="a160a-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="a160a-126">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="a160a-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="a160a-127">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="a160a-127">Click **Designer**.</span></span>
5. <span data-ttu-id="a160a-128">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a160a-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="a160a-129">Kirjoita **Nimi**-kenttään Juuri.</span><span class="sxs-lookup"><span data-stu-id="a160a-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="a160a-130">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a160a-130">Click **Add**.</span></span>
8. <span data-ttu-id="a160a-131">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a160a-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="a160a-132">Kirjoita **Nimi**-kenttään Luettelo.</span><span class="sxs-lookup"><span data-stu-id="a160a-132">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="a160a-133">Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.</span><span class="sxs-lookup"><span data-stu-id="a160a-133">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="a160a-134">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a160a-134">Click **Add**.</span></span>
12.    <span data-ttu-id="a160a-135">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a160a-135">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="a160a-136">Kirjoita **Nimi**-kenttään Koodi.</span><span class="sxs-lookup"><span data-stu-id="a160a-136">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="a160a-137">Valitse **Nimiketyyppi**-kentässä **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="a160a-137">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="a160a-138">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a160a-138">Click **Add**.</span></span>
16.    <span data-ttu-id="a160a-139">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a160a-139">Click **Save**.</span></span>
17.    <span data-ttu-id="a160a-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a160a-140">Close the page.</span></span>
18.    <span data-ttu-id="a160a-141">Valitse **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="a160a-141">Click **Change status**.</span></span>
19.    <span data-ttu-id="a160a-142">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="a160a-142">Click **Complete**.</span></span>
20.    <span data-ttu-id="a160a-143">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a160a-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="a160a-144">Tietojen tuontimuodon luominen</span><span class="sxs-lookup"><span data-stu-id="a160a-144">Create a format for data import</span></span>
1. <span data-ttu-id="a160a-145">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="a160a-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="a160a-146">Kirjoita **Uusi**-kenttään Muoto perustuu tietomalliin Xml-tiedoston tuontimalli.</span><span class="sxs-lookup"><span data-stu-id="a160a-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="a160a-147">Kirjoita **Nimi**-kenttään Xml-tiedoston tuontimuoto.</span><span class="sxs-lookup"><span data-stu-id="a160a-147">In the **Nam** e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="a160a-148">Valitse **Tukee tietojen tuontia** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a160a-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="a160a-149">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="a160a-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="a160a-150">Muodon suunnitteleminen jäsentämään saapuvan tiedosto xml-muodossa</span><span class="sxs-lookup"><span data-stu-id="a160a-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="a160a-151">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="a160a-151">Click **Designer**.</span></span>
2. <span data-ttu-id="a160a-152">Avaa valintaikkuna valitsemalla **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="a160a-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="a160a-153">Valitse puussa **XML\Elementti**.</span><span class="sxs-lookup"><span data-stu-id="a160a-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="a160a-154">Kirjoita **Nimi**-kenttään root.</span><span class="sxs-lookup"><span data-stu-id="a160a-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="a160a-155">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a160a-155">Click **OK**.</span></span>
6. <span data-ttu-id="a160a-156">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a160a-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="a160a-157">Valitse puussa **XML\Elementti**.</span><span class="sxs-lookup"><span data-stu-id="a160a-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="a160a-158">Kirjoita **Nimi**-kenttään document.</span><span class="sxs-lookup"><span data-stu-id="a160a-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="a160a-159">Valitse **Monimuotoisuus**-kentässä **Yksi tai useita**.</span><span class="sxs-lookup"><span data-stu-id="a160a-159">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="a160a-160">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a160a-160">Click **OK**.</span></span>
11.    <span data-ttu-id="a160a-161">Valitse puussa **root\document**.</span><span class="sxs-lookup"><span data-stu-id="a160a-161">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="a160a-162">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a160a-162">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="a160a-163">Valitse puussa **XML\Määrite**.</span><span class="sxs-lookup"><span data-stu-id="a160a-163">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="a160a-164">Kirjoita **Nimi**-kenttään id.</span><span class="sxs-lookup"><span data-stu-id="a160a-164">In the **Name** field, type 'id'.</span></span>
15.    <span data-ttu-id="a160a-165">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a160a-165">Click **OK**.</span></span>
16.    <span data-ttu-id="a160a-166">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a160a-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="a160a-167">Muodon yhdistämisen suunnitteleminen tallentamaan jäsennetty tieto tietomalliin</span><span class="sxs-lookup"><span data-stu-id="a160a-167">Design a format mapping to save parsed information to data model</span></span>
1.    <span data-ttu-id="a160a-168">Valitse **Yhdistä muoto malliin**.</span><span class="sxs-lookup"><span data-stu-id="a160a-168">Click **Map format to model**.</span></span>
2.    <span data-ttu-id="a160a-169">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a160a-169">Click **New**.</span></span>
3.    <span data-ttu-id="a160a-170">Anna tai valitse **Määritys**-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="a160a-170">In the **Definition** field, enter or select a value.</span></span>
4.    <span data-ttu-id="a160a-171">Kirjoita **Nimi**-kenttään Yhdistäminen.</span><span class="sxs-lookup"><span data-stu-id="a160a-171">In the **Name** field, type 'Mapping'.</span></span>
5.    <span data-ttu-id="a160a-172">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a160a-172">Click **Save**.</span></span>
6.    <span data-ttu-id="a160a-173">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="a160a-173">Click **Designer**.</span></span>
7.    <span data-ttu-id="a160a-174">Laajenna puussa **format**.</span><span class="sxs-lookup"><span data-stu-id="a160a-174">In the tree, expand **format**.</span></span>
8.    <span data-ttu-id="a160a-175">Laajenna puussa **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="a160a-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.    <span data-ttu-id="a160a-176">Valitse puussa \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="a160a-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="a160a-177">(tiedosto)\*\*.</span><span class="sxs-lookup"><span data-stu-id="a160a-177">(document)\*\*.</span></span>
10.    <span data-ttu-id="a160a-178">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="a160a-178">Click **Bind**.</span></span>
11.    <span data-ttu-id="a160a-179">Laajenna puussa \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="a160a-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="a160a-180">(tiedosto)\*\*.</span><span class="sxs-lookup"><span data-stu-id="a160a-180">(document)\*\*.</span></span>
12.    <span data-ttu-id="a160a-181">Valitse puussa \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="a160a-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="a160a-182">(tiedosto)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="a160a-182">(document)\id\*\*.</span></span>
13.    <span data-ttu-id="a160a-183">Laajenna puussa **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="a160a-183">In the tree, expand **List = format.root.document**.</span></span>
14.    <span data-ttu-id="a160a-184">Valitse puussa **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="a160a-184">In the tree, select **List = format.root.document\Code**.</span></span>
15.    <span data-ttu-id="a160a-185">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="a160a-185">Click **Bind**.</span></span>
16.    <span data-ttu-id="a160a-186">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a160a-186">Click **Save**.</span></span>
17.    <span data-ttu-id="a160a-187">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a160a-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="a160a-188">Muodon yhdistämisen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="a160a-188">Run format mapping</span></span>
1. <span data-ttu-id="a160a-189">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="a160a-189">Click **Run**.</span></span>
2. <span data-ttu-id="a160a-190">Valitse ensin **Selaa** ja sitten tiedosto **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="a160a-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="a160a-191">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a160a-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a160a-192">Valittua tiedostoa ei ole tuotu, sillä muodon rakenne olettaa, että document-elementissä on id-määrite mutta tuodussa tiedostossa tätä määritettä ei ole.</span><span class="sxs-lookup"><span data-stu-id="a160a-192">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="a160a-193">Muodon rakenteen muokkaaminen käsittelemään xml-määritettä valinnaisena</span><span class="sxs-lookup"><span data-stu-id="a160a-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="a160a-194">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a160a-194">Close the page.</span></span>
2. <span data-ttu-id="a160a-195">Laajenna puussa **root\document**.</span><span class="sxs-lookup"><span data-stu-id="a160a-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="a160a-196">Valitse puussa **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="a160a-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="a160a-197">Valitse **Puuttuvan määritteen tyhjä merkkijono** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a160a-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="a160a-198">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a160a-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="a160a-199">Muutosten testaaminen suorittamalla muodon yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="a160a-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="a160a-200">Valitse **Yhdistä muoto malliin**.</span><span class="sxs-lookup"><span data-stu-id="a160a-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="a160a-201">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="a160a-201">Click **Run**.</span></span>
3. <span data-ttu-id="a160a-202">Valitse ensin **Selaa** ja sitten tiedosto **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="a160a-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="a160a-203">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a160a-203">Click **OK**.</span></span>
5. <span data-ttu-id="a160a-204">Tarkista luotu tiedosto.</span><span class="sxs-lookup"><span data-stu-id="a160a-204">Review the generated file.</span></span> <span data-ttu-id="a160a-205">Huomaa, että sama tiedosto on tuotu, sillä muodon rakenne käsittelee document-elementit id-määritettä nyt valinnaisena.</span><span class="sxs-lookup"><span data-stu-id="a160a-205">Note that same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]