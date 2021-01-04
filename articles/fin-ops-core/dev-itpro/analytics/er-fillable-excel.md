---
title: Excel-muotoisia tiedostoja luovan määrityksen suunnitteleminen
description: Tässä ohjeaiheessa on tietoja Excel-mallin täyttävän sähköisen raportointimuodon (ER-muodon) suunnittelemisesta ja lähtevien Excel-muotoisten tiedostojen luonnista.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5733e40c67f9c97b04f126f7c3cfea9d4f8f5b5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686535"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a><span data-ttu-id="262bf-103">Excel-muotoisia tiedostoja luovan määrityksen suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="262bf-103">Design a configuration for generating documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="262bf-104">Voit suunnitella [sähköisen raportoinnin (ER)](general-electronic-reporting.md) muotomäärityksen, jonka ER[-muoto-osan](general-electronic-reporting.md#FormatComponentOutbound) voi määrittää luomaan lähtevän tiedoston Microsoft Excel -muotoisena työkirjana.</span><span class="sxs-lookup"><span data-stu-id="262bf-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) format configuration that has an ER [format component](general-electronic-reporting.md#FormatComponentOutbound) that you can configure to generate an outbound document in a Microsoft Excel workbook format.</span></span> <span data-ttu-id="262bf-105">Tätä tarkoitusta varten on käytettävä tiettyjä ER-muoto-osia.</span><span class="sxs-lookup"><span data-stu-id="262bf-105">Specific ER format components must be used for this purpose.</span></span>

<span data-ttu-id="262bf-106">Lisätietoja tästä toiminnosta on ohjeaiheen [Konfiguraation suunnitteleminen raporttien luomiseksi OPENXML-muodossa](tasks/er-design-reports-openxml-2016-11.md) ohjeissa.</span><span class="sxs-lookup"><span data-stu-id="262bf-106">To learn more about this feature, follow the steps in the topic, [Design a configuration for generating reports in OPENXML format](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="add-a-new-er-format"></a><span data-ttu-id="262bf-107">Uuden ER-muodon lisääminen</span><span class="sxs-lookup"><span data-stu-id="262bf-107">Add a new ER format</span></span>

<span data-ttu-id="262bf-108">Kun Excel-työkirjamuotoisen lähtevän tiedoston luontia varten lisätään uusi ER-muotomääritys, muodon **Muodon tyyppi** -määritteeksi on joko valittava **Excel**-arvo tai **Muodon tyyppi** -määrite on jätettävä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="262bf-108">When you add a new ER format configuration to generate an outbound document in an Excel workbook format, you must either select the **Excel** value for the **Format type** attribute of the format or leave the **Format type** attribute blank.</span></span>

- <span data-ttu-id="262bf-109">Jos valitse **Excel**, muoto voidaan määrittää luomaan lähtevä tiedosto vain Excel-muodossa.</span><span class="sxs-lookup"><span data-stu-id="262bf-109">If you select **Excel**, you can configure the format to generate an outbound document only in Excel format.</span></span>
- <span data-ttu-id="262bf-110">Jos määrite jätetään tyhjäksi, voit määrittää lähtevän tiedoston luovaksi muodoksi minkä tahansa ER-kehyksen tukeman muodon.</span><span class="sxs-lookup"><span data-stu-id="262bf-110">If you leave the attribute blank, you can configure the format to generate an outbound document in any format that is supported by the ER framework.</span></span>

<span data-ttu-id="262bf-111">Määrityksen Er-muoto-osa määritetään valitsemalla toimintoruudussa **Suunnitteluohjelma** ja avaamalla ER-muoto-osa muokattavaksi ER-toiminnon suunnitteluohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="262bf-111">To configure the ER format component of the configuration, select **Designer** on the Action Pane, and open the ER format component for editing in the ER Operation designer.</span></span>

![Konfiguroinnit-sivu](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a><span data-ttu-id="262bf-113">Excel-tiedosto-osa</span><span class="sxs-lookup"><span data-stu-id="262bf-113">Excel file component</span></span>

### <a name="manual-entry"></a><span data-ttu-id="262bf-114">Manuaalinen kirjaus</span><span class="sxs-lookup"><span data-stu-id="262bf-114">Manual entry</span></span>

<span data-ttu-id="262bf-115">**Excel\\Tiedosto**-osa on lisättävä määritettyyn ER-muotoon luomaan lähtevä tiedosto Excel-muodossa.</span><span class="sxs-lookup"><span data-stu-id="262bf-115">You must add an **Excel\\File** component to the configured ER format to generate an outbound document in Excel format.</span></span>

![Excel\Tiedosto-osa](./media/er-excel-format-add-file-component.png)

<span data-ttu-id="262bf-117">Lähtevän tiedoston asettelu määritetään liittämällä Excel-työkirja, jossa on .xlsx-tunniste, **Excel\\Tiedosto**-osaan lähtevien tiedostojen mallina.</span><span class="sxs-lookup"><span data-stu-id="262bf-117">To specify the layout of the outbound document, attach an Excel workbook that has the .xlsx extension to the **Excel\\File** component as the template for outbound documents.</span></span>

> [!NOTE]
> <span data-ttu-id="262bf-118">Jos malli liitetään manuaalisesti, käytettävän [tiedostotyypin](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) on oltava määritetty tätä tarkoitusta varten [ER-parametreissa](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span><span class="sxs-lookup"><span data-stu-id="262bf-118">When you manually attach a template, you must use a [document type](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) that has been configured for that purpose in the [ER parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).</span></span>

![Liitteen lisääminen Excel\Tiedosto-osaan](./media/er-excel-format-add-file-component2.png)

<span data-ttu-id="262bf-120">Voit määrittää tavan, jolla liitetty malli täytetään määritettyä ER-muotoa suoritettaessa, lisäämällä sisäkkäiset **Taulukko**-, **Alue**- ja **Solu**-osat **Excel\\Tiedosto**-osaan.</span><span class="sxs-lookup"><span data-stu-id="262bf-120">To specify how the attached template will be filled in when you run the configured ER format, you must add nested **Sheet**, **Range**, and **Cell** components to the **Excel\\File** component.</span></span> <span data-ttu-id="262bf-121">Kukin sisäkkäinen osa on liitettävä Excelin nimettyyn kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="262bf-121">Each nested component must be associated with an Excel named item.</span></span>

### <a name="template-import"></a><span data-ttu-id="262bf-122">Mallin tuonti</span><span class="sxs-lookup"><span data-stu-id="262bf-122">Template import</span></span>

<span data-ttu-id="262bf-123">Uusi malli voidaan tuoda tyhjään ER-muotoon valitsemalla **Tuo Excelistä** toimintoruudun **Tuonti**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="262bf-123">You can select **Import from Excel** on the **Import** tab of the Action Pane to import a new template into a blank ER format.</span></span> <span data-ttu-id="262bf-124">Tässä esimerkissä **Excel\\Tiedosto**-osa luodaan automaattisesti ja tuotu malli liitetään siihen.</span><span class="sxs-lookup"><span data-stu-id="262bf-124">In this example, an **Excel\\File** component will be created automatically, and the imported template will be attached to it.</span></span> <span data-ttu-id="262bf-125">Myös kaikki pakolliset ER-osat luodaan automaattisesti löydetyn Excelin nimettyjen kohteiden luettelon perusteella.</span><span class="sxs-lookup"><span data-stu-id="262bf-125">All required ER components will also be created automatically, based on the list of Excel named items that are discovered.</span></span>

![Tuo Excelistä -toiminnon valinta](./media/er-excel-format-import-template.png)

> [!NOTE]
> <span data-ttu-id="262bf-127">Jos muokattavaan ER-muotoon halutaan luoda valinnainen **Taulukko**-elementti, määritä **Luo Excel-taulukkomuotoinen elementti** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="262bf-127">If you want to create the optional **Sheet** element in the editable ER format, set the **Create Excel Sheet format element** option to **Yes**.</span></span>

## <a name="sheet-component"></a><span data-ttu-id="262bf-128">Taulukko-osa</span><span class="sxs-lookup"><span data-stu-id="262bf-128">Sheet component</span></span>

<span data-ttu-id="262bf-129">**Taulukko**-osa ilmaisee sen liitetyn Excel-työtyökirjan laskentataulukon, joka on täytettävä.</span><span class="sxs-lookup"><span data-stu-id="262bf-129">The **Sheet** component indicates a worksheet of the attached Excel workbook that must be filled in.</span></span> <span data-ttu-id="262bf-130">Excel-mallissa olevan laskentataulukon nimi määritetään tämän osan **Taulukko**-ominaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="262bf-130">The name of the worksheet in an Excel template is defined in the **Sheet** property of this component.</span></span>

> [!NOTE]
> <span data-ttu-id="262bf-131">Tämä osa on valinnainen vain yhden laskentataulukon sisältävissä Excel-työkirjoissa.</span><span class="sxs-lookup"><span data-stu-id="262bf-131">This component is optional for Excel workbooks that contain a single worksheet.</span></span>

<span data-ttu-id="262bf-132">ER-toiminnon suunnitteluohjelman **Yhdistämismääritys**-välilehdessä **Taulukko**-osan **Käytössä**-ominaisuus voidaan määrittää määrittämään, onko osa sijoitettava luotuun tiedostoon:</span><span class="sxs-lookup"><span data-stu-id="262bf-132">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Sheet** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="262bf-133">Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Tosi** tai jos mitään lauseketta ei ole määritetty, sopiva laskentataulukko asetetaan luotuun tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="262bf-133">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate worksheet will be put in the generated document.</span></span>
- <span data-ttu-id="262bf-134">Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi**, luotu tiedosto ei sisällä laskentataulukkoa.</span><span class="sxs-lookup"><span data-stu-id="262bf-134">If an expression of the **Enabled** property is configured to return **False** at runtime, the generated document won't contain a worksheet.</span></span>

![Esimerkki Taulukko-osasta](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a><span data-ttu-id="262bf-136">Alue-osa</span><span class="sxs-lookup"><span data-stu-id="262bf-136">Range component</span></span>

<span data-ttu-id="262bf-137">**Alue**-osa ilmaisee Excel-alueen, joka on oltava tämän ER-osan hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="262bf-137">The **Range** component indicates an Excel range that must be controlled by this ER component.</span></span> <span data-ttu-id="262bf-138">Alueen nimi määritetään tämän osan **Excel-alue**-ominaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="262bf-138">The name of the range is defined in the **Excel range** property of this component.</span></span>

<span data-ttu-id="262bf-139">**Replikointisuunta**-ominaisuus määrittää, toistetaanko alue luodussa tiedostossa ja millä tavoin se toistetaan:</span><span class="sxs-lookup"><span data-stu-id="262bf-139">The **Replication direction** property specifies whether and how the range will be repeated in a generated document:</span></span>

- <span data-ttu-id="262bf-140">Jos **Replikointisuunta**-ominaisuudeksi on määritetty **Ei replikointia**, soveltuvaa Excel-aluetta ei toisteta luodussa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="262bf-140">If the **Replication direction** property is set to **No replication**, the appropriate Excel range won't be repeated in the generated document.</span></span>
- <span data-ttu-id="262bf-141">Jos **Replikointisuunta**-ominaisuudeksi on määritetty **Pystysuuntainen**, soveltuvaa Excel-alue toistetaan luodussa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="262bf-141">If the **Replication direction** property is set to **Vertical**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="262bf-142">Jokainen replikoitu alue sijoitetaan Excel-mallin alkuperäisen alueen alapuolelle.</span><span class="sxs-lookup"><span data-stu-id="262bf-142">Every replicated range is put below the original range in an Excel template.</span></span> <span data-ttu-id="262bf-143">Toistojen määrä määräytyy tähän ER-osaan sidotun **Tietueluettelo**-tyypin tietolähteen tietueiden määrän mukaan.</span><span class="sxs-lookup"><span data-stu-id="262bf-143">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>
- <span data-ttu-id="262bf-144">Jos **Replikointisuunta**-ominaisuudeksi on määritetty **Vaakasuuntainen**, soveltuvaa Excel-alue toistetaan luodussa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="262bf-144">If the **Replication direction** property is set to **Horizontal**, the appropriate Excel range will be repeated in the generated document.</span></span> <span data-ttu-id="262bf-145">Jokainen replikoitu alue sijoitetaan Excel-mallin alkuperäisen alueen oikealle puolelle.</span><span class="sxs-lookup"><span data-stu-id="262bf-145">Every replicated range is put to the right of the original range in an Excel template.</span></span> <span data-ttu-id="262bf-146">Toistojen määrä määräytyy tähän ER-osaan sidotun **Tietueluettelo**-tyypin tietolähteen tietueiden määrän mukaan.</span><span class="sxs-lookup"><span data-stu-id="262bf-146">The number of repetitions is defined by the number of records in a data source of the **Record list** type that is bound to this ER component.</span></span>

<span data-ttu-id="262bf-147">Lisätietoja vaakasuuntaisesta replikoinnista on kohdan [Vaakasuunnassa laajennettavien alueiden käyttö sarakkeiden dynaamiseen lisäämiseen Excel-raportteihin](tasks/er-horizontal-1.md) ohjeissa.</span><span class="sxs-lookup"><span data-stu-id="262bf-147">To learn more about horizontal replication, follow the steps in [Use horizontally expandable ranges to dynamically add columns in Excel reports](tasks/er-horizontal-1.md).</span></span>

<span data-ttu-id="262bf-148">**Alue**-osassa voi olla muita sisäkkäisiä ER-osia, joiden avulla annetaan arvoja soveltuvilla Excelin nimetyillä alueilla.</span><span class="sxs-lookup"><span data-stu-id="262bf-148">The **Range** component can have other nested ER components that are used to enter values in the appropriate Excel named ranges.</span></span>

- <span data-ttu-id="262bf-149">Jos arvoja annetaan jollakin **Teksti**-ryhmän osalla, arvo annetaan Excel-alueella tekstiarvona.</span><span class="sxs-lookup"><span data-stu-id="262bf-149">If any component of the **Text** group is used to enter values, the value is entered in an Excel range as a text value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="262bf-150">Tämän mallin avulla voi muotoilla annettuja arvoja sovelluksen määritettyjen alueasetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="262bf-150">Use this pattern to format entered values based on the locale that is defined in the application.</span></span>

- <span data-ttu-id="262bf-151">Jos **Excel**-ryhmän **Solu**-osaa käytetään arvojen antamiseen, arvo annetaan Excel-alueelle sen tietotyypin arvona, joka on määritetty kyseisen **Solu**-osan sidonnalla (kuten **Merkkijono**, **Reaaliluku** tai **Kokonaisluku**).</span><span class="sxs-lookup"><span data-stu-id="262bf-151">If the **Cell** component of the **Excel** group is used to enter values, the value is entered in an Excel range as a value of the data type that is defined by the binding of that **Cell** component (for example, **String**, **Real**, or **Integer**).</span></span>

    > [!NOTE]
    > <span data-ttu-id="262bf-152">Tämän mallin avulla Excel-sovelluksessa voidaan ottaa käyttöön annettujen arvojen muotoilu sen paikallisen tietokoneen alueasetusten perusteella, joka avaa lähtevän tiedoston.</span><span class="sxs-lookup"><span data-stu-id="262bf-152">Use this pattern to enable the Excel application to format entered values based on the locale of the local computer that opens the outbound document.</span></span>

<span data-ttu-id="262bf-153">ER-toiminnon suunnitteluohjelman **Yhdistämismääritys**-välilehdessä **Alue**-osan **Käytössä**-ominaisuus voidaan määrittää määrittämään, onko osa sijoitettava luotuun tiedostoon:</span><span class="sxs-lookup"><span data-stu-id="262bf-153">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Range** component to specify whether the component must be put in a generated document:</span></span>

- <span data-ttu-id="262bf-154">Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Tosi** tai jos mitään lauseketta ei ole määritetty, sopiva alue täytetään luotuun tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="262bf-154">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate range will be filled in in the generated document.</span></span>
- <span data-ttu-id="262bf-155">Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi** tai jos tämä alue ei vastaa kokonaisia rivejä tai sarakkeita, sopivaa aluetta ei täytetä luotuun tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="262bf-155">If an expression of the **Enabled** property is configured to return **False** at runtime, and if this range doesn't represent the entire rows or columns, the appropriate range won't be filled in in the generated document.</span></span>
- <span data-ttu-id="262bf-156">Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi** tai jos tämä alue vastaa kokonaisia rivejä tai sarakkeita, luoto tiedosto sisältää kyseiset rivit ja sarakkeet piilotettuina riveinä ja sarakkeina.</span><span class="sxs-lookup"><span data-stu-id="262bf-156">If an expression of the **Enabled** property is configured to return **False** at runtime, and this range represents the entire rows or columns, the generated document will contain those rows and columns as hidden rows and columns.</span></span>

## <a name="cell-component"></a><span data-ttu-id="262bf-157">Solu-osa</span><span class="sxs-lookup"><span data-stu-id="262bf-157">Cell component</span></span>

<span data-ttu-id="262bf-158">**Solu**-osaa käytetään täyttämään Excelin nimetyt solut, muodot ja kuvat.</span><span class="sxs-lookup"><span data-stu-id="262bf-158">The **Cell** component is used to fill in Excel named cells, shapes, and pictures.</span></span> <span data-ttu-id="262bf-159">Sellainen Excelin nimetty objekti, jonka **Solu**-ER-osan on täytettävä, ilmaistaan määrittämällä kyseisen objektin nimi **Solu**-osan **Excel-alue**-ominaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="262bf-159">To indicate an Excel named object that must be filled in by a **Cell** ER component, you must specify the name of that object in the **Excel range** property of the **Cell** component.</span></span>

<span data-ttu-id="262bf-160">ER-toiminnon suunnitteluohjelman **Yhdistämismääritys**-välilehdessä **Solu**-osan **Käytössä**-ominaisuus voidaan määrittää määrittämään, onko objekti täytettävä luodussa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="262bf-160">On the **Mapping** tab of the ER Operation designer, you can configure the **Enabled** property for a **Cell** component to specify whether the object must be filled in in a generated document:</span></span>

- <span data-ttu-id="262bf-161">Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Tosi** tai jos mitään lauseketta ei ole määritetty, sopiva objekti täytetään luodussa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="262bf-161">If an expression of the **Enabled** property is configured to return **True** at runtime, or if no expression is configured at all, the appropriate object will be filled in in the generated document.</span></span> <span data-ttu-id="262bf-162">Tämän **Solu**-osan sidonta määrittää arvo, joka sijoitetaan sopivaan objektiin.</span><span class="sxs-lookup"><span data-stu-id="262bf-162">The binding of this **Cell** component specifies a value that is put in the appropriate object.</span></span>
- <span data-ttu-id="262bf-163">Jos **Käytössä**-ominaisuuden lauseke on määritetty palauttamaan suorituksen aikana **Epätosi**, sopivaa objektia ei täytetä luodussa tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="262bf-163">If an expression of the **Enabled** property is configured to return **False** at runtime, the appropriate object won't be filled in in the generated document.</span></span>

<span data-ttu-id="262bf-164">Jos **Solu**-osa on määritetty antamaan solun arvo, se voidaan sitoa tietolähteeseen, joka palauttaa alkeistietotyypin arvon (kuten **Merkkijono**, **Reaaliluku** tai **Kokonaisluku**).</span><span class="sxs-lookup"><span data-stu-id="262bf-164">When a **Cell** component is configured to enter a value in a cell, it can be bound with a data source that returns the value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="262bf-165">Tässä tapauksessa arvo annetaan solussa saman tietotyypin arvona.</span><span class="sxs-lookup"><span data-stu-id="262bf-165">In this case, the value is entered in the cell as a value of the same data type.</span></span>

<span data-ttu-id="262bf-166">Jos **Solu**-osa on määritetty antamaan arvo Excel-muotona, se voidaan sitoa tietolähteeseen, joka palauttaa alkeistietotyypin arvon (kuten **Merkkijono**, **Reaaliluku** tai **Kokonaisluku**).</span><span class="sxs-lookup"><span data-stu-id="262bf-166">When a **Cell** component is configured to enter a value in an Excel shape, it can be bound with a data source that returns a value of a primitive data type (for example, **String**, **Real**, or **Integer**).</span></span> <span data-ttu-id="262bf-167">Tässä tapauksessa arvo annetaan Excel-muodossa kyseisen muodon tekstinä.</span><span class="sxs-lookup"><span data-stu-id="262bf-167">In this case, the value is entered in the Excel shape as the text of that shape.</span></span> <span data-ttu-id="262bf-168">Muissa kuin **Merkkijono**-tietotyypin arvoissa muunto tekstiksi tehdään automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="262bf-168">For values of data types that aren't **String**, the conversion to text is done automatically.</span></span>

> [!NOTE]
> <span data-ttu-id="262bf-169">**Solu**-osan voi määrittää täyttämään muodon vain tapauksissa, joissa muodon tekstiominaisuutta tuetaan.</span><span class="sxs-lookup"><span data-stu-id="262bf-169">You can configure a **Cell** component to fill in a shape only in cases where a shape text property is supported.</span></span>

<span data-ttu-id="262bf-170">Jos **Solu**-osa on määritetty antamaan arvo Excel-kuvana, se voidaan sitoa tietolähteeseen, joka palauttaa kuvan binaarimuodossa ilmaisevan **Säilö**-tyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="262bf-170">When a **Cell** component is configured to enter a value in an Excel picture, it can be bound with a data source that returns a value of the **Container** data type that represents an image in binary format.</span></span> <span data-ttu-id="262bf-171">Tässä tapauksessa arvo annetaan Excel-kuvassa kuvana.</span><span class="sxs-lookup"><span data-stu-id="262bf-171">In this case, the value is entered in the Excel picture as an image.</span></span>

> [!NOTE]
> <span data-ttu-id="262bf-172">Jokainen Excel-kuva ja -muoto katsotaan ankkuroiduksi vasemmasta yläkulmasta tiettyyn Excel-soluun tai -alueeseen.</span><span class="sxs-lookup"><span data-stu-id="262bf-172">Every Excel picture and shape is considered to be anchored by its upper-left corner to a specific Excel cell or range.</span></span> <span data-ttu-id="262bf-173">Jos Excel-kuva tai -muoto halutaan replikoida, se solu tai alue, johon se on ankkuroitu, on määritettävä replikoiduksi soluksi tai alueeksi.</span><span class="sxs-lookup"><span data-stu-id="262bf-173">If you want to replicate an Excel picture or shape, you must configure the cell or range that it's anchored to as a replicated cell or range.</span></span>

<span data-ttu-id="262bf-174">Lisätietoja kuvien ja muotojen upottamisesta on kohdassa [Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="262bf-174">To learn more about how to embed images and shapes, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="page-break-component"></a><span data-ttu-id="262bf-175">Sivunvaihto-osa</span><span class="sxs-lookup"><span data-stu-id="262bf-175">Page break component</span></span>

<span data-ttu-id="262bf-176">**Sivunvaihto**-osa pakottaa Excelin aloittamaan uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="262bf-176">The **PageBreak** component forces Excel to start a new page.</span></span> <span data-ttu-id="262bf-177">Tämä osa ei ole pakollinen, jos haluat käyttää Excelin oletussivusta, mutta sitä kannattaa käyttää, jos haluat Excelin jäsentävän sivutuksen ER-muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="262bf-177">This component isn't required when you want to use Excel's default paging, but you should use it when you want Excel to follow your ER format to structure paging.</span></span>

## <a name="edit-an-added-er-format"></a><span data-ttu-id="262bf-178">Lisätyn ER-muodon muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="262bf-178">Edit an added ER format</span></span>

### <a name="update-a-template"></a><span data-ttu-id="262bf-179">Mallin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="262bf-179">Update a template</span></span>

<span data-ttu-id="262bf-180">Päivitetty malli voidaan tuoda muokattavaan ER-muotoon valitsemalla **Päivitä Excelistä** toimintoruudun **Tuonti**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="262bf-180">You can select **Update from Excel** on the **Import** tab of the Action Pane to import an updated template into an editable ER format.</span></span> <span data-ttu-id="262bf-181">Valitun **Excel\\Tiedosto**-osan malli korvataan uudella mallin tämän prosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="262bf-181">During this process, a template of the selected **Excel\\File** component will be replaced by a new template.</span></span> <span data-ttu-id="262bf-182">Muokattavan ER-muodon sisältö synkronoidaan päivitetyn ER-mallin sisällön kanssa.</span><span class="sxs-lookup"><span data-stu-id="262bf-182">The content of the editable ER format will be synced with the content of the updated ER template.</span></span>

- <span data-ttu-id="262bf-183">Jokaiselle Excel-nimelle luodaan automaattisesti uusi ER-muoto, jos muokattavassa muodossa olevaa ER-muoto-osaa ei löydy.</span><span class="sxs-lookup"><span data-stu-id="262bf-183">A new ER format component will automatically be created for every Excel name if the ER format component isn't found in the editable format.</span></span>
- <span data-ttu-id="262bf-184">Jokainen ER-muoto-osa on poistettava muokattavasta ER-muodosta, jos sille ei löydy sopivaa Excel-nimeä.</span><span class="sxs-lookup"><span data-stu-id="262bf-184">Every ER format component will be deleted from the editable ER format if the appropriate Excel name isn't found for it.</span></span>

> [!NOTE]
> <span data-ttu-id="262bf-185">Jos muokattavaan ER-muotoon halutaan luoda valinnainen **Taulukko**-elementti, määritä **Luo Excel-taulukkomuotoinen elementti** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="262bf-185">Set the **Create Excel Sheet format element** option to **Yes** if you want to create the optional **Sheet** element in the editable ER format.</span></span>
>
> <span data-ttu-id="262bf-186">Jos muokattavassa ER-muoto sisälsi alun perin **Taulukko**-elementtejä, määritä **Luo Excel-taulukkomuotoinen elementti** -asetukseksi **Kyllä** päivitettyä mallia tuotaessa.</span><span class="sxs-lookup"><span data-stu-id="262bf-186">If the editable ER format originally contained **Sheet** elements, we recommend that you set the **Create Excel Sheet format element** option to **Yes** when you import an updated template.</span></span> <span data-ttu-id="262bf-187">Muussa tapauksessa kaikki alkuperäisen **Taulukko**-elementin sisäkkäiset elementit luodaan alusta.</span><span class="sxs-lookup"><span data-stu-id="262bf-187">Otherwise, all nested elements of the original **Sheet** element will be created from scratch.</span></span> <span data-ttu-id="262bf-188">Tämän vuoksi kaikki uudelleenluotujen muotoelementtien sidonnat menetetään päivitetyssä ER-muodossa.</span><span class="sxs-lookup"><span data-stu-id="262bf-188">Therefore, all bindings of the re-created format elements will be lost in the updated ER format.</span></span>

![Luo Excel-taulukkomuotoinen elementti -vaihtoehto Päivitä Excelistä -valintaikkunassa](./media/er-excel-format-update-template.png)

<span data-ttu-id="262bf-190">Lisätietoja tästä toiminnosta on kohdan [Sähköisen raportoinnin muotojen muokkaaminen käyttämällä Excel-malleja uudelleen](modify-electronic-reporting-format-reapply-excel-template.md) ohjeissa.</span><span class="sxs-lookup"><span data-stu-id="262bf-190">To learn more about this feature, follow the steps in [Modify Electronic reporting formats by reapplying Excel templates](modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

## <a name="validate-an-er-format"></a><span data-ttu-id="262bf-191">ER-muodon vahvistaminen</span><span class="sxs-lookup"><span data-stu-id="262bf-191">Validate an ER format</span></span>

<span data-ttu-id="262bf-192">Muokattavaa ER-muotoa vahvistettaessa tehdään yhdenmukaisuustarkistus, jolla varmistetaan, että Excel-nimi esiintyy käytettävässä Excel-mallissa.</span><span class="sxs-lookup"><span data-stu-id="262bf-192">When you validate an ER format that can be edited, a consistency check is done to make sure that the Excel name is present in the Excel template that is currently used.</span></span> <span data-ttu-id="262bf-193">Saat ilmoituksen mahdollisista ristiriidoista.</span><span class="sxs-lookup"><span data-stu-id="262bf-193">You will be notified about any inconsistencies.</span></span> <span data-ttu-id="262bf-194">Joidenkin ristiriitojen osalta tarjotaan mahdollisuutta korjata ongelmat automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="262bf-194">For some inconsistencies, the option to automatically fix issues will be offered.</span></span>

![Vahvistusvirhesanoma](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a><span data-ttu-id="262bf-196">Excel-kaavojen laskemisen hallinta</span><span class="sxs-lookup"><span data-stu-id="262bf-196">Control the calculation of Excel formulas</span></span>

<span data-ttu-id="262bf-197">Kun Microsoft Excel -työkirjamuodossa oleva lähtevä asiakirja luodaan, jotkin tämän asiakirjan solut voivat sisältää Excel-kaavoja.</span><span class="sxs-lookup"><span data-stu-id="262bf-197">When an outbound document in a Microsoft Excel workbook format is generated, some cells of this document might contain Excel formulas.</span></span> <span data-ttu-id="262bf-198">Kun **Ota käyttöön EPPlus-kirjaston sähköinen raportointijärjestelmä** -toiminto on käytössä, voit määrittää, milloin kaavat lasketaan, muuttamalla **Laskentavalinnat**-[parametrin](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) arvoa käytetyssä Excel-mallissa:</span><span class="sxs-lookup"><span data-stu-id="262bf-198">When the **Enable usage of EPPlus library in Electronic reporting framework** feature is enabled, you can control when the formulas are calculated by changing the value of the **Calculation Options** [parameter](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) in the Excel template that is being used:</span></span>

- <span data-ttu-id="262bf-199">Valitse **Automaattinen**, jos haluat laskea kaikki riippuvaiset kaavat uudelleen aina, kun luotu tiedosto liitetään uusilla alueilla, soluissa jne.</span><span class="sxs-lookup"><span data-stu-id="262bf-199">Select **Automatic** to recalculate all dependent formulas every time a generated document is appended by new ranges, cells, etc.</span></span>
    >[!NOTE]
    > <span data-ttu-id="262bf-200">Tämä saattaa aiheuttaa suorituskykyongelman niille Excel-malleille, jotka sisältävät useita toisiinsa liittyviä kaavoja.</span><span class="sxs-lookup"><span data-stu-id="262bf-200">This might cause a performance issue for Excel templates that contain multiple related formulas.</span></span>
- <span data-ttu-id="262bf-201">Valitse **Manuaalinen**, jos haluat välttää kaavojen uudelleenlaskennan, kun asiakirja luodaan.</span><span class="sxs-lookup"><span data-stu-id="262bf-201">Select **Manual** to avoid formula recalculation when a document is generated.</span></span>
    >[!NOTE]
    > <span data-ttu-id="262bf-202">Kaavan uudelleenlaskenta pakotetaan manuaalisesti, kun luotu asiakirja avataan esikatselua varten Excelissä.</span><span class="sxs-lookup"><span data-stu-id="262bf-202">Formula recalculation is manually forced when a generated document is opened for preview using Excel.</span></span>
    > <span data-ttu-id="262bf-203">Älä käytä tätä vaihtoehtoa, jos määrität ER-kohteen, joka olettaa, että luotu tiedosto on käytössä ilman sen esikatselua Excelissä (PDF-muunnos, sähköpostin lähetys jne.) koska luotu tiedosto ei ehkä sisällä kaavoja sisältävien solujen arvoja.</span><span class="sxs-lookup"><span data-stu-id="262bf-203">Don't use this option if you configure an ER destination that assumes the usage of a generated document without its preview in Excel (PDF conversion, emailing, etc.)because the generated document might not contain values in cells that contain formulas.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="262bf-204">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="262bf-204">Additional resources</span></span>

[<span data-ttu-id="262bf-205">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="262bf-205">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="262bf-206">Suunnittele kokoonpano, jolla raportit voi luoda OPENXML-muodossa</span><span class="sxs-lookup"><span data-stu-id="262bf-206">Design a configuration for generating reports in OPENXML format</span></span>](tasks\er-design-reports-openxml-2016-11.md)

[<span data-ttu-id="262bf-207">Sähköisen raportoinnin muotojen muokkaaminen käyttämällä Excel-malleja</span><span class="sxs-lookup"><span data-stu-id="262bf-207">Modify Electronic reporting formats by reapplying Excel templates</span></span>](modify-electronic-reporting-format-reapply-excel-template.md)

[<span data-ttu-id="262bf-208">Vaakasuunnassa laajennettavien alueiden käyttö sarakkeiden dynaamiseen lisäykseen Excel-raportissa</span><span class="sxs-lookup"><span data-stu-id="262bf-208">Use horizontally expandable ranges to dynamically add columns in Excel reports</span></span>](tasks/er-horizontal-1.md)

[<span data-ttu-id="262bf-209">Kuvien ja muotojen upottaminen luomiisi asiakirjoihin ER:n avulla</span><span class="sxs-lookup"><span data-stu-id="262bf-209">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md)

[<span data-ttu-id="262bf-210">Sähköisen raportoinnin (ER) määrittäminen hakemaan tiedot Power BI:hin</span><span class="sxs-lookup"><span data-stu-id="262bf-210">Configure Electronic reporting (ER) to pull data into Power BI</span></span>](general-electronic-reporting-report-configuration-get-data-powerbi.md)
