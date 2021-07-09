---
title: Warehouse Management -mobiilisovelluksen uudet ja muuttuneet ominaisuudet
description: Tässä aiheessa luetellaan jokaisen Microsoft Dynamics 365 Supply Chain Managementin Warehouse Management -mobiilisovelluksen vapautetun version uudet ja muuttuneet ominaisuudet.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261774"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="1a83b-103">Warehouse Management -mobiilisovelluksen uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="1a83b-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a83b-104">Tässä aiheessa luetellaan ominaisuudet, korjaukset, parannukset ja tunnetut ongelmat jokaisen Microsoft Dynamics 365 Supply Chain Managementin Warehouse Management -mobiilisovelluksen vapautetun version osalta.</span><span class="sxs-lookup"><span data-stu-id="1a83b-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="1a83b-105">Versio 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="1a83b-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="1a83b-106">Uudet ominaisuudet, korjaukset ja parannukset versiossa 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="1a83b-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="1a83b-107">Tämä versio sisältää seuraavat uudet ominaisuudet, korjaukset ja parannukset:</span><span class="sxs-lookup"><span data-stu-id="1a83b-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="1a83b-108">Demotila näyttää nyt kaikki etiketit laitteen kielellä.</span><span class="sxs-lookup"><span data-stu-id="1a83b-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="1a83b-109">Näyttöön tulee vähemmän todennäköisesti seuraava virhesanoma: "Sopivaa näkymää ei pystytä näyttämään määritetyssä koossa".</span><span class="sxs-lookup"><span data-stu-id="1a83b-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="1a83b-110">Työkorttien vähimmäiskorkeus on kasvanut (jos työluettelossa on määritetty näkymään vähintään kolme kenttää).</span><span class="sxs-lookup"><span data-stu-id="1a83b-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="1a83b-111">Tietokorttien alaosassa olevia marginaaleja (häivytetään) on parannettu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="1a83b-112">Palvelimessa vaihdeltavat XML-tiedostojen virheelliset symbolit käsitellään nyt onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="1a83b-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="1a83b-113">(Esimerkiksi tulostettavat merkit käsitellään nyt onnistuneesti, eikä sovelluksen enää tarvitse lopettaa vastaamista.)</span><span class="sxs-lookup"><span data-stu-id="1a83b-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="1a83b-114">HTTP-virheet (kuten virhe 503), kun palvelinpyyntö lähetetään, käsitellään nyt onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="1a83b-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="1a83b-115">Kun näyttöön tulee virhe, vaihtoehtoluetteloa ei enää näytetä automaattisesti yhdistelmäruudun ohjausobjekteille.</span><span class="sxs-lookup"><span data-stu-id="1a83b-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="1a83b-116">Sovellus ei enää lakkaa vastaamasta käyttäjäasetuksissa on valittu näytön suunnan vuoksi.</span><span class="sxs-lookup"><span data-stu-id="1a83b-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="1a83b-117">Tuotekuvat näkyvät nyt itsepalveluympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="1a83b-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="1a83b-118">(Tämä muutos koskee vain matalan resoluution versioita.</span><span class="sxs-lookup"><span data-stu-id="1a83b-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="1a83b-119">Tiedostonhallintapalvelu ei tue täysikokoisia kuvia itsepalveluympäristöissä.)</span><span class="sxs-lookup"><span data-stu-id="1a83b-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="1a83b-120">Ongelma, johon liittyi nollamäärän lyhyitä poimintoja, on korjattu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="1a83b-121">Sovellus ei enää lakkaa vastaamasta, kun tietokortissa näkyy useita samanlaisia kenttiä.</span><span class="sxs-lookup"><span data-stu-id="1a83b-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="1a83b-122">Tiedossa olevat virheet versiossa 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="1a83b-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="1a83b-123">Tässä versiossa on seuraavia tiedossa olevia virheitä:</span><span class="sxs-lookup"><span data-stu-id="1a83b-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="1a83b-124">Sovellus (erityisesti työluettelo) hidastuu ajan mittaan.</span><span class="sxs-lookup"><span data-stu-id="1a83b-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="1a83b-125">**Windows-versio:** Kun skannaukseen käytetään USB-asetta Windowsissa, epäjohdonmukaiset tulokset aiheuttavat skannattujen symbolien sekoittumisen.</span><span class="sxs-lookup"><span data-stu-id="1a83b-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="1a83b-126">Versio 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="1a83b-126">Version 2.0.5.0</span></span>

<span data-ttu-id="1a83b-127">Tämä versio sisältää seuraavat uudet ominaisuudet, korjaukset ja parannukset:</span><span class="sxs-lookup"><span data-stu-id="1a83b-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="1a83b-128">Asiakasohjelma ei ole enää piilotettu yhteysasetusten määritysten avulla.</span><span class="sxs-lookup"><span data-stu-id="1a83b-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="1a83b-129">Voit nyt painaa pitkään mitä tahansa tekstiä, jos haluat nähdä sen kokonaan.</span><span class="sxs-lookup"><span data-stu-id="1a83b-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="1a83b-130">Virheilmoitusta on parannettu, kun tallennuskäyttöoikeudet puuttuvat.</span><span class="sxs-lookup"><span data-stu-id="1a83b-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="1a83b-131">Joihinkin työnkulkuihin on lisätty uusia ohjaussarjoja.</span><span class="sxs-lookup"><span data-stu-id="1a83b-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="1a83b-132">Lähetyspainiketta ei enää voi käyttää virheellisesti ikkunan koon vuoksi.</span><span class="sxs-lookup"><span data-stu-id="1a83b-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="1a83b-133">Liukusäätimien käyttöä voi nyt jatkaa pienemmillä näytöillä, kun käytössä on suurempia painikekokoja.</span><span class="sxs-lookup"><span data-stu-id="1a83b-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="1a83b-134">Nelipainikkeen peittoa ei enää ole katkaistu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="1a83b-135">Näppäimistö tukee nyt Poista-painiketta.</span><span class="sxs-lookup"><span data-stu-id="1a83b-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="1a83b-136">Kirkkausongelma, joka voi ilmetä näppäimistöä painettaessa, on korjattu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="1a83b-137">Erilaisia demotietojen ongelmia on korjattu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="1a83b-138">Ongelma, johon tietosivun numeeriset kentät vaikuttavat, on korjattu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="1a83b-139">Näyttönäppäimistön käyttö ei enää ajoittain poistu näkyvistä joillakin laitteilla.</span><span class="sxs-lookup"><span data-stu-id="1a83b-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="1a83b-140">Erilaisia käyttöliittymävikoja (UI) on korjattu, kuten virheitä, jotka vaikuttivat taustaväriin ja asemointiin.</span><span class="sxs-lookup"><span data-stu-id="1a83b-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="1a83b-141">Venäjänkielistä käyttöliittymää on parannettu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="1a83b-142">Useita ongelmia, jotka saivat järjestelmän lopettamaan vastaamisen, on korjattu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="1a83b-143">Laskimen avaamiseen uudelleen liittyvä ongelma on korjattu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="1a83b-144">**Android-versio:** Virhe, joka aiheutti sen, että Android 4.4-versio lopetti vastaamisen käynnistyksen yhteydessä, on korjattu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="1a83b-145">**Android-versio:** Vähimmäisskaalaus on vähennetty 50 prosentiksi.</span><span class="sxs-lookup"><span data-stu-id="1a83b-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="1a83b-146">Versio 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="1a83b-146">Version 2.0.4.0</span></span>

<span data-ttu-id="1a83b-147">Versio 2.0.4.0 on Warehouse Management -mobiilisovelluksen ensimmäinen yleisesti saatavilla oleva versio.</span><span class="sxs-lookup"><span data-stu-id="1a83b-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="1a83b-148">Uudet ominaisuudet, korjaukset ja parannukset versiossa 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="1a83b-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="1a83b-149">Tässä versiossa esitellään seuraavat uudet ominaisuudet, korjaustiedostot ja parannukset, jotka eivät ole käytettävissä esiversiossa:</span><span class="sxs-lookup"><span data-stu-id="1a83b-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="1a83b-150">Jos tietokortissa on kaksi etikettiä, joissa on samanlaiset tiedot, toinen etiketistä piilotetaan.</span><span class="sxs-lookup"><span data-stu-id="1a83b-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="1a83b-151">Oletusarvon mukaan näytetään erikoismerkit, ja niiden piilovaihtoehto on poistettu käyttäjän asetuksista.</span><span class="sxs-lookup"><span data-stu-id="1a83b-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="1a83b-152">Käytöstä poistetut lähetyspainikkeet näytetään nyt niin, että ne eivät ole käytettävissä tässä näkymässä.</span><span class="sxs-lookup"><span data-stu-id="1a83b-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="1a83b-153">Muutokset ohjausobjektien järjestyksen logiikkaan varmistavat, että laitteiden skaalaukset ovat joustavampia.</span><span class="sxs-lookup"><span data-stu-id="1a83b-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="1a83b-154">Fonttien tai painikkeiden skaalaamista ei tarvitse enää muuttaa.</span><span class="sxs-lookup"><span data-stu-id="1a83b-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="1a83b-155">Oletusväriteema on muutettu *tummaksi*.</span><span class="sxs-lookup"><span data-stu-id="1a83b-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="1a83b-156">Käytöstä poistettujen lähetyspainikkeiden puuttuva kuvake on lisätty nauhanäkymään.</span><span class="sxs-lookup"><span data-stu-id="1a83b-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="1a83b-157">Aikakatkaisupoikkeukset vievät nyt yhteyssivulle linjavirheen näyttämisen sijaan.</span><span class="sxs-lookup"><span data-stu-id="1a83b-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="1a83b-158">Jos lähetystoimintoa ei ole käytettävissä (esimerkiksi **OK**, **Kyllä**, **Hyväksy**, **Valmis** tai **Valmis**), lähetyspainike poistetaan käytöstä.</span><span class="sxs-lookup"><span data-stu-id="1a83b-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="1a83b-159">Sovelluksen vakautta on parannettu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-159">App stability has been improved.</span></span>
- <span data-ttu-id="1a83b-160">[CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701) -suojausongelmat voidaan korjata.</span><span class="sxs-lookup"><span data-stu-id="1a83b-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="1a83b-161">**Windows-versio:** Windows-ongelma, jonka valikot eivät olleet responsiivisia ikkunan muuttamisen jälkeen, on korjattu.</span><span class="sxs-lookup"><span data-stu-id="1a83b-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="1a83b-162">Tiedossa oleva virhe versiossa 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="1a83b-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="1a83b-163">Tässä versiossa on seuraava tiedossa oleva virhe:</span><span class="sxs-lookup"><span data-stu-id="1a83b-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="1a83b-164">Tässä versiossa on ongelma, joka koskee laitteita, jotka käyttävät Android 4.4 -versiota.</span><span class="sxs-lookup"><span data-stu-id="1a83b-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="1a83b-165">Saatat kohdata ongelmia, kun käytät sovellusta tässä Android-versiossa.</span><span class="sxs-lookup"><span data-stu-id="1a83b-165">You might experience issues when you use the app on this Android version.</span></span>
