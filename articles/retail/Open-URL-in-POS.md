---
title: URL-linkin avaaminen POS-sovelluksessa
description: Tämä ohjeaihe sisältää yleiskatsauksen parannuksista, jotka on tehty Microsoft Dynamics 365 for Retailin tuote- ja asiakashakuihin.
author: AamirAllaq
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b07406b4e218b45bdde87c4a579814fe0edbc286
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556964"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="ab8d2-103">URL-osoitteen avaaminen POS:ssä</span><span class="sxs-lookup"><span data-stu-id="ab8d2-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ab8d2-104">Tässä aiheessa kerrotaan, miten Retail POS:ssä voi määrittää painikkeen avaaman URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-104">This topic describes how you can configure a button in Retail point of sale (POS) to open a URL.</span></span> <span data-ttu-id="ab8d2-105">Tätä ominaisuutta varten ei tarvitse muokata koodia ja sen voi määrittää myös henkilö, jolla ei ole kehittäjän roolia.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> <span data-ttu-id="ab8d2-106">Tämä ominaisuus on käytettävissä osana Dynamics 365 for Finance and Operations 8.1.3 -versiota (koontiversio 8.1.227.10014) ja sitä uudempaa versiota.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-106">This feature is available as part of the Dynamics 365 for Finance and Operations version 8.1.3 release (build 8.1.227.10014) and later.</span></span> 

<span data-ttu-id="ab8d2-107">Tällä ominaisuudella voi määrittää POS:n painikkeen avaamaan URL-osoitteen käyttämällä painikeruudukon suunnittelutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-107">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="ab8d2-108">Ominaisuutta tuetaan tällä hetkellä seuraavissa määrityksissä:</span><span class="sxs-lookup"><span data-stu-id="ab8d2-108">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="ab8d2-109">Avaa uudessa ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-109">Open in new window.</span></span>
- <span data-ttu-id="ab8d2-110">Avaa POS-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-110">Open within POS.</span></span>
- <span data-ttu-id="ab8d2-111">Avaa alkuperäinen sovellus.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-111">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="ab8d2-112">Avaa uudessa ikkunassa</span><span class="sxs-lookup"><span data-stu-id="ab8d2-112">Open in new window</span></span>

<span data-ttu-id="ab8d2-113">Tämä määritys määrittää, avataanko URL-osoite uudessa ikkunassa tai sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-113">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="ab8d2-114">Jos URL-osoite on määritetty avautumaan sovelluksessa, reunan siirtymispaneeli ja POS-yläpalkki ovat näkyvissä ja käyttäjän käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-114">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="ab8d2-115">Jos URL-osoite on määritetty avautumaan uudessa ikkunassa, URL avautuu uudessa sovellusikkunassa tai Modern POS for Windowsissa ja uudessa selainvälilehdessä kaikissa muissa POS-asiakasohjelmissa.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-115">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="ab8d2-116">Voit ottaa ominaisuuden käyttöön määrittämällä URL-osoitteen siten, että **Avaa uudessa ikkunassa** -asetus on valittu.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-116">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="ab8d2-117">Avaaminen POS-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="ab8d2-117">Open within POS</span></span>

<span data-ttu-id="ab8d2-118">URL-osoitteen avaamista POS-sovelluksessa tuetaan tällä hetkellä vai Modern POS for Windowsissa.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-118">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="ab8d2-119">Tätä toimintoa kehitetään vielä muissa asiakasohjelmissa, ja sen julkaisu on suunniteltu tuleviin päivityksiin.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-119">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="ab8d2-120">Voit ottaa ominaisuuden käyttöön määrittämällä URL-osoitteen siten, että **Avaa uudessa ikkunassa** -asetusta ei ole valittu.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-120">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="ab8d2-121">Alkuperäisen sovelluksen avaaminen</span><span class="sxs-lookup"><span data-stu-id="ab8d2-121">Open a native app</span></span>

