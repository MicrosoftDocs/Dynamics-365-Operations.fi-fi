---
title: IoT-analytiikkalisäosan asentaminen LCS:ssä
description: Tässä ohjeaiheessa käsitellään IoT-analytiikkalisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS).
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386509"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="52060-103">IoT-analytiikkalisäosan asentaminen LCS:ssä</span><span class="sxs-lookup"><span data-stu-id="52060-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52060-104">Tässä ohjeaiheessa käsitellään IoT-analytiikkalisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS).</span><span class="sxs-lookup"><span data-stu-id="52060-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="52060-105">Ennen lisäosan asentamista on [luotava Azure-resurssit](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="52060-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="52060-106">LCS-ympäristön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="52060-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="52060-107">Avaa LCS ja siirry Microsoft Dynamics 365 Supply Chain Management -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="52060-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="52060-108">Vieritä **Ympäristön lisäosat** -osaan.</span><span class="sxs-lookup"><span data-stu-id="52060-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="52060-109">Valitse **Asenna uusi lisäosa**, jolloin näkyviin tulee luettelo ympäristössä käyttöönotetuista lisäosista.</span><span class="sxs-lookup"><span data-stu-id="52060-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="52060-110">Valitse **Valitse asennettava lisäosa** -valintaikkunassa **IoT-analytiikka**.</span><span class="sxs-lookup"><span data-stu-id="52060-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="52060-111">Anna **Määritä lisäosa** -valintaikkunassa IoT-keskittimen ja Redis-välimuistin tiedot.</span><span class="sxs-lookup"><span data-stu-id="52060-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="52060-112">Tarvittavat arvot sijaitsevat avainsäilössä, joka luotiin kohdassa [Azure-resurssien luonti](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="52060-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="52060-113">**Vuokraajan tunnus** – Siirry Azure-portaalissa avainsäilöön ja valitse sitten vasemmassa siirtymisruudussa **Yleiskatsaus** ja kopioi **Hakemistotunnus**-arvo.</span><span class="sxs-lookup"><span data-stu-id="52060-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="52060-114">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="52060-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="52060-115">**IoT-tapahtuman keskittimen kanssa yhteensopiva päätepisteen avainsäilön URI** – Siirry avainsäilöön, valitse vasemmassa siirtymisruudussa **Yleiskatsaus** ja kopioi **DNS-nimi**-arvo.</span><span class="sxs-lookup"><span data-stu-id="52060-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="52060-116">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="52060-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="52060-117">**IoT-tapahtuman keskittimen kanssa yhteensopivan päätepisteen salaisuuden nimi** – Siirry avainsäilöön ja valitse sitten vasemmassa siirtymisruudussa **Salaisuudet** ja kopioi salaisuuden nimi sinne, mihin IoT-keskittimen tapahtuman keskittimen yhteysmerkkijono on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="52060-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="52060-118">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="52060-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="52060-119">**Redis-välimuistin avainsäilön URI** – Siirry avainsäilöön, valitse vasemmassa siirtymisruudussa **Yleiskatsaus** ja kopioi **DNS-nimi**-arvo.</span><span class="sxs-lookup"><span data-stu-id="52060-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="52060-120">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="52060-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="52060-121">**Redis-välimuistin päätepisteen salaisuuden nimi** – Siirry avainsäilöön ja valitse sitten vasemmassa siirtymisruudussa **Salaisuudet** ja kopioi salaisuuden nimi sinne, mihin Redis-välimuistin yhteysmerkkijono on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="52060-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="52060-122">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="52060-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="52060-123">Hyväksy ehdot valitsemalla valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="52060-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="52060-124">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="52060-124">Select **Install**.</span></span>
8. <span data-ttu-id="52060-125">Avautuva sanomaruutu ilmoitta, että lisäosan käynnistäminen asennettavaksi onnistui.</span><span class="sxs-lookup"><span data-stu-id="52060-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="52060-126">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="52060-126">Select **OK**.</span></span>

<span data-ttu-id="52060-127">LCS-määritys on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="52060-127">LCS setup is now completed.</span></span> <span data-ttu-id="52060-128">Seuraavaksi [määritetään skenaariot](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="52060-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="52060-129">Lisäosan asennuksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="52060-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="52060-130">[Poista skenaariot käytöstä](iot-scenario-setup.md#how-to-disable-a-scenario) Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="52060-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="52060-131">Siirry LCS:ssä Supply Chain Management -ympäristön tietoihin.</span><span class="sxs-lookup"><span data-stu-id="52060-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="52060-132">Vieritä **Ympäristön lisäosat** -osaan.</span><span class="sxs-lookup"><span data-stu-id="52060-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="52060-133">Valitse IoT-analytiikkalisäosan osalta **Poista asennus**.</span><span class="sxs-lookup"><span data-stu-id="52060-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>