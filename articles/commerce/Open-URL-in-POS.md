---
title: URL-linkin avaaminen POS-sovelluksessa
description: Tämä ohjeaihe sisältää yleiskatsauksen parannuksista, jotka on tehty Dynamics 365 Commercen tuote- ja asiakashakuihin.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 43f28d9b7acb05a83544b04f6786dfe91f2d9f18
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193200"
---
# <a name="open-url-in-pos"></a><span data-ttu-id="4d237-103">URL-osoitteen avaaminen myyntipisteessä</span><span class="sxs-lookup"><span data-stu-id="4d237-103">Open URL in POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d237-104">Tässä aiheessa kerrotaan, miten Dynamics 365 Commerce -myyntipisteessä (POS) voi määrittää painikkeen avaaman URL-osoitteen.</span><span class="sxs-lookup"><span data-stu-id="4d237-104">This topic describes how you can configure a button in Dynamics 365 Commerce point of sale (POS) to open a URL.</span></span> <span data-ttu-id="4d237-105">Tätä ominaisuutta varten ei tarvitse muokata koodia ja sen voi määrittää myös henkilö, jolla ei ole kehittäjän roolia.</span><span class="sxs-lookup"><span data-stu-id="4d237-105">This feature does not require a code customization, and can be configured by someone in a non-developer role.</span></span> 

<span data-ttu-id="4d237-106">Tällä ominaisuudella voi määrittää POS:n painikkeen avaamaan URL-osoitteen käyttämällä painikeruudukon suunnittelutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="4d237-106">This feature allows configuration of a button in POS, using the button grid designer to open a URL.</span></span> <span data-ttu-id="4d237-107">Ominaisuutta tuetaan tällä hetkellä seuraavissa määrityksissä:</span><span class="sxs-lookup"><span data-stu-id="4d237-107">Currently, this is supported in the following configurations:</span></span>

- <span data-ttu-id="4d237-108">Avaa uudessa ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="4d237-108">Open in new window.</span></span>
- <span data-ttu-id="4d237-109">Avaa POS-sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="4d237-109">Open within POS.</span></span>
- <span data-ttu-id="4d237-110">Avaa alkuperäinen sovellus.</span><span class="sxs-lookup"><span data-stu-id="4d237-110">Open a native app.</span></span>

## <a name="open-in-new-window"></a><span data-ttu-id="4d237-111">Avaa uudessa ikkunassa</span><span class="sxs-lookup"><span data-stu-id="4d237-111">Open in new window</span></span>

<span data-ttu-id="4d237-112">Tämä määritys määrittää, avataanko URL-osoite uudessa ikkunassa tai sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="4d237-112">This configuration defines whether to open the URL in a new window or within the app.</span></span> <span data-ttu-id="4d237-113">Jos URL-osoite on määritetty avautumaan sovelluksessa, reunan siirtymispaneeli ja POS-yläpalkki ovat näkyvissä ja käyttäjän käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4d237-113">When configured to open a web URL within the app, the side navigation panel and top bar of POS are visible and available for user interaction.</span></span> <span data-ttu-id="4d237-114">Jos URL-osoite on määritetty avautumaan uudessa ikkunassa, URL avautuu uudessa sovellusikkunassa tai Modern POS for Windowsissa ja uudessa selainvälilehdessä kaikissa muissa POS-asiakasohjelmissa.</span><span class="sxs-lookup"><span data-stu-id="4d237-114">When configured to open in a new window, the URL will open in a new app window on Modern POS for Windows, and in a new browser tab in all other POS clients.</span></span> <span data-ttu-id="4d237-115">Voit ottaa ominaisuuden käyttöön määrittämällä URL-osoitteen siten, että **Avaa uudessa ikkunassa** -asetus on valittu.</span><span class="sxs-lookup"><span data-stu-id="4d237-115">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

## <a name="open-within-pos"></a><span data-ttu-id="4d237-116">Avaaminen POS-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="4d237-116">Open within POS</span></span>

