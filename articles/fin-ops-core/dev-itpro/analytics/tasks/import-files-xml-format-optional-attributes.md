---
title: (RCS) Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä
description: Tässä ohjeaiheessa on tietoja tavalla, jolla käyttäjä voi suunnitella ER-muodon määrityksen tuomaan tiedostoja valinnaisia määritteitä sisältävän XML-muodon.
author: NickSelin
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 25ced72bc1bb1b18996c8bab986270fde0557ed3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744864"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="9a17e-103">(RCS) Tiedostojen tuonti XML-muodossa valinnaisilla määritteillä</span><span class="sxs-lookup"><span data-stu-id="9a17e-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a17e-104">Seuraavissa vaiheissa käsitellään, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi suunnitella ER-muotomäärityksen tuomaan valinnaisia määritteitä sisältävän XML-muotoisia tiedostoja.</span><span class="sxs-lookup"><span data-stu-id="9a17e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="9a17e-105">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="9a17e-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="9a17e-106">Ennen kuin aloitat, lataa ja tallenna IncomingDocumentToLearnHowToHandleOptionalAttributes.xml-tiedosto paikallisesti [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="9a17e-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="9a17e-107">Valitse **Kaikki työtilat** > **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="9a17e-108">Varmista, että Litware, Inc. -malliyrityksen konfiguraation lähde on käytettävissä ja merkitty **aktiiviseksi**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="9a17e-109">Jos konfiguraation lähde ei ole näkyvissä, suorita [Konfigurointipalvelujen luominen ja merkitseminen aktiivisiksi](er-configuration-provider-mark-it-active-2016-11.md) -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="9a17e-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="9a17e-110">Valitse **Raportointikonfiguraatiot**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="9a17e-111">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="9a17e-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="9a17e-112">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="9a17e-113">Kirjoita **Nimi**-kenttään Xml-tiedoston tuontimalli.</span><span class="sxs-lookup"><span data-stu-id="9a17e-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="9a17e-114">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="9a17e-115">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="9a17e-116">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="9a17e-117">Kirjoita **Nimi**-kenttään Juuri.</span><span class="sxs-lookup"><span data-stu-id="9a17e-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="9a17e-118">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-118">Click **Add**.</span></span>
8.    <span data-ttu-id="9a17e-119">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="9a17e-120">Kirjoita **Nimi**-kenttään Luettelo.</span><span class="sxs-lookup"><span data-stu-id="9a17e-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="9a17e-121">Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="9a17e-122">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-122">Click **Add**.</span></span>
12.    <span data-ttu-id="9a17e-123">Avaa valintaikkuna valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="9a17e-124">Kirjoita **Nimi**-kenttään Koodi.</span><span class="sxs-lookup"><span data-stu-id="9a17e-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="9a17e-125">Valitse **Nimiketyyppi**-kentässä **Merkkijono**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="9a17e-126">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-126">Click **Add**.</span></span>
16.    <span data-ttu-id="9a17e-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-127">Click **Save**.</span></span>
17.    <span data-ttu-id="9a17e-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9a17e-128">Close the page.</span></span>
18.    <span data-ttu-id="9a17e-129">Valitse **Muuta tila**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="9a17e-130">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="9a17e-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="9a17e-132">Tietojen tuontimuodon luominen</span><span class="sxs-lookup"><span data-stu-id="9a17e-132">Create a format for data import</span></span>
1.    <span data-ttu-id="9a17e-133">Avaa valintaikkuna valitsemalla **Luo konfigurointi**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="9a17e-134">Kirjoita **Uusi**-kenttään Muoto perustuu tietomalliin Xml-tiedoston tuontimalli.</span><span class="sxs-lookup"><span data-stu-id="9a17e-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="9a17e-135">Kirjoita **Nimi**-kenttään Xml-tiedoston tuontimuoto.</span><span class="sxs-lookup"><span data-stu-id="9a17e-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="9a17e-136">Valitse **Tukee tietojen tuontia** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="9a17e-137">Valitse **Luo konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="9a17e-138">Muodon suunnitteleminen jäsentämään saapuvan tiedosto xml-muodossa</span><span class="sxs-lookup"><span data-stu-id="9a17e-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="9a17e-139">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="9a17e-140">Avaa valintaikkuna valitsemalla **Lisää juuri**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="9a17e-141">Valitse puussa **XML\Elementti**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="9a17e-142">Kirjoita **Nimi**-kenttään root.</span><span class="sxs-lookup"><span data-stu-id="9a17e-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="9a17e-143">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-143">Click **OK**.</span></span>
6.    <span data-ttu-id="9a17e-144">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="9a17e-145">Valitse puussa **XML\Elementti**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="9a17e-146">Kirjoita **Nimi**-kenttään document.</span><span class="sxs-lookup"><span data-stu-id="9a17e-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="9a17e-147">Valitse **Monimuotoisuus**-kentässä **Yksi tai useita**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="9a17e-148">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-148">Click **OK**.</span></span>
11.    <span data-ttu-id="9a17e-149">Valitse puussa **root\document**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="9a17e-150">Avaa valintaikkuna valitsemalla **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="9a17e-151">Valitse puussa **XML\Määrite**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="9a17e-152">Kirjoita **Nimi**-kenttään ID.</span><span class="sxs-lookup"><span data-stu-id="9a17e-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="9a17e-153">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-153">Click **OK**.</span></span>
16.    <span data-ttu-id="9a17e-154">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="9a17e-155">Muodon yhdistämisen suunnitteleminen tallentamaan jäsennetty tieto tietomalliin</span><span class="sxs-lookup"><span data-stu-id="9a17e-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="9a17e-156">Valitse **Yhdistä muoto malliin**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="9a17e-157">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-157">Click **New**.</span></span>
3. <span data-ttu-id="9a17e-158">Anna tai valitse **Määritys**-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="9a17e-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="9a17e-159">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9a17e-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9a17e-160">Kirjoita **Nimi**-kenttään Yhdistäminen.</span><span class="sxs-lookup"><span data-stu-id="9a17e-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="9a17e-161">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-161">Click **Save**.</span></span>
7. <span data-ttu-id="9a17e-162">Valitse **Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-162">Click **Designer**.</span></span>
8. <span data-ttu-id="9a17e-163">Laajenna puussa **format**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="9a17e-164">Laajenna puussa **format\root: XML Element(root)**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="9a17e-165">Valitse puussa \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="9a17e-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="9a17e-166">(tiedosto)\*\*.</span><span class="sxs-lookup"><span data-stu-id="9a17e-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="9a17e-167">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="9a17e-168">Laajenna puussa \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="9a17e-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="9a17e-169">(tiedosto)\*\*.</span><span class="sxs-lookup"><span data-stu-id="9a17e-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="9a17e-170">Valitse puussa \**format\root: XML Element(root)\document: XML Element 1..*</span><span class="sxs-lookup"><span data-stu-id="9a17e-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="9a17e-171">(tiedosto)\id\*\*.</span><span class="sxs-lookup"><span data-stu-id="9a17e-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="9a17e-172">Laajenna puussa **List = format.root.document**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="9a17e-173">Valitse puussa **List = format.root.document\Code**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="9a17e-174">Valitse **Sido**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="9a17e-175">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-175">Click **Save**.</span></span>
18.    <span data-ttu-id="9a17e-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9a17e-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="9a17e-177">Muodon yhdistämisen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="9a17e-177">Run format mapping</span></span>
1. <span data-ttu-id="9a17e-178">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-178">Click **Run**.</span></span>
2. <span data-ttu-id="9a17e-179">Valitse ensin **Selaa** ja sitten **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="9a17e-180">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="9a17e-181">Valittua tiedostoa ei ole tuotu, sillä muodon rakenne olettaa, että document-elementissä on id-määrite mutta tuodussa tiedostossa tätä määritettä ei ole.</span><span class="sxs-lookup"><span data-stu-id="9a17e-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="9a17e-182">Muodon rakenteen muokkaaminen käsittelemään xml-määritettä valinnaisena</span><span class="sxs-lookup"><span data-stu-id="9a17e-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="9a17e-183">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9a17e-183">Close the page.</span></span>
2. <span data-ttu-id="9a17e-184">Laajenna puussa **root\document**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="9a17e-185">Valitse puussa **root\document\id**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="9a17e-186">Valitse **Puuttuvan määritteen tyhjä merkkijono** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="9a17e-187">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="9a17e-188">Muutosten testaaminen suorittamalla muodon yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="9a17e-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="9a17e-189">Valitse **Yhdistä muoto malliin**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="9a17e-190">Valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-190">Click **Run**.</span></span>
3. <span data-ttu-id="9a17e-191">Valitse ensin **Selaa** ja sitten **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**-tiedosto.</span><span class="sxs-lookup"><span data-stu-id="9a17e-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="9a17e-192">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a17e-192">Click **OK**.</span></span>
5. <span data-ttu-id="9a17e-193">Tarkista luotu tiedosto.</span><span class="sxs-lookup"><span data-stu-id="9a17e-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="9a17e-194">Sama tiedosto on tuotu, sillä muodon rakenne käsittelee document-elementit id-määritettä nyt valinnaisena.</span><span class="sxs-lookup"><span data-stu-id="9a17e-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]