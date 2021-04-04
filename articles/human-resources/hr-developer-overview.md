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
ms.openlocfilehash: 8e390592b000c8f6006aa489fd3823c4f15cb2cb
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467792"
---
# <a name="development-overview"></a><span data-ttu-id="21965-104">Kehityksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="21965-104">Development overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="21965-105">Tämä kehittäjän opas sisältää ohjelmointirajapinta- ja mukautetut kentät -viittaukset.</span><span class="sxs-lookup"><span data-stu-id="21965-105">This Developer Guide provides an API and custom fields reference.</span></span> <span data-ttu-id="21965-106">Se sisältää myös tietoja integroinnista muihin sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="21965-106">It also provides information on integrating with other apps.</span></span>

- [<span data-ttu-id="21965-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="21965-107">Overview</span></span>](hr-developer-overview.md)

- [<span data-ttu-id="21965-108">Laajentaminen Power Appsin ja Power Automaten avulla</span><span class="sxs-lookup"><span data-stu-id="21965-108">Extend with Power Apps and Power Automate</span></span>](hr-developer-power-apps.md)

- [<span data-ttu-id="21965-109">Henkilöstöhallinnon ilmentymät Dataversessä</span><span class="sxs-lookup"><span data-stu-id="21965-109">Human Resources entities in Dataverse</span></span>](hr-developer-entities.md)

- [<span data-ttu-id="21965-110">Mukautetut kentät</span><span class="sxs-lookup"><span data-stu-id="21965-110">Custom fields</span></span>](hr-developer-custom-fields.md)

- <span data-ttu-id="21965-111">Määritä dataintegrointi</span><span class="sxs-lookup"><span data-stu-id="21965-111">Set up data integration</span></span>
  - [<span data-ttu-id="21965-112">Tietojen integrointiteknologian valitseminen</span><span class="sxs-lookup"><span data-stu-id="21965-112">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)
  - [<span data-ttu-id="21965-113">Dataverse -integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="21965-113">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)
  - [<span data-ttu-id="21965-114">Integroinnin määrittäminen Financen kanssa</span><span class="sxs-lookup"><span data-stu-id="21965-114">Configure integration with Finance</span></span>](hr-admin-integration-finance.md)
  - [<span data-ttu-id="21965-115">Integroinnin määrittäminen Dayforcen kanssa</span><span class="sxs-lookup"><span data-stu-id="21965-115">Configure integration with Dayforce</span></span>](hr-admin-integration-dayforce.md)
  - [<span data-ttu-id="21965-116">Toistuvan tietojen viennin sovelluksen luominen</span><span class="sxs-lookup"><span data-stu-id="21965-116">Create a recurring data export app</span></span>](hr-admin-integration-recurring-data-export.md)
  - <span data-ttu-id="21965-117">Office-integraatio</span><span class="sxs-lookup"><span data-stu-id="21965-117">Integrate with Office</span></span>
    - [<span data-ttu-id="21965-118">Office-integraation opasohjelma</span><span class="sxs-lookup"><span data-stu-id="21965-118">Office integration tutorial</span></span>](../dev-itpro/office-integration/office-integration-tutorial.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="21965-119">Yksikkötietojen päivittäminen Excelissä</span><span class="sxs-lookup"><span data-stu-id="21965-119">Update entity data in Excel</span></span>](../dev-itpro/office-integration/use-excel-add-in.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="21965-120">Avaa Excelissä -kokemusten luominen</span><span class="sxs-lookup"><span data-stu-id="21965-120">Create Open in Excel experiences</span></span>](../dev-itpro/office-integration/office-integration-edit-excel.md?toc=/dynamics365/unified-operations/talent/toc.json)
    - [<span data-ttu-id="21965-121">Office-integraation vianmääritys</span><span class="sxs-lookup"><span data-stu-id="21965-121">Troubleshoot Office integration</span></span>](../dev-itpro/office-integration/office-integration-troubleshooting.md?toc=/dynamics365/unified-operations/talent/toc.json)

- <span data-ttu-id="21965-122">Yksikön ohjelmointirajapinnan viite</span><span class="sxs-lookup"><span data-stu-id="21965-122">Entity API reference</span></span>
  - [<span data-ttu-id="21965-123">Todennus</span><span class="sxs-lookup"><span data-stu-id="21965-123">Authentication</span></span>](hr-developer-api-authentication.md)
  - <span data-ttu-id="21965-124">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="21965-124">Entities</span></span>
    - [<span data-ttu-id="21965-125">MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="21965-125">MyLeaveRequests</span></span>](hr-developer-api-myleaverequests-overview.md)
    - [<span data-ttu-id="21965-126">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="21965-126">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)

## <a name="see-also"></a><span data-ttu-id="21965-127">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="21965-127">See also</span></span>

- [<span data-ttu-id="21965-128">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="21965-128">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="21965-129">Järjestelmänvalvojan opas</span><span class="sxs-lookup"><span data-stu-id="21965-129">Administrator Guide</span></span>](hr-admin-overview.md)
- [<span data-ttu-id="21965-130">Käyttöopas</span><span class="sxs-lookup"><span data-stu-id="21965-130">User Guide</span></span>](hr-hrpro-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]