<span data-ttu-id="ab8d2-122">Tällä ominaisuudella voi määrittää myös verkon ulkopuoliset URL-osoitteet avaa alkuperäisen sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-122">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="ab8d2-123">Voit esimerkiksi määrittää URL-protokollat, kuten MailTo, SIP, IM tai MSTEAMS, joita voidaan käsitellä kunkin protokollan alkuperäisellä sovelluksella isäntälaitteessa.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-123">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="ab8d2-124">Voit ottaa ominaisuuden käyttöön määrittämällä URL-osoitteen siten, että **Avaa uudessa ikkunassa** -asetus on valittu.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-124">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="ab8d2-125">Lisätietoja Windows-tietokoneita koskevista oletusprotokollaliitoksista, jos tietokone määritetään DISM:n (Deployment Image Servicing and Management) avulla, on kohdassa [Sovelluksen oletusliitosten vienti tai tuonti](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span><span class="sxs-lookup"><span data-stu-id="ab8d2-125">For Windows computers, see [Export or Import Default Application Associations](https://docs.microsoft.com/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="ab8d2-126">Jos Windows-tietokoneiden hallintaan käytetään MDM:ää, kuten Intunea, lisätietoja on kohdassa [CSP-käytäntö – ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="ab8d2-126">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](https://docs.microsoft.com/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="ab8d2-127">Jos olet mukautettua sivustoa rakentava kehittäjä, katso [URI:n oletussovelluksen käynnistäminen](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="ab8d2-127">If you are a developer building a custom website, see [Launch the default app for a URI](https://docs.microsoft.com/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="ab8d2-128">Alkuperäisen sovelluksen sujuva avaaminen</span><span class="sxs-lookup"><span data-stu-id="ab8d2-128">Open a native app seamlessly</span></span>

