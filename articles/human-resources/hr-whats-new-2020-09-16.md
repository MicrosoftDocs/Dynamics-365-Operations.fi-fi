---
title: Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet (16. syyskuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 16. syyskuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6b07bfb27bbe5e546dac9d72666b3225cc202670
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890696"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="ff916-103">Dynamics 365 Human Resources:n uudet tai muuttuneet ominaisuudet (16. syyskuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="ff916-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ff916-104">Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ff916-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ff916-105">Muutokset koskevat koontiversion numeroa 8.1.3557.</span><span class="sxs-lookup"><span data-stu-id="ff916-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="ff916-106">Joidenkin toimintojen vieressä suluissa olevat luvut viittaavat Lifecycle Services (LCS) -palveluiden tukinumeroihin.</span><span class="sxs-lookup"><span data-stu-id="ff916-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="ff916-107">Tässä julkaisussa mukana olevat ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="ff916-107">Included in this release</span></span>

-  [<span data-ttu-id="ff916-108">Tallennetut näkymät – yleinen saatavuus</span><span class="sxs-lookup"><span data-stu-id="ff916-108">Saved views - general availability</span></span>](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="ff916-109">- Lisätietoja: [Tallennetut näkymät](../fin-ops-core/fin-ops/get-started/saved-views.md).</span><span class="sxs-lookup"><span data-stu-id="ff916-109">- For more information, see [Saved views](../fin-ops-core/fin-ops/get-started/saved-views.md).</span></span> 

- <span data-ttu-id="ff916-110">**Toimen toiminnot** -lomakkeessa on päivitetty dimensioruudukko ja uusi valintaikkuna (469495).</span><span class="sxs-lookup"><span data-stu-id="ff916-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="ff916-111">Jos määrität kohdan **Rajoita työntekijätietojen käyttöoikeuksien** arvoksi kyllä **Jaetut henkilöstöhallinnon parametrit** -kohdan kohdassa **Lisäkäyttöoikeudet**, lomakkeissa näkyvät nyt vain sopivat työntekijät (393384).</span><span class="sxs-lookup"><span data-stu-id="ff916-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="ff916-112">Uuden kalenterin luontivaihtoehdot **WorkCalendar**-yksikössä (477055):</span><span class="sxs-lookup"><span data-stu-id="ff916-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="ff916-113">- Oletusarvoinen päättymisaika</span><span class="sxs-lookup"><span data-stu-id="ff916-113">- Default ending time</span></span><br><span data-ttu-id="ff916-114">-    Oletusarvoinen alkamisaika</span><span class="sxs-lookup"><span data-stu-id="ff916-114">-    Default starting time</span></span><br><span data-ttu-id="ff916-115">-  Perjantai työpäivä?</span><span class="sxs-lookup"><span data-stu-id="ff916-115">-  Is Friday working day</span></span><br><span data-ttu-id="ff916-116">-  Maanantai työpäivä?</span><span class="sxs-lookup"><span data-stu-id="ff916-116">-  Is Monday working day</span></span><br><span data-ttu-id="ff916-117">-  Lauantai työpäivä?</span><span class="sxs-lookup"><span data-stu-id="ff916-117">-  Is Saturday working day</span></span><br><span data-ttu-id="ff916-118">-  Sunnuntai työpäivä?</span><span class="sxs-lookup"><span data-stu-id="ff916-118">- Is Sunday working day</span></span><br><span data-ttu-id="ff916-119">-  Torstai työpäivä?</span><span class="sxs-lookup"><span data-stu-id="ff916-119">- Is Thursday working day</span></span><br><span data-ttu-id="ff916-120">-  Tiistai työpäivä?</span><span class="sxs-lookup"><span data-stu-id="ff916-120">- Is Tuesday working day</span></span><br><span data-ttu-id="ff916-121">-  Keskiviikko työpäivä?</span><span class="sxs-lookup"><span data-stu-id="ff916-121">- Is Wednesday working day</span></span><br><span data-ttu-id="ff916-122">- Työkalenterin lomatunnus</span><span class="sxs-lookup"><span data-stu-id="ff916-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="ff916-123">**LeaveBankTransactionV1**-yksikkö sisältää nyt syykoodin (477823).</span><span class="sxs-lookup"><span data-stu-id="ff916-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="ff916-124">Voit nyt tallentaa tehtävätallenteita (492923).</span><span class="sxs-lookup"><span data-stu-id="ff916-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="ff916-125">Tietoja julkaistaan nyt onnistuneesti yksiköstä **HCMWorkerContactEntity** (427620).</span><span class="sxs-lookup"><span data-stu-id="ff916-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="ff916-126">**Kompensaatio**-pikavälilehti näkyy nyt alihankkijan työntekijätyypin osalta **Työntekijätoiminnot**-lomakkeessa (482494).</span><span class="sxs-lookup"><span data-stu-id="ff916-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="ff916-127">**Taso**- ja **Suunnitelma**-kentät ovat nyt pakollisia, kun määritetään **Kiinteä kompensaatio**.</span><span class="sxs-lookup"><span data-stu-id="ff916-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="ff916-128">Jos jätät nämä kentät tyhjiksi, näkyviin tulee virhesanoma (482497).</span><span class="sxs-lookup"><span data-stu-id="ff916-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="ff916-129">**Etuudet**-kohdan **Suunnitelma**-kenttä on nyt avattava luettelo (488768).</span><span class="sxs-lookup"><span data-stu-id="ff916-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="ff916-130">Järjestelmänvalvojat saavat nyt ilmoituksen, jos mukautettu kenttä poistetaan henkilöstöresursseista (481408).</span><span class="sxs-lookup"><span data-stu-id="ff916-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="ff916-131">Työntekijän työsuhteen päättymisen yhteydessä henkilöstöhallinto toimii odotetusti eikä muuta valittua yritystä lukitsemisen jälkeen (479877).</span><span class="sxs-lookup"><span data-stu-id="ff916-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="ff916-132">Esimiehet eivät voi enää lisätä numerosaraketta mukautuksen kautta (485317).</span><span class="sxs-lookup"><span data-stu-id="ff916-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="ff916-133">Esimiehet eivät voi enää poistaa tietoalueen suodatinta vanhentuvista tunnusnumeroista (485321).</span><span class="sxs-lookup"><span data-stu-id="ff916-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="ff916-134">Kun **Raportoi toimelle** -kenttä on tyhjä, aseman tiedot näkyvät edelleen, kun hiiren osoitin on aseman päällä (433328).</span><span class="sxs-lookup"><span data-stu-id="ff916-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="ff916-135">Työntekijät voivat nyt tarkastella etuussuunnitelmien tietoja työntekijän itsepalvelussa (481676).</span><span class="sxs-lookup"><span data-stu-id="ff916-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="ff916-136">Työntekijät voivat nyt nähdä kaikki rekisteröidyt kurssit (429048).</span><span class="sxs-lookup"><span data-stu-id="ff916-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="ff916-137">Voit nyt rajoittaa **Ammattisertifikaatit**-sivun tarkastelumahdollisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ff916-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="ff916-138">Voit rajoittaa tarkasteluoikeudet nykyiseen yritykseen, työntekijän tilan perusteella sekä työntekijän tyypin perusteella (451501).</span><span class="sxs-lookup"><span data-stu-id="ff916-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="ff916-139">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="ff916-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="ff916-140">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="ff916-140">Human Resources app in Teams</span></span>

<span data-ttu-id="ff916-141">Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä.</span><span class="sxs-lookup"><span data-stu-id="ff916-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="ff916-142">Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="ff916-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="ff916-143">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="ff916-143">For more information, see:</span></span>

- <span data-ttu-id="ff916-144">[Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 1 -suunnitelmassa</span><span class="sxs-lookup"><span data-stu-id="ff916-144">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="ff916-145">[Teamsin Human Resources -sovellus](./hr-admin-teams-leave-app.md) Human Resources -sovelluksen dokumentaatiossa</span><span class="sxs-lookup"><span data-stu-id="ff916-145">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="ff916-146">Human Resources -sovellus Teamsin esiversiotoiminnoissa</span><span class="sxs-lookup"><span data-stu-id="ff916-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="ff916-147">**Ilmoitukset**: Poissaolopyyntöjen lähettäjät ja hyväksyjät saavat ilmoitukset Teamsin Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ff916-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="ff916-148">Hyväksyjät voivat hyväksyä tai hylätä poissaolopyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="ff916-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="ff916-149">Lähettäjille ilmoitetaan, jos pyyntö on hyväksytty tai hylätty.</span><span class="sxs-lookup"><span data-stu-id="ff916-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="ff916-150">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="ff916-150">For more information, see:</span></span>
   - <span data-ttu-id="ff916-151">[Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 2 -suunnitelmassa</span><span class="sxs-lookup"><span data-stu-id="ff916-151">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="ff916-152">[Teamsin Human Resources -sovelluksen ilmoitusten käyttöönotto](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) Human Resources -sovelluksen dokumentaatiossa</span><span class="sxs-lookup"><span data-stu-id="ff916-152">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="ff916-153">[Teams-ilmoitusten käyttöönotto tai käytöstäpoisto yksittäisille käyttäjille](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) Human Resources -sovelluksen dokumentaatiossa</span><span class="sxs-lookup"><span data-stu-id="ff916-153">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="ff916-154">[Teams-ilmoitukset](./hr-teams-leave-app.md#respond-to-teams-notifications) Human Resources -sovelluksen dokumentaatiossa</span><span class="sxs-lookup"><span data-stu-id="ff916-154">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="ff916-155">[Ryhmän lomakalenterin tarkasteleminen](./hr-teams-leave-app.md#view-your-teams-leave-calendar) Human Resources -sovelluksen dokumentaatiossa</span><span class="sxs-lookup"><span data-stu-id="ff916-155">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="ff916-156">**Esimiehen poissaolokalenteri**: Esimiehet voivat nähdä suorien alaisten hyväksytyt ja odottavat poissaolot kalenterinäkymässä.</span><span class="sxs-lookup"><span data-stu-id="ff916-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="ff916-157">Tämän näkymän avulla on helppo hahmottaa, milloin ryhmä jäsenet ovat poissa töistä.</span><span class="sxs-lookup"><span data-stu-id="ff916-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="ff916-158">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="ff916-158">For more information, see:</span></span>
   - <span data-ttu-id="ff916-159">[Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 2 -suunnitelmassa</span><span class="sxs-lookup"><span data-stu-id="ff916-159">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="ff916-160">[Ryhmän lomakalenterin tarkasteleminen](./hr-teams-leave-app.md#view-your-teams-leave-calendar) Human Resources -sovelluksen dokumentaatiossa</span><span class="sxs-lookup"><span data-stu-id="ff916-160">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="ff916-161">Toimen Itselle määritetyt työnimikkeet -luettelon määritysasetus (477004)</span><span class="sxs-lookup"><span data-stu-id="ff916-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="ff916-162">Uusi asetus on nyt käytettävissä toimelle **Itselle määritetyt työnimikkeet** -luettelossa koontinäytön oikeanpuoleisessa sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="ff916-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="ff916-163">Tämän muutoksen myötä kaikki työnimikkeet ja tehtäväluettelot näkyvät samalla alueella.</span><span class="sxs-lookup"><span data-stu-id="ff916-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="ff916-164">Jos haluat tämän toiminnon käyttöön, ota käyttöön **Esikatselu - työnkulun käyttökokemuksen parannukset** -kohta ominaisuuksien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="ff916-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="ff916-165">Lisätietoja esikatseluominaisuuksien ottamisesta käyttöön on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="ff916-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="ff916-166">Tämä toiminto edistää myös henkilöstön toimintojen lomakkeissa olevia työnkulkuasetuksia.</span><span class="sxs-lookup"><span data-stu-id="ff916-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="ff916-167">Työnkulunasetukset näkyvät myös toiminnon nopean käytön pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ff916-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="ff916-168">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="ff916-168">For more information, see:</span></span> 

- <span data-ttu-id="ff916-169">[Organisaation ja henkilöstön hallinnan työnkulun käyttökokemuksen parannukset](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) Dynamics 365:n vuoden 2020 julkaisuaallon 2 suunnitelmassa</span><span class="sxs-lookup"><span data-stu-id="ff916-169">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Minulle määritetyt työnimikkeet](./media/hr-workflow-work-items-assigned-to-me.png)

![Työnkulkunimikkeiden nopea käyttö](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="ff916-172">Loma- ja poissaolokalenteri</span><span class="sxs-lookup"><span data-stu-id="ff916-172">Leave and absence calendar</span></span>

<span data-ttu-id="ff916-173">Tämä julkaisu sisältää lisää kalenterivaihtoehtoja loma- ja poissaolokalentereja varten.</span><span class="sxs-lookup"><span data-stu-id="ff916-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="ff916-174">Lisätietoja on kohdassa [Ryhmä- ja yrityskalenterien tarkasteleminen](./hr-employee-self-service-calendar.md).</span><span class="sxs-lookup"><span data-stu-id="ff916-174">For more information, see [View team and company calendars](./hr-employee-self-service-calendar.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="ff916-175">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="ff916-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="ff916-176">Dataverseen sisältyvät tarkistusluettelokohdat</span><span class="sxs-lookup"><span data-stu-id="ff916-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="ff916-177">Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="ff916-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="ff916-178">Etujen hallinnan syykoodit</span><span class="sxs-lookup"><span data-stu-id="ff916-178">Benefits management reason codes</span></span>

<span data-ttu-id="ff916-179">Etujen hallinnan syykoodit yhdistetään pian olemassa oleviin syykoodeihin Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ff916-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="ff916-180">Jos olet määrittänyt etujen hallinnassa syykoodeja, joiden pituus on yli 15 merkkiä, syykoodin nimeä on muutettava etujen hallinnan **Syykoodit**-lomakkeessa niin, että pituus on enintään 15 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="ff916-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="ff916-181">Kun olet päivittänyt nimen, syykoodi näkyy olemassa olevan syykoodilomakkeen henkilöstön hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="ff916-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="ff916-182">Tämä muutos on käytettävissä tulevaisuudessa. Se ei vaikuta olemassa oleviin toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="ff916-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="ff916-183">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="ff916-183">See also</span></span>

[<span data-ttu-id="ff916-184">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="ff916-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="ff916-185">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="ff916-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="ff916-186">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="ff916-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="ff916-187">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="ff916-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
