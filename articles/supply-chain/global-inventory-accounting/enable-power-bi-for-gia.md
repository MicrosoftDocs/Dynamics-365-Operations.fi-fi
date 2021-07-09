---
title: Power BI:n ottaminen käyttöön yleisessä varastokirjanpidossa
description: Tässä aiheessa kuvataan, kuinka Microsoft Power BI otetaan käyttöön yleisessä varastokirjanpidossa.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273149"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="55ea0-103">Power BI:n ottaminen käyttöön yleisessä varastokirjanpidossa</span><span class="sxs-lookup"><span data-stu-id="55ea0-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="55ea0-104">Voit kiinnittää ruutuja, koontinäyttöjä ja raportteja [PowerBI.com](https://powerbi.com/)-tilitäsi Microsoft Dynamics 365 -sovelluksen työtilaan.</span><span class="sxs-lookup"><span data-stu-id="55ea0-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="55ea0-105">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="55ea0-105">Prerequisites</span></span>

<span data-ttu-id="55ea0-106">Seuraavien edellytysten on oltava käytössä, ennen kuin voit ottaa Power BI -raportoinnin käyttöön:</span><span class="sxs-lookup"><span data-stu-id="55ea0-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="55ea0-107">Sinun tulee olla Dynamics 365 -sovelluksen järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="55ea0-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="55ea0-108">Sinulla on oltava [PowerBI.com](https://powerbi.com/)-tili.</span><span class="sxs-lookup"><span data-stu-id="55ea0-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="55ea0-109">Tililläsi on oltava vähintään yksi koontinäyttö ja yksi raportti Power BI -tililläsi.</span><span class="sxs-lookup"><span data-stu-id="55ea0-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="55ea0-110">Vain oman Azure Active Directory (Azure AD) -tilisi järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="55ea0-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="55ea0-111">Azure AD -toimialueen on oltava sama toimialue, jota käytät [PowerBI.com](https://powerbi.com/)-tilissäsi.</span><span class="sxs-lookup"><span data-stu-id="55ea0-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="55ea0-112">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="55ea0-112">Setup</span></span>

<span data-ttu-id="55ea0-113">Määritä Power BI -integrointi noudattamalla näitä ohjeita.</span><span class="sxs-lookup"><span data-stu-id="55ea0-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="55ea0-114">Kirjaudu [Microsoft Dynamics Lifecycle Servicesiin (LCS)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="55ea0-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="55ea0-115">Siirry **Jaettuun resurssikirjastoon**, valitse **Power BI -raporttimalli** resurssin tyypiksi ja lataa **Yleinen varastokirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="55ea0-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="55ea0-116">Kirjaudu sisään [PowerBI.comiin](https://app.powerbi.com/) ja lataa **Yleisen varastokirjanpidon** Power BI -raporttitiedosto noudattamalla seuraavia vaiheita:</span><span class="sxs-lookup"><span data-stu-id="55ea0-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="55ea0-117">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="55ea0-117">Select **New**.</span></span>
    1. <span data-ttu-id="55ea0-118">Valitse **Lataa tiedosto palveluun**.</span><span class="sxs-lookup"><span data-stu-id="55ea0-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="55ea0-119">Valitse **Yleisen varastokirjanpidon** Power BI -raporttitiedosto.</span><span class="sxs-lookup"><span data-stu-id="55ea0-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="55ea0-120">Konfiguroi **Yleisen varastokirjanpidon** Power BI -raportti seuraavien vaiheiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="55ea0-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="55ea0-121">Siirry kohtaan **Oma työtila**, etsi yleisen varastokirjanpidon tietojoukko ja valitse **Asetukset** **Asetukset**-valikosta.</span><span class="sxs-lookup"><span data-stu-id="55ea0-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="55ea0-122">Laajenna **Yleisen varastokirjanpidon asetukset** -kohdassa **Parametrit** ja päivitä kaikki parametrit tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="55ea0-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="55ea0-123">Rekisteröi sovellus [Määritä PowerBI.com-integrointi](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process) -kohdassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="55ea0-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="55ea0-124">Integroi **Yleisen varastokirjanpidon** Power BI -raporttitiedosto Dynamics 365 Supply Chain Managementiin seuraavien vaiheiden mukaisesti:</span><span class="sxs-lookup"><span data-stu-id="55ea0-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="55ea0-125">Valitse **Järjestelmän hallinta \> Asetukset \> PowerBI.comin konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="55ea0-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="55ea0-126">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="55ea0-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="55ea0-127">Valitse **Ota käyttöön PowerBI.Com -integrointi**.</span><span class="sxs-lookup"><span data-stu-id="55ea0-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="55ea0-128">Syötä **Sovellustunnus**-kenttään sovellustunnus.</span><span class="sxs-lookup"><span data-stu-id="55ea0-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="55ea0-129">Syötä **Sovellusavain**-kenttään sovellusavain.</span><span class="sxs-lookup"><span data-stu-id="55ea0-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="55ea0-130">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="55ea0-130">Select **Save**.</span></span>

1. <span data-ttu-id="55ea0-131">Päivitä sivu, jotta Power BIn kirjautumisvalintaikkuna tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="55ea0-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="55ea0-132">Valitse **Asetukset**-välilehdestä **Avaa raporttiluettelo** ja valitse sitten aiemmin lataamasi **Yleisen varastokirjanpidon** Power BI -raporttitiedosto.</span><span class="sxs-lookup"><span data-stu-id="55ea0-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="55ea0-133">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="55ea0-133">Refresh the page.</span></span> <span data-ttu-id="55ea0-134">Näin voit nähdä, että raporttisi on lisätty.</span><span class="sxs-lookup"><span data-stu-id="55ea0-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="55ea0-135">Valitse **Power BI -raportit** kohdasta **Yleinen varastokirjanpito** -linkki.</span><span class="sxs-lookup"><span data-stu-id="55ea0-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="55ea0-136">Lisätietoja kohdasta [Konfiguroi PowerBI.com-integraatiosi](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span><span class="sxs-lookup"><span data-stu-id="55ea0-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
