---
title: Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (11. tammikuuta 2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Talent - Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461062"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a><span data-ttu-id="dc04a-103">Dynamics 365 Talent - Core HR:n uudet tai muuttuneet ominaisuudet (11. tammikuuta 2019)</span><span class="sxs-lookup"><span data-stu-id="dc04a-103">What's new or changed in Dynamics 365 Talent - Core HR (January 11, 2019)</span></span>

<span data-ttu-id="dc04a-104">**Koontiversio 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="dc04a-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="dc04a-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="dc04a-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="dc04a-106">Muutokset</span><span class="sxs-lookup"><span data-stu-id="dc04a-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="dc04a-107">Lomapyyntöjen vahvistaminen ennakoimalla käytettävissä oleva saldo</span><span class="sxs-lookup"><span data-stu-id="dc04a-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="dc04a-108">Tähän versioon tehtyjen muutosten ansiosta työntekijät voivat tehdä lomapyynnön ilman, että se vähennetään heidän nykyisestä saldostaan.</span><span class="sxs-lookup"><span data-stu-id="dc04a-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="dc04a-109">Tulevaisuuteen sijoittuvissa pyynnöissä käytetään vakiotyönkulkua.</span><span class="sxs-lookup"><span data-stu-id="dc04a-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="dc04a-110">Lisätietoja on kohdassa [Jaksotettu poissaolo tehtyjen työtuntien mukaan](leave-accrue-hours-worked.md).</span><span class="sxs-lookup"><span data-stu-id="dc04a-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="dc04a-111">Ennakoidun lomasaldon näyttäminen ESS- ja Henkilöt-työtiloissa</span><span class="sxs-lookup"><span data-stu-id="dc04a-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="dc04a-112">Tämän ominaisuuden ansiosta henkilöstöosasto, esimiehet ja työntekijät voivat tarkastella tulevien lomajaksojen saldoja.</span><span class="sxs-lookup"><span data-stu-id="dc04a-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="dc04a-113">Työntekijät voivat tarkastella tulevia saldoja **Työntekijän itsepalvelu** -työtilassa, kun taas henkilöstöosasto saa samat tiedot käyttöönsä **Ihmiset**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="dc04a-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="dc04a-114">Lomasaldojen muutosilmoitukset</span><span class="sxs-lookup"><span data-stu-id="dc04a-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="dc04a-115">Lomasaldot näyttävät työntekijöiden nykyisen saldon.</span><span class="sxs-lookup"><span data-stu-id="dc04a-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="dc04a-116">Tulevat saldot saadaan näkyviin **Työntekijän itsepalvelu**- ja **Henkilöt**-työtiloissa antamalla alkaen-päivämäärä, jonka perusteella ennakoitu saldo lasketaan.</span><span class="sxs-lookup"><span data-stu-id="dc04a-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="dc04a-117">Siirtyminen on lisätty seuraaville alueille ennakoitujen saldojen katsomista varten:</span><span class="sxs-lookup"><span data-stu-id="dc04a-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="dc04a-118">**Poissaoloaika**-kortti **Työntekijän itsepalvelu** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="dc04a-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="dc04a-119">**Loma ja poissaolo** -kortti **Esimiehen itsepalvelu** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="dc04a-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="dc04a-120">**Loma ja poissaolo**-sivu **Henkilöt**-työtilassa.</span><span class="sxs-lookup"><span data-stu-id="dc04a-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="dc04a-121">Desimaalien salliminen muuttuvan kompensaation suunnitelmissa (käteissuunnitelmat)</span><span class="sxs-lookup"><span data-stu-id="dc04a-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="dc04a-122">Muuttuvat käteispalkkiot ja -suunnitelmat on nyt entistä joustavampia sellaisten summien ja ohitusten osalta, joiden arvoissa on desimaaleja.</span><span class="sxs-lookup"><span data-stu-id="dc04a-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="dc04a-123">Muuttuvan kompensaation rekisteröintien päivämääriä ei voi muuttaa suunnitelman tallennuksen jälkeen</span><span class="sxs-lookup"><span data-stu-id="dc04a-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="dc04a-124">Tämän muutoksen ansiosta suunnitelma ja päivämäärä voidaan päivittää (pidennetty tai päätetty) suunnitelman tallennuksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="dc04a-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="dc04a-125">Voit edelleen aktivoida suunnitelmat tai poistaa niiden aktivoinnin aloitus- ja päättymispäivämääristä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="dc04a-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="dc04a-126">Palkanlaskentatietojen käytettävissä määritetyn palkanlaskentakoordinaattorin käyttöoikeusroolin myötä</span><span class="sxs-lookup"><span data-stu-id="dc04a-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="dc04a-127">Palkanlaskentakoordinaattorin rooli on päivitetty antaa palkanlaskentatietojen käyttöoikeus pyyntöprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="dc04a-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="dc04a-128">Työntekijän itsepalvelu | Toimihierarkiaan porautuminen ruudusta ei päädy pääsolmuun</span><span class="sxs-lookup"><span data-stu-id="dc04a-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="dc04a-129">Tehdyillä muutoksilla estetään virhe, joka esiintyi, kun toimihierarkia lisättiin uuteen työtilaan ja organisaatiohierarkiassa siirryttäessä.</span><span class="sxs-lookup"><span data-stu-id="dc04a-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="dc04a-130">Uusi vahvistussanoma henkilöstönumerosarjaa käytettäessä</span><span class="sxs-lookup"><span data-stu-id="dc04a-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="dc04a-131">Tehty muutos selkeyttää, mistä ongelmasta oli kyse, kun palkkasit työntekijän ja käytössä on seuraava henkilöstönumero.</span><span class="sxs-lookup"><span data-stu-id="dc04a-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="dc04a-132">Työntekijän itsepalvelu -työtila valittu alkuperäiseksi aloitussivuksi</span><span class="sxs-lookup"><span data-stu-id="dc04a-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="dc04a-133">Kun **Työntekijän itsepalvelu** -työtila on valittu käyttäjän alkuperäiseksi aloitussivuksi mutta kyseiselle käyttäjälle ei ole määritetty työntekijäroolia, järjestelmää ohjaa käyttäjän oletuskoontinäyttöön.</span><span class="sxs-lookup"><span data-stu-id="dc04a-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="dc04a-134">Työsuhteen päättämisen syykoodi päivittää toimen määritystietueen</span><span class="sxs-lookup"><span data-stu-id="dc04a-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="dc04a-135">Työsuhteen päättämisen syykoodi päivittää nyt toimimäärityksen, kun työntekijän työsuhde päättyy ja toimi lopetetaan.</span><span class="sxs-lookup"><span data-stu-id="dc04a-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
