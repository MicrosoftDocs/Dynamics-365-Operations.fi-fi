---
title: Yleisen varastokirjanpidon käytön aloittaminen
description: Tässä aiheessa kuvataan, kuinka yleinen varastokirjanpito otetaan käyttöön.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301695"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="661ae-103">Yleisen varastokirjanpidon käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="661ae-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="661ae-104">Yleisen varastokirjanpidon avulla voit suorittaa useita varastokirjanpitoja määrittämissäsi yleisissä varastokirjanpitorekistereissä.</span><span class="sxs-lookup"><span data-stu-id="661ae-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="661ae-105">Kukin yleinen varastokirjanpitotapahtuma liitetään *käytäntöön*.</span><span class="sxs-lookup"><span data-stu-id="661ae-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="661ae-106">Yleissopimus on kokoelma seuraavantyyppisiä kirjanpitokäytäntöjä:</span><span class="sxs-lookup"><span data-stu-id="661ae-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="661ae-107">Kustannusobjekti</span><span class="sxs-lookup"><span data-stu-id="661ae-107">Cost object</span></span>
- <span data-ttu-id="661ae-108">Syötteen mittaperuste</span><span class="sxs-lookup"><span data-stu-id="661ae-108">Input measurement basis</span></span>
- <span data-ttu-id="661ae-109">Kustannusvirran oletus</span><span class="sxs-lookup"><span data-stu-id="661ae-109">Cost flow assumption</span></span>
- <span data-ttu-id="661ae-110">Kustannustaso</span><span class="sxs-lookup"><span data-stu-id="661ae-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="661ae-111">Vaikka olet ottanut yleisen varastokirjanpidon käyttöön, voit silti tehdä varastokirjanpidon Microsoft Dynamics 365 Supply Chain Management -ohjelmassa tavalliseen tapaan.</span><span class="sxs-lookup"><span data-stu-id="661ae-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="661ae-112">Yleinen varastokirjanpito on apuohjelma.</span><span class="sxs-lookup"><span data-stu-id="661ae-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="661ae-113">Jos haluat käyttää sen toimintoja, sinun on asennettava se Microsoft Dynamics Lifecycle Servicesistä (LCS).</span><span class="sxs-lookup"><span data-stu-id="661ae-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="661ae-114">Voit valita, että se arvioidaan testiympäristössä, ennen kuin otat sen käyttöön tuotantoympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="661ae-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="661ae-115">Yleinen varastolaskenta ei tällä hetkellä tue kaikkia Supply Chain Managementiin integroituja kustannustenhallintaominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="661ae-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="661ae-116">Tämän vuoksi on tärkeää arvioida, vastaako tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="661ae-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="661ae-117">Yleisen varastolaskennan julkisen esiversion saaminen</span><span class="sxs-lookup"><span data-stu-id="661ae-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="661ae-118">Jotta voit käyttää yleistä varastokirjanpitoa, sinulla on oltava LCS-yhteensopiva korkean käytettävyyden ympäristö (ei OneBox-ympäristö).</span><span class="sxs-lookup"><span data-stu-id="661ae-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="661ae-119">Lisäksi käytössä tulee olla Supply Chain Managementin versio 10.0.19 tai sitä myöhempi.</span><span class="sxs-lookup"><span data-stu-id="661ae-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="661ae-120">Jos haluat rekisteröityä yleisen varastokirjanpidon julkiseen esiversioon, lähetä LCS-ympäristötunnus sähköpostitse [yleiselle varastokirjanpitotiimille](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="661ae-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="661ae-121">Kun olet hyväksynyt ohjelman, tiimi lähettää sinulle seurantasähköpostiviestin, joka sisältää yleisen varastokirjanpidon beta-avaimen ja huollon päätepisteet.</span><span class="sxs-lookup"><span data-stu-id="661ae-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="661ae-122">Kun olet saanut beta-avaimen, [voit asentaa lisäosan](#install).</span><span class="sxs-lookup"><span data-stu-id="661ae-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="661ae-123">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="661ae-123">Licensing</span></span>

<span data-ttu-id="661ae-124">Yleinen varastokirjanpito on lisensoitu yhdessä Supply Chain Managementin käytettävissä olevien varastokirjanpidon vakiotoimintojen kanssa.</span><span class="sxs-lookup"><span data-stu-id="661ae-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="661ae-125">Sinun ei tarvitse ostaa lisäkäyttöoikeutta, jotta voisit käyttää yleistä varastokirjanpitoa.</span><span class="sxs-lookup"><span data-stu-id="661ae-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="661ae-126">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="661ae-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="661ae-127">Määritä Microsoft Power Platform -integroinnin asetukset</span><span class="sxs-lookup"><span data-stu-id="661ae-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="661ae-128">Ennen kuin voit ottaa apuohjelmatoiminnon käyttöön, sinun on integroitava Microsoft Power Platformiin noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="661ae-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="661ae-129">Avaa LCS-ympäristö, johon haluat lisätä palvelun.</span><span class="sxs-lookup"><span data-stu-id="661ae-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="661ae-130">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="661ae-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="661ae-131">Valitse **Määritys** **Power Platform -integrointi** -osasta.</span><span class="sxs-lookup"><span data-stu-id="661ae-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="661ae-132">Valitse valintaruutu **Power platform -ympäristön asetus** -valintaikkunassa ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="661ae-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="661ae-133">Asetusten määritys kestää yleensä 60 - 90 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="661ae-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="661ae-134">Kun Microsoft Power Platform -ympäristö on tehty valmiiksi, sivulla näkyy ympäristösi nimi.</span><span class="sxs-lookup"><span data-stu-id="661ae-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="661ae-135">**Power Platform -Integrointi** -osassa näkyy myös lauseke "Power Platform -ympäristöasetukset on tehty".</span><span class="sxs-lookup"><span data-stu-id="661ae-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="661ae-136">Yleinen varastokirjanpito ei edellytä kaksoiskirjoitussovellusta.</span><span class="sxs-lookup"><span data-stu-id="661ae-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="661ae-137">Lisätietoja on ohjeaiheessa [Asennus ympäristön käyttöönoton jälkeen](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="661ae-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="661ae-138">Dataversen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="661ae-138">Set up Dataverse</span></span>

<span data-ttu-id="661ae-139">Lisää yleiset varastokirjanpidon palveluperiaatteet vuokraajaasi ennen Dataversen käyttöä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="661ae-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="661ae-140">Asenna Azure AD Module for Windows PowerShell v2, kuten kuvattu kohdassa [Asenna Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="661ae-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="661ae-141">Suorita seuraava PowerShell-komento.</span><span class="sxs-lookup"><span data-stu-id="661ae-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="661ae-142">Luo seuraavaksi sovelluskäyttäjät yleistä varastokirjanpitoa varten Dataversessä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="661ae-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="661ae-143">Avaa Dataverse-ympäristön URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="661ae-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="661ae-144">Valitse **Lisäasetukset \> Järjestelmä \> Suojaus \> Käyttäjät** ja luo sovelluskäyttäjä.</span><span class="sxs-lookup"><span data-stu-id="661ae-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="661ae-145">Vaihda sivunäkymäksi *Sovelluskäyttäjät* **Näkymä**-valikossa.</span><span class="sxs-lookup"><span data-stu-id="661ae-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="661ae-146">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="661ae-146">Select **New**.</span></span>
1. <span data-ttu-id="661ae-147">Määritä **Sovellustunnus**-kentän arvoksi *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="661ae-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="661ae-148">Valitse **Määritä rooli** ja valitse sitten *Järjestelmänvalvoja*.</span><span class="sxs-lookup"><span data-stu-id="661ae-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="661ae-149">Jos saatavana on rooli nimeltä *Common Data Service -käyttäjä*, valitse myös se.</span><span class="sxs-lookup"><span data-stu-id="661ae-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="661ae-150">Toista edelliset vaiheet, mutta määritä **Sovellustunnus**-kentän arvoksi *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="661ae-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="661ae-151">Lisätietoja on kohdassa [Sovelluskäyttäjän luominen](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="661ae-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="661ae-152">Jos Dataverse-asennuksen oletuskieli ei ole englanti, noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="661ae-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="661ae-153">Siirry kohtaan **Lisäasetukset \> Hallinta \> Kielet**.</span><span class="sxs-lookup"><span data-stu-id="661ae-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="661ae-154">Valitse *englanti* (*LanguageCode=1033*) ja valitse **Ota käyttöön**.</span><span class="sxs-lookup"><span data-stu-id="661ae-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="661ae-155">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="661ae-155">Install the add-in</span></span>

<span data-ttu-id="661ae-156">Asenna lisäosa noudattamalla seuraavia ohjeita, jotta voit käyttää yleistä varastokirjanpitoa.</span><span class="sxs-lookup"><span data-stu-id="661ae-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="661ae-157">[Kirjaudu](#sign-up) yleisen varastolaskennan julkisen esiversioon.</span><span class="sxs-lookup"><span data-stu-id="661ae-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="661ae-158">Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="661ae-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="661ae-159">Mene kohtaan **Toimintojen hallinnan esiversio**.</span><span class="sxs-lookup"><span data-stu-id="661ae-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="661ae-160">Valitse plusmerkki (**+**).</span><span class="sxs-lookup"><span data-stu-id="661ae-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="661ae-161">Syötä **Koodi**-kenttään yleisen varastokirjanpidon apuohjelman beeta-avain.</span><span class="sxs-lookup"><span data-stu-id="661ae-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="661ae-162">(Sinun olisi pitänyt saada beeta-avain sähköpostitse rekisteröityessäsi.)</span><span class="sxs-lookup"><span data-stu-id="661ae-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="661ae-163">Valitse **Poista esto**.</span><span class="sxs-lookup"><span data-stu-id="661ae-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="661ae-164">Avaa LCS-ympäristö, johon haluat lisätä palvelun.</span><span class="sxs-lookup"><span data-stu-id="661ae-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="661ae-165">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="661ae-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="661ae-166">Siirry **Power Platform -integrointiin** ja valitse **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="661ae-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="661ae-167">Valitse valintaruutu **Power platform -ympäristön asetus** -valintaikkunassa ja valitse sitten **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="661ae-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="661ae-168">Asetusten määritys kestää yleensä 60 - 90 minuuttia.</span><span class="sxs-lookup"><span data-stu-id="661ae-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="661ae-169">Kun Microsoft Power Platform -ympäristö on tehty valmiiksi, valitse **Ympäristö-lisäosat**-pikavälilehdillä **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="661ae-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="661ae-170">Valitse **Yleinen varastokirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="661ae-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="661ae-171">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="661ae-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="661ae-172">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="661ae-172">Select **Install**.</span></span>
1. <span data-ttu-id="661ae-173">**Ympäristön apuohjelmat** -pikavälilehdessä näkyy, että yleistä varastokirjanpitoa asennetaan.</span><span class="sxs-lookup"><span data-stu-id="661ae-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="661ae-174">Muutaman minuutin kuluttua tilan pitäisi muuttua tilasta *Asennetaan* tilaan *Asennettu*.</span><span class="sxs-lookup"><span data-stu-id="661ae-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="661ae-175">(Sivu on ehkä päivitettävä, jotta näet tämän muutoksen.) Tässä vaiheessa yleinen varastokirjanpito on valmis käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="661ae-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="661ae-176">Määritä integraatio</span><span class="sxs-lookup"><span data-stu-id="661ae-176">Set up the integration</span></span>

<span data-ttu-id="661ae-177">Seuraavia ohjeita noudattamalla voit määrittää yleisen varastokirjanpidon ja Supply Chain Managementin integroinnin.</span><span class="sxs-lookup"><span data-stu-id="661ae-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="661ae-178">Kirjaudu Supply Chain Managementiin.</span><span class="sxs-lookup"><span data-stu-id="661ae-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="661ae-179">Siirry kohtaan **Järjestelmänhallinta \> Ominaisuuksien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="661ae-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="661ae-180">Valitse **Tarkista päivitysten saatavuus**.</span><span class="sxs-lookup"><span data-stu-id="661ae-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="661ae-181">Etsi **Kaikki**-välilehdestä toiminto, jonka nimi on *Yleinen varastokirjanpito*.</span><span class="sxs-lookup"><span data-stu-id="661ae-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="661ae-182">Valitse **Ota käyttöön nyt**.</span><span class="sxs-lookup"><span data-stu-id="661ae-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="661ae-183">Siirry kohtaan **Yleinen varastokirjanpito \> Asetukset \> Yleisen varastokirjanpidon parametrit \> Integrointi-parametrit**.</span><span class="sxs-lookup"><span data-stu-id="661ae-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="661ae-184">Kirjoita **Tietopalvelun päätepiste**- ja **Yleisen varastokirjanpidon päätepiste** -kenttiin sen sähköpostiviestin URL-osoitteet, jonka yleinen varastokirjanpitotiimi on lähettänyt rekisteröityessäsi esiversioon.</span><span class="sxs-lookup"><span data-stu-id="661ae-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="661ae-185">Yleinen varastokirjanpito on nyt valmis käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="661ae-185">Global Inventory Accounting is now ready to use.</span></span>
