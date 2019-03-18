---
title: Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (23. tammikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 01/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 135be837a82af8cee22d83c015a78da3b89b7978
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304148"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-23-2019"></a><span data-ttu-id="dbfb0-103">Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (23. tammikuuta 2019)</span><span class="sxs-lookup"><span data-stu-id="dbfb0-103">What's new or changed in Dynamics 365 for Talent Core HR (January 23, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dbfb0-104">**Koontiversio 8.1.2121**</span><span class="sxs-lookup"><span data-stu-id="dbfb0-104">**Build 8.1.2121**</span></span>

<span data-ttu-id="dbfb0-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="dbfb0-106">Muutokset</span><span class="sxs-lookup"><span data-stu-id="dbfb0-106">Changes</span></span>

### <a name="import-of-employee-fixed-compensation-not-working-when-creating-new-fixed-compensation-records"></a><span data-ttu-id="dbfb0-107">Työntekijän kiinteän kompensaation tuonti ei onnistu uusia kiinteän kompensaation tietueita luotaessa</span><span class="sxs-lookup"><span data-stu-id="dbfb0-107">Import of employee fixed compensation not working when creating new fixed compensation records</span></span>
<span data-ttu-id="dbfb0-108">Työntekijän kiinteän kompensaation yksikköön on tehty muutos, jolla kompensaatiotaso voidaan noutaa tuonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-108">A change has been made to the employee fixed compensation entity to retrieve the compensation level upon import.</span></span> <span data-ttu-id="dbfb0-109">Ennen tätä versiota avautuva sanoma ilmoitti, että taso oli pakollinen.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-109">Prior to this release, a message was displayed indicating that the level was required.</span></span>

### <a name="remove-the-minimum-balance-field-from-the-time-off-request-dialog-box"></a><span data-ttu-id="dbfb0-110">Vähimmäissaldon kenttä poistettu poissaolopyynnön valintaikkunasta</span><span class="sxs-lookup"><span data-stu-id="dbfb0-110">Remove the minimum balance field from the time off request dialog box</span></span>
<span data-ttu-id="dbfb0-111">**Vähimmäissaldo**-kenttä on poistettu **Poissaolopyyntö**-valintaikkunasta.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-111">The **Minimum balance** field has been removed from the **Time off request** dialog box.</span></span> <span data-ttu-id="dbfb0-112">Tämä muutos vaikuttaa kaikkiin alueisiin, jossa poissaoloa voidaan pyytää.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-112">This change affects all areas where time off can be requested.</span></span>

### <a name="data-upgrade-for-compensation-levels-not-updating-in-all-scenarios"></a><span data-ttu-id="dbfb0-113">Kompensaatiotasojen tietojen päivitys ei tapahdu kaikissa skenaarioissa</span><span class="sxs-lookup"><span data-stu-id="dbfb0-113">Data upgrade for compensation levels not updating in all scenarios</span></span>
<span data-ttu-id="dbfb0-114">Kiinteiden kompensaatiosuunnitelmien kompensaatiotason päivitykseen on tehty muutos.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-114">A change has been made to update the compensation level on fixed compensation plans.</span></span> <span data-ttu-id="dbfb0-115">Tämä muutos täyttää työntekijälle määritetyn työn kiinteiden suunnitelmien kompensaatiotason.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-115">This change will populate the compensation level on fixed plans for the job assigned to the employee.</span></span>

### <a name="payroll-information-in-the-manage-changes-page-is-only-available-when-logged-in-as-system-administrator"></a><span data-ttu-id="dbfb0-116">Muutostenhallintasivun palkanlaskentatiedot ovat käytettävissä vain järjestelmänvalvoja kirjauduttaessa</span><span class="sxs-lookup"><span data-stu-id="dbfb0-116">Payroll information in the Manage changes page is only available when logged in as System Administrator</span></span>
<span data-ttu-id="dbfb0-117">Tämän muutoksen ansiosta työntekijät, joilla on palkanlaskentakoordinaattorin rooli, voivat käyttää palkanlaskentatietoja toimien **Muutosten aikajana > Muutosten hallinta** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-117">This change allows employees with the Payroll Administrator role access to the payroll information on the **Changes timeline > Manage changes** page for the position.</span></span>

### <a name="job-fields-default-to-positions"></a><span data-ttu-id="dbfb0-118">Työkentät palautuvat toimiin</span><span class="sxs-lookup"><span data-stu-id="dbfb0-118">Job fields default to positions</span></span>
<span data-ttu-id="dbfb0-119">Kun toimen työtä muutetaan, työkentät palautuvat toimeen.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-119">When changing the job on a position, job fields will default to the position.</span></span> <span data-ttu-id="dbfb0-120">Avautuva ilmoitus antaa mahdollisuuden hyväksyä oletusarvot tai säilyttää kyseisten kenttien nykyiset arvot.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-120">An alert message will appear giving an option to accept the default values or keep the existing values for those fields.</span></span>

### <a name="probation-period-and-calendar-are-not-displayed-for-future-hired-employees"></a><span data-ttu-id="dbfb0-121">Koeaikaa ja kalenteria ei näytetä tulevaisuudessa palkatuille työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-121">Probation period and calendar are not displayed for future hired employees.</span></span>
<span data-ttu-id="dbfb0-122">Tällä muutoksella **Koeaika**- ja **Kalenteri**-kentät on lisätty **Muutosten hallinta** -sivulla, mikä mahdollistaa tietojen antamisen tuleville ja entisille työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-122">With this change, **Probation period** and **Calendar** fields have been added to the **Manage changes** page to allow for data entry for future and past employees.</span></span>

### <a name="platform-update-23"></a><span data-ttu-id="dbfb0-123">Ympäristön update 23 -päivitys</span><span class="sxs-lookup"><span data-stu-id="dbfb0-123">Platform update 23</span></span>
<span data-ttu-id="dbfb0-124">Platform update 23 sisältää pieniä ohjelmavirhekorjauksia.</span><span class="sxs-lookup"><span data-stu-id="dbfb0-124">Minor bug fixes have been included as part of Platform update 23.</span></span> <span data-ttu-id="dbfb0-125">Lisätietoja on kohdassa [Dynamics 365 for Finance and Operations platform update 23:n uudet tai muuttuneet ominaisuudet (tammikuu 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span><span class="sxs-lookup"><span data-stu-id="dbfb0-125">For more information, see [What's new or changed in Dynamics 365 for Finance and Operations platform update 23 (January 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-23).</span></span> 