---
title: Luo tulostettavia FTI-lomakkeita
description: Tässä ohjeaiheessa käsitellään, miten sähköisen raportoinnin (ER) runkoa käsitellään siten, että tulostettavan vapaatekstilaskun (FTI) lomakkeita luodaan Microsoft Office -asiakirjoina.
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: d27a11a0d925b0f1164578f9c04e6abd4736b2b2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "325523"
---
# <a name="generate-printable-fti-forms"></a><span data-ttu-id="5eb67-103">Tulostettavien FTI-lomakkeiden luominen</span><span class="sxs-lookup"><span data-stu-id="5eb67-103">Generate printable FTI forms</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5eb67-104">Sähköisen raportoinnin (ER) runko sallii sinun luoda tulostettavan vapaatekstilaskun (FTI) lomakkeita Microsoft Office -asiakirjoina.</span><span class="sxs-lookup"><span data-stu-id="5eb67-104">The Electronic reporting (ER) framework lets you generate printable free text invoice (FTI) forms as Microsoft Office documents.</span></span> <span data-ttu-id="5eb67-105">Tässä aiheessa on tietoja siitä, miten voit luoda omia konfiguraatioita sekä tietoja käytettävissä olevien kokoonpanomallien yksityiskohdista.</span><span class="sxs-lookup"><span data-stu-id="5eb67-105">This topic provides information about how to build your own configurations as well as details of available configuration templates.</span></span>

## <a name="overview"></a><span data-ttu-id="5eb67-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="5eb67-106">Overview</span></span>

<span data-ttu-id="5eb67-107">Sen lisäksi, että voit olemassa olevan kyvyn avulla tulostaa FTI-lomakkeita käyttämällä Microsoft SQL Server Reporting Servicesiä (SSRS), voit nyt käyttää ER-runkoa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-107">In addition to the existing capability of generating printable FTI forms by using Microsoft SQL Server Reporting Services (SSRS), you can now use the ER framework.</span></span> <span data-ttu-id="5eb67-108">Voit hallita tulostettavia FTI-lomakkeita Microsoft Office Excelissä ja Wordissa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-108">You can manage printable FTI forms in Microsoft Office Excel and Word.</span></span> <span data-ttu-id="5eb67-109">Voit myös muokata asettelua, tietojen kulkua ja muotoilua vaatimustesi mukaan muuttamatta koodia.</span><span class="sxs-lookup"><span data-stu-id="5eb67-109">You can also modify the layout, data flow, and formatting to meet specific requirements without making code changes.</span></span>

> [!NOTE]
> <span data-ttu-id="5eb67-110">Jos haluat aloittaa yleiskuvalla tulostettavien FTI-lomakkeiden ratkaisun olemassa olevista ER-kokoonpanoista, voit siirtyä suoraan osioon **Lataa malli ER-konfiguraatioista tulostettavien FTI-lomakkeiden luomiseksi** myöhemmin tässä ohjeessa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-110">If you want to start with an overview of existing ER configurations for this sample of the printable FTI forms solution, you can go directly to section **Download sample ER configurations to generate printable FTI forms** later in this topic.</span></span>

## <a name="create-customized-configurations-for-fti-printable-forms"></a><span data-ttu-id="5eb67-111">Luo muokatut kokoonpanot FTI-tulostettaville lomakkeille</span><span class="sxs-lookup"><span data-stu-id="5eb67-111">Create customized configurations for FTI printable forms</span></span>
<span data-ttu-id="5eb67-112">Osana räätälöityä ratkaisua tulostettaviin FTI-lomakkeisiin sinun on luotava joukko ER-kokoonpanoja.</span><span class="sxs-lookup"><span data-stu-id="5eb67-112">As part of your customized solution for printable FTI forms, you must create a set of ER configurations.</span></span>

### <a name="configure-the-er-data-model"></a><span data-ttu-id="5eb67-113">ER-kohteiden tietomallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5eb67-113">Configure the ER data model</span></span>
<span data-ttu-id="5eb67-114">Sovelluksesi on sisällytettävä ER-kohteiden tietomallin konfiguraatio, joka sisältää tietomallin, joka kuvaa asiakkaan laskutuskauden yrityksen liiketoiminta-aluetta.</span><span class="sxs-lookup"><span data-stu-id="5eb67-114">Your application must include the ER data model configuration that contains a data model that describes the customer invoicing business domain.</span></span> <span data-ttu-id="5eb67-115">Vaatimuksena on, että tietomallin nimen täytyy olla **CustomersInvoicing**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-115">As a requirement, the name of the data model must be **CustomersInvoicing**.</span></span> <span data-ttu-id="5eb67-116">Saadaksesi lisätietoja siitä, miten suunnitella ER-tietomalleja, katso [Suunnittele sähköisen raportoinnin (ER) verkkotunnukseen perustuva tietomalli](tasks/er-design-domain-specific-data-model-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5eb67-116">For information about how to design ER data models, see [Design a domain-specific data model for electronic reporting (ER)](tasks/er-design-domain-specific-data-model-2016-11.md).</span></span>

