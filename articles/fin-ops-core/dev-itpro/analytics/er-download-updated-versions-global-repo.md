---
title: Tuo päivitetyt versiot sähköisen raportoinnin konfiguraatioista
description: Tässä ohjeaiheessa selitetään, miten sähköisen raportoinnin (ER) konfiguraatioiden päivitetyt versiot tuodaan Configuration Service -palvelun yleisestä säilöstä.
author: NickSelin
manager: AnnBe
ms.date: 06/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 0c65315c4fa6a42b4bbb0d008b58f8df9cc0ea3d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561875"
---
# <a name="import-updated-versions-of-er-configurations"></a><span data-ttu-id="77970-103">Tuo päivitetyt versiot sähköisen raportoinnin konfiguraatioista</span><span class="sxs-lookup"><span data-stu-id="77970-103">Import updated versions of ER configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="77970-104">Sähköisen raportoinnin (ER) [säilöjä](general-electronic-reporting.md#Repository) käytetään [sähköisen raportoinnin konfiguraatioiden](general-electronic-reporting.md#Configuration) jakamiseen.</span><span class="sxs-lookup"><span data-stu-id="77970-104">Electronic reporting (ER) [repositories](general-electronic-reporting.md#Repository) are used to share [ER configurations](general-electronic-reporting.md#Configuration).</span></span> <span data-ttu-id="77970-105">Voit [tuoda](download-electronic-reporting-configuration-lcs.md) sähköisen raportoinnin konfiguraatioita eri säilöistä omaan Microsoft Dynamics 365 Finance -esiintymääsi.</span><span class="sxs-lookup"><span data-stu-id="77970-105">You can [import](download-electronic-reporting-configuration-lcs.md) ER configurations from different repositories into your instance of Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="77970-106">Kun tuot sähköisen raportoinnin konfiguraatioita, [konfiguraation lähteet](general-electronic-reporting.md#Provider) voivat julkaista uusia [versioita](general-electronic-reporting.md#component-versioning) säilöistä, jotta ne voidaan jakaa.</span><span class="sxs-lookup"><span data-stu-id="77970-106">When you import ER configurations, [configuration providers](general-electronic-reporting.md#Provider) can publish new [versions](general-electronic-reporting.md#component-versioning) repositories so that they can be shared.</span></span>

<span data-ttu-id="77970-107">Tässä ohjeaiheessa selitetään, miten sähköisen raportoinnin konfiguraatioiden päivitetyt versiot tuodaan Configuration Service -palvelun yleisestä säilöstä.</span><span class="sxs-lookup"><span data-stu-id="77970-107">This topic explains how to import updated versions of ER configurations from the Global repository of the Configuration service.</span></span> <span data-ttu-id="77970-108">Lisätietoja on kohdassa [Microsoft Dynamics 365 for Finance and Operations -Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span><span class="sxs-lookup"><span data-stu-id="77970-108">For more information, see [Microsoft Dynamics 365 for Finance and Operations - Regulatory Services, Configuration service](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).</span></span>

## <a name="review-the-available-updated-versions"></a><span data-ttu-id="77970-109">Tarkasta saatavilla olevat päivitetyt versiot</span><span class="sxs-lookup"><span data-stu-id="77970-109">Review the available updated versions</span></span>

1. <span data-ttu-id="77970-110">Kirjaudu Financeen yhdellä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="77970-110">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="77970-111">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="77970-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="77970-112">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="77970-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="77970-113">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="77970-113">System administrator</span></span>

2. <span data-ttu-id="77970-114">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="77970-114">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="77970-115">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Tuo konfiguraatioversioiden päivitykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="77970-115">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>

    ![Lokalisoinnin konfiguraatiot -sivu](./media/er-download-updated-versions-global-repo1.png)

4. <span data-ttu-id="77970-117">Valitse **Tuo sähköisen raportoinnin konfiguraatioversioiden päivitykset** -valintaikkunan **Suoritustila** -kentässä **Näytä vain saatavilla olevat päivitykset**.</span><span class="sxs-lookup"><span data-stu-id="77970-117">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Only show available updates**.</span></span> <span data-ttu-id="77970-118">Valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="77970-118">Then select **OK**.</span></span> 

    ![Suoritustila-kentän asetus on Näytä vain saatavilla olevat päivitykset](./media/er-download-updated-versions-global-repo2.png)

5. <span data-ttu-id="77970-120">Tarkista saamasi sanomat.</span><span class="sxs-lookup"><span data-stu-id="77970-120">Review the messages that you receive.</span></span> <span data-ttu-id="77970-121">Nämä sanomat antavat seuraavia tietoja sähköisen raportoinnin konfiguraatioista nykyisessä Finance-esiintymässä ja vertaa niitä yleisen säilön sisältöön:</span><span class="sxs-lookup"><span data-stu-id="77970-121">These messages provide the following information about the ER configurations in the current Finance instance and how they compare to the content of the Global repository:</span></span>

    - <span data-ttu-id="77970-122">Sähköisen raportoinnin konfiguraatioiden kokonaismäärä</span><span class="sxs-lookup"><span data-stu-id="77970-122">The total number of ER configurations</span></span>
    - <span data-ttu-id="77970-123">Sähköisen raportoinnin konfiguraatiot, joita ei ole yleisessä säilössä</span><span class="sxs-lookup"><span data-stu-id="77970-123">ER configurations that aren't present in the Global repository</span></span>
    - <span data-ttu-id="77970-124">Sähköisen raportoinnin konfiguraatiot, joiden viimeisin versio on jo saatavilla nykyisessä Finance-esiintymässä (katso täydellinen luettelo näistä sähköisen raportoinnin konfiguraatioista valitsemalla **Sanoman tiedot** -linkki.)</span><span class="sxs-lookup"><span data-stu-id="77970-124">ER configurations for which the latest version is already available in the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Seuraavien konfiguraatioiden viimeisimmät versiot on jo tuotu -sanoma ja sanoman tiedot](./media/er-download-updated-versions-global-repo3.png)

    - <span data-ttu-id="77970-126">Sähköisen raportoinnin konfiguraatiot, joiden viimeisin versio on saatavilla yleisessä säilössä ja voidaan tuoda nykyiseen Finance-esiintymään (katso täydellinen luettelo näistä sähköisen raportoinnin konfiguraatioista valitsemalla **Sanoman tiedot** -linkki.)</span><span class="sxs-lookup"><span data-stu-id="77970-126">ER configurations for which the latest version is available in the Global repository and can be imported into the current Finance instance (To view the full list of these ER configurations, select the **Message details** link.)</span></span>

        ![Saatavilla olevat päivitykset -sanoma ja sanoman tiedot](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a><span data-ttu-id="77970-128">Päivitettyjen versioiden tuonti saatavilla</span><span class="sxs-lookup"><span data-stu-id="77970-128">Import available updated versions</span></span>

1. <span data-ttu-id="77970-129">Kirjaudu Financeen yhdellä seuraavista rooleista:</span><span class="sxs-lookup"><span data-stu-id="77970-129">Sign in to Finance by using one of the following roles:</span></span>

    - <span data-ttu-id="77970-130">Sähköisen raportoinnin kehittäjä</span><span class="sxs-lookup"><span data-stu-id="77970-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="77970-131">Sähköisen raportoinnin toiminnallinen konsultti</span><span class="sxs-lookup"><span data-stu-id="77970-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="77970-132">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="77970-132">System administrator</span></span>

2. <span data-ttu-id="77970-133">Valitse **Organisaation hallinto** \> **Työtilat** \> **Sähköinen raportointi**.</span><span class="sxs-lookup"><span data-stu-id="77970-133">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="77970-134">Valitse **Lokalisoinnin konfiguraatiot**-sivun **Liittyvät linkit**-osassa **Tuo konfiguraatioversioiden päivitykset**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="77970-134">On the **Localization configurations** page, in the **Related links** section, select **Import configurations versions updates**.</span></span>
4. <span data-ttu-id="77970-135">Valitse **Tuo sähköisen raportoinnin konfiguraatioversioiden päivitykset** -valintaikkunan **Suoritustila**-kentässä **Tuo viimeisimmät päivitykset** tuodaksesi sähköisen raportoinnin konfiguraatioiden viimeisimmät versiot yleisestä säilöstä nykyiseen Finance-esiintymään.</span><span class="sxs-lookup"><span data-stu-id="77970-135">In the **Import electronic reporting configurations versions updates** dialog box, in the **Run mode** field, select **Import latest updates** to import the latest versions of ER configurations from the Global repository into the current Finance instance.</span></span>
5. <span data-ttu-id="77970-136">Voit ajastaa erätyön tuonnille **Suorita taustalla** -pikavälilehdessä määrittämällä **Eräkäsittely**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="77970-136">To schedule a batch job for the import, on the **Run in the background** FastTab, set the **Batch processing** option to **Yes**.</span></span> <span data-ttu-id="77970-137">Jos haluat toistaa tuonnin säännöllisesti, määritä tarvittava toistuminen.</span><span class="sxs-lookup"><span data-stu-id="77970-137">If you want to repeat the import periodically, configure the required recurrence.</span></span>

    ![Suoritustila-kentän asetukseksi on määritetty Tuo viimeisimmät päivitykset](./media/er-download-updated-versions-global-repo5.png)

6. <span data-ttu-id="77970-139">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="77970-139">Select **OK**.</span></span>
7. <span data-ttu-id="77970-140">Jos haluat tietää, mitä konfiguraatioversioita on tuotu, noudata jotakin näistä ohjeista:</span><span class="sxs-lookup"><span data-stu-id="77970-140">To learn what configuration versions have been imported, follow one of these steps:</span></span>

    - <span data-ttu-id="77970-141">Jos suoritat tuonnin interaktiivisesti erätyön käyttämisen sijaan, tarkista saamasi sanomat.</span><span class="sxs-lookup"><span data-stu-id="77970-141">If you run the import interactively instead of using a batch job, review the messages that you receive.</span></span>

        ![Interaktiivisen tuonnin suorittamisen aikana saadut sanomat](./media/er-download-updated-versions-global-repo6.png)

    - <span data-ttu-id="77970-143">Jos suoritat tuonnin erätilassa, noudata näitä ohjeita:</span><span class="sxs-lookup"><span data-stu-id="77970-143">If you run the import in batch mode, follow these steps:</span></span>

        1. <span data-ttu-id="77970-144">Siirry kohtaan **Yleinen** \> **Kyselyt** \> **Erätyöt** \> **Omat erätyöt**.</span><span class="sxs-lookup"><span data-stu-id="77970-144">Go to **Common** \> **Inquiries** \> **Batch jobs** \> **My batch jobs**.</span></span>
        2. <span data-ttu-id="77970-145">Etsi ja valitse **Tuo sähköisen raportoinnin konfiguraatioversioiden päivitykset** -työ ja valitse sitten toimintoruudun **Erätyö**-välilehdessä **Erätyöhistoria** nähdäksesi työhistorian.</span><span class="sxs-lookup"><span data-stu-id="77970-145">Find and select the **Import electronic reporting configurations versions updates** job, and then, on the Action Pane, on the **Batch job** tab, select **Batch job history** to view the job history.</span></span>
        3. <span data-ttu-id="77970-146">Valitse **Erätyöhistoria**-sivulla **Loki**.</span><span class="sxs-lookup"><span data-stu-id="77970-146">On the **Batch job history** page, select **Log**.</span></span> <span data-ttu-id="77970-147">Valitse sitten saamassasi sanomassa **Sanoman tiedot** -linkki nähdäksesi työn lokin.</span><span class="sxs-lookup"><span data-stu-id="77970-147">Then, in the message that you receive, select the **Message details** link to view the job log.</span></span>

        ![Työloki](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> <span data-ttu-id="77970-149">Emme suosittele ajoittamaan toistuvaa erätyötä tuomaan sähköisen raportoinnin konfiguraatioiden päivitettyjä versioita suoraan yleisestä säilöstä tuotantoympäristöön, sillä tuodut versiot tulevat välittömästi saataville.</span><span class="sxs-lookup"><span data-stu-id="77970-149">We don't recommend that you schedule a recurring batch job to import updated versions of ER configurations directly from the Global repository into a production environment, because the imported versions will immediately be available for use.</span></span> <span data-ttu-id="77970-150">Käytä sen sijaan tätä lähestymistapaa ottaaksesi sähköisen raportoinnin konfiguraatioiden versiot käyttöön eristysympäristössä.</span><span class="sxs-lookup"><span data-stu-id="77970-150">Instead, use this approach to deploy versions of ER configurations to a sandbox environment.</span></span> <span data-ttu-id="77970-151">Tällöin ne voidaan arvioida eristysympäristössä ennen niiden käyttöönottoa tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="77970-151">They can then be evaluated in the sandbox environment before they are deployed to a production environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="77970-152">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="77970-152">Additional resources</span></span>

- [<span data-ttu-id="77970-153">Sähköisen raportoinnin (ER) yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="77970-153">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="77970-154">Lataa ER-konfiguraatiot konfigurointipalvelun yleisestä varastosta</span><span class="sxs-lookup"><span data-stu-id="77970-154">Download ER configurations from the Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]