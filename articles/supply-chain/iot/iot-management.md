---
title: IoT-analytiikan seuranta ja hallinta
description: Tässä ohjeaiheessa käsitellään IoT-analytiikan seurantaa ja hallintaa.
author: robinarh
ms.date: 08/16/2019
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
ms.openlocfilehash: 94665b3646456b689a8e65e94b098e86e467d5e3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813072"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="b0631-103">IoT-analytiikan seuranta ja hallinta</span><span class="sxs-lookup"><span data-stu-id="b0631-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0631-104">Tässä ohjeaiheessa käsitellään IoT-analytiikan seurantaa ja hallintaa.</span><span class="sxs-lookup"><span data-stu-id="b0631-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="b0631-105">Microsoft Dynamics 365 Supply Chain Managementin valvontaskenaariot</span><span class="sxs-lookup"><span data-stu-id="b0631-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="b0631-106">IoT-analytiikan käsittelyä voi seurata monessa paikassa:</span><span class="sxs-lookup"><span data-stu-id="b0631-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="b0631-107">**Moduulit \> Tuotannonhallinta \> Kyselyt ja raportit \> IoT-analytiikka \> Ilmoitukset** – ratkaisemattomia ilmoituksia sisältävän luettelon tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="b0631-108">**Moduulit \> Tuotannonhallinta \> Kyselyt ja raportit \> IoT-analytiikka \> Suljetut ilmoitukset** – ratkaistut tai hylätyt ilmoitukset sisältävän luettelon tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="b0631-109">**Moduulit \> Tuotannonhallinta \> Kyselyt ja raportit \> IoT-analytiikka \> Arvoavaimet** – **Resurssin tila** -aikasarjakaavioiden arvojen näyttäminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="b0631-110">**Moduulit \> Tuotannonhallinta \> Tuotannonohjaus \> Resurssin tila** – tiettyjen mittarien seuranta **Määritä**-valintaikkunan avulla.</span><span class="sxs-lookup"><span data-stu-id="b0631-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="b0631-111">Jos skenaario havaitsee poikkeuksen, ilmoitus näyttää poikkeuksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="b0631-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="b0631-112">**Työtilat \> Tuotannon hallinta \> Ilmoitukset** – ratkaisemattomien ilmoitusten luettelon tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="b0631-113">Meneillään olevan IoT-analytiikkaskenaarion muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="b0631-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="b0631-114">Meneillään olevaan skenaarioon voi tehdä seuraavat muutokset:</span><span class="sxs-lookup"><span data-stu-id="b0631-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="b0631-115">Uuden anturin rakennemäärityksen lisääminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="b0631-116">Uusien signaalin tietoarvojen valitseminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-116">Select new signal data values.</span></span>
+ <span data-ttu-id="b0631-117">Aiemmin luotujen signaalin tietoarvojen peruuttaminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="b0631-118">Uuden signaalin tietoarvojen lisääminen ja yhdistäminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="b0631-119">Raja-arvojen päivittäminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-119">Update threshold values.</span></span>

<span data-ttu-id="b0631-120">Seuraavat muutokset meneillään olevaan skenaarioon on kielletty:</span><span class="sxs-lookup"><span data-stu-id="b0631-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="b0631-121">Käyttöönotetun skenaarion parhaillaan käyttämien rakennemääritysten poistaminen tai muokkaaminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="b0631-122">Käyttöönotetun skenaarion rakennepolkujen muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="b0631-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="b0631-123">Simulointiasetukset</span><span class="sxs-lookup"><span data-stu-id="b0631-123">Simulation options</span></span>

<span data-ttu-id="b0631-124">Tehtaan laitteen signaaleja voi simuloida.</span><span class="sxs-lookup"><span data-stu-id="b0631-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="b0631-125">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="b0631-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="b0631-126">IoT DevKit AZ3166:n yhdistäminen Azuren IoT-keskittimeen</span><span class="sxs-lookup"><span data-stu-id="b0631-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="b0631-127">Raspberry Pi -verkkosimulaattorin yhdistäminen Azuren IoT-keskittimeen (Node.js)</span><span class="sxs-lookup"><span data-stu-id="b0631-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="b0631-128">Laitesimulaatioratkaisun apuohjelman yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b0631-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]