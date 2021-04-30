---
title: Tavujärjestysmerkkejä luoduissa tiedostoissa estävien ER-määritysten suunnitteleminen
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) muotojen määrittäminen luomaan raportteja, jotka estävät tavujärjestysmerkit.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ada93c0192aadac70c38c8c8c4f3af86ff6fc3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893273"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="478a9-103">Tavujärjestysmerkkejä luoduissa tiedostoissa estävien ER-määritysten suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="478a9-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="478a9-104">[Sähköisen raportoinnin (ER)](general-electronic-reporting.md) [ratkaisu](er-quick-start1-new-solution.md) voidaan suunnitella luomaan lähteviä asiakirjoja.</span><span class="sxs-lookup"><span data-stu-id="478a9-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="478a9-105">Teksti- tai XML-tiedostojen kaltaisten asiakirjojen luominen edellyttää, että ratkaisussa on oltava ER-[määritys](general-electronic-reporting.md#Configuration), joka sisältää ER-[muoto](general-electronic-reporting.md#FormatComponentOutbound)-osan</span><span class="sxs-lookup"><span data-stu-id="478a9-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="478a9-106">Luotujen tiedostojen merkkijoukon ilmaisevan [merkkikoodaus](/windows/win32/intl/character-sets) edellyttää, että ER-muoto sisältää **Yleinen\\Tiedosto**-muotoelementin.</span><span class="sxs-lookup"><span data-stu-id="478a9-106">To specify the [character encoding](/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="478a9-107">ER-muoto-osan määritetään avaamalla ER-määrityksen [luonnos](general-electronic-reporting.md#component-versioning) ER-muodon suunnittelutoiminnossa ja lisäämällä **Yleinen\\Tiedosto**-elementti.</span><span class="sxs-lookup"><span data-stu-id="478a9-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="478a9-108">**Koodaus**-kenttään määritetään niiden lähtevien tiedostojen koodaus, jotka luodaan suorituksen aikana tätä osaa käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="478a9-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="478a9-109">Jos muodon sisältämän koodauksen nimi on virheellinen, seurauksena on virhe, kun muutokset tallennetaan muotoasetuksiin.</span><span class="sxs-lookup"><span data-stu-id="478a9-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Juurielementin lisääminen Muodon suunnittelija -sivulla](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="478a9-111">Jos koodaukseksi määritettään **UTF-8**, **UTF-16** tai **UTF-32**, **Estä tavujärjestysmerkit**-vaihtoehto on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="478a9-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="478a9-112">Kun asetuksena on **Kyllä**, [tavujärjestysmerkit](/globalization/encoding/byte-order-mark) estetään lähtevissä tiedostoissa, jotka luodaan suorituksen aikana suoritettaessa muokattavaa ER-muotoa.</span><span class="sxs-lookup"><span data-stu-id="478a9-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="478a9-113">Jos **Koodaus**-kenttä jätetään tyhjäksi, **UTF-8**-oletuskoodausta käytetään.</span><span class="sxs-lookup"><span data-stu-id="478a9-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![Estä tavujärjestysmerkit -vaihtoehdon määrittäminen Muodon suunnittelija -sivulla](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="478a9-115">Toiminnon tarkastelu suorituksen aikana edellyttää soveltuvan menettelyn suorittamista.</span><span class="sxs-lookup"><span data-stu-id="478a9-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="478a9-116">Voit noudattaa esimerkiksi aiheen [ER-muotojen XML-elementtien suorittamisen lykkääminen](er-defer-xml-element.md) ohjeissa.</span><span class="sxs-lookup"><span data-stu-id="478a9-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="478a9-117">Kun kyseisen aiheen kohdan [Muodon muokkaaminen siten, että laskeminen perustuu luotuun tulokseen](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) vaiheet on suoritettu, tee seuraavat lisävaiheet:</span><span class="sxs-lookup"><span data-stu-id="478a9-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="478a9-118">UTF-koodauksen määrittäminen:</span><span class="sxs-lookup"><span data-stu-id="478a9-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="478a9-119">Valitse **Yleinen\\Tiedosto**-tyypin **Raportti**-elementti.</span><span class="sxs-lookup"><span data-stu-id="478a9-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="478a9-120">Määritä **Koodaus**-kenttään **UTF-8**-koodaus.</span><span class="sxs-lookup"><span data-stu-id="478a9-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="478a9-121">Luo XML-tiedosto, joka sisältää tavujärjestysmerkin:</span><span class="sxs-lookup"><span data-stu-id="478a9-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="478a9-122">Sisällytä tavujärjestysmerkit luotuihin XML-tiedostoihin määrittämällä **Estä tavujärjestysmerkit** -asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="478a9-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="478a9-123">Suorita aiheen [ER-muotojen XML-elementtien suorittamisen lykkääminen](er-defer-xml-element.md) kohdassa [XML-elementin suorittamisen lykkääminen siten, että käytetään laskettua summaa](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) olevat vaiheet ja tallenna luotu tiedosto nimellä **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="478a9-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="478a9-124">Luo XML-tiedosto, joka ei sisällä tavujärjestysmerkkiä:</span><span class="sxs-lookup"><span data-stu-id="478a9-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="478a9-125">Estä tavujärjestysmerkit luoduissa XML-tiedostoissa määrittämällä **Estä tavujärjestysmerkit** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="478a9-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="478a9-126">Suorita aiheen [ER-muotojen XML-elementtien suorittamisen lykkääminen](er-defer-xml-element.md) kohdassa [XML-elementin suorittamisen lykkääminen siten, että käytetään laskettua summaa](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) olevat vaiheet ja tallenna luotu tiedosto nimellä **SampleXmlReport (1).xml**.</span><span class="sxs-lookup"><span data-stu-id="478a9-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="478a9-127">Vertaa luotuja tiedostoja tiedostovertailun apuohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="478a9-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="478a9-128">Ensimmäinen ero on nähtävissä tiedoston otsikossa.</span><span class="sxs-lookup"><span data-stu-id="478a9-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="478a9-129">SampleXmlReport.xml-tiedosto sisältää tavujärjestysmerkin, mutta sitä ei ole SampleXmlReport (1).xml-tiedostossa.</span><span class="sxs-lookup"><span data-stu-id="478a9-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Luotujen tiedostojen vertaaminen tiedostovertailun apuohjelmalla](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="478a9-131">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="478a9-131">See also</span></span>

- [<span data-ttu-id="478a9-132">Sähköisen raportoinnin muotojen XML-elementtien suorittamisen lykkääminen</span><span class="sxs-lookup"><span data-stu-id="478a9-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]