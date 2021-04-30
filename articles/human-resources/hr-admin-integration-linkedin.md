---
title: LinkedIn Talent Hub -integrointi
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin ja LinkedIn Talent Hubin integroinnin määrittämistä.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 208998b5c09416407612352da7a8ef5dd9491914
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889977"
---
# <a name="integrate-with-linkedin-talent-hub"></a><span data-ttu-id="8c030-103">LinkedIn Talent Hub -integrointi</span><span class="sxs-lookup"><span data-stu-id="8c030-103">Integrate with LinkedIn Talent Hub</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](includes/preview-feature.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8c030-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) on ATS (hakijoiden seurantajärjestelmä) -ympäristö.</span><span class="sxs-lookup"><span data-stu-id="8c030-104">[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) is an applicant tracking system (ATS) platform.</span></span> <span data-ttu-id="8c030-105">Sen avulla voit hakea, hallita ja palkata työntekijöitä samassa paikassa.</span><span class="sxs-lookup"><span data-stu-id="8c030-105">It lets you source, manage, and hire employees all in one place.</span></span> <span data-ttu-id="8c030-106">Kun Microsoft Dynamics 365 Human Resources integroidaan LinkedIn Talent Hubiin, Human Resourcesissa on helppo luoda työntekijätietueita toimeen palkatuille hakijoille.</span><span class="sxs-lookup"><span data-stu-id="8c030-106">By integrating Microsoft Dynamics 365 Human Resources with LinkedIn Talent Hub, you can easily create employee records in Human Resources for applicants who have been hired for a position.</span></span>

## <a name="setup"></a><span data-ttu-id="8c030-107">Luo perustiedot</span><span class="sxs-lookup"><span data-stu-id="8c030-107">Setup</span></span>

<span data-ttu-id="8c030-108">Järjestelmänvalvojan on tehtävä määritykset, joita tarvitaan LinkedIn Talent Hub -integrointia varten.</span><span class="sxs-lookup"><span data-stu-id="8c030-108">A system administrator must complete setup tasks to enable integration with LinkedIn Talent Hub.</span></span> <span data-ttu-id="8c030-109">Power Apps -ympäristössä on määritettävä ensin käyttäjä ja käyttöoikeusrooli, jolla LinkedIn Talent Hubille myönnetään tietojen kirjoitusoikeudet Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="8c030-109">First, in the Power Apps environment, you must set up a user and security role to grant LinkedIn Talent Hub the appropriate permissions to write data into Human Resources.</span></span>

### <a name="link-your-environment-to-linkedin-talent-hub"></a><span data-ttu-id="8c030-110">Ympäristön linkittäminen LinkedIn Talent Hubiin</span><span class="sxs-lookup"><span data-stu-id="8c030-110">Link your environment to LinkedIn Talent Hub</span></span>

1. <span data-ttu-id="8c030-111">Avaa [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span><span class="sxs-lookup"><span data-stu-id="8c030-111">Open [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).</span></span>

2. <span data-ttu-id="8c030-112">Valitse käyttäjän avattavassa valikossa **Tuotteen asetukset**.</span><span class="sxs-lookup"><span data-stu-id="8c030-112">On the user drop-down menu, select **Product Settings**.</span></span>

3. <span data-ttu-id="8c030-113">Valitse vasemman siirtymisruudun **Lisäasetukset**-osassa **Integroinnit**.</span><span class="sxs-lookup"><span data-stu-id="8c030-113">In the left navigation pane, in the **Advanced** section, select **Integrations**.</span></span>

4. <span data-ttu-id="8c030-114">Valitse Microsoft Dynamics 365 Human Resources -integroinnin osalta **Valtuuta**.</span><span class="sxs-lookup"><span data-stu-id="8c030-114">Select **Authorize** for the Microsoft Dynamics 365 Human Resources integration.</span></span>

5. <span data-ttu-id="8c030-115">Valitse **Dynamics 365 Human Resources** -sivulla ympäristö, johon LinkedIn Talent Hub linkitetään, ja valitse sitten **Linkitä**.</span><span class="sxs-lookup"><span data-stu-id="8c030-115">On the **Dynamics 365 Human Resources** page, select the environment to link LinkedIn Talent Hub to, and then select **Link**.</span></span>

    ![LinkedIn Talent Hubin käyttöönotto](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > <span data-ttu-id="8c030-117">Linkityksen voi tehdä vain sellaisiin ympäristöihin, joissa linkittäjän käyttäjätilillä on järjestelmänvalvojan oikeudet sekä Human Resources -ympäristössä että liitetyissä Power Apps -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="8c030-117">You can link only to environments where your user account has administrator access to both the Human Resources environment and the associated Power Apps environment.</span></span> <span data-ttu-id="8c030-118">Jos Human Resourcesin linkkisivulla ei ole yhtään ympäristöä, varmista, että vuokraajan Human Resources -ympäristöillä on käyttöoikeus ja että linkkisivulle kirjautumiseen käytetyllä käyttäjällään sekä Human Resources- että Power Apps -ympäristön järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="8c030-118">If no environments are listed on the Human Resources link page, make sure that you have licensed Human Resources environments on the tenant, and that the user that you signed in to the link page as has administrator permissions to both the Human Resources environment and the Power Apps environment.</span></span>

### <a name="create-a-power-apps-security-role"></a><span data-ttu-id="8c030-119">Power Apps -käyttöoikeusroolin luominen</span><span class="sxs-lookup"><span data-stu-id="8c030-119">Create a Power Apps security role</span></span>

1. <span data-ttu-id="8c030-120">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="8c030-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="8c030-121">Valitse **Ympäristöt**-luettelossa ympäristö, joka on liitetty siihen Human Resources -ympäristöön, johon haluat linkittää LinkedIn Talent Hub -esiintymän.</span><span class="sxs-lookup"><span data-stu-id="8c030-121">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="8c030-122">Valitse **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="8c030-122">Select **Settings**.</span></span>

4. <span data-ttu-id="8c030-123">Laajenna **Käyttäjät ja käyttöoikeudet** -solmu ja valitse **Käyttöoikeusroolit**.</span><span class="sxs-lookup"><span data-stu-id="8c030-123">Expand the **Users + Permissions** node, and select **Security Roles**.</span></span>

5. <span data-ttu-id="8c030-124">Valitse **Käyttöoikeusroolit**-sivun työkalurivillä **Uusi rooli**.</span><span class="sxs-lookup"><span data-stu-id="8c030-124">On the **Security Roles** page, on the toolbar, select **New role**.</span></span>

6. <span data-ttu-id="8c030-125">Anna roolille nimi **Tiedot**-välilehdessä. Se voi olla vaikkapa **LinkedIn Talent Hub HRIS integraatio**.</span><span class="sxs-lookup"><span data-stu-id="8c030-125">On the **Details** tab, enter a name for the role, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>

7. <span data-ttu-id="8c030-126">Valitsee **Mukauttaminen**-välilehdessä organisaatiotason **Luku**-oikeudet seuraaville entiteeteille:</span><span class="sxs-lookup"><span data-stu-id="8c030-126">On the **Customization** tab, select organization-level **Read** permission for the following entities:</span></span>

    - <span data-ttu-id="8c030-127">Kokonaisuus</span><span class="sxs-lookup"><span data-stu-id="8c030-127">Entity</span></span>
    - <span data-ttu-id="8c030-128">Kenttä</span><span class="sxs-lookup"><span data-stu-id="8c030-128">Field</span></span>
    - <span data-ttu-id="8c030-129">Suhde</span><span class="sxs-lookup"><span data-stu-id="8c030-129">Relationship</span></span>

8. <span data-ttu-id="8c030-130">Tallenna ja sulje käyttöoikeusrooli.</span><span class="sxs-lookup"><span data-stu-id="8c030-130">Save and close the security role.</span></span>

### <a name="create-a-power-apps-application-user"></a><span data-ttu-id="8c030-131">Power Apps -sovelluskäyttäjän luominen</span><span class="sxs-lookup"><span data-stu-id="8c030-131">Create a Power Apps application user</span></span>

<span data-ttu-id="8c030-132">LinkedIn Talent Hub -sovittimeen on luotava sovelluskäyttäjä, jotta sovittimelle voidaan myöntää oikeudet hakijatietueiden kirjoittamiseen Power Apps -ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="8c030-132">An application user must be created for the LinkedIn Talent Hub adapter to grant permissions to the adapter to write candidate records into the Power Apps environment.</span></span>

1. <span data-ttu-id="8c030-133">Avaa [Power Platform -hallintakeskus](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="8c030-133">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com).</span></span>

2. <span data-ttu-id="8c030-134">Valitse **Ympäristöt**-luettelossa ympäristö, joka on liitetty siihen Human Resources -ympäristöön, johon haluat linkittää LinkedIn Talent Hub -esiintymän.</span><span class="sxs-lookup"><span data-stu-id="8c030-134">In the **Environments** list, select the environment that is associated with the Human Resources environment that you want to link your instance of LinkedIn Talent Hub to.</span></span>

3. <span data-ttu-id="8c030-135">Valitse **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="8c030-135">Select **Settings**.</span></span>

4. <span data-ttu-id="8c030-136">Laajenna **Käyttäjät ja käyttöoikeudet** -solmu ja valitse **Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="8c030-136">Expand the **Users + Permissions** node, and select **Users**.</span></span>

5. <span data-ttu-id="8c030-137">Valitse **Käyttäjien hallinta Dynamics 365:ssä**.</span><span class="sxs-lookup"><span data-stu-id="8c030-137">Select **Manage users in Dynamics 365**.</span></span>

6. <span data-ttu-id="8c030-138">Voit vaihtaa luettelon yläpuolella olevassa avattavassa valikossa **Aktivoidut käyttäjät** -oletusnäkymän **Sovelluskäyttäjät**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="8c030-138">Use the drop-down menu above the list to change the view from the default **Enabled Users** view to **Application Users**.</span></span>

    ![Sovelluskäyttäjät-näkymä](./media/hr-admin-integration-power-apps-application-users.jpg)

7. <span data-ttu-id="8c030-140">Valitse työkalurivillä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="8c030-140">On the toolbar, select **New**.</span></span>

8. <span data-ttu-id="8c030-141">Toimi seuraavasti **Uusi käyttäjä** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="8c030-141">On the **New user** page, follow these steps:</span></span>

    1. <span data-ttu-id="8c030-142">Vaihda **Käyttäjätyyppi**-kentän arvoksi **Sovelluskäyttäjä**.</span><span class="sxs-lookup"><span data-stu-id="8c030-142">Change the value of the **User type** field to **Application User**.</span></span>
    2. <span data-ttu-id="8c030-143">Määritä **Käyttäjänimi**-kentän arvoksi **Dynamics365 HR LinkedIn HRIS -integraatio**.</span><span class="sxs-lookup"><span data-stu-id="8c030-143">Set the **User Name** field to **Dynamics365 HR LinkedIn HRIS Integration**.</span></span>
    3. <span data-ttu-id="8c030-144">Määritä **Sovellustunnus**-kentän arvoksi **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="8c030-144">Set the **Application ID** field to **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    4. <span data-ttu-id="8c030-145">Anna **Etunimi**-, **Sukunimi**- ja **Ensisijainen sähköposti** -kenttiin jokin arvo.</span><span class="sxs-lookup"><span data-stu-id="8c030-145">Enter any value in the **First Name**, **Last Name**, and **Primary Email** fields.</span></span>
    5. <span data-ttu-id="8c030-146">Valitse työkalurivillä **Tallenna \& sulje**.</span><span class="sxs-lookup"><span data-stu-id="8c030-146">On the toolbar, select **Save \& Close**.</span></span>

### <a name="assign-a-security-role-to-the-new-user"></a><span data-ttu-id="8c030-147">Käyttöoikeusroolin määrittäminen uudelle käyttäjälle</span><span class="sxs-lookup"><span data-stu-id="8c030-147">Assign a security role to the new user</span></span>

<span data-ttu-id="8c030-148">Kun uusi sovelluskäyttäjä on tallennettu ja suljettu edellisessä osassa, olet takaisin **Käyttäjäluettelo**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8c030-148">After you save and close the new application user in the previous section, you're returned to the **Users list** page.</span></span>

1. <span data-ttu-id="8c030-149">Vaihda **Käyttäjäluettelo**-sivulla **Sovelluskäyttäjät**-näkymään.</span><span class="sxs-lookup"><span data-stu-id="8c030-149">On the **Users list** page, change the view to **Application Users**.</span></span>

2. <span data-ttu-id="8c030-150">Valitse edellisessä osassa luotu sovelluskäyttäjä.</span><span class="sxs-lookup"><span data-stu-id="8c030-150">Select the application user that you created in the previous section.</span></span>

3. <span data-ttu-id="8c030-151">Valitse työkalurivillä **Roolien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="8c030-151">On the toolbar, select **Manage Roles**.</span></span>

4. <span data-ttu-id="8c030-152">Valitse aiemmin integraatiota varten luotu käyttöoikeusrooli.</span><span class="sxs-lookup"><span data-stu-id="8c030-152">Select the security role that you created earlier for the integration.</span></span>

5. <span data-ttu-id="8c030-153">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c030-153">Select **OK**.</span></span>

### <a name="add-an-azure-active-directory-app-in-human-resources"></a><span data-ttu-id="8c030-154">Azure Active Directory -sovelluksen lisääminen Human Resourcesiin</span><span class="sxs-lookup"><span data-stu-id="8c030-154">Add an Azure Active Directory app in Human Resources</span></span>

1. <span data-ttu-id="8c030-155">Avaa Dynamics 365 Human Resourcesissa **Azure Active Directory -sovellukset** -sivu.</span><span class="sxs-lookup"><span data-stu-id="8c030-155">In Dynamics 365 Human Resources, open the **Azure Active Directory applications** page.</span></span>
2. <span data-ttu-id="8c030-156">Lisää uusi tietue luetteloon ja määritä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="8c030-156">Add a new record to the list, and set the following fields:</span></span>

    - <span data-ttu-id="8c030-157">**Asiakastunnus**: anna **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span><span class="sxs-lookup"><span data-stu-id="8c030-157">**Client ID**: Enter **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.</span></span>
    - <span data-ttu-id="8c030-158">**Nimi**: anna aiemmin luodun Power Appsin käyttöoikeusroolin nimi, kuten **LinkedIn Talent Hub HRIS integraatio**.</span><span class="sxs-lookup"><span data-stu-id="8c030-158">**Name**: Enter the name of the Power Apps security role that you created earlier, such as **LinkedIn Talent Hub HRIS Integration**.</span></span>
    - <span data-ttu-id="8c030-159">**Käyttäjätunnus**: valitse käyttäjä, jolla on tietojen kirjoitusoikeudet henkilöstöhallinnossa.</span><span class="sxs-lookup"><span data-stu-id="8c030-159">**User ID**: Select a user who has permissions to write data in Personnel Management.</span></span>

### <a name="create-the-table-in-dataverse"></a><span data-ttu-id="8c030-160">Taulun luominen Dataversessa</span><span class="sxs-lookup"><span data-stu-id="8c030-160">Create the table in Dataverse</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c030-161">LinkedIn Talent Hub -integraatio määräytyy Human Resourcesille Dataverse-virtuaalitaulukoiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="8c030-161">The integration with LinkedIn Talent Hub depends on virtual tables in Dataverse for Human Resources.</span></span> <span data-ttu-id="8c030-162">Määritysten tätä vaihetta varten on määritettävä virtuaalitaulukoita.</span><span class="sxs-lookup"><span data-stu-id="8c030-162">As a prerequisite for this step in the setup, you must configure virtual tables.</span></span> <span data-ttu-id="8c030-163">Lisätietoja virtuaalitaulukoiden määrittämisestä on kohdassa [Dataversen virtuaalitaulukoiden määrittäminen](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="8c030-163">For information about how to configure virtual tables, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

1. <span data-ttu-id="8c030-164">Avaa Human Resourcesissa **Dataverse-integraatio** -sivu.</span><span class="sxs-lookup"><span data-stu-id="8c030-164">In Human Resources, open the **Dataverse integration** page.</span></span>

2. <span data-ttu-id="8c030-165">Valitse **Virtuaalitaulukot**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8c030-165">Select the **Virtual tables** tab.</span></span>

3. <span data-ttu-id="8c030-166">Etsi **LinkedInin viety ehdokas** suodattamalla yksikköluetteloa yksikön otsikon perusteella.</span><span class="sxs-lookup"><span data-stu-id="8c030-166">Filter the entity list by entity label to find **LinkedIn exported candidate**.</span></span>

4. <span data-ttu-id="8c030-167">Valitse ensin yksikkö ja sitten **Luo/päivitä**.</span><span class="sxs-lookup"><span data-stu-id="8c030-167">Select the entity, and then select **Generate/refresh**.</span></span>

## <a name="exporting-candidate-records"></a><span data-ttu-id="8c030-168">Hakijatietojen vieminen</span><span class="sxs-lookup"><span data-stu-id="8c030-168">Exporting candidate records</span></span>

<span data-ttu-id="8c030-169">Kun määritykset on tehty, työhönottaja ja henkilöstöhallinnon (HR) ammattilaiset voivat viedä palkattujen hakijoiden tietueet LinkedIn Talent Hubista Human Resourcesiin LinkedIn Talent Hubin **Vie HRIS-järjestelmään** -toiminnolla.</span><span class="sxs-lookup"><span data-stu-id="8c030-169">After the setup is completed, recruiters and human resources (HR) professionals can use the **Export to HRIS** function in LinkedIn Talent Hub to export hired candidate records from LinkedIn Talent Hub to Human Resources.</span></span>

### <a name="export-records-from-linkedin-talent-hub"></a><span data-ttu-id="8c030-170">Tietojen vieminen LinkedIn Talent Hubista</span><span class="sxs-lookup"><span data-stu-id="8c030-170">Export records from LinkedIn Talent Hub</span></span>

<span data-ttu-id="8c030-171">Kun hakija on siirtynyt työhönottoprosessin läpi ja hänet on palkattu, hakijan tietue voidaan viedä LinkedIn Talent Hubista Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="8c030-171">After a candidate has moved through the recruiting process and has been hired, you can export the candidate record from LinkedIn Talent Hub to Human Resources.</span></span>

1. <span data-ttu-id="8c030-172">Avaa LinkedIn Talent Hubissa projekti, johon uusi työntekijä on palkattu.</span><span class="sxs-lookup"><span data-stu-id="8c030-172">In LinkedIn Talent Hub, open the project that you hired the new employee for.</span></span>

2. <span data-ttu-id="8c030-173">Valitse hakijatietue.</span><span class="sxs-lookup"><span data-stu-id="8c030-173">Select a candidate record.</span></span>

3. <span data-ttu-id="8c030-174">Valitse **Muuta tilaa** ja valitse sitten **Otettu työhön**.</span><span class="sxs-lookup"><span data-stu-id="8c030-174">Select **Change stage**, and then select **Hired**.</span></span>

4. <span data-ttu-id="8c030-175">Valitse hakijan kolmen pisteen valikossa (**...**) **Vie HRIS-järjestelmään**.</span><span class="sxs-lookup"><span data-stu-id="8c030-175">On the ellipsis menu (**...**) for the candidate, select **Export to HRIS**.</span></span>

5. <span data-ttu-id="8c030-176">Anna **Vie HRIS-järjestelmään** -ruudussa tiedot, jotka on vietävä:</span><span class="sxs-lookup"><span data-stu-id="8c030-176">In the **Export to HRIS** pane, enter the information that must be exported:</span></span>

    - <span data-ttu-id="8c030-177">Valitse **HRIS-palvelu**-kentässä **Microsoft Dynamics 365 Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="8c030-177">In the **HRIS provider** field, select **Microsoft Dynamics 365 Human Resources**.</span></span>
    - <span data-ttu-id="8c030-178">Valitse **Alkamispäivä**-kentässä arvo uudelle työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="8c030-178">In the **Start date** field, select a value for the new employee.</span></span>
    - <span data-ttu-id="8c030-179">Anna **Työnimike**-kentässä uuden työntekijän toimen työnimike.</span><span class="sxs-lookup"><span data-stu-id="8c030-179">In the **Job title** field, enter a job title for the new employee's job.</span></span>
    - <span data-ttu-id="8c030-180">Anna **Sijainti**-kentässä sijainti, joka on työntekijän ensisijainen työpaikka.</span><span class="sxs-lookup"><span data-stu-id="8c030-180">In the **Location** field, enter the location where the employee will be based.</span></span>
    - <span data-ttu-id="8c030-181">Anna tai tarkista työntekijän sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="8c030-181">Enter or verify the employee's email address.</span></span>

![Vie HRIS-järjestelmään -ruutu LinkedIn Talent Hubissa](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a><span data-ttu-id="8c030-183">Käyttöönoton päättäminen Human Resourcesissa</span><span class="sxs-lookup"><span data-stu-id="8c030-183">Complete onboarding in Human Resources</span></span>

<span data-ttu-id="8c030-184">LinkedIn Talent Hubista Human Resourcesiin vietävät hakijatietueet näkyvät **Henkilöstöhallinto**-sivun **Työhönotettavat hakijat** -osassa.</span><span class="sxs-lookup"><span data-stu-id="8c030-184">Candidate records that are exported from LinkedIn Talent Hub to Human Resources appear in the **Candidates to hire** section of the **Personnel management** page.</span></span>

1. <span data-ttu-id="8c030-185">Avaa Human Resourcesissa **Henkilöstöhallinto**-sivu.</span><span class="sxs-lookup"><span data-stu-id="8c030-185">In Human Resources, open the **Personnel management** page.</span></span>

2. <span data-ttu-id="8c030-186">Valitse **Työhön otettavat hakijat** -osassa **Työhönotto** valitun hakijan kohdalla.</span><span class="sxs-lookup"><span data-stu-id="8c030-186">In the **Candidates to hire** section, select **Hire** for the selected candidate.</span></span>

3. <span data-ttu-id="8c030-187">Tarkista tietue **Ota palvelukseen uusi työntekijä** -valintaikkunassa ja lisää mahdolliset pakolliset tiedot.</span><span class="sxs-lookup"><span data-stu-id="8c030-187">In the **Hire new worker** dialog box, review the record, and add any required information.</span></span> <span data-ttu-id="8c030-188">Voit myös valita sen toimen numeron, jota varten hakija on otettu töihin.</span><span class="sxs-lookup"><span data-stu-id="8c030-188">You can also select the position number that the candidate has been hired for.</span></span>

<span data-ttu-id="8c030-189">Kun pakolliset tiedot on annettu, voit jatkaa työntekijätietueiden luonnin ja työntekijöiden perehdyttämisen vakioprosesseja.</span><span class="sxs-lookup"><span data-stu-id="8c030-189">After the required information has been entered, you can continue with your standard processes for creating employee records and onboarding employees.</span></span>

<span data-ttu-id="8c030-190">Seuraava tiedot tuodaan, ja ne sisältyvät työntekijätietueeseen:</span><span class="sxs-lookup"><span data-stu-id="8c030-190">The following details are imported and included on the new employee record:</span></span>

- <span data-ttu-id="8c030-191">Etunimi</span><span class="sxs-lookup"><span data-stu-id="8c030-191">First name</span></span>
- <span data-ttu-id="8c030-192">Sukunimi</span><span class="sxs-lookup"><span data-stu-id="8c030-192">Last name</span></span>
- <span data-ttu-id="8c030-193">Työsuhteen alkamispäivä</span><span class="sxs-lookup"><span data-stu-id="8c030-193">Employment start date</span></span>
- <span data-ttu-id="8c030-194">Sähköpostiosoite</span><span class="sxs-lookup"><span data-stu-id="8c030-194">Email address</span></span>
- <span data-ttu-id="8c030-195">Puhelinnumero</span><span class="sxs-lookup"><span data-stu-id="8c030-195">Phone number</span></span>

## <a name="see-also"></a><span data-ttu-id="8c030-196">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="8c030-196">See also</span></span>

[<span data-ttu-id="8c030-197">Määritä Dataverse -virtuaalitaulukot</span><span class="sxs-lookup"><span data-stu-id="8c030-197">Configure Dataverse virtual tables</span></span>](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="8c030-198">Mikä on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="8c030-198">What is Microsoft Dataverse?</span></span>](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]