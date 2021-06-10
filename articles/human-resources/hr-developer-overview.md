---
title: Kehityksen yleiskatsaus
description: Tämä kehittäjän opas sisältää ohjelmointirajapinta- ja mukautetut kentät -viittaukset. Se sisältää myös tietoja integroinnista muihin sovelluksiin.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 94652ba35879c043121cc5e74b4230b5a250e4bf
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054040"
---
# <a name="development-overview"></a><span data-ttu-id="19738-104">Kehityksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="19738-104">Development overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="19738-105">Tämä kehittäjän opas sisältää ohjelmointirajapinta- ja mukautetut kentät -viittaukset.</span><span class="sxs-lookup"><span data-stu-id="19738-105">This Developer Guide provides an API and custom fields reference.</span></span> <span data-ttu-id="19738-106">Se sisältää myös tietoja integroinnista muihin sovelluksiin.</span><span class="sxs-lookup"><span data-stu-id="19738-106">It also provides information on integrating with other apps.</span></span>

- [<span data-ttu-id="19738-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="19738-107">Overview</span></span>](hr-developer-overview.md)

- [<span data-ttu-id="19738-108">Laajentaminen Power Appsin ja Power Automaten avulla</span><span class="sxs-lookup"><span data-stu-id="19738-108">Extend with Power Apps and Power Automate</span></span>](hr-developer-power-apps.md)

- [<span data-ttu-id="19738-109">Henkilöstöhallinnon ilmentymät Dataversessä</span><span class="sxs-lookup"><span data-stu-id="19738-109">Human Resources entities in Dataverse</span></span>](hr-developer-entities.md)

- [<span data-ttu-id="19738-110">Mukautetut kentät</span><span class="sxs-lookup"><span data-stu-id="19738-110">Custom fields</span></span>](hr-developer-custom-fields.md)

- <span data-ttu-id="19738-111">Määritä dataintegrointi</span><span class="sxs-lookup"><span data-stu-id="19738-111">Set up data integration</span></span>
  - [<span data-ttu-id="19738-112">Tietojen integrointiteknologian valitseminen</span><span class="sxs-lookup"><span data-stu-id="19738-112">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)
  - [<span data-ttu-id="19738-113">Dataverse -integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="19738-113">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)
  - [<span data-ttu-id="19738-114">Integroinnin määrittäminen Financen kanssa</span><span class="sxs-lookup"><span data-stu-id="19738-114">Configure integration with Finance</span></span>](hr-admin-integration-finance.md)
  - [<span data-ttu-id="19738-115">Integroinnin määrittäminen Dayforcen kanssa</span><span class="sxs-lookup"><span data-stu-id="19738-115">Configure integration with Dayforce</span></span>](hr-admin-integration-dayforce.md)
  - [<span data-ttu-id="19738-116">Toistuvan tietojen viennin sovelluksen luominen</span><span class="sxs-lookup"><span data-stu-id="19738-116">Create a recurring data export app</span></span>](hr-admin-integration-recurring-data-export.md)
  - <span data-ttu-id="19738-117">Office-integraatio</span><span class="sxs-lookup"><span data-stu-id="19738-117">Integrate with Office</span></span>
    - [<span data-ttu-id="19738-118">Office-integraation opasohjelma</span><span class="sxs-lookup"><span data-stu-id="19738-118">Office integration tutorial</span></span>](../fin-ops-core/dev-itpro/office-integration/office-integration-tutorial.md?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)
    - [<span data-ttu-id="19738-119">Yksikkötietojen päivittäminen Excelissä</span><span class="sxs-lookup"><span data-stu-id="19738-119">Update entity data in Excel</span></span>](../fin-ops-core/dev-itpro/office-integration/use-excel-add-in.md?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)
    - [<span data-ttu-id="19738-120">Avaa Excelissä -kokemusten luominen</span><span class="sxs-lookup"><span data-stu-id="19738-120">Create Open in Excel experiences</span></span>](../fin-ops-core/dev-itpro/office-integration/office-integration-edit-excel.md?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)
    - [<span data-ttu-id="19738-121">Office-integraation vianmääritys</span><span class="sxs-lookup"><span data-stu-id="19738-121">Troubleshoot Office integration</span></span>](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json)

- <span data-ttu-id="19738-122">Yksikön ohjelmointirajapinnan viite</span><span class="sxs-lookup"><span data-stu-id="19738-122">Entity API reference</span></span>
  - [<span data-ttu-id="19738-123">Todennus</span><span class="sxs-lookup"><span data-stu-id="19738-123">Authentication</span></span>](hr-developer-api-authentication.md)
  - <span data-ttu-id="19738-124">Yksiköt</span><span class="sxs-lookup"><span data-stu-id="19738-124">Entities</span></span>
    - [<span data-ttu-id="19738-125">MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="19738-125">MyLeaveRequests</span></span>](hr-developer-api-myleaverequests-overview.md)
    - [<span data-ttu-id="19738-126">Lähetä lomapyyntö työnkulkuun</span><span class="sxs-lookup"><span data-stu-id="19738-126">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)

## <a name="see-also"></a><span data-ttu-id="19738-127">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="19738-127">See also</span></span>

- [<span data-ttu-id="19738-128">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="19738-128">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)
- [<span data-ttu-id="19738-129">Järjestelmänvalvojan opas</span><span class="sxs-lookup"><span data-stu-id="19738-129">Administrator Guide</span></span>](hr-admin-overview.md)
- [<span data-ttu-id="19738-130">Käyttöopas</span><span class="sxs-lookup"><span data-stu-id="19738-130">User Guide</span></span>](hr-hrpro-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]