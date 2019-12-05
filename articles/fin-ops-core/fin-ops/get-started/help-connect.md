---
title: Yhdistäminen ohjejärjestelmään
description: Tämä ohjeaihe sisältää Finance and Operations -sovellusten ohjejärjestelmän osien kuvauksen, niiden yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen yhteenvedon.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2955464aa8a220563db1b9ebbb348be52f520659
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812577"
---
# <a name="connect-the-help-system"></a><span data-ttu-id="6e2e4-103">Yhdistäminen ohjejärjestelmään</span><span class="sxs-lookup"><span data-stu-id="6e2e4-103">Connect the Help system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e2e4-104">Tässä ohjeaiheessa kuvataan Finance and Operations -sovellusten, kuten Dynamics 365 Financen, Supply Chain Managementin, Retailin ja Talentin ohjejärjestelmän komponentteja.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-104">This topic describes the components of the Help system for Finance and Operations apps, such as Dynamics 365 Finance, Supply Chain Management, Retail, and Talent.</span></span> <span data-ttu-id="6e2e4-105">Se tarjoaa näiden komponenttien yhdistämistapojen yleiskatsauksen ja mukautetun ohjeen luomisen yhteenvedon.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-105">It provides an overview of how to connect these components and a summary of how to create custom help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="6e2e4-106">Ohjearkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="6e2e4-106">Help architecture</span></span>

<span data-ttu-id="6e2e4-107">Seuraavassa kuvassa on osa ohjejärjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-107">The following illustration shows the parts of the Help system.</span></span> <span data-ttu-id="6e2e4-108">Tuotteen ohjejärjestelmä käyttää sivuston https://docs.microsoft.com artikkeleja sekä Lifecycle Servicesin (LCS) liiketoimintaprosessin mallintajaan tallennettuja tehtäväoppaita.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-108">The in-product Help system pulls articles from https://docs.microsoft.com, as well as task guides stored in Business Process Modeler in Lifecycle Services (LCS).</span></span>

> [!NOTE]
> <span data-ttu-id="6e2e4-109">Jos kaaviossa on ominaisuuden vieressä tähtimerkki (\*), ominaisuutta suunnitellaan mutta se ei ole vielä käytössä.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-109">The features listed in the diagram with an asterisk (\*) are planned, but are not available yet.</span></span>