### <a name="configure-the-er-model-mapping"></a><span data-ttu-id="5eb67-117">ER-tietomallien kartoituksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5eb67-117">Configure the ER model mapping</span></span>
<span data-ttu-id="5eb67-118">Sovelluksessasi on oltava ER-tietomallien kartoitus CustomersInvoicing-tietomallia varten.</span><span class="sxs-lookup"><span data-stu-id="5eb67-118">Your application must include the ER model mapping for the CustomersInvoicing data model.</span></span> <span data-ttu-id="5eb67-119">Mallin määritys voi olla joko ER-tietomallin konfiguraatio tai ER-tietomallin kartoituksen konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="5eb67-119">The model mapping can be in either the ER data model configuration or the ER model mapping configuration.</span></span> <span data-ttu-id="5eb67-120">Joka tapauksessa mallikartoituksen juuren kuvaajan nimen on oltava **FreeTextInvoice**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-120">However, the name of the root descriptor of the model mapping must be **FreeTextInvoice**.</span></span>

<span data-ttu-id="5eb67-121">Kartoituksen tulee sisältää seuraavat tietolähteet:</span><span class="sxs-lookup"><span data-stu-id="5eb67-121">The mapping must contain the following data sources:</span></span>

- <span data-ttu-id="5eb67-122">Tietolähteen tyyppi: **Taulukkotietueet**</span><span class="sxs-lookup"><span data-stu-id="5eb67-122">Data source type: **Table records**</span></span>

    - <span data-ttu-id="5eb67-123">Tämän tietolähteen nimen on oltava **CustInvoiceJour**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-123">This data source must be named **CustInvoiceJour**.</span></span>
    - <span data-ttu-id="5eb67-124">Sen on viitattava CustInvoiceJour-sovellustaulukkoon.</span><span class="sxs-lookup"><span data-stu-id="5eb67-124">It must refer to the CustInvoiceJour application table.</span></span>
    - <span data-ttu-id="5eb67-125">Sitä käytetään ajon aikana siirryttäessä sovelluksesta ER-malliin, joka kartoittaa luettelon laskuista, jotka on valittu tulostettavaksi.</span><span class="sxs-lookup"><span data-stu-id="5eb67-125">It's used at runtime to pass from the application to the ER model mapping the list of invoices that have been selected for printing.</span></span>

- <span data-ttu-id="5eb67-126">tietolähteen tyyppi: **Esine**</span><span class="sxs-lookup"><span data-stu-id="5eb67-126">Data source type: **Object**</span></span>

    - <span data-ttu-id="5eb67-127">Tämän tietolähteen nimen on oltava **PrintMgmtPrintSettingDetail**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-127">This data source must be named **PrintMgmtPrintSettingDetail**.</span></span>
    - <span data-ttu-id="5eb67-128">Sen on viitattava **PrintMgmtPrintSettingDetail** -sovellusluokkaan.</span><span class="sxs-lookup"><span data-stu-id="5eb67-128">It must refer to the **PrintMgmtPrintSettingDetail** application class.</span></span>
    - <span data-ttu-id="5eb67-129">Sitä käytetään ajon aikana siirrettäessä sovelluksesta ER-mallin tarkat kartoitustiedot tulostuksen hallinnan asetuksista ER-muotoon, joka on käynnissä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-129">It's used at runtime to pass from the application to the ER model mapping details of the print management settings for the ER format that is running.</span></span>

<span data-ttu-id="5eb67-130">Sovelluksen integrointi ER - kehykseen löytyy **ERPrintMgmtReportFormatSubscriber** -luokasta (ER Application Suite -integraation malli) sovelluksen lähdekoodissa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-130">The details of the application integration with the ER framework can be found in the **ERPrintMgmtReportFormatSubscriber** class (ER Application Suite integration model) in the source code of the application.</span></span>

<span data-ttu-id="5eb67-131">Lisätietoja ER-mallikartoitusten suunnittelusta, katso [Määritä mallikartoitus ja valitse tietolähteet sähköiseen raportointiin (ER)](tasks/er-define-model-mapping-select-data-sources-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5eb67-131">For more information about the design of ER model mappings, see [Define model mapping and select data sources for electronic reporting (ER)](tasks/er-define-model-mapping-select-data-sources-2016-11.md).</span></span>

### <a name="configure-the-er-format"></a><span data-ttu-id="5eb67-132">ER-muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5eb67-132">Configure the ER format</span></span>
<span data-ttu-id="5eb67-133">Sovellusesiintymässäsi sinulla on oltava ER-muotokonfiguraatio, jota käytetään, kun luodaan FTI-lomakkeita.</span><span class="sxs-lookup"><span data-stu-id="5eb67-133">In your application instance, you must have the ER format configuration that will be used to generate FTI forms.</span></span> 

> [!NOTE]
> <span data-ttu-id="5eb67-134">Tämä muotoiluasetus on luotava CustomersInvoicing-tietomallissa ja sen on käytettävä mallinkartoitusta, jolla on **FreeTextInvoice**-juuren kuvaaja.</span><span class="sxs-lookup"><span data-stu-id="5eb67-134">This format configuration must be created for the CustomersInvoicing data model, and it must use the model mapping that has the **FreeTextInvoice** root descriptor.</span></span>

<span data-ttu-id="5eb67-135">Lisätietoja siitä, miten konfiguroida ER-malleja, katso [Luo muotoiluasetus sähköiselle raportoinnille (ER)](tasks/er-format-configuration-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5eb67-135">For information about how to configure ER formats, see [Create a format configuration for electronic reporting (ER)](tasks/er-format-configuration-2016-11.md).</span></span> <span data-ttu-id="5eb67-136">Lisätietoja siitä, miten suunnitella ER-malleja, joilla voi luoda raportteja OpenXML-muodossa, katso [Suunnittele asetus, jonka avulla voi luoda raportteja OpenXML-muodossa sähköiseen raportointiin (ER)](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="5eb67-136">For information about how to design ER formats to generate reports in OpenXML format, see [Design a configuration for generating reports in OpenXML format for electronic reporting (ER)](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="configure-print-management"></a><span data-ttu-id="5eb67-137">Tulostuksenhallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5eb67-137">Configure print management</span></span>
<span data-ttu-id="5eb67-138">Voit luoda FTI-lomakkeita ER-kehyksen avulla käyttämällä ER-muotoja samalla tavalla kuin SSRS-raportteja.</span><span class="sxs-lookup"><span data-stu-id="5eb67-138">To generate FTI forms by using the ER framework, you can assign ER formats in the same way that you assign SSRS reports.</span></span> <span data-ttu-id="5eb67-139">Voit liittää ER-mallin myyntisaamisten FTI:t , katso **Myyntisaamiset** \> **Asetukset** \> **Lomakkeet** \> **Lomakkeiden asetukset** \> **Yleinen** \> **Tulostuksen hallinta** \> **Vapaatekstilasku** \> **Alkuperäinen**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-139">To associate the ER format with all Accounts receivable FTIs, go to **Accounts receivable** \> **Setup** \> **Forms** \> **Form setup** \> **General** \> **Print management** \> **Free text invoice** \> **Original**.</span></span> <span data-ttu-id="5eb67-140">Voit yhdistää ER-muodon tiettyyn asiakkaaseen tai laskuun noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="5eb67-140">To associate the ER format with a specific customer or invoice, follow these steps.</span></span>

1. <span data-ttu-id="5eb67-141">Siirry kohtaan **Myyntisaamiset** \> **Laskut** \> **Kaikki vapaatekstilaskut**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-141">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="5eb67-142">Valitse FTI, joka yhdistetään ER-muotoon, ja avaa **Tulostuksenhallinnan asetukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="5eb67-142">Select the FTI to associate the ER format with, and open the **Print management setup** page.</span></span>
3. <span data-ttu-id="5eb67-143">Määritä soveltamisala valitsemalla asiakirjataso laskujen käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="5eb67-143">Select the document level to specify the scope of invoices for processing.</span></span>
4. <span data-ttu-id="5eb67-144">Valitse ER-muoto määrätyn asiakirjatason mukaan</span><span class="sxs-lookup"><span data-stu-id="5eb67-144">Select the ER format for the specified document level.</span></span>

![Tulostuksenhallinnan asetukset](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> <span data-ttu-id="5eb67-146">Vain ER-muodot, jotka käyttävät **FreeTextInvoice**-juuren kuvaajaa **CustomersInvoicing** -tietomallia näkyvät **Raportin muodon haku** -kentässä valitulle muodolle.</span><span class="sxs-lookup"><span data-stu-id="5eb67-146">Only ER formats that use the **FreeTextInvoice** root descriptor of the **CustomersInvoicing** data model appear in the **Report format lookup** field for the selected format.</span></span>

## <a name="generate-fti-forms"></a><span data-ttu-id="5eb67-147">Luo FTI-lomakkeet</span><span class="sxs-lookup"><span data-stu-id="5eb67-147">Generate FTI forms</span></span>
<span data-ttu-id="5eb67-148">FTI-lomakkeet luodaan käyttämällä ER-muotoja samaan tapaan kuin SSRS-raportit muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="5eb67-148">FTI forms are generated in the ER framework in the same way that SSRS reports are generated.</span></span>

<span data-ttu-id="5eb67-149">Luodaksesi FTI-lomakkeita, voit valita laskut joko alueen tai valinnan mukaan.</span><span class="sxs-lookup"><span data-stu-id="5eb67-149">To generate FTI forms, you can select invoices either by range or by selection.</span></span> 

![Laskuvalinta](media/FTIbyGER-InvoiceSelection.png)

![Laskun esikatselu](media/FTIbyGER-InvoiceExcelPreview.png)

<span data-ttu-id="5eb67-152">Kun käytät ER-muotoja tulostamalla FTI-lomakkeita tällä tavalla, käytetään oletusarvoisia ER-tiedostojen kohteita.</span><span class="sxs-lookup"><span data-stu-id="5eb67-152">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="5eb67-153">Et voi muuttaa kohdetta.</span><span class="sxs-lookup"><span data-stu-id="5eb67-153">You can't change the destination.</span></span> <span data-ttu-id="5eb67-154">Lisätietoja siitä, miten konfiguroida ER-malleja, katso [Luo muotoiluasetus sähköisen raportoinnin kohteille (ER)](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="5eb67-154">For more information about how to configure the ER destinations for ER formats, see [Electronic reporting destinations](electronic-reporting-destinations.md).</span></span>

<span data-ttu-id="5eb67-155">Voit myös luoda FTI-lomakkeita, kun lähetät FTI:n, laittamalla valinnan **Tulosta lasku** päälle ja laittamalla **Käytä tulostuksen hallintakohteet** pois päältä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-155">You can also generate FTI forms when you post an FTI, by turning **Print invoice** on and turning **Use print management destinations** off.</span></span>

> [!NOTE]
> <span data-ttu-id="5eb67-156">Kun käytät ER-muotoja tulostamalla FTI-lomakkeita tällä tavalla, käytetään oletusarvoisia ER-tiedostojen kohteita.</span><span class="sxs-lookup"><span data-stu-id="5eb67-156">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="5eb67-157">Voit muuttaa oletuskohteen ajon aikana, jos kohde on jo määritetty.</span><span class="sxs-lookup"><span data-stu-id="5eb67-157">You can change the default destination at runtime if the destination has already been configured.</span></span> <span data-ttu-id="5eb67-158">Muuttaaksesi kohdetta sinulla on oltava seuraava suojauksen etuoikeus:</span><span class="sxs-lookup"><span data-stu-id="5eb67-158">To change the destination, you must have the following security privilege:</span></span>
>
> - <span data-ttu-id="5eb67-159">**Nimi:** ERFormatDestinationRuntimeMaintain</span><span class="sxs-lookup"><span data-stu-id="5eb67-159">**Name:** ERFormatDestinationRuntimeMaintain</span></span>
> - <span data-ttu-id="5eb67-160">**Otsikko:** Ylläpidä sähköisen raportoinnin muodon kohdetta ajon aikana</span><span class="sxs-lookup"><span data-stu-id="5eb67-160">**Label:** Maintain electronic reporting format destination during runtime</span></span>

![Sähköisen raportoinnin kohde](media/FTIbyGER-ERFileDestinationSetting.png)

![Sähköisen raportoinnin muodon kohde](media/FTIbyGER-ERFileDestinationUsage.png)

<span data-ttu-id="5eb67-163">ER-kehys tukee tällä hetkellä seuraavia kohteita tuotetuille asiakirjoille:</span><span class="sxs-lookup"><span data-stu-id="5eb67-163">The ER framework currently supports the following destinations for generated documents:</span></span>

- <span data-ttu-id="5eb67-164">**Ladattu tiedosto** – Luodut lomakkeet ovat käytettävissä myös kuin ladattavat tiedostot tallennetaan selaimella.</span><span class="sxs-lookup"><span data-stu-id="5eb67-164">**Downloaded file** – Generated forms are offered as downloads that you can save by using the browser.</span></span>
- <span data-ttu-id="5eb67-165">**Näyttö** – Microsoft Office 365 Exceliä käytetään FTI-lomakkeiden esikatseluun Excel-muodossa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-165">**Screen** – Microsoft Office 365 Excel is used to preview generated FTI forms in Excel format.</span></span>
- <span data-ttu-id="5eb67-166">**SharePoint-kansio** – Luodut lomakkeet tallennetaan asiakirjojen hallintajärjestelmän asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="5eb67-166">**SharePoint folder** – Generated forms are stored based on the settings of the Document management framework.</span></span>
- <span data-ttu-id="5eb67-167">**Sovellusarkisto** – Luodut lomakkeet tallennetaan liitteinä suorituslokin tietueina Microsoft Azure -varastoon.</span><span class="sxs-lookup"><span data-stu-id="5eb67-167">**Application archive** – Generated forms are stored as attachments of execution log records in the Microsoft Azure Storage.</span></span>
- <span data-ttu-id="5eb67-168">**Sähköposti** – Luodut lomakkeet lähetetään sähköpostiliitteinä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-168">**Email** – Generated forms are sent as email attachments.</span></span>

> [!NOTE]
> <span data-ttu-id="5eb67-169">Et voi lähettää FTI-lomakkeita, jotka on luotu suoraan tulostimeen, koska Dynamics-tulostusreititysagenttia käyttävää suoraa tulostusta ei tällä hetkellä tueta.</span><span class="sxs-lookup"><span data-stu-id="5eb67-169">You can't send the FTI forms that are generated directly to the printer, because direct printing that uses the Dynamics Printer Routing Agent isn't currently supported.</span></span>

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a><span data-ttu-id="5eb67-170">Lataa esimerkki ER-kokoonpanoista tulostettavien FTI-lomakkeiden luomiseksi</span><span class="sxs-lookup"><span data-stu-id="5eb67-170">Download sample ER configurations to generate printable FTI forms</span></span>
<span data-ttu-id="5eb67-171">Voit ladata esimerkkejä ER-kokoonpanoista käytettäväksi mallina FTI-ratkaisussasi.</span><span class="sxs-lookup"><span data-stu-id="5eb67-171">You can download sample ER configurations to use as a template for your FTI solution.</span></span> <span data-ttu-id="5eb67-172">Konfiguraatiot tallennetaan jaettujen käyttöomaisuuksien kirjastossa Microsoft Dynamics Lifecycle Services:ssä (LCS).</span><span class="sxs-lookup"><span data-stu-id="5eb67-172">The configurations are stored in the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5eb67-173">Konfiguraatioihin sisältyy:</span><span class="sxs-lookup"><span data-stu-id="5eb67-173">The configurations include:</span></span>

- <span data-ttu-id="5eb67-174">**Asiakaslaskutusmalli** Konfiguraatio sisältää määritettävän tietomallin ja mallin määrityksen.</span><span class="sxs-lookup"><span data-stu-id="5eb67-174">The **Customer invoicing model** configuration contains the required data model and model mapping.</span></span>
- <span data-ttu-id="5eb67-175">**Asiakkaan FTI-raportti (GER)** konfiguraatio sisältää esimerkkimallin.</span><span class="sxs-lookup"><span data-stu-id="5eb67-175">The **Customer FTI report (GER)** configuration contains the sample format.</span></span>

> [!NOTE]
> <span data-ttu-id="5eb67-176">Nämä kokoonpanot on luotu näytteiksi selventämään mahdollisia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="5eb67-176">These configurations have been created as samples to help clarify possible scenarios.</span></span> <span data-ttu-id="5eb67-177">Näiden kokoonpanojen tulevaisuus riippuu tämän arvioinnin tuloksista ja vastaanotetusta palautteesta.</span><span class="sxs-lookup"><span data-stu-id="5eb67-177">The future of these configurations depends on the results of this evaluation and any feedback that is received.</span></span>

### <a name="features-that-are-implemented-in-the-sample-er-format"></a><span data-ttu-id="5eb67-178">Ominaisuuksia, jotka ovat käytössä ER-esimerkkimuodossa</span><span class="sxs-lookup"><span data-stu-id="5eb67-178">Features that are implemented in the sample ER format</span></span>
<span data-ttu-id="5eb67-179">ER-formaatin näytteessä Excel-tiedostoa käytetään mallina FTI-lomakkeiden luomiseen.</span><span class="sxs-lookup"><span data-stu-id="5eb67-179">In the sample ER format configuration, an Excel file is used as a template to generate FTI forms.</span></span>

![Muodon suunnittelija](media/FTIbyGER-ERFormat.png)

<span data-ttu-id="5eb67-181">Tällä hetkellä tämä ER-muoto tukee seuraavia ominaisuuksia luoda FTI-lomakkeita:</span><span class="sxs-lookup"><span data-stu-id="5eb67-181">Currently, this sample ER format supports the following features to generate FTI forms:</span></span>

- <span data-ttu-id="5eb67-182">FTI-lomakkeet on muodostettu sekä alkuperäisiä kirjattuja laskuja, että alkuperäisiä laskuja varten, joita ei ole vielä kirjattu.</span><span class="sxs-lookup"><span data-stu-id="5eb67-182">FTI forms are generated for both original invoices that have been posted and original invoices that haven't yet been posted.</span></span> <span data-ttu-id="5eb67-183">Korjattuja laskujen ja hyvityslaskuja ei tueta.</span><span class="sxs-lookup"><span data-stu-id="5eb67-183">Corrected invoices and credit notes aren't supported.</span></span>
- <span data-ttu-id="5eb67-184">FTI-lomakkee on luotu laskun kielellä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-184">FTI forms are generated in the invoice language.</span></span> <span data-ttu-id="5eb67-185">Luotujen lomakkeiden arvojen ja päivämäärien muoto perustuu käyttäjän asiakkaan paikallisverkon asetuksiin.</span><span class="sxs-lookup"><span data-stu-id="5eb67-185">The format of values and dates in the generated forms is based on the settings of the user's client locale.</span></span>
- <span data-ttu-id="5eb67-186">Luodut laskut näyttävät tietojen virheilmoituksia, jos käsiteltävissä laskuissa ei ole rivejä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-186">Generated invoices show data unavailability notifications if there are no lines in the invoices that are processed.</span></span>
- <span data-ttu-id="5eb67-187">Luodut laskutusotsikot perustuvat paperimuotoon, joka on valittu FTI-lomakkeelle **Myyntisaamiset**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="5eb67-187">Generated invoice headers are based on the paper format that has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="5eb67-188">Yrityksen tiedot näkyvät luodun laskun lomakkeen otsikossa vain, jos paperimuoto on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-188">Company details appear in the header of the generated invoice form only if the paper format is blank.</span></span>
- <span data-ttu-id="5eb67-189">Luodut laskulomakkeet näyttävät yritykselle ja asiakkaalle verovapaita numeroita, kun FTI-lomakkeelle on valittu oikea vaihtoehto **Myyntisaamisten parametrit** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="5eb67-189">Generated invoice forms show company and customer tax exempt numbers when the appropriate option has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="5eb67-190">Luotujen laskujen rivit ja laskun kokonaissummat näyttävät oletuslaskun rahalliset tiedot laskun rekisteröintivaluutassa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-190">The generated invoice lines and invoice totals sections show the default invoice's monetary details in the invoice registration currency.</span></span>
- <span data-ttu-id="5eb67-191">luodun laskun kokonaismäärän osa voi näyttää rahallisia tietoja eurovaluutasta ja laskujen rekisteröintivaluutasta, kun **Tulosta summa euroina** -vaihtoehto on otettu käyttöön **Myyntisaamisten parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5eb67-191">The generated invoice totals section can show monetary details in the euro currency and the invoice registration currency when the **Print amount in currency representing the euro** option is enabled on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="5eb67-192">Luodut laskulomakkeet näyttävät kaikki saatavilla olevat prosessilaskuilmoitukset **Myyntisaamisten parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5eb67-192">Generated invoice forms show any process invoice notes that are available, based on settings on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="5eb67-193">Huomautukset sisältyvät sekä koko laskuun että jokaisen laskun riville.</span><span class="sxs-lookup"><span data-stu-id="5eb67-193">Notes are included for both the whole invoice and each invoice line.</span></span>
- <span data-ttu-id="5eb67-194">Luodut laskulomakkeet sisältävät asiakkaan FTI-lomakkeen ja laskutuskielet, kun ne on määritetty AR-lomakkeiden luetteloon.</span><span class="sxs-lookup"><span data-stu-id="5eb67-194">Generated invoice forms include notes for the customer FTI form and the processing invoice language when they have been configured in the AR form notes list.</span></span>
- <span data-ttu-id="5eb67-195">Tulostusasetusten mukaan tuotetuissa laskuissa on mukautettu alatunnistekirja, kun se on määritetty laskutuskielen, ER-muodon ja FTI-asiakirjan soveltamisalueelle.</span><span class="sxs-lookup"><span data-stu-id="5eb67-195">Depending on the Print management settings, generated invoices include custom footer text when it has been configured for the invoice language, the ER format, and the FTI document scope.</span></span>
- <span data-ttu-id="5eb67-196">Luotujen laskujen lomakkeiden kokonaissumma sisältää käytettävissä olevat kassa-alennustiedot.</span><span class="sxs-lookup"><span data-stu-id="5eb67-196">The totals section of generated invoice forms includes any cash discount information that is available.</span></span>
- <span data-ttu-id="5eb67-197">Luotujen laskujen lomakkeiden maksutietoryhmä sisältää mahdolliset käytettävissä olevat maksuaikataulun yksityiskohdat.</span><span class="sxs-lookup"><span data-stu-id="5eb67-197">The payment schedule section of generated invoice forms includes any payment schedule details that are available.</span></span>
- <span data-ttu-id="5eb67-198">Luotujen laskujen lomakkeiden merkintäosuus sisältää kaikki tehdyt maksutapahtumat.</span><span class="sxs-lookup"><span data-stu-id="5eb67-198">The markup section of generated invoice forms includes any charges transactions that are available.</span></span>
- <span data-ttu-id="5eb67-199">Luodut laskulomakkeet sisältävät myyntiverotiedot **Myyntimääritelmä**-asetuksen **Myyntisaamisten parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5eb67-199">Generated invoice forms include sales tax details, based on the **Sales tax specification** setting on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="5eb67-200">Tämä osio voi näyttää verotiedot joko vain laskun rekisteröintivaluutassa tai laskurekisteröintivaluutassa ja yrityksen kirjanpitoarvossa samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="5eb67-200">This section can show tax details either in the invoice registration currency only, or in the invoice registration currency and the company accounting currency at the same time.</span></span>
- <span data-ttu-id="5eb67-201">Luodut laskulomakkeet näyttävät suoraveloitusilmoituksen yksityiskohtia.</span><span class="sxs-lookup"><span data-stu-id="5eb67-201">Generated invoice forms show direct debit notification details.</span></span> <span data-ttu-id="5eb67-202">Esimerkiksi he osoittavat, milloin laskuille on valittu maksutapa, jolla on pakollinen suoraveloitusvaltuutuksen tunnus, kun käsittelylasku on rekisteröity eurovaluutalla ja kun laskuille on määritetty suoraveloitusvaltuutuksen tunnusnumero.</span><span class="sxs-lookup"><span data-stu-id="5eb67-202">For example, they show when the method of payment that has the mandatory direct debit mandate ID was selected for the invoice, when the processing invoice was registered in the euro currency, and when the direct debit mandate ID was defined for the invoice.</span></span>
- <span data-ttu-id="5eb67-203">Luodut laskut näyttävät kaikki ennakkomaksutiedot, jotka ovat saatavilla lähetetyille laskuille.</span><span class="sxs-lookup"><span data-stu-id="5eb67-203">Generated invoices show any prepayment details that are available for posted invoices.</span></span>
- <span data-ttu-id="5eb67-204">Luodut laskulomakkeet voidaan lähettää sähköpostiviestin liitteenä laskuasiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="5eb67-204">Generated invoice forms can be sent to an invoice customer as an email attachment.</span></span> <span data-ttu-id="5eb67-205">Asianmukaisen ER-tiedoston määränpää on määritettävä käytettävän ER-muotoon.</span><span class="sxs-lookup"><span data-stu-id="5eb67-205">The appropriate ER file destination should be configured for the ER format that is being used.</span></span>

### <a name="countryregion-specific-features"></a><span data-ttu-id="5eb67-206">Maa-/aluekohtaiset ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="5eb67-206">Country/region-specific features</span></span> 
<span data-ttu-id="5eb67-207">ER-muotoon on sisällytetty seuraavat maa- tai aluekohtaiset ominaisuudet, jotka osoittavat, kuinka erityisiä vaatimuksia voidaan käsitellä ER-kokoonpanoissa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-207">The following country/region-specific features are included in the sample ER format to show how specific requirements can be handled in ER configurations.</span></span>

#### <a name="norway"></a><span data-ttu-id="5eb67-208">Norja</span><span class="sxs-lookup"><span data-stu-id="5eb67-208">Norway</span></span>
<span data-ttu-id="5eb67-209">Yritysrekisterin termi asetetaan luodun laskusivun otsikkoon, kun lasku käsitellään oikeussubjektille, joka on konfiguroitu seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="5eb67-209">The Enterprise register term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="5eb67-210">Norjan maa/alue-konteksti käytössä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-210">The country/region context for Norway is used.</span></span>
- <span data-ttu-id="5eb67-211">**Tulosta Foretaksregisteret** -parameteri on aktiivinen myyntidokumenteissa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-211">The **Print Foretaksregisteret** parameter is active on sales documents.</span></span>

#### <a name="spain"></a><span data-ttu-id="5eb67-212">Espanja</span><span class="sxs-lookup"><span data-stu-id="5eb67-212">Spain</span></span>
<span data-ttu-id="5eb67-213">**Kassaperusteisen kirjanpitomenetelmän erityisjärjestelmä** -termi asetetaan luodun laskusivun otsikkoon, kun lasku käsitellään oikeussubjektille, joka on määritetty seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5eb67-213">The **Special regime for cash accounting method** term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="5eb67-214">Espanjan maa/alue-konteksti käytössä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-214">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="5eb67-215">Kassaperusteisen kirjanpitojärjestelmän erityisjärjestelmä on otettu käyttöön laskujen käsittelypäivänä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-215">The special regime for the cash accounting method is enabled on the invoice processing date.</span></span>

<span data-ttu-id="5eb67-216">Kun käytettävissä on kassa-alennuksen yksityiskohdat, kuten kassa-alennusmäärä ja laskutilin nettomäärä, ne esitetään laskutetun lomakkeen laskun kokonaissummassa, kun se on käsitelty oikeussubjektille, joka on määritetty seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5eb67-216">When cash discount details, such as the cash discount amount and invoice line net amount, are available, they are presented in the invoice totals section of the generated invoice form when it has been processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="5eb67-217">Espanjan maa/alue-konteksti käytössä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-217">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="5eb67-218">**Laskuun lasketaan käteisalennus** on päällä laskuvaihtoehdossa (**Yleiset pääkirjaparametrit** \> **Myyntivero**).</span><span class="sxs-lookup"><span data-stu-id="5eb67-218">**Cash discount is applied in the invoice** is turned on in the invoice option (**General ledger parameters** \> **Sales tax section**).</span></span>

#### <a name="italy"></a><span data-ttu-id="5eb67-219">Italia</span><span class="sxs-lookup"><span data-stu-id="5eb67-219">Italy</span></span>
<span data-ttu-id="5eb67-220">Tavaroiden alennusluku sisältyy laskutetun laskun laskutuslinjoihin, kun sitä käsitellään oikeussubjektille, joka on määritetty käyttäen maa- tai aluekontekstia Italiassa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-220">The goods discount mark is included on the invoice lines of the generated invoice when it's being processed for a legal entity that is configured using the country/region context for Italy.</span></span>

#### <a name="finland"></a><span data-ttu-id="5eb67-221">Suomi</span><span class="sxs-lookup"><span data-stu-id="5eb67-221">Finland</span></span>
<span data-ttu-id="5eb67-222">Luotujen laskujen lomakkeen lisäksi Giron rahansiirtolomakkeita voidaan tuottaa seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="5eb67-222">In addition to the generated invoice form, Giro money transfer slips can be generated as follows:</span></span>

- <span data-ttu-id="5eb67-223">Sellaiselle oikeushenkilölle, joka käyttää maata/aluekonttoria Suomelle ja jolla on vähintään yksi pankkitili, joka on merkitty nimellä **Giro-tili** ja **Pankkikoodi**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-223">For the legal entity that uses the country/region context for Finland, and that has at least one bank account that is marked as **Giro account** and **Bank bar code**.</span></span> 
- <span data-ttu-id="5eb67-224">Laskusta, joka on merkitty vaaditulla tavalla **suomalainen** liittyvä maksuliike.</span><span class="sxs-lookup"><span data-stu-id="5eb67-224">For an invoice that is marked as required for the **Finnish** associated payment attachment.</span></span>

![Tilisiirtolomake](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> <span data-ttu-id="5eb67-226">Esimerkki ER-muodosta on konfiguroitu valinnaisesti generoimaan Giron rahansiirtoliput erillisessä laskentataulukossa.</span><span class="sxs-lookup"><span data-stu-id="5eb67-226">The sample ER format has been configured to optionally generate the Giro money transfer slips in the separate worksheet.</span></span>

> [!NOTE]
> <span data-ttu-id="5eb67-227">Sinun on ensin asennettava fontti, jota käytetään viivakoodin generoimiseen paikallisessa koneessa, jossa esitelty Excel-muodossa luotu laskulomake.</span><span class="sxs-lookup"><span data-stu-id="5eb67-227">You must first install the font that is used to generate the bar code on the local machine where the generated invoice form in Excel format will be previewed.</span></span>

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a><span data-ttu-id="5eb67-228">Määritä sähköpostien kohteet ER-formaatin avulla</span><span class="sxs-lookup"><span data-stu-id="5eb67-228">Use the sample ER format to configure email destinations</span></span>
<span data-ttu-id="5eb67-229">Käytä seuraavia elementtejä ER-muotoa sähköpostiosoitteiden määrittämiseen:</span><span class="sxs-lookup"><span data-stu-id="5eb67-229">Use the following elements of the sample ER format to configure email destinations:</span></span>

- <span data-ttu-id="5eb67-230">Asiakkaan yhteyshenkilön sähköpostiosoitetta voi käyttää seuraavan ER-lausekkeen kautta: **model.InvoiceBase.Contact.ElectronicMail**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-230">The email address of a customer contact can be accessed through the following ER expression: **model.InvoiceBase.Contact.ElectronicMail**.</span></span>
- <span data-ttu-id="5eb67-231">Sähköpostiaiheen tekstiä voi käyttää seuraavan ER-lausekkeen kautta: **Emailing.TxtToUse.Subject**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-231">The email subject text can be accessed through the following ER expression: **Emailing.TxtToUse.Subject**.</span></span>
- <span data-ttu-id="5eb67-232">Sähköpostielimen tekstiä voi käyttää seuraavan ER-lausekkeen kautta: **Emailing.TxtToUse.Body**.</span><span class="sxs-lookup"><span data-stu-id="5eb67-232">The email body text can be accessed through the following ER expression: **Emailing.TxtToUse.Body**.</span></span>

![Kohdeasetukset](media/FTIbyGER-ERFileDestinationSettingEmail.png)

<span data-ttu-id="5eb67-234">Sähköpostin aiheen ja kehon oletusteksti on määritetty ER-mallinäytteessä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-234">The default text of the email's subject and body is defined in the sample ER format.</span></span> <span data-ttu-id="5eb67-235">Kieli määräytyy lomakkeen etiketeistä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-235">The language depends on the format's labels.</span></span> <span data-ttu-id="5eb67-236">Tätä oletustekstiä käytetään sähköpostiviesteissä, jos muokattua organisaation sähköpostimallia, jolla on ennalta määritetty **ERFTITMP**-tunnus, ei ole lisätty..</span><span class="sxs-lookup"><span data-stu-id="5eb67-236">This default text will be used for emails if a custom organization email template that has the predefined **ERFTITMP** ID hasn't been added.</span></span>

> [!NOTE]
> <span data-ttu-id="5eb67-237">**ERFTITMP** sähköpostimallin tunnus on määritetty ER-mallinäytteessä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-237">The **ERFTITMP** email template ID has been defined in the sample ER format.</span></span> <span data-ttu-id="5eb67-238">Sitä voidaan muuttaa tarpeen mukaan uudessa ER-muodossa, joka on luotu tästä otosmuodosta.</span><span class="sxs-lookup"><span data-stu-id="5eb67-238">It can be changed as required in a new ER format that is created from this sample format.</span></span>

<span data-ttu-id="5eb67-239">Jos organisaation sähköpostimalli on ennalta määritetty **ERFTITMP** ID-tunnus on lisätty oikeushenkilölle, jolle käsittelyt laskut on, sähköpostiviestin mallia ja kehon tekstiä käytetään sähköpostin luomiseen.</span><span class="sxs-lookup"><span data-stu-id="5eb67-239">If the organization email template that has the predefined **ERFTITMP** ID has been added for the legal entity that you're processing the invoice for, the template for the email subject and body text will be used to generate the email.</span></span> 

![Organisaation sähköpostimallit](media/FTIbyGER-EmailTemplate.png)

![Lataa sähköpostimalli](media/FTIbyGER-EmailTemplateBody.png)

<span data-ttu-id="5eb67-242">**Emailing.TxtToUse.Subject**-näytteen ER-muotoinen ER-lauseke on määritetty korvaamaan paikkamerkin %1 mahdolliset esiintymät käsittelylaskun tunnuksella.</span><span class="sxs-lookup"><span data-stu-id="5eb67-242">The **Emailing.TxtToUse.Subject** ER expression of the sample ER format is configured to replace any occurrences of the placeholder %1 by the processing invoice ID.</span></span>

<span data-ttu-id="5eb67-243">**Emailing.TxtToUse.Body** näyteformaatin lauseke on määritetty paikanvaraajille seuraaville korvauksille:</span><span class="sxs-lookup"><span data-stu-id="5eb67-243">The **Emailing.TxtToUse.Body** expression of the sample format is configured for the following substitutions for placeholders:</span></span>

- <span data-ttu-id="5eb67-244">%1 korvataan asiakkaan yhteyshenkilön nimellä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-244">"%1" is replaced with the name of the customer's contact person.</span></span>
- <span data-ttu-id="5eb67-245">%2 korvataan yrityksen nimellä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-245">"%2" is replaced with the company name.</span></span>
- <span data-ttu-id="5eb67-246">%3 korvataan asiakkaan nimellä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-246">"%3" is replaced with the customer name.</span></span>
- <span data-ttu-id="5eb67-247">%4 korvataan yrityksen yhteyshenkilön nimellä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-247">"%4" is replaced with the name of the company's contact person.</span></span>
- <span data-ttu-id="5eb67-248">%5 korvataan yrityksen yhteyshenkilön tittelillä.</span><span class="sxs-lookup"><span data-stu-id="5eb67-248">"%5" is replaced with the job title of the company's contact person.</span></span>
- <span data-ttu-id="5eb67-249">%6 korvataan yrityksen yhteyshenkilön sähköpostiosoitteella.</span><span class="sxs-lookup"><span data-stu-id="5eb67-249">"%6" is replaced with the email address of the company's contact person.</span></span>

![Sähköposti](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a><span data-ttu-id="5eb67-251">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5eb67-251">Additional resources</span></span>
[<span data-ttu-id="5eb67-252">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5eb67-252">Electronic reporting overview</span></span>](general-electronic-reporting.md)
