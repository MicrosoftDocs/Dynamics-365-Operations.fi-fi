---
title: "Yhdistäminen ohjejärjestelmään"
description: "Tämä ohjeaihe sisältää Microsoft Dynamics 365 for Finance and Operations -ohjejärjestelmän komponenttien kuvauksen, niiden yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen yhteenvedon."
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 673b01648127fe1d19fb3c75c4d6812c4f22c761
ms.contentlocale: fi-fi
ms.lasthandoff: 12/18/2018

---

# <a name="connect-the-help-system"></a><span data-ttu-id="fc657-103">Yhdistäminen ohjejärjestelmään</span><span class="sxs-lookup"><span data-stu-id="fc657-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc657-104">Tämä ohjeaihe kuvaa Finance and Operationsin ohjejärjestelmän komponentit.</span><span class="sxs-lookup"><span data-stu-id="fc657-104">This topic describes the components of the Help system for Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fc657-105">Se tarjoaa näiden komponenttien yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen luomisen yhteenvedon.</span><span class="sxs-lookup"><span data-stu-id="fc657-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="fc657-106">Ohjearkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="fc657-106">Help architecture</span></span>

<span data-ttu-id="fc657-107">Seuraavassa kuvassa on osa Finance and Operationsin ohjejärjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="fc657-107">The following illustration shows the parts of the Finance and Operations Help system.</span></span> <span data-ttu-id="fc657-108">Tuotteen ohjejärjestelmä käyttää Dynamics 365 for Finance and Operations -sivuston (https://docs.microsoft.com) artikkeleja sekä Lifecycle Servicesin (LCS) liiketoimintaprosessin mallintajaan tallennettuja tehtäväoppaita.</span><span class="sxs-lookup"><span data-stu-id="fc657-108">The in-product Help system pulls articles from the Finance and Operations site on https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="fc657-109">Jos kaaviossa on ominaisuuden vieressä tähtimerkki (\*), ominaisuutta suunnitellaan mutta se ei ole vielä käytössä.</span><span class="sxs-lookup"><span data-stu-id="fc657-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="fc657-110">[![Ohjearkkitehtuuri](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="fc657-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="fc657-111">Yhteyden muodostaminen ohjejärjestelmään</span><span class="sxs-lookup"><span data-stu-id="fc657-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="fc657-112">**Tehtäväoppaat**-välilehti ei ole tällä hetkellä käytettävissä Microsoft Dynamics 365 for Talentissa ja Microsoft Dynamics 365 for Retailissa.</span><span class="sxs-lookup"><span data-stu-id="fc657-112">The **Task guides** tab is currently not available in Microsoft Dynamics 365 for Talent and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="fc657-113">Tämän toiminnon käyttöönottamista myöhemmissä versiossa ollaan toteuttamassa.</span><span class="sxs-lookup"><span data-stu-id="fc657-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="fc657-114">Perustoimintoja koskevat Talentin aloituskokemuksen tehtäväoppaat ovat edelleen käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="fc657-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="fc657-115">Retailin ja Talentin menettelyohje on saatavana myös docs.microsoft.com-sivustossa ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)).</span><span class="sxs-lookup"><span data-stu-id="fc657-115">Procedural help is also available on the docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) for both Retail and Talent.</span></span>

<span data-ttu-id="fc657-116">Järjestelmänvalvojat voivat muodostaa **Järjestelmäparametrit**-lomakkeella yhteyden käyttöönotettaviin ohjejärjestelmän osiin.</span><span class="sxs-lookup"><span data-stu-id="fc657-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="fc657-117">[![Järjestelmäparametrit-lomake ja ohjeen asetukset](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="fc657-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="fc657-118">Toimi seuraavasti **Järjestelmän parametrit** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="fc657-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc657-119">Kun avaat **Ohje**-välilehden ensimmäisen kerran, sinun on muodostettava yhteys Lifecycle Services -palveluun.</span><span class="sxs-lookup"><span data-stu-id="fc657-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="fc657-120">Valitse lomakkeen keskellä oleva linkki, odota yhteyden muodostumista, sulje valintaikkuna ja nouda **Järjestelmäparametrit**-sivu valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc657-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="fc657-121">[![Yhdistäminen LCS:ään](./media/connect-to-lcs-crop-1024x365.png "Yhdistäminen LCS:ään")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="fc657-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="fc657-122">Valitse Lifecycle Services -projekti, johon yhteys muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="fc657-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="fc657-123">Valitse BPM-kirjastot (valitussa projektissa), josta tehtävätallenteet noudetaan.</span><span class="sxs-lookup"><span data-stu-id="fc657-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>

    - <span data-ttu-id="fc657-124">Valitse Finance and Operationsissa Microsoft-sisältöä varten uusimman APQC Unified Library for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fc657-124">For Finance and Operations, for Microsoft content, select the most recent APQC Unified Library for Finance and Operations.</span></span>
    - <span data-ttu-id="fc657-125">Retail-kirjasto julkaistaan pian.</span><span class="sxs-lookup"><span data-stu-id="fc657-125">For Retail, we will be releasing a library in the near future.</span></span>
    - <span data-ttu-id="fc657-126">Talent-kirjastoa ei tarvitse valita, sillä järjestelmä muodostaa yhteyden oikeaan kirjastoon puolestasi.</span><span class="sxs-lookup"><span data-stu-id="fc657-126">You do not need to select a library for Talent—the connection to the correct library is established for you.</span></span>

3. <span data-ttu-id="fc657-127">Määritä BPM-kirjastojen näyttöjärjestys.</span><span class="sxs-lookup"><span data-stu-id="fc657-127">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="fc657-128">Tämä asetus määrittää, missä järjestyksessä kirjastojen tehtävätallenteet näkyvät **Ohje**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="fc657-128">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="fc657-129">Kun olet suorittanut nämä vaiheet, voit avata **ohjeruudun** ja valita **Tehtäväoppaat**-välilehden, jolla on näkyvissä on avointa Finance and Operations -sivua käsitteleviä tehtäväoppaita.</span><span class="sxs-lookup"><span data-stu-id="fc657-129">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations.</span></span> <span data-ttu-id="fc657-130">Jos tehtävän ohjauksia ei löydy, tarkenna hakua avainsanoilla.</span><span class="sxs-lookup"><span data-stu-id="fc657-130">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="fc657-131">Käännettyjen tehtäväoppaiden näyttäminen</span><span class="sxs-lookup"><span data-stu-id="fc657-131">Showing translated task guides</span></span>

<span data-ttu-id="fc657-132">Käännetyt tehtäväoppaat toimitettiin toukokuun 2016 yhdistetyssä APQC-kirjastossa ja käytön aloituskirjastossa.</span><span class="sxs-lookup"><span data-stu-id="fc657-132">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="fc657-133">Jos haluat avata lokalisoidun tehtäväoppaan ohjeen Finance and Operationsissa, varmista, että olet muodostanut yhteyden toukokuun kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="fc657-133">In Finance and Operations, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="fc657-134">Kullekin käyttäjälle avautuvan tehtäväoppaan kieli määräytyy kieliasetuksissa, jotka on valittu kohdassa **Asetukset** &gt; **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="fc657-134">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="fc657-135">Vaikka useita tehtäväoppaita on käännetty, tehtäväoppaiden nimet eivät näy tällä hetkellä Finance and Operationsin asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="fc657-135">Even though many task guides have been translated, right now the Finance and Operations client is not showing the translated task guide names.</span></span> <span data-ttu-id="fc657-136">Lisäksi vain helmikuussa 2016 julkaistujen tehtäväoppaiden käännökset ovat saatavana toukokuun kirjastossa.</span><span class="sxs-lookup"><span data-stu-id="fc657-136">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="fc657-137">Lisää käännöksiä julkaistaan päivitetyssä kirjastossa.</span><span class="sxs-lookup"><span data-stu-id="fc657-137">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="fc657-138">Jos tehtäväopas on käännetty, tehtäväopas avautuu valitsemallasi kielellä.</span><span class="sxs-lookup"><span data-stu-id="fc657-138">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="fc657-139">Jos tehtäväopasta ei ole vielä käännetty, vain osa tekstistä (ohjausobjektien teksti) näkyy valitun kielisenä.</span><span class="sxs-lookup"><span data-stu-id="fc657-139">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="fc657-140">Mukautetun ohjeen luominen</span><span class="sxs-lookup"><span data-stu-id="fc657-140">Creating custom help</span></span>

<span data-ttu-id="fc657-141">Voit luoda tehtäväoppaiden avulla mukautetun ohjeen tai yhdistää sivuston Ohje-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="fc657-141">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="fc657-142">Mukautetun ohjeen luominen tehtäväoppaiden avulla</span><span class="sxs-lookup"><span data-stu-id="fc657-142">Create custom help with task guides</span></span>

<span data-ttu-id="fc657-143">Voit luoda oman mukautetun Finance and Operations- ja Retail -ohjeen luomalla sille tehtävätallenteita ja tallentamalla ne LCS:n liiketoimintaprosessien kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="fc657-143">You can create custom help for Finance and Operations, and for Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="fc657-144">Mukautettuja tehtäväoppaita ei voi luoda Talentissa.</span><span class="sxs-lookup"><span data-stu-id="fc657-144">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="fc657-145">Kumppanit voivat puolestaan siirtää kirjasto yrityskirjastoon ja sisällyttää sen ratkaisuun, jos se halutaan asiakkaiden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="fc657-145">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="fc657-146">Voit myös kopioida yhdistetyn yleisen APQC-kirjaston sekä avata oman kopion, avata tehtävätallenteet sieltä, muokata niitä ja tallentaa sitten muutetut tallenteet.</span><span class="sxs-lookup"><span data-stu-id="fc657-146">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="fc657-147">Lisätietoja on artikkelissa [Ohjeistuksena tai koulutuksena käytettävien tehtävätallenteiden luominen](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="fc657-147">For more information, see [How to create a task recording to use as documentation or training](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="fc657-148">Mukautetun sivuston yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="fc657-148">Connect a custom site</span></span>

<span data-ttu-id="fc657-149">Microsoftilla on raportti ja näytekoodi, jossa selitetään, miten mukautettu ohjesivusto luodaan ja yhdistetään Ohje-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="fc657-149">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="fc657-150">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="fc657-150">For more information, see:</span></span>

- [<span data-ttu-id="fc657-151">Finance and Operationsin mukautetun ohjeen luominen (raportti)</span><span class="sxs-lookup"><span data-stu-id="fc657-151">Create Custom Help for Finance and Operations (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="fc657-152">Mukautetun ohjeen GitHub-säilö</span><span class="sxs-lookup"><span data-stu-id="fc657-152">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="fc657-153">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="fc657-153">Additional resources</span></span>

[<span data-ttu-id="fc657-154">Ohjeen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fc657-154">Help overview</span></span>](help-overview.md)

[<span data-ttu-id="fc657-155">Tehtävän tallennustoiminnon yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="fc657-155">Task recorder overview</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="fc657-156">Dokumentaation tai koulutuksen luominen tehtävätallenteiden avulla</span><span class="sxs-lookup"><span data-stu-id="fc657-156">How to create a task recording to use as documentation or training</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)