<span data-ttu-id="6e2e4-110">[![Ohjearkkitehtuuri](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="6e2e4-110">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

## <a name="connecting-the-help-system"></a><span data-ttu-id="6e2e4-111">Yhteyden muodostaminen ohjejärjestelmään</span><span class="sxs-lookup"><span data-stu-id="6e2e4-111">Connecting the Help system</span></span>

> [!NOTE]
> <span data-ttu-id="6e2e4-112">**Tehtäväoppaat**-välilehteä ei ole tällä hetkellä Dynamics 365 Talentissa tai Retailissa.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-112">The **Task guides** tab is currently not available in Dynamics 365 Talent or Retail.</span></span> <span data-ttu-id="6e2e4-113">Tämän toiminnon käyttöönottamista myöhemmissä versiossa ollaan toteuttamassa.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-113">We are currently working to enable this functionality in a future release.</span></span> <span data-ttu-id="6e2e4-114">Perustoimintoja koskevat Talentin aloituskokemuksen tehtäväoppaat ovat edelleen käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-114">The Task guides in the Getting Started experience in Talent remain available to cover basic functionality.</span></span> <span data-ttu-id="6e2e4-115">Menettelyohjeet ovat käytettävissä myös docs.microsoft.com-sivustossa sekä Retailille että Talentille.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-115">Procedural help is also available on the docs.microsoft.com site for both Retail and Talent.</span></span>

<span data-ttu-id="6e2e4-116">Järjestelmänvalvojat voivat muodostaa **Järjestelmäparametrit**-lomakkeella yhteyden käyttöönotettaviin ohjejärjestelmän osiin.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-116">Using the **System Parameters** page, system administrators connect the pieces of the Help system for an implementation.</span></span>

<span data-ttu-id="6e2e4-117">[![Järjestelmäparametrit-lomake ja ohjeen asetukset](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="6e2e4-117">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="6e2e4-118">Toimi seuraavasti **Järjestelmän parametrit** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="6e2e4-118">On the **System parameters** page, follow these steps:</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e2e4-119">Kun avaat **Ohje**-välilehden ensimmäisen kerran, sinun on muodostettava yhteys Lifecycle Services -palveluun.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-119">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="6e2e4-120">Valitse lomakkeen keskellä oleva linkki, odota yhteyden muodostumista, sulje valintaikkuna ja nouda **Järjestelmäparametrit**-sivu valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-120">Be sure to click the link in the middle of the form, wait for the connection, close the dialog box, and then click **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="6e2e4-121">[![Muodosta yhteys LCS:ään](./media/connect-to-lcs-crop-1024x365.png "Muodosta yhteys LCS:ään")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="6e2e4-121">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="6e2e4-122">Valitse Lifecycle Services -projekti, johon yhteys muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-122">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="6e2e4-123">Valitse BPM-kirjastot (valitussa projektissa), josta tehtävätallenteet noudetaan.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-123">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="6e2e4-124">Määritä BPM-kirjastojen näyttöjärjestys.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-124">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="6e2e4-125">Tämä asetus määrittää, missä järjestyksessä kirjastojen tehtävätallenteet näkyvät **Ohje**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-125">This determines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="6e2e4-126">Kun olet suorittanut nämä vaiheet, voit avata **ohjeruudun** ja valita **Tehtäväoppaat**-välilehden, jolla on näkyvissä on avointa Finance and Operations -sovelluksen sivua käsitteleviä tehtäväoppaita.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-126">After you complete these steps, you can open the **Help** pane and click the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="6e2e4-127">Jos tehtävän ohjauksia ei löydy, tarkenna hakua avainsanoilla.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-127">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="6e2e4-128">Käännettyjen tehtäväoppaiden näyttäminen</span><span class="sxs-lookup"><span data-stu-id="6e2e4-128">Showing translated task guides</span></span>

<span data-ttu-id="6e2e4-129">Käännetyt tehtäväoppaat toimitettiin toukokuun 2016 yhdistetyssä APQC-kirjastossa ja käytön aloituskirjastossa.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-129">Translated task guides were first shipped in the May 2016 APQC Unified Library, and the Getting Started library.</span></span> <span data-ttu-id="6e2e4-130">Jos haluat avata lokalisoidun tehtäväoppaan ohjeen Finance and Operations -sovelluksissa, varmista, että olet muodostanut yhteyden toukokuun kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-130">In Finance and Operations apps, to see localized task guide help, make sure that you are connected to the May library.</span></span> <span data-ttu-id="6e2e4-131">Kullekin käyttäjälle avautuvan tehtäväoppaan kieli määräytyy kieliasetuksissa, jotka on valittu kohdassa **Asetukset** &gt; **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-131">The language that a task guide appears in is controlled for each user by the Language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="6e2e4-132">Vaikka useita tehtäväoppaita on käännetty, tehtäväoppaiden nimet eivät näy tällä hetkellä asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-132">Even though many task guides have been translated, right now the client is not showing the translated task guide names.</span></span> <span data-ttu-id="6e2e4-133">Lisäksi vain helmikuussa 2016 julkaistujen tehtäväoppaiden käännökset ovat saatavana toukokuun kirjastossa.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-133">Also, only the task guides that were released in February 2016 are available in translation in the May library.</span></span> <span data-ttu-id="6e2e4-134">Lisää käännöksiä julkaistaan päivitetyssä kirjastossa.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-134">We will release an updated library with additional translations.</span></span>
>
> - <span data-ttu-id="6e2e4-135">Jos tehtäväopas on käännetty, tehtäväopas avautuu valitsemallasi kielellä.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-135">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="6e2e4-136">Jos tehtäväopasta ei ole vielä käännetty, vain osa tekstistä (ohjausobjektien teksti) näkyy valitun kielisenä.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-136">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="creating-custom-help"></a><span data-ttu-id="6e2e4-137">Mukautetun ohjeen luominen</span><span class="sxs-lookup"><span data-stu-id="6e2e4-137">Creating custom help</span></span>

<span data-ttu-id="6e2e4-138">Voit luoda tehtäväoppaiden avulla mukautetun ohjeen tai yhdistää sivuston Ohje-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-138">You can use task guides to create custom help, or connect a website to the Help pane.</span></span>

### <a name="create-custom-help-with-task-guides"></a><span data-ttu-id="6e2e4-139">Mukautetun ohjeen luominen tehtäväoppaiden avulla</span><span class="sxs-lookup"><span data-stu-id="6e2e4-139">Create custom help with task guides</span></span>

<span data-ttu-id="6e2e4-140">Voit luoda oman mukautetun Finance-, Supply Chain Management- tai Retail -ohjeen luomalla sille tehtävätallenteita ja tallentamalla ne LCS:n liiketoimintaprosessien kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-140">You can create custom help for Finance, Supply Chain Management, and Retail by creating task recordings that reflect your implementation, and saving them to an LCS Business Process Library.</span></span> <span data-ttu-id="6e2e4-141">Mukautettuja tehtäväoppaita ei voi luoda Talentissa.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-141">You cannot create custom task guides for Talent.</span></span>

<span data-ttu-id="6e2e4-142">Kumppanit voivat puolestaan siirtää kirjasto yrityskirjastoon ja sisällyttää sen ratkaisuun, jos se halutaan asiakkaiden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-142">For partners, if you promote a library to be a corporate library, and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="6e2e4-143">Voit myös kopioida yhdistetyn yleisen APQC-kirjaston sekä avata oman kopion, avata tehtävätallenteet sieltä, muokata niitä ja tallentaa sitten muutetut tallenteet.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-143">You can also make a copy of the APQC Unified global library, and then open your copy, open task recordings from it, modify them, and save the recordings with your changes.</span></span> <span data-ttu-id="6e2e4-144">Lisätietoja on kohdassa [Tehtävän tallennustoiminnon resurssit](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="6e2e4-144">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-site"></a><span data-ttu-id="6e2e4-145">Mukautetun sivuston yhdistäminen</span><span class="sxs-lookup"><span data-stu-id="6e2e4-145">Connect a custom site</span></span>

<span data-ttu-id="6e2e4-146">Microsoftilla on raportti ja näytekoodi, jossa selitetään, miten mukautettu ohjesivusto luodaan ja yhdistetään Ohje-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="6e2e4-146">Microsoft has provided a white paper and sample code that describe how to create and connect a custom help site to the Help pane.</span></span> <span data-ttu-id="6e2e4-147">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="6e2e4-147">For more information, see:</span></span>

- [<span data-ttu-id="6e2e4-148">Finance and Operations -sovellusten mukautetun ohjeen luominen (raportti)</span><span class="sxs-lookup"><span data-stu-id="6e2e4-148">Create Custom Help for Finance and Operations apps (white paper)</span></span>](https://go.microsoft.com/fwlink/?linkid=2041185)
- [<span data-ttu-id="6e2e4-149">Mukautetun ohjeen GitHub-säilö</span><span class="sxs-lookup"><span data-stu-id="6e2e4-149">Custom help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a><span data-ttu-id="6e2e4-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6e2e4-150">Additional resources</span></span>

[<span data-ttu-id="6e2e4-151">Ohjejärjestelmä</span><span class="sxs-lookup"><span data-stu-id="6e2e4-151">Help system</span></span>](help-overview.md)

[<span data-ttu-id="6e2e4-152">Tehtävän tallennustoiminnon resurssit</span><span class="sxs-lookup"><span data-stu-id="6e2e4-152">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)

[<span data-ttu-id="6e2e4-153">Dokumentaation tai koulutuksen luominen tehtävien tallennustoiminnolla</span><span class="sxs-lookup"><span data-stu-id="6e2e4-153">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)
