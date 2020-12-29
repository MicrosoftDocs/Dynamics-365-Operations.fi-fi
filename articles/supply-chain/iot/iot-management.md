---
title: IoT-analytiikan seuranta ja hallinta
description: Tässä ohjeaiheessa käsitellään IoT-analytiikan seurantaa ja hallintaa.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 15021281b9ec33cd0552bca16e3054d0d3cdd589
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427324"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="2ddbf-103">IoT-analytiikan seuranta ja hallinta</span><span class="sxs-lookup"><span data-stu-id="2ddbf-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ddbf-104">Tässä ohjeaiheessa käsitellään IoT-analytiikan seurantaa ja hallintaa.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="2ddbf-105">Microsoft Dynamics 365 Supply Chain Managementin valvontaskenaariot</span><span class="sxs-lookup"><span data-stu-id="2ddbf-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="2ddbf-106">IoT-analytiikan käsittelyä voi seurata monessa paikassa:</span><span class="sxs-lookup"><span data-stu-id="2ddbf-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="2ddbf-107">**Moduulit \> Tuotannonhallinta \> Kyselyt ja raportit \> IoT-analytiikka \> Ilmoitukset** – ratkaisemattomia ilmoituksia sisältävän luettelon tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="2ddbf-108">**Moduulit \> Tuotannonhallinta \> Kyselyt ja raportit \> IoT-analytiikka \> Suljetut ilmoitukset** – ratkaistut tai hylätyt ilmoitukset sisältävän luettelon tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="2ddbf-109">**Moduulit \> Tuotannonhallinta \> Kyselyt ja raportit \> IoT-analytiikka \> Arvoavaimet** – **Resurssin tila** -aikasarjakaavioiden arvojen näyttäminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="2ddbf-110">**Moduulit \> Tuotannonhallinta \> Tuotannonohjaus \> Resurssin tila** – tiettyjen mittarien seuranta **Määritä**-valintaikkunan avulla.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="2ddbf-111">Jos skenaario havaitsee poikkeuksen, ilmoitus näyttää poikkeuksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="2ddbf-112">**Työtilat \> Tuotannon hallinta \> Ilmoitukset** – ratkaisemattomien ilmoitusten luettelon tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="2ddbf-113">Meneillään olevan IoT-analytiikkaskenaarion muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="2ddbf-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="2ddbf-114">Meneillään olevaan skenaarioon voi tehdä seuraavat muutokset:</span><span class="sxs-lookup"><span data-stu-id="2ddbf-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="2ddbf-115">Uuden anturin rakennemäärityksen lisääminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="2ddbf-116">Uusien signaalin tietoarvojen valitseminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-116">Select new signal data values.</span></span>
+ <span data-ttu-id="2ddbf-117">Aiemmin luotujen signaalin tietoarvojen peruuttaminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="2ddbf-118">Uuden signaalin tietoarvojen lisääminen ja yhdistäminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="2ddbf-119">Raja-arvojen päivittäminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-119">Update threshold values.</span></span>

<span data-ttu-id="2ddbf-120">Seuraavat muutokset meneillään olevaan skenaarioon on kielletty:</span><span class="sxs-lookup"><span data-stu-id="2ddbf-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="2ddbf-121">Käyttöönotetun skenaarion parhaillaan käyttämien rakennemääritysten poistaminen tai muokkaaminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="2ddbf-122">Käyttöönotetun skenaarion rakennepolkujen muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="2ddbf-123">Simulointiasetukset</span><span class="sxs-lookup"><span data-stu-id="2ddbf-123">Simulation options</span></span>

<span data-ttu-id="2ddbf-124">Tehtaan laitteen signaaleja voi simuloida.</span><span class="sxs-lookup"><span data-stu-id="2ddbf-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="2ddbf-125">Lisätietoja on seuraavissa aiheissa:</span><span class="sxs-lookup"><span data-stu-id="2ddbf-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="2ddbf-126">IoT DevKit AZ3166:n yhdistäminen Azuren IoT-keskittimeen</span><span class="sxs-lookup"><span data-stu-id="2ddbf-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="2ddbf-127">Raspberry Pi -verkkosimulaattorin yhdistäminen Azuren IoT-keskittimeen (Node.js)</span><span class="sxs-lookup"><span data-stu-id="2ddbf-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="2ddbf-128">Laitesimulaatioratkaisun apuohjelman yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2ddbf-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
