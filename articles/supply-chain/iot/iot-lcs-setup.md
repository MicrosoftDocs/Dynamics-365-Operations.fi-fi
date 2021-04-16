---
title: IoT-analytiikkalisäosan asentaminen LCS:ssä
description: Tässä ohjeaiheessa käsitellään IoT-analytiikkalisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS).
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d1cc9a7535be05a3e466c27e53047d694cf0160
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826440"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="a49f7-103">IoT-analytiikkalisäosan asentaminen LCS:ssä</span><span class="sxs-lookup"><span data-stu-id="a49f7-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a49f7-104">Tässä ohjeaiheessa käsitellään IoT-analytiikkalisäosan asentamista Microsoft Dynamics Lifecycle Servicesiin (LCS).</span><span class="sxs-lookup"><span data-stu-id="a49f7-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="a49f7-105">Huomaa, että lisäosia ei voi asentaa esittely- tai kokeiluympäristöön.</span><span class="sxs-lookup"><span data-stu-id="a49f7-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="a49f7-106">Ennen lisäosan asentamista on [luotava Azure-resurssit](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a49f7-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="a49f7-107">LCS-ympäristön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a49f7-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="a49f7-108">Avaa LCS ja siirry Microsoft Dynamics 365 Supply Chain Management -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="a49f7-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="a49f7-109">Vieritä **Ympäristön lisäosat** -osaan.</span><span class="sxs-lookup"><span data-stu-id="a49f7-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="a49f7-110">Valitse **Asenna uusi lisäosa**, jolloin näkyviin tulee luettelo ympäristössä käyttöönotetuista lisäosista.</span><span class="sxs-lookup"><span data-stu-id="a49f7-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="a49f7-111">Valitse **Valitse asennettava lisäosa** -valintaikkunassa **IoT-analytiikka**.</span><span class="sxs-lookup"><span data-stu-id="a49f7-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="a49f7-112">Anna **Määritä lisäosa** -valintaikkunassa IoT-keskittimen ja Redis-välimuistin tiedot.</span><span class="sxs-lookup"><span data-stu-id="a49f7-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="a49f7-113">Tarvittavat arvot sijaitsevat avainsäilössä, joka luotiin kohdassa [Azure-resurssien luonti](iot-azure-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a49f7-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="a49f7-114">**Vuokraajan tunnus** – Siirry Azure-portaalissa avainsäilöön ja valitse sitten vasemmassa siirtymisruudussa **Yleiskatsaus** ja kopioi **Hakemistotunnus**-arvo.</span><span class="sxs-lookup"><span data-stu-id="a49f7-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="a49f7-115">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="a49f7-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="a49f7-116">**IoT-tapahtuman keskittimen kanssa yhteensopiva päätepisteen avainsäilön URI** – Siirry avainsäilöön, valitse vasemmassa siirtymisruudussa **Yleiskatsaus** ja kopioi **DNS-nimi**-arvo.</span><span class="sxs-lookup"><span data-stu-id="a49f7-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="a49f7-117">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="a49f7-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="a49f7-118">**IoT-tapahtuman keskittimen kanssa yhteensopivan päätepisteen salaisuuden nimi** – Siirry avainsäilöön ja valitse sitten vasemmassa siirtymisruudussa **Salaisuudet** ja kopioi salaisuuden nimi sinne, mihin IoT-keskittimen tapahtuman keskittimen yhteysmerkkijono on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="a49f7-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="a49f7-119">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="a49f7-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="a49f7-120">**Redis-välimuistin avainsäilön URI** – Siirry avainsäilöön, valitse vasemmassa siirtymisruudussa **Yleiskatsaus** ja kopioi **DNS-nimi**-arvo.</span><span class="sxs-lookup"><span data-stu-id="a49f7-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="a49f7-121">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="a49f7-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="a49f7-122">**Redis-välimuistin päätepisteen salaisuuden nimi** – Siirry avainsäilöön ja valitse sitten vasemmassa siirtymisruudussa **Salaisuudet** ja kopioi salaisuuden nimi sinne, mihin Redis-välimuistin yhteysmerkkijono on tallennettu.</span><span class="sxs-lookup"><span data-stu-id="a49f7-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="a49f7-123">Liitä tämä arvo **Määritä lisäosa** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="a49f7-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="a49f7-124">Hyväksy ehdot valitsemalla valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="a49f7-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="a49f7-125">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="a49f7-125">Select **Install**.</span></span>
8. <span data-ttu-id="a49f7-126">Avautuva sanomaruutu ilmoitta, että lisäosan käynnistäminen asennettavaksi onnistui.</span><span class="sxs-lookup"><span data-stu-id="a49f7-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="a49f7-127">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a49f7-127">Select **OK**.</span></span>

<span data-ttu-id="a49f7-128">LCS-määritys on nyt valmis.</span><span class="sxs-lookup"><span data-stu-id="a49f7-128">LCS setup is now completed.</span></span> <span data-ttu-id="a49f7-129">Seuraavaksi [määritetään skenaariot](iot-scenario-setup.md).</span><span class="sxs-lookup"><span data-stu-id="a49f7-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="a49f7-130">Lisäosan asennuksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="a49f7-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="a49f7-131">[Poista skenaariot käytöstä](iot-scenario-setup.md#disable-a-scenario) Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="a49f7-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#disable-a-scenario).</span></span>
2. <span data-ttu-id="a49f7-132">Siirry LCS:ssä Supply Chain Management -ympäristön tietoihin.</span><span class="sxs-lookup"><span data-stu-id="a49f7-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="a49f7-133">Vieritä **Ympäristön lisäosat** -osaan.</span><span class="sxs-lookup"><span data-stu-id="a49f7-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="a49f7-134">Valitse IoT-analytiikkalisäosan osalta **Poista asennus**.</span><span class="sxs-lookup"><span data-stu-id="a49f7-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]