<span data-ttu-id="4d237-117">URL-osoitteen avaamista POS-sovelluksessa tuetaan tällä hetkellä vai Modern POS for Windowsissa.</span><span class="sxs-lookup"><span data-stu-id="4d237-117">Opening a web URL within POS is currently only supported for Modern POS on Windows.</span></span> <span data-ttu-id="4d237-118">Tätä toimintoa kehitetään vielä muissa asiakasohjelmissa, ja sen julkaisu on suunniteltu tuleviin päivityksiin.</span><span class="sxs-lookup"><span data-stu-id="4d237-118">On other clients, this capability is under development and planned for release in future updates.</span></span> <span data-ttu-id="4d237-119">Voit ottaa ominaisuuden käyttöön määrittämällä URL-osoitteen siten, että **Avaa uudessa ikkunassa** -asetusta ei ole valittu.</span><span class="sxs-lookup"><span data-stu-id="4d237-119">To enable this, you must configure the URL with the **Open in new window** option not selected.</span></span>

## <a name="open-a-native-app"></a><span data-ttu-id="4d237-120">Alkuperäisen sovelluksen avaaminen</span><span class="sxs-lookup"><span data-stu-id="4d237-120">Open a native app</span></span>

<span data-ttu-id="4d237-121">Tällä ominaisuudella voi määrittää myös verkon ulkopuoliset URL-osoitteet avaa alkuperäisen sovelluksen.</span><span class="sxs-lookup"><span data-stu-id="4d237-121">This feature also allows you to specify non-web URLs to open a native app.</span></span> <span data-ttu-id="4d237-122">Voit esimerkiksi määrittää URL-protokollat, kuten MailTo, SIP, IM tai MSTEAMS, joita voidaan käsitellä kunkin protokollan alkuperäisellä sovelluksella isäntälaitteessa.</span><span class="sxs-lookup"><span data-stu-id="4d237-122">For example, you can specify URL protocols such as MailTo, SIP, IM, or MSTEAMS, which can then be handled by respective native apps on the host device.</span></span> <span data-ttu-id="4d237-123">Voit ottaa ominaisuuden käyttöön määrittämällä URL-osoitteen siten, että **Avaa uudessa ikkunassa** -asetus on valittu.</span><span class="sxs-lookup"><span data-stu-id="4d237-123">To enable this, you must configure the URL with the **Open in new window** option selected.</span></span>

- <span data-ttu-id="4d237-124">Lisätietoja Windows-tietokoneita koskevista oletusprotokollaliitoksista, jos tietokone määritetään DISM:n (Deployment Image Servicing and Management) avulla, on kohdassa [Sovelluksen oletusliitosten vienti tai tuonti](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations).</span><span class="sxs-lookup"><span data-stu-id="4d237-124">For Windows computers, see [Export or Import Default Application Associations](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) to set the default protocol associations if you are setting up your computer using Deployment Image Servicing and Management (DISM).</span></span>
- <span data-ttu-id="4d237-125">Jos Windows-tietokoneiden hallintaan käytetään MDM:ää, kuten Intunea, lisätietoja on kohdassa [CSP-käytäntö – ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span><span class="sxs-lookup"><span data-stu-id="4d237-125">If you are using MDM, such as Intune to manage your Windows computers, see [Policy CSP - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).</span></span>
- <span data-ttu-id="4d237-126">Jos olet mukautettua sivustoa rakentava kehittäjä, katso [URI:n oletussovelluksen käynnistäminen](/windows/uwp/launch-resume/launch-default-app).</span><span class="sxs-lookup"><span data-stu-id="4d237-126">If you are a developer building a custom website, see [Launch the default app for a URI](/windows/uwp/launch-resume/launch-default-app).</span></span>

## <a name="open-a-native-app-seamlessly"></a><span data-ttu-id="4d237-127">Alkuperäisen sovelluksen sujuva avaaminen</span><span class="sxs-lookup"><span data-stu-id="4d237-127">Open a native app seamlessly</span></span>

<span data-ttu-id="4d237-128">Windows, iOS ja Android sallivat lisäksi sovellusten entistä sujuvamman avaamisen sovelluksen protokollaliitoksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="4d237-128">Windows, iOS, and Android also allow opening of apps more seamlessly, based on app protocol association.</span></span> <span data-ttu-id="4d237-129">Jos sovellusta ei ole vielä määritetty käsittelemään avaamista selaimesta, kehittäjän on ehkä määritettävä tämä.</span><span class="sxs-lookup"><span data-stu-id="4d237-129">If your app is not already configured to handle opening from a web browser, you may need a developer to configure this.</span></span>

- <span data-ttu-id="4d237-130">Windows: katso [Sovellusten käyttöönotto sivustoja varten sovelluksen URI-käsittelijöiden avulla](/windows/uwp/launch-resume/web-to-app-linking).</span><span class="sxs-lookup"><span data-stu-id="4d237-130">For Windows, see [Enable apps for websites using app URI handlers](/windows/uwp/launch-resume/web-to-app-linking).</span></span>
- <span data-ttu-id="4d237-131">iOS: katso [Kehittäjien yleiset linkit](https://developer.apple.com/ios/universal-links/).</span><span class="sxs-lookup"><span data-stu-id="4d237-131">For iOS, see [Universal Links for Developers](https://developer.apple.com/ios/universal-links/).</span></span>
- <span data-ttu-id="4d237-132">Android: katso [Android-sovelluksen linkkien käsitteleminen](https://developer.android.com/training/app-links/).</span><span class="sxs-lookup"><span data-stu-id="4d237-132">For Android, see [Handling Android App Links](https://developer.android.com/training/app-links/).</span></span>

| <span data-ttu-id="4d237-133">Asiakas</span><span class="sxs-lookup"><span data-stu-id="4d237-133">Client</span></span>                | <span data-ttu-id="4d237-134">Avaa uudessa ikkunassa</span><span class="sxs-lookup"><span data-stu-id="4d237-134">Open in new window</span></span> | <span data-ttu-id="4d237-135">Alkuperäisen sovelluksen avaaminen</span><span class="sxs-lookup"><span data-stu-id="4d237-135">Open native app</span></span> | <span data-ttu-id="4d237-136">Avaaminen POS-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="4d237-136">Open within POS</span></span> | <span data-ttu-id="4d237-137">Yksityiskohdat</span><span class="sxs-lookup"><span data-stu-id="4d237-137">Details</span></span>                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| <span data-ttu-id="4d237-138">Windowsin Modern POS</span><span class="sxs-lookup"><span data-stu-id="4d237-138">Modern POS on Windows</span></span> | <span data-ttu-id="4d237-139">✓\*</span><span class="sxs-lookup"><span data-stu-id="4d237-139">✓\*</span></span>                | <span data-ttu-id="4d237-140">✓</span><span class="sxs-lookup"><span data-stu-id="4d237-140">✓</span></span>               | <span data-ttu-id="4d237-141">✓</span><span class="sxs-lookup"><span data-stu-id="4d237-141">✓</span></span>              | <span data-ttu-id="4d237-142">\* Avautuu uudessa Modern POS -ikkunassa</span><span class="sxs-lookup"><span data-stu-id="4d237-142">\* Opens in new Modern POS window</span></span> |
| <span data-ttu-id="4d237-143">Cloud POS</span><span class="sxs-lookup"><span data-stu-id="4d237-143">Cloud POS</span></span>             | <span data-ttu-id="4d237-144">✓\*</span><span class="sxs-lookup"><span data-stu-id="4d237-144">✓\*</span></span>                | <span data-ttu-id="4d237-145">✓</span><span class="sxs-lookup"><span data-stu-id="4d237-145">✓</span></span>               | <span data-ttu-id="4d237-146">X</span><span class="sxs-lookup"><span data-stu-id="4d237-146">X</span></span>              | <span data-ttu-id="4d237-147">\* Avautuu uudessa selainvälilehdessä</span><span class="sxs-lookup"><span data-stu-id="4d237-147">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="4d237-148">iOS:n Modern POS</span><span class="sxs-lookup"><span data-stu-id="4d237-148">Modern POS on iOS</span></span>     | <span data-ttu-id="4d237-149">✓\*</span><span class="sxs-lookup"><span data-stu-id="4d237-149">✓\*</span></span>                | <span data-ttu-id="4d237-150">✓</span><span class="sxs-lookup"><span data-stu-id="4d237-150">✓</span></span>               | <span data-ttu-id="4d237-151">X</span><span class="sxs-lookup"><span data-stu-id="4d237-151">X</span></span>              | <span data-ttu-id="4d237-152">\* Avautuu uudessa selainvälilehdessä</span><span class="sxs-lookup"><span data-stu-id="4d237-152">\* Opens in new browser tab</span></span>        |
| <span data-ttu-id="4d237-153">Modern POS:n Android-versio</span><span class="sxs-lookup"><span data-stu-id="4d237-153">Modern POS on Android</span></span> | <span data-ttu-id="4d237-154">✓\*</span><span class="sxs-lookup"><span data-stu-id="4d237-154">✓\*</span></span>                | <span data-ttu-id="4d237-155">✓</span><span class="sxs-lookup"><span data-stu-id="4d237-155">✓</span></span>               | <span data-ttu-id="4d237-156">X</span><span class="sxs-lookup"><span data-stu-id="4d237-156">X</span></span>              | <span data-ttu-id="4d237-157">\* Avautuu uudessa selainvälilehdessä</span><span class="sxs-lookup"><span data-stu-id="4d237-157">\* Opens in new browser tab</span></span>        |

## <a name="before-you-begin"></a><span data-ttu-id="4d237-158">Ennen aloittamista</span><span class="sxs-lookup"><span data-stu-id="4d237-158">Before you begin</span></span>

<span data-ttu-id="4d237-159">Tarkista ennen aloittamista, miten [myyntipisteen (POS) näytön asettelut](pos-screen-layouts.md) määritetään.</span><span class="sxs-lookup"><span data-stu-id="4d237-159">Before you begin, review how to configure [Screen layouts for the point of sale (POS)](pos-screen-layouts.md).</span></span>

## <a name="open-url-in-pos"></a><span data-ttu-id="4d237-160">URL-linkin avaaminen POS-sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="4d237-160">Open URL in POS</span></span>

<span data-ttu-id="4d237-161">Määritä URL-osoite avautumaan POS:ssä seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="4d237-161">To configure a URL to be opened in POS, perform the following steps.</span></span>

1. <span data-ttu-id="4d237-162">Valitse pääkonttorissa **Vähittäismyynti ja kauppa \> Kanavan asetukset \> POS-asetukset \> Myyntipiste \> Näytön asettelut**.</span><span class="sxs-lookup"><span data-stu-id="4d237-162">In head office, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> Screen Layouts**.</span></span>
2. <span data-ttu-id="4d237-163">Valitse **Painikeruudukot \> Suunnittelutoiminto**.</span><span class="sxs-lookup"><span data-stu-id="4d237-163">Select **Button Grids \> Designer**.</span></span>
3. <span data-ttu-id="4d237-164">Luo uusi painike.</span><span class="sxs-lookup"><span data-stu-id="4d237-164">Create a new button.</span></span>
4. <span data-ttu-id="4d237-165">Valitse **Painikeominaisuudet**.</span><span class="sxs-lookup"><span data-stu-id="4d237-165">Select **Button** properties.</span></span>
5. <span data-ttu-id="4d237-166">Valitse **Avaa URL** toimintona.</span><span class="sxs-lookup"><span data-stu-id="4d237-166">Select **Open URL** as the action.</span></span>
6. <span data-ttu-id="4d237-167">Anna käytettävä URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="4d237-167">Enter the URL that you want to use.</span></span>
7. <span data-ttu-id="4d237-168">Määritä, avataanko URL-osoite uudessa ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="4d237-168">Configure whether to open the URL in a new window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