<span data-ttu-id="ab8d2-129">Windows, iOS ja Android sallivat lisäksi sovellusten entistä sujuvamman avaamisen sovelluksen protokollaliitoksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-129">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="ab8d2-130">Jos sovellusta ei ole vielä määritetty käsittelemään avaamista selaimesta, kehittäjän on ehkä määritettävä tämä.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-130">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="ab8d2-131">Windows: katso [Sovellusten käyttöönotto sivustoja varten sovelluksen URI-käsittelijöiden avulla](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="ab8d2-131">For Windows, see [Enable apps for websites using app URI handlers](https://docs.microsoft.com/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="ab8d2-132">iOS: katso [Kehittäjien yleiset linkit](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="ab8d2-132">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="ab8d2-133">Android: katso [Android-sovelluksen linkkien käsitteleminen](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="ab8d2-133">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="ab8d2-134">Asiakas</span><span class="sxs-lookup"><span data-stu-id="ab8d2-134">Client</span></span>                | <span data-ttu-id="ab8d2-135">Avaa uudessa ikkunassa</span><span class="sxs-lookup"><span data-stu-id="ab8d2-135">Open in new window</span></span> | <span data-ttu-id="ab8d2-136">Alkuperäisen sovelluksen avaaminen</span><span class="sxs-lookup"><span data-stu-id="ab8d2-136">Open native app</span></span> | <span data-ttu-id="ab8d2-137">Avaaminen POS-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="ab8d2-137">Open within POS</span></span> | <span data-ttu-id="ab8d2-138">Yksityiskohdat</span><span class="sxs-lookup"><span data-stu-id="ab8d2-138">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="ab8d2-139">Windowsin Modern POS</span><span class="sxs-lookup"><span data-stu-id="ab8d2-139">Modern POS on Windows</span></span> | <span data-ttu-id="ab8d2-140">✓\*</span><span class="sxs-lookup"><span data-stu-id="ab8d2-140">✓\*</span></span>                | <span data-ttu-id="ab8d2-141">✓</span><span class="sxs-lookup"><span data-stu-id="ab8d2-141">✓</span></span>               | <span data-ttu-id="ab8d2-142">✓</span><span class="sxs-lookup"><span data-stu-id="ab8d2-142">✓</span></span>              | <span data-ttu-id="ab8d2-143">\* Avautuu uudessa Modern POS -ikkunassa</span><span class="sxs-lookup"><span data-stu-id="ab8d2-143">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="ab8d2-144">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="ab8d2-144">Cloud POS</span></span>             | <span data-ttu-id="ab8d2-145">✓\*</span><span class="sxs-lookup"><span data-stu-id="ab8d2-145">✓\*</span></span>                | <span data-ttu-id="ab8d2-146">✓</span><span class="sxs-lookup"><span data-stu-id="ab8d2-146">✓</span></span>               | <span data-ttu-id="ab8d2-147">X</span><span class="sxs-lookup"><span data-stu-id="ab8d2-147">X</span></span>              | <span data-ttu-id="ab8d2-148">\* Avautuu uudessa selainvälilehdessä</span><span class="sxs-lookup"><span data-stu-id="ab8d2-148">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="ab8d2-149">iOS:n Modern POS</span><span class="sxs-lookup"><span data-stu-id="ab8d2-149">Modern POS on iOS</span></span>     | <span data-ttu-id="ab8d2-150">✓\*</span><span class="sxs-lookup"><span data-stu-id="ab8d2-150">✓\*</span></span>                | <span data-ttu-id="ab8d2-151">✓</span><span class="sxs-lookup"><span data-stu-id="ab8d2-151">✓</span></span>               | <span data-ttu-id="ab8d2-152">X</span><span class="sxs-lookup"><span data-stu-id="ab8d2-152">X</span></span>              | <span data-ttu-id="ab8d2-153">\* Avautuu uudessa selainvälilehdessä</span><span class="sxs-lookup"><span data-stu-id="ab8d2-153">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="ab8d2-154">Modern POS:n Android-versio</span><span class="sxs-lookup"><span data-stu-id="ab8d2-154">Modern POS on Android</span></span> | <span data-ttu-id="ab8d2-155">✓\*</span><span class="sxs-lookup"><span data-stu-id="ab8d2-155">✓\*</span></span>                | <span data-ttu-id="ab8d2-156">✓</span><span class="sxs-lookup"><span data-stu-id="ab8d2-156">✓</span></span>               | <span data-ttu-id="ab8d2-157">X</span><span class="sxs-lookup"><span data-stu-id="ab8d2-157">X</span></span>              | <span data-ttu-id="ab8d2-158">\* Avautuu uudessa selainvälilehdessä</span><span class="sxs-lookup"><span data-stu-id="ab8d2-158">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="ab8d2-159">Ennen aloittamista</span><span class="sxs-lookup"><span data-stu-id="ab8d2-159">Before you begin</span></span>

<span data-ttu-id="ab8d2-160">Tarkista ennen aloittamista, miten [myyntipisteen (POS) näytön asettelut](pos-screen-layouts.md) määritetään.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-160">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="ab8d2-161">URL-linkin avaaminen POS-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="ab8d2-161">Open URL in POS</span></span>

<span data-ttu-id="ab8d2-162">Määritä URL-osoite avautumaan POS:ssä seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-162">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="ab8d2-163">Valitse pääkonttorissa **Vähittäismyynti \> Kanavan asetukset \> POS-asetukset \> Myyntipiste \> Näytön asettelut**.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-163">In head office, go to **Retail \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="ab8d2-164">Valitse **Painikeruudukot \> Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-164">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="ab8d2-165">Luo uusi painike.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-165">Create a new button.</span></span>
4. <span data-ttu-id="ab8d2-166">Valitse **Painikeominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-166">Select **Button** properties.</span></span>
5. <span data-ttu-id="ab8d2-167">Valitse **Avaa URL** toimintona.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-167">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="ab8d2-168">Anna käytettävä URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-168">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="ab8d2-169">Määritä, avataanko URL-osoite uudessa ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="ab8d2-169">Configure whether to open the URL in a new window.</span></span>
