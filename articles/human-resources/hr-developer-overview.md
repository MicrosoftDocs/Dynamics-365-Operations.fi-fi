---
title: Kehityksen yleiskatsaus
description: Tämä kehittäjän opas sisältää ohjelmointirajapinta- ja mukautetut kentät -viittaukset. Se sisältää myös tietoja integroinnista muihin sovelluksiin.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 517febd7967350956a28dfd9d11e4042456c7da0
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115387"
---
# <a name="development-overview"></a><span data-ttu-id="baca7-104">Kehityksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="baca7-104">Development overview</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="baca7-105">Tämä kehittäjän opas sisältää ohjelmointirajapinta- ja mukautetut kentät -viittaukset.</span><span class="sxs-lookup"><span data-stu-id="baca7-105">This Developer Guide provides an API and custom fields reference.</span></span> <span data-ttu-id="baca7-106">Se sisältää myös tietoja integroinnista muihin sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="baca7-106">It also provides information on integrating with other apps.</span></span>

- [<span data-ttu-id="baca7-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="baca7-107">Overview</span></span>](hr-developer-overview.md)

- [<span data-ttu-id="baca7-108">Laajentaminen Power Appsin ja Power Automaten avulla</span><span class="sxs-lookup"><span data-stu-id="baca7-108">Extend with Power Apps and Power Automate</span></span>](hr-developer-power-apps.md)

- [<span data-ttu-id="baca7-109">Henkilöstöhallinnon ilmentymät Dataversessä</span><span class="sxs-lookup"><span data-stu-id="baca7-109">Human Resources entities in Dataverse</span></span>](hr-developer-entities.md)

- [<span data-ttu-id="baca7-110">Mukautetut kentät</span><span class="sxs-lookup"><span data-stu-id="baca7-110">Custom fields</span></span>](hr-developer-custom-fields.md)

- <span data-ttu-id="baca7-111">Määritä dataintegrointi</span><span class="sxs-lookup"><span data-stu-id="baca7-111">Set up data integration</span></span>
  - [<span data-ttu-id="baca7-112">Tietojen integrointiteknologian valitseminen</span><span class="sxs-lookup"><span data-stu-id="baca7-112">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)
  - [<span data-ttu-id="baca7-113">Dataverse -integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="baca7-113">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)
  - [<span data-ttu-id="baca7-114">Integraation määrittäminen Financen kanssa</span><span class="sxs-lookup"><span data-stu-id="baca7-114">Configure integration with Finance</span></span>](hr-admin-integration-finance.md)
  - [<span data-ttu-id="baca7-115">Integraation määrittäminen Dayforcen kanssa</span><span class="sxs-lookup"><span data-stu-id="baca7-115">Configure integration with Dayforce</span></span>](hr-admin-integration-dayforce.md)
  - [<span data-ttu-id="baca7-116">Toistuvan tietojen viennin sovelluksen luominen</span><span class="sxs-lookup"><span data-stu-id="baca7-116">Create a recurring data export app</span></span>](hr-admin-integration-recurring-data-export.md)
  - <span data-ttu-id="baca7-117">Office-integraatio</span><span class="sxs-lookup"><span data-stu-id="baca7-117">Integrate with Office</span></span>
    - [<span data-ttu-id="baca7-118">Office-integraation opasohjelma</span><span class="sxs-lookup"><span data-stu-id="baca7-118">Office integration tutorial</span></span>](../dev-itpro/office-integration/office-integration-tutorial.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="baca7-119">Yksikkötietojen päivittäminen Excelissä</span><span class="sxs-lookup"><span data-stu-id="baca7-119">Update entity data in Excel</span></span>](../dev-itpro/office-integration/use-excel-add-in.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="baca7-120">Avaa Excelissä -kokemusten luominen</span><span class="sxs-lookup"><span data-stu-id="baca7-120">Create Open in Excel experiences</span></span>](../dev-itpro/office-integration/office-integration-edit-excel.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="baca7-121">Office-integraation vianmääritys</span><span class="sxs-lookup"><span data-stu-id="baca7-121">Troubleshoot Office integration</span></span>](../dev-itpro/office-integration/office-integration-troubleshooting.md?toc=/dynamics365/unified-operations/talent/toc.json)

- <span data-ttu-id="baca7-122">Yksikön ohjelmointirajapinnan viite</span><span class="sxs-lookup"><span data-stu-id="baca7-122">Entity API reference</span></span>
  - [<span data-ttu-id="baca7-123">Todennus</span><span class="sxs-lookup"><span data-stu-id="baca7-123">Authentication</span></span>](hr-developer-api-authentication.md)
  - <span data-ttu-id="baca7-124">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="baca7-124">Entities</span></span>
    - [<span data-ttu-id="baca7-125">MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="baca7-125">MyLeaveRequests</span></span>](hr-developer-api-myleaverequests-overview.md)
    - [<span data-ttu-id="baca7-126">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="baca7-126">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)

## <a name="see-also"></a><span data-ttu-id="baca7-127">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="baca7-127">See also</span></span>

- [<span data-ttu-id="baca7-128">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="baca7-128">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="baca7-129">Järjestelmänvalvojan opas</span><span class="sxs-lookup"><span data-stu-id="baca7-129">Administrator Guide</span></span>](hr-admin-overview.md)
- [<span data-ttu-id="baca7-130">Käyttöopas</span><span class="sxs-lookup"><span data-stu-id="baca7-130">User Guide</span></span>](hr-hrpro-overview.md)
