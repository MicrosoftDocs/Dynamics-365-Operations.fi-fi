---
title: Työntekijän itsepalvelutyöntilan nimen muuttaminen
description: Tässä ohjeaiheessa käsitellään työntekijän itsepalvelutyötilan näyttönimen muuttamisesta Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 07/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51adcb2c06044b030ce3b96f0c71129e8c0acd8c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790665"
---
# <a name="change-employee-self-service-workspace-name"></a><span data-ttu-id="8ea7d-103">Työntekijän itsepalvelutyöntilan nimen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="8ea7d-103">Change Employee self service workspace name</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8ea7d-104">Jos organisaatiossa on vapaaehtoisia tai muita ei-työntekijöitä, haluat ehkä muuttaa **Työntekijän itsepalvelu** -työtilan nimen.</span><span class="sxs-lookup"><span data-stu-id="8ea7d-104">If you have volunteers or other non-employees, you might want to change the name of the **Employee self-service** workspace.</span></span> <span data-ttu-id="8ea7d-105">Työtilan nimen voi muuttaa muotoon **Itsepalvelu**.</span><span class="sxs-lookup"><span data-stu-id="8ea7d-105">You can change this workspace to **Self service** instead.</span></span>

> [!NOTE]
> <span data-ttu-id="8ea7d-106">**Työntekijän itsepalvelu** -työtilan nimen muuttaminen muuttaa myös Dynamics 365 Human Resourcesin sisäisesti käyttämän valikkovaihtoehdon nimen.</span><span class="sxs-lookup"><span data-stu-id="8ea7d-106">Changing the name of the **Employee self-service** workspace also changes the menu item that is used internally by Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8ea7d-107">Jos olet aiemmin käyttäjät suojauksen mukautuksia **HcmEmployeeSelfServiceWorkspace**-valikkovaihtoehdossa, samoja muutoksia kannattaa käyttää myös **HcmSelfServiceWorkspace**-valikkovaihtoehdossa pariteetin säilyttämisen vuoksi.</span><span class="sxs-lookup"><span data-stu-id="8ea7d-107">If you previously applied security customizations to the **HcmEmployeeSelfServiceWorkspace** menu item, we recommend applying the same changes to **HcmSelfServiceWorkspace** to maintain parity.</span></span>

1. <span data-ttu-id="8ea7d-108">Valitse Human Resourcesissa ensin **Henkilöstön hallinta**, sitten **Linkit** ja lopuksi **Henkilöstöhallintoparametrit**.</span><span class="sxs-lookup"><span data-stu-id="8ea7d-108">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

2. <span data-ttu-id="8ea7d-109">Valitse **Työntekijän itsepalvelu** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="8ea7d-109">Select the **Employee self-service** tab.</span></span>

3. <span data-ttu-id="8ea7d-110">Valitse **Näyttönimi**-kohdassa **Itsepalvelu**.</span><span class="sxs-lookup"><span data-stu-id="8ea7d-110">Under **Display name**, select **Self service**.</span></span>

   ![Työntekijän itsepalvelutyöntilan nimen muuttaminen itsepalveluksi](./media/hr-employee-self-service-workspace-name.png)

4. <span data-ttu-id="8ea7d-112">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="8ea7d-112">Select **Save**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ea7d-113">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8ea7d-113">Additional resources</span></span>

- [<span data-ttu-id="8ea7d-114">Työntekijän ja esimiehen itsepalvelun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8ea7d-114">Employee and Manager self-service overview</span></span>](hr-employee-manager-self-service-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]