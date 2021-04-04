---
title: Finance and Operations -sovellusten ohjekokemuksen määrittäminen
description: Tässä ohjeaiheessa käsitellään joidenkin Microsoft Dynamics 365 -sovellusten ohjejärjestelmän osista. Siinä käsitellään myös kyseisten sovellusten yhdistämistä ja annetaan yhteenveto mukautetun ohjeen luontiprosessista.
author: margoc
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 467cce5a80dc7577647e82c8652c8a7adc67a498
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565925"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a><span data-ttu-id="98a7c-104">Finance and Operations -sovellusten ohjekokemuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="98a7c-104">Configure the Help experience for Finance and Operations apps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98a7c-105">Tässä ohjeaiheessa on Finance and Operations -sovellusten, kuten Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Human Resources, ohjejärjestelmän osien yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="98a7c-105">In this topic, you will find an overview of the components of the Help system for Finance and Operations apps, such as Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources.</span></span> <span data-ttu-id="98a7c-106">Ohjeaiheessa käsitellään myös kyseisten osien yhdistämistä ja annetaan yhteenveto mukautetun ohjeen luontiprosessista.</span><span class="sxs-lookup"><span data-stu-id="98a7c-106">The topic also explains how to connect these components and provides a summary of the process for creating custom Help.</span></span>

## <a name="help-architecture"></a><span data-ttu-id="98a7c-107">Ohjearkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="98a7c-107">Help architecture</span></span>

<span data-ttu-id="98a7c-108">Finance and Operations -sovellukset sisältävä käsitteellisiä yleiskatsauksia ja muita aiheita, jotka on julkaistu [https://docs.microsoft.com/dynamics365](/dynamics365/)-sivustossa.</span><span class="sxs-lookup"><span data-stu-id="98a7c-108">Finance and Operations apps include conceptual overviews and other topics that are published to the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span> <span data-ttu-id="98a7c-109">Tätä sisältöä voidaan sitten käyttöön tuotteen **Ohje**-ruudussa.</span><span class="sxs-lookup"><span data-stu-id="98a7c-109">This content can then be accessed from the in-product **Help** pane.</span></span> <span data-ttu-id="98a7c-110">Seuraavassa kuvassa on osa ohjejärjestelmästä.</span><span class="sxs-lookup"><span data-stu-id="98a7c-110">The following illustration shows the parts of the Help system.</span></span>

<span data-ttu-id="98a7c-111">[![Ohjearkkitehtuuri](./media/help-architecture.png)](./media/help-architecture.png)</span><span class="sxs-lookup"><span data-stu-id="98a7c-111">[![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)</span></span>

<span data-ttu-id="98a7c-112">Tuotteen ohjejärjestelmä hakee artikkeleita docs.microsoft.comista ja muista yhdistetyistä sivustoista.</span><span class="sxs-lookup"><span data-stu-id="98a7c-112">The in-product Help system pulls articles from docs.microsoft.com and other connected websites.</span></span> <span data-ttu-id="98a7c-113">Se hakee myös liiketoimintaprosessien mallintajaan Microsoft Dynamics Lifecycle Servicesissä (LCS) tallennetuista tehtäväoppaista.</span><span class="sxs-lookup"><span data-stu-id="98a7c-113">It also pulls in task guides that are stored in Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="adding-task-guides"></a><span data-ttu-id="98a7c-114">Tehtäväoppaiden lisääminen</span><span class="sxs-lookup"><span data-stu-id="98a7c-114">Adding task guides</span></span>

> [!NOTE]
> <span data-ttu-id="98a7c-115">**Tehtäväoppaat**-välilehteä ei ole tällä hetkellä Human Resourcesissa tai Commercessa.</span><span class="sxs-lookup"><span data-stu-id="98a7c-115">The **Task guides** tab isn't currently available in Human Resources or Commerce.</span></span> <!--We are currently working to enable this functionality in a future release.--> <span data-ttu-id="98a7c-116">Perustoimintoja koskevat Human Resourcesin aloituskokemuksen tehtäväoppaat ovat kuitenkin edelleen käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="98a7c-116">However, the task guides in the Getting Started experience in Human Resources remain available to cover basic functionality.</span></span> <span data-ttu-id="98a7c-117">Sekä Human Resourcesin että Commercen menettelyohjeet ovat käytettävissä [https://docs.microsoft.com/dynamics365](/dynamics365/)-sivustossa.</span><span class="sxs-lookup"><span data-stu-id="98a7c-117">For both Human Resources and Commerce, procedural Help is available on the [https://docs.microsoft.com/dynamics365](/dynamics365/) site.</span></span>

<span data-ttu-id="98a7c-118">Järjestelmänvalvojat voivat määrittää **Järjestelmän parametrit** -sivulla käyttöönottoon soveltuvien tehtäväopaskirjastojen käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="98a7c-118">On the **System parameters** page, system admins can configure access to the relevant task guide libraries for an implementation.</span></span>

> [!NOTE]
> - <span data-ttu-id="98a7c-119">Ohjeen määrittämistä varten kirjauduttava tilille sinä vuokraajana, jossa sovellus on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="98a7c-119">To configure Help, you must sign in by using an account in the same tenant as the tenant where the app is deployed.</span></span>
> - <span data-ttu-id="98a7c-120">LCS-kirjastoon ei voi muodostaa yhteyttä sovelluksen siitä esiintymästä, jota käytetään paikallisella virtuaalikiintolevyllä (VHD).</span><span class="sxs-lookup"><span data-stu-id="98a7c-120">An LCS library can't be connected from an instance of the app that is running on a local virtual hard drive (VHD).</span></span>

<span data-ttu-id="98a7c-121">[![Järjestelmäparametrit-lomake ja ohjeen asetukset](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span><span class="sxs-lookup"><span data-stu-id="98a7c-121">[![System Parameters form with Help settings](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)</span></span>

<span data-ttu-id="98a7c-122">Ratkaisun tehtäväoppaiden määrittämisohjeet ovat **Järjestelmän parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="98a7c-122">To configure task guides for a solution, follow these steps on the **System parameters** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98a7c-123">Kun avaat **Ohje**-välilehden ensimmäisen kerran, sinun on muodostettava yhteys Lifecycle Services -palveluun.</span><span class="sxs-lookup"><span data-stu-id="98a7c-123">The first time that you open the **Help** tab, you must connect to Lifecycle Services.</span></span> <span data-ttu-id="98a7c-124">Valitse lomakkeen keskellä oleva linkki, odota yhteyden muodostumista, sulje valintaikkuna ja hae **Järjestelmäparametrit**-sivu valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="98a7c-124">Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the **System Parameters** page.</span></span>
>
> <span data-ttu-id="98a7c-125">[![Muodosta yhteys LCS:ään](./media/connect-to-lcs-crop-1024x365.png "Muodosta yhteys LCS:ään")](./media/connect-to-lcs-crop.png)</span><span class="sxs-lookup"><span data-stu-id="98a7c-125">[![Connect to LCS](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)</span></span>

1. <span data-ttu-id="98a7c-126">Valitse Lifecycle Services -projekti, johon yhteys muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="98a7c-126">Select the Lifecycle Services project to connect to.</span></span>
2. <span data-ttu-id="98a7c-127">Valitse BPM-kirjastot (valitussa projektissa), josta tehtävätallenteet noudetaan.</span><span class="sxs-lookup"><span data-stu-id="98a7c-127">Select the BPM libraries (within the selected project) to retrieve task recordings from.</span></span>
3. <span data-ttu-id="98a7c-128">Määritä BPM-kirjastojen näyttöjärjestys.</span><span class="sxs-lookup"><span data-stu-id="98a7c-128">Set the display order of the BPM libraries.</span></span> <span data-ttu-id="98a7c-129">Näyttöjärjestys määrittää, missä järjestyksessä kirjastojen tehtävätallenteet näkyvät **Ohje**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="98a7c-129">The display order defines the order in which task recordings from the libraries will appear in the **Help** pane.</span></span>

<span data-ttu-id="98a7c-130">Kun olet suorittanut nämä vaiheet, voit avata **Ohje**-ruudun ja valita **Tehtäväoppaat**-välilehden, jossa on näkyvissä avointa Finance and Operations -sivua käsitteleviä tehtäväoppaita.</span><span class="sxs-lookup"><span data-stu-id="98a7c-130">After you complete these steps, you can open the **Help** pane and select the **Task guides** tab. You'll now see the task guides that apply to the page that you're currently on in Finance and Operations apps.</span></span> <span data-ttu-id="98a7c-131">Jos tehtävän ohjauksia ei löydy, tarkenna hakua avainsanoilla.</span><span class="sxs-lookup"><span data-stu-id="98a7c-131">If no task guides are found, you can enter keywords to refine your search.</span></span>

### <a name="showing-translated-task-guides"></a><span data-ttu-id="98a7c-132">Käännettyjen tehtäväoppaiden näyttäminen</span><span class="sxs-lookup"><span data-stu-id="98a7c-132">Showing translated task guides</span></span>

<span data-ttu-id="98a7c-133">Käännetyt tehtäväoppaat julkaistiin ensimmäisen kerran toukokuun 2016 yhdistetyssä APQC-kirjastossa ja käytön aloituskirjastossa.</span><span class="sxs-lookup"><span data-stu-id="98a7c-133">Translated task guides were first released in the May 2016 APQC Unified Library and in the Getting Started library.</span></span> <span data-ttu-id="98a7c-134">Lokalisoidun tehtäväoppaan ohjeen katsominen edellyttää, että Dynamics 365 -ratkaisu on yhdistetty toukokuun 2016 kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="98a7c-134">To view localized task guide Help, make sure that your Dynamics 365 solution is connected to the May 2016 library.</span></span> <span data-ttu-id="98a7c-135">Käyttäjät voivat muuttaa kielen, jota käytetään avautuvassa tehtäväoppaassa, muuttamalla kieliasetuksia kohdassa **Asetukset** &gt; **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="98a7c-135">Users can change the language that a task guide appears in by changing the language settings under **Options** &gt; **Preferences**.</span></span>

> [!NOTE]
> <span data-ttu-id="98a7c-136">Vaikka useita tehtäväoppaita on käännetty, tehtäväoppaiden nimet eivät näy tällä hetkellä asiakasohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="98a7c-136">Although many task guides have been translated, the client doesn't currently show the translated task guide names.</span></span> <span data-ttu-id="98a7c-137">Lisäksi vain helmikuussa 2016 julkaistujen tehtäväoppaiden käännökset ovat saatavana toukokuun 2016 kirjastossa.</span><span class="sxs-lookup"><span data-stu-id="98a7c-137">Additionally, in the May 2016 library, translations are available only for the task guides that were released in February 2016.</span></span> <span data-ttu-id="98a7c-138">Microsoft julkaisee lisää käännöksiä sisältävän päivitetyn kirjaston.</span><span class="sxs-lookup"><span data-stu-id="98a7c-138">Microsoft will release an updated library that includes additional translations.</span></span>
>
> - <span data-ttu-id="98a7c-139">Jos tehtäväopas on käännetty, tehtäväopas avautuu valitsemallasi kielellä.</span><span class="sxs-lookup"><span data-stu-id="98a7c-139">If a task guide has been translated, when you open that task guide all the text of the task guide will appear in your selected language.</span></span>
> - <span data-ttu-id="98a7c-140">Jos tehtäväopasta ei ole vielä käännetty, vain osa tekstistä (ohjausobjektien teksti) näkyy valitun kielisenä.</span><span class="sxs-lookup"><span data-stu-id="98a7c-140">If a task guide has not yet been translated, when you open it, only some of the text (the text of the controls) will appear in your selected language.</span></span>

## <a name="adding-custom-help"></a><span data-ttu-id="98a7c-141">Mukautetun ohjeen lisääminen</span><span class="sxs-lookup"><span data-stu-id="98a7c-141">Adding custom Help</span></span>

<span data-ttu-id="98a7c-142">Voit luoda tehtäväoppaiden avulla mukautetun ohjeen tai yhdistää mukautetun Ohje-sivuston **Ohje**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="98a7c-142">You can use task guides to create custom Help, or you can connect a custom Help website to the **Help** pane.</span></span>

### <a name="create-custom-help-by-using-task-guides"></a><span data-ttu-id="98a7c-143">Mukautetun ohjeen luominen tehtäväoppaiden avulla</span><span class="sxs-lookup"><span data-stu-id="98a7c-143">Create custom Help by using task guides</span></span>

<span data-ttu-id="98a7c-144">Voit luoda tuettujen sovellusten oman mukautetun ohjeen luomalla toteutusta vastaavia tehtävätallenteita ja tallentamalla ne sitten LCS:n liiketoimintaprosessien kirjastoon.</span><span class="sxs-lookup"><span data-stu-id="98a7c-144">You can create custom Help for the supported apps by creating task recordings that reflect your implementation and then saving them to a Business process library in LCS.</span></span> <span data-ttu-id="98a7c-145">Human Resourcesiin ei voi luoda mukautettuja tehtäväoppaita.</span><span class="sxs-lookup"><span data-stu-id="98a7c-145">You can't create custom task guides for Human Resources.</span></span>

<span data-ttu-id="98a7c-146">Kumppanit voivat puolestaan siirtää kirjaston yrityskirjastoon ja sisällyttää sen ratkaisuun, jos se halutaan asiakkaiden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="98a7c-146">If you're a partner, and you promote a library to a corporate library and include it in a solution, it will be available to your customers.</span></span> <span data-ttu-id="98a7c-147">Voit myös kopioida yhdistetyn APQC-kirjaston sekä avata tehtävätallenteet kopioissa, muokata niitä ja tallentaa sitten muutetut tallenteet.</span><span class="sxs-lookup"><span data-stu-id="98a7c-147">You can also make a copy of the APQC Unified Library, and then open the task recordings in the copy, edit them, and save your changes.</span></span> <span data-ttu-id="98a7c-148">Lisätietoja on kohdassa [Tehtävän tallennustoiminnon resurssit](../../dev-itpro/user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="98a7c-148">For more information, see [Task recorder resources](../../dev-itpro/user-interface/task-recorder.md).</span></span>

### <a name="connect-a-custom-help-site"></a><span data-ttu-id="98a7c-149">Yhdistäminen mukautettuun ohjesivustoon</span><span class="sxs-lookup"><span data-stu-id="98a7c-149">Connect a custom Help site</span></span>

<span data-ttu-id="98a7c-150">Finance and Operations -sovelluksia käytetään vain harvoin sellaisenaan.</span><span class="sxs-lookup"><span data-stu-id="98a7c-150">Finance and Operations apps are rarely used in their out-of-box form.</span></span> <span data-ttu-id="98a7c-151">Ratkaisu sen mukautetaan ja laajennetaan organisaation tarpeita vastaavaksi.</span><span class="sxs-lookup"><span data-stu-id="98a7c-151">Instead, the solution is customized and extended to fit the organization's needs.</span></span> <span data-ttu-id="98a7c-152">Myös ohjekokemusta voi mukauttaa ja laajentaa.</span><span class="sxs-lookup"><span data-stu-id="98a7c-152">You can also customize and extend the Help experience.</span></span> <span data-ttu-id="98a7c-153">Mukautetun ohjeen voi esimerkiksi lisätä tuotteen **Ohje**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="98a7c-153">For example, you can add custom Help to the in-product **Help** pane.</span></span>

<span data-ttu-id="98a7c-154">Microsoftilla on työkalut, joilla mukautetun ohjeen voi ottaa käyttöön **Ohje**-ruudussa ja yhdistää siihen.</span><span class="sxs-lookup"><span data-stu-id="98a7c-154">Microsoft has provided a toolkit to help you deploy and connect custom Help to the **Help** pane.</span></span> <span data-ttu-id="98a7c-155">Lisätietoja **Ohje**-ruutuun yhdistetyn mukautetun ohjeratkaisun määrittämisestä on kohdassa [Mukautetun ohjeen yleiskatsaus](../../dev-itpro/help/custom-help-overview.md).</span><span class="sxs-lookup"><span data-stu-id="98a7c-155">For information about how you can set up a custom Help solution that is connected to the **Help** pane, see [Custom Help overview](../../dev-itpro/help/custom-help-overview.md).</span></span>

<span data-ttu-id="98a7c-156">Jos haluat tehdä Microsoftin kanssa yhteistyötä ohjeen mukauttamistyökalujen ja -prosessien osalta, täytä lomake osoitteessa [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span><span class="sxs-lookup"><span data-stu-id="98a7c-156">If you want to collaborate with Microsoft on tools and processes for customizing Help, fill in the form at [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).</span></span>

## <a name="see-also"></a><span data-ttu-id="98a7c-157">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="98a7c-157">See also</span></span>

[<span data-ttu-id="98a7c-158">Ohjejärjestelmä</span><span class="sxs-lookup"><span data-stu-id="98a7c-158">Help system</span></span>](help-overview.md)  
[<span data-ttu-id="98a7c-159">Mukautetun ohjeen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="98a7c-159">Custom Help overview</span></span>](../../dev-itpro/help/custom-help-overview.md)  
[<span data-ttu-id="98a7c-160">Tehtävän tallennustoiminnon resurssit</span><span class="sxs-lookup"><span data-stu-id="98a7c-160">Task recorder resources</span></span>](../../dev-itpro/user-interface/task-recorder.md)  
[<span data-ttu-id="98a7c-161">Dokumentaation tai koulutuksen luominen tehtävien tallennustoiminnolla</span><span class="sxs-lookup"><span data-stu-id="98a7c-161">Create documentation or training with Task Recorder</span></span>](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[<span data-ttu-id="98a7c-162">Mukautetun ohjeen GitHub-säilö</span><span class="sxs-lookup"><span data-stu-id="98a7c-162">Custom Help GitHub repository</span></span>](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]