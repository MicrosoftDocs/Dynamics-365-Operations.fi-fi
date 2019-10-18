---
title: Kuluraporttien uusi toteutus
description: Tässä ohjeaiheessa on tietoja uudelleensuunnitelluista ja uudistetuista kuluraporttikirjauksen kokemuksista Microsoft Dynamics 365 Financessa. Uusi kokemus yksinkertaistaa kuluraporttien täyttämistä ja lyhentää tarvittavaa aikaa.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 8a8ad1ad84b8acaa54d8b03327157a930e562f59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187656"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="2169c-104">Kuluraporttien uusi toteutus</span><span class="sxs-lookup"><span data-stu-id="2169c-104">Expense reports reimagined</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2169c-105">Kuluraporttimerkintää on uudistettu siten, että se yksinkertaistaa täyttämisprosessia ja lyhentää tarvittavaa aikaa.</span><span class="sxs-lookup"><span data-stu-id="2169c-105">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="2169c-106">Tässä ovat uuden kulukokemuksen tärkeimmät osat:</span><span class="sxs-lookup"><span data-stu-id="2169c-106">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="2169c-107">Uusi kulujenhallintatyötila, jonka avulla voit käyttää edustajan kuluja.</span><span class="sxs-lookup"><span data-stu-id="2169c-107">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="2169c-108">Uusi kuittien vastaavuuskokemus, joka näyttää paremmin otsikkotason vastaanotot ja helpottaa vastaanottojen liittämistä kuluriveihin.</span><span class="sxs-lookup"><span data-stu-id="2169c-108">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="2169c-109">Uusi vain luku -muotoinen ruudukko, jonka avulla voit tarkastella useita muita kulurivejä ja muita tietosarakkeita.</span><span class="sxs-lookup"><span data-stu-id="2169c-109">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="2169c-110">Voit nyt tarkastella kaikkia eriteltyjä ja jaettuja rivejä sekä niiden pääkuluja.</span><span class="sxs-lookup"><span data-stu-id="2169c-110">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="2169c-111">Yksinkertaistettu ruutu kulujen muokkaamista varten.</span><span class="sxs-lookup"><span data-stu-id="2169c-111">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="2169c-112">Uusitut virhe-, varoitus- ja käytäntösanomat auttavat takaamaan, että sinulla on oikea konteksti, jotta ymmärrät, mikä ongelma on ja miten se ratkaistaan.</span><span class="sxs-lookup"><span data-stu-id="2169c-112">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="2169c-113">Microsoft on poistanut useita sanomia, jotka tulivat näkyviin, ennen kuin käyttäjillä oli mahdollisuus suorittaa tehtävänsä ja käsitellä ongelmia, kuten epätäydellinen erittelysanoma.</span><span class="sxs-lookup"><span data-stu-id="2169c-113">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="2169c-114">Uusi sivu, jonka avulla voit määrittää, mitkä kentät ovat pakollisia organisaatiossa, mitkä kentät ovat valinnaisia ja mitä kenttiä ei saa siepata.</span><span class="sxs-lookup"><span data-stu-id="2169c-114">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="2169c-115">Tämän sivun avulla voit pienentää käyttäjien määrittämien kenttien määrää.</span><span class="sxs-lookup"><span data-stu-id="2169c-115">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="2169c-116">Kuluraporttien uusi ulkoasu ja tuntuma, jolloin raportit eivät enää vaikuta siltä kuin ne olisi suunniteltu kirjanpitoihmisille.</span><span class="sxs-lookup"><span data-stu-id="2169c-116">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="2169c-117">Voit ottaa uuden käyttökokemuksen käyttöön käyttämällä **Ominaisuuksien hallinta** -työtilaa, kun haluat ottaa **Kuluraporttien uusi toteutus** -ominaisuuden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2169c-117">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="2169c-118">Kun otat tämän toiminnon käyttöön, seuraavat toiminnot toteutuvat:</span><span class="sxs-lookup"><span data-stu-id="2169c-118">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="2169c-119">Aiemmin luotu kulujen työtila korvataan uudella työtilalla.</span><span class="sxs-lookup"><span data-stu-id="2169c-119">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="2169c-120">Uusi kulukentän näkyvyyden valikkovaihtoehto lisätään.</span><span class="sxs-lookup"><span data-stu-id="2169c-120">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="2169c-121">Kuluraporttien (aiemmin luodun sivun) tai kuluraportin kenttien aiemmin luotuja valikkokohteita ei poisteta.</span><span class="sxs-lookup"><span data-stu-id="2169c-121">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="2169c-122">Työn kulut ja hyväksynnät ovat edelleen olemassa kuluraportit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="2169c-122">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="2169c-123">Aloitusvideo uusille käyttäjille</span><span class="sxs-lookup"><span data-stu-id="2169c-123">Getting started video for new users</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

<span data-ttu-id="2169c-124">[Kulukokemus Dynamics 365 for Finance and Operationsissa](https://youtu.be/Ocy-MsTvEE0) -video (näkyy ylempänä) sisältyy [Finance and Operations -soittolistaan](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavilla YouTubessa.</span><span class="sxs-lookup"><span data-stu-id="2169c-124">The [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="new-features"></a><span data-ttu-id="2169c-125">Uudet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="2169c-125">New features</span></span>

| <span data-ttu-id="2169c-126">Uusi ominaisuus</span><span class="sxs-lookup"><span data-stu-id="2169c-126">New feature</span></span> | <span data-ttu-id="2169c-127">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="2169c-127">Description</span></span> |
|---|----|
| <span data-ttu-id="2169c-128">Kulukentän näkyvyys</span><span class="sxs-lookup"><span data-stu-id="2169c-128">Expense field visibility</span></span> | <span data-ttu-id="2169c-129">Uuden asetussivun avulla voit määrittää, mitkä kentät poistetaan käytöstä organisaatiossa, mitä kenttiä tarvitaan ja mitkä kentät ovat suositeltavia.</span><span class="sxs-lookup"><span data-stu-id="2169c-129">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="2169c-130">Pakolliset kentät</span><span class="sxs-lookup"><span data-stu-id="2169c-130">Required fields</span></span> | <span data-ttu-id="2169c-131">Uuden yksinkertaisen konfiguraation avulla voit tehdä joitakin tarvittavia kenttiä tarvitsematta käyttää käytäntökehystä.</span><span class="sxs-lookup"><span data-stu-id="2169c-131">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="2169c-132">Valinnaiset kentät</span><span class="sxs-lookup"><span data-stu-id="2169c-132">Optional fields</span></span> | <span data-ttu-id="2169c-133">Valinnaisten kenttien toinen sivu lisätään.</span><span class="sxs-lookup"><span data-stu-id="2169c-133">A second page for optional fields is added.</span></span> <span data-ttu-id="2169c-134">Näin työntekijät eivät tunne, että heidän on asetettava kentät, mutta kentät ovat edelleen helposti saatavilla.</span><span class="sxs-lookup"><span data-stu-id="2169c-134">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="2169c-135">Lisää vastaanotot, joita ei ole liitetty</span><span class="sxs-lookup"><span data-stu-id="2169c-135">Add unattached receipts</span></span> | <span data-ttu-id="2169c-136">Mahdollisuus lisätä ei-liitettyjä vastaanottoja kuluraporttiin näkyy enemmän työtilassa ja kuluraportissa.</span><span class="sxs-lookup"><span data-stu-id="2169c-136">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="2169c-137">Parannettu sanoman välitys</span><span class="sxs-lookup"><span data-stu-id="2169c-137">Improved messaging</span></span> | <span data-ttu-id="2169c-138">Parempi näkyvyys kuluriveille, joilla on varoituksia tai virheitä.</span><span class="sxs-lookup"><span data-stu-id="2169c-138">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="2169c-139">Sanomapalkin sanomien vähentäminen</span><span class="sxs-lookup"><span data-stu-id="2169c-139">Reduction in messages in the message bar</span></span>| <span data-ttu-id="2169c-140">Infolokin sanomien määrä väheni ja useissa tapauksissa yritettiin estää kaksoisarvoja sisältävien sanomien näkyminen.</span><span class="sxs-lookup"><span data-stu-id="2169c-140">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="2169c-141">Yhteen ryhmiteltyinä yhteiset toimenpiteet</span><span class="sxs-lookup"><span data-stu-id="2169c-141">Grouped together common actions</span></span> | <span data-ttu-id="2169c-142">Käyttöliittymä siivottiin lisäämällä uusia toimintoja -painike useimmille yleisille rivitason toiminnoille ja lisäämällä kolme pistettä (...) otsikolle ja muille harvemmin käytetyille toiminnoille.</span><span class="sxs-lookup"><span data-stu-id="2169c-142">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="2169c-143">Uusi työtila näkyvyyden lisäämiseksi</span><span class="sxs-lookup"><span data-stu-id="2169c-143">New workspace to increase visibility</span></span> | <span data-ttu-id="2169c-144">Uusi työtila yhdistää ominaisuudet ja linkit, joiden avulla käyttäjät voivat siirtyä eri alueille.</span><span class="sxs-lookup"><span data-stu-id="2169c-144">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="2169c-145">Aiemmin luotujen kulujen ja vastaanottojen lisääminen kulujen luonnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="2169c-145">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="2169c-146">Kun luot kuluraportteja, voit lisätä kaikki tai valitut kulut ja vastaanotot.</span><span class="sxs-lookup"><span data-stu-id="2169c-146">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="2169c-147">Vaihtokurssin laskin</span><span class="sxs-lookup"><span data-stu-id="2169c-147">Exchange rate calculator</span></span> | <span data-ttu-id="2169c-148">Järjestelmä lisää vaihtokurssin laskimen, jonka avulla voit laskea käteistapahtumien vaihtokurssin.</span><span class="sxs-lookup"><span data-stu-id="2169c-148">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="2169c-149">Tallenna ja lisää uusia kulurivejä</span><span class="sxs-lookup"><span data-stu-id="2169c-149">Save and add new expense lines</span></span> | <span data-ttu-id="2169c-150">**Tallenna**- ja **Uusi**-painikkeet ovat käytettävissä, kun uusia kuluja syötetään, jotta kulurivit voidaan syöttää nopeasti.</span><span class="sxs-lookup"><span data-stu-id="2169c-150">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="2169c-151">Parempi näkyvyys jaetuille ja eritellyille riveille</span><span class="sxs-lookup"><span data-stu-id="2169c-151">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="2169c-152">Eritellyt ja jaetut rivit lisätään suoraan kulujen luetteloon, mikä parantaa näkyvyyttä ja auttaa selvittämään, onko käytössä käytäntövirheitä tai muita virheitä.</span><span class="sxs-lookup"><span data-stu-id="2169c-152">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="2169c-153">Näytä kuitit erittelyissä</span><span class="sxs-lookup"><span data-stu-id="2169c-153">Show receipts during itemization</span></span> | <span data-ttu-id="2169c-154">Kuitit voidaan näyttää erittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="2169c-154">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="2169c-155">Ensimmäinen julkaisu keskittyy kulukirjaus skenaarioon.</span><span class="sxs-lookup"><span data-stu-id="2169c-155">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="2169c-156">Kuluraporttien tarkistus tai hyväksymisskenaario käyttää edelleen aiemmin luotua kulukirjaussivua.</span><span class="sxs-lookup"><span data-stu-id="2169c-156">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="2169c-157">Aiemmin luodussa sivussa on seuraavat ominaisuudet, mutta ne eivät ole vielä näkyvissä uudella sivulla.</span><span class="sxs-lookup"><span data-stu-id="2169c-157">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="2169c-158">Nämä ominaisuudet otetaan uudelleen käyttöön seuraavien useiden julkaisujen aikana:</span><span class="sxs-lookup"><span data-stu-id="2169c-158">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="2169c-159">Hyväksynnät</span><span class="sxs-lookup"><span data-stu-id="2169c-159">Approvals</span></span>
- <span data-ttu-id="2169c-160">Ostoreskontran hyväksynnät ja kirjanpidon muokkausmahdollisuus</span><span class="sxs-lookup"><span data-stu-id="2169c-160">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="2169c-161">Useita aloituskohtia</span><span class="sxs-lookup"><span data-stu-id="2169c-161">Multiple entry points</span></span>
- <span data-ttu-id="2169c-162">Matkustusehdotuksen integrointi</span><span class="sxs-lookup"><span data-stu-id="2169c-162">Travel requisition integration</span></span>
- <span data-ttu-id="2169c-163">Kulukentän näkyvyyden tietoyksikkö</span><span class="sxs-lookup"><span data-stu-id="2169c-163">Data entity for expense field visibility</span></span>
- <span data-ttu-id="2169c-164">Päivärahakulujen kirjaus</span><span class="sxs-lookup"><span data-stu-id="2169c-164">Entry for per-diem expenses</span></span>
- <span data-ttu-id="2169c-165">Rivitason työnkulku</span><span class="sxs-lookup"><span data-stu-id="2169c-165">Line-level workflow</span></span>
- <span data-ttu-id="2169c-166">Väliaikaisen hyväksyjän tuki</span><span class="sxs-lookup"><span data-stu-id="2169c-166">Interim approver support</span></span>
- <span data-ttu-id="2169c-167">Lisäerittely</span><span class="sxs-lookup"><span data-stu-id="2169c-167">Advanced itemization</span></span>