---
title: Laajenna Talent käyttämällä PowerApps- ja Microsoft Flow -esimerkkejä
description: Tässä ohjeaiheessa käsitellään Microsoft PowerAppsia ja Microsoft Flow'ta käyttäviä Microsoft Dynamics 365 for Talentin laajennusesimerkkejä.
author: negudava
manager: Annbe
ms.date: 05/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: Dynamics 365 for Talent;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent;Core;Experience Apps
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2019-03-04
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c113b0f4ab2c8e44d00fcfca3f0a6ca828a854ae
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517878"
---
# <a name="extend-talent-by-using-powerapps-and-microsoft-flow---example-scenarios"></a><span data-ttu-id="42061-103">Laajenna Talent käyttämällä PowerApps- ja Microsoft Flow -esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="42061-103">Extend Talent by using PowerApps and Microsoft Flow - Example scenarios</span></span>

<span data-ttu-id="42061-104">Tässä ohjeaiheessa käsitellään Microsoft PowerAppsia ja Microsoft Flow'ta käyttäviä Microsoft Dynamics 365 for Talentin laajennusesimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="42061-104">This topic describes some examples of extensibility scenarios for Microsoft Dynamics 365 for Talent that use Microsoft PowerApps and Microsoft Flow.</span></span> <span data-ttu-id="42061-105">Voit tuoda kumpaankin esimerkkiin liitetyt ratkaisupaketin PowerApps-ympäristöön.</span><span class="sxs-lookup"><span data-stu-id="42061-105">You can import the solution package that is associated with each example into your PowerApps environment.</span></span> <span data-ttu-id="42061-106">Voit sitten käyttää paketteja joka ohjeena tai lähtökohtana, jonka avulla toteutat organisaatioon sopivia skenaarioita.</span><span class="sxs-lookup"><span data-stu-id="42061-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42061-107">Jos haluat käyttää tässä ohjeaiheessa kuvattuja malleja ja sovellusta sellaisenaan, varmista testaamalla, että ne kattavat kaikki toteutukseen kuuluvat skenaariot.</span><span class="sxs-lookup"><span data-stu-id="42061-107">If you want to use the templates and app that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="42061-108">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="42061-108">Prerequisites</span></span>

- <span data-ttu-id="42061-109">Pakettien tuontia varten käyttäjät tarvitsevat **Ympäristön tekijä** -käyttöoikeuden.</span><span class="sxs-lookup"><span data-stu-id="42061-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="42061-110">Sovellusten vientiä ja tuontia varten käyttäjillä on oltava PowerApps-palvelupaketin käyttöoikeus tai PowerApps -palvelupaketin 2 kokeiluversion käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="42061-110">To export or import apps, users must have a PowerApps Plan 2 license or a PowerApps Plan 2 trial license.</span></span>

## <a name="flow--form-connect"></a><span data-ttu-id="42061-111">Työnkulku – lomakeyhteys</span><span class="sxs-lookup"><span data-stu-id="42061-111">Flow – Form Connect</span></span>

<span data-ttu-id="42061-112">**Työnkulku – lomakeyhteys** -mallin avulla voi lukea tietoja Microsoft Formsista ja tallentaa ne Common Data Service -yksikköön.</span><span class="sxs-lookup"><span data-stu-id="42061-112">The **Flow – Form Connect** template can be used to read data from Microsoft Forms and store it in a Common Data Service entity.</span></span>

<span data-ttu-id="42061-113">Mallia voidaan laajentaa siten, että sitä voidaan käyttää muissa skenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="42061-113">This template can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="42061-114">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="42061-114">Here are some examples:</span></span>

- <span data-ttu-id="42061-115">Ehdokasarviointien taltiointi.</span><span class="sxs-lookup"><span data-stu-id="42061-115">Capture candidate assessments.</span></span>
- <span data-ttu-id="42061-116">Kurssin kyselylomakkeiden tulosten taltiointi.</span><span class="sxs-lookup"><span data-stu-id="42061-116">Capture results from course questionnaires.</span></span>
- <span data-ttu-id="42061-117">Haastattelukysymyskirjaston kokoaminen henkilöstöhallinnon järjestelmänvalvojille.</span><span class="sxs-lookup"><span data-stu-id="42061-117">Compile a library of interview questions for Human resources (HR) administrators.</span></span>
- <span data-ttu-id="42061-118">Ehdokkaan haastatteluprosessin arvioinnin taltiointi.</span><span class="sxs-lookup"><span data-stu-id="42061-118">Capture a candidate's evaluation of the interview process</span></span>

<span data-ttu-id="42061-119">Lomakkeet voivat näkyä Microsoft Dynamics 365: Attractissa ehdokasportaalissa ja ehdokkaat voit täyttää tiedot.</span><span class="sxs-lookup"><span data-stu-id="42061-119">In Microsoft Dynamics 365: Attract, forms can appear in Candidate portal, and candidates can fill in details.</span></span> <span data-ttu-id="42061-120">Lomakkeet voidaan myös upottaa tehtävinä työmalliin.</span><span class="sxs-lookup"><span data-stu-id="42061-120">Forms can also be embedded as activities in a job template.</span></span>

<span data-ttu-id="42061-121">Kun ehdokas lähettää lomakkeen, Microsoft Flow taltioi lomakkeen lähetyksen, lukee tiedot ja tallentaa sen Common Data Service -yksikköön.</span><span class="sxs-lookup"><span data-stu-id="42061-121">When a candidate submits a form, Microsoft Flow captures the form submission, reads the data, and stores it in the Common Data Service entity.</span></span>

<span data-ttu-id="42061-122">Voit ladata **Työnkulku – lomakeyhteys** -mallin ja mukautetun yksikkörakenteen siirtymällä Microsoft Download Centerissä kohtaan [Työnkulku – lomakeyhteys](https://go.microsoft.com/fwlink/?linkid=2081988).</span><span class="sxs-lookup"><span data-stu-id="42061-122">To download the **Flow – Form Connect** template and Custom Entity Structure, go to [Flow – Form Connect](https://go.microsoft.com/fwlink/?linkid=2081988) on the Microsoft Download Center.</span></span>

## <a name="initiate-and-extract-parameters-passed-to-powerapps"></a><span data-ttu-id="42061-123">Powerappsiin välitettyjen parametrien aloittaminen ja purkaminen</span><span class="sxs-lookup"><span data-stu-id="42061-123">Initiate and Extract Parameters Passed to Powerapps</span></span>

<span data-ttu-id="42061-124">**Powerappsiin välitettyjen parametrien aloittaminen ja purkaminen** -mallia voidaan käyttää minkä tahansa Attractin PowerApps-skenaarion aloituskohtana.</span><span class="sxs-lookup"><span data-stu-id="42061-124">The **Initiate and Extract Parameters Passed to Powerapps** template can be used as a starting point for any PowerApps scenario that is specific to Attract.</span></span> <span data-ttu-id="42061-125">Se sisältää kaikki Attractin välittämät oletusparametrit, kuten **Työhakemus**, **Ehdokkaan tunnus** ja **Työn tunnus**.</span><span class="sxs-lookup"><span data-stu-id="42061-125">It includes all the default parameters that are passed by Attract, such as **Job Application**, **Candidate ID**, and **JobID**.</span></span>

<span data-ttu-id="42061-126">Tällä mallilla voi hakea ehdokkaan arviointilomakkeen, jotta työhön ottava esimies voi tarkastella ehdokkaan täyttämää arviointia.</span><span class="sxs-lookup"><span data-stu-id="42061-126">This template can be used to retrieve a candidate assessment form, so that a hiring manager can view the assessment that a candidate filled in.</span></span>

<span data-ttu-id="42061-127">PowerAppsilla luodut sovellukset voidaan upottaa työmalliin Attractissa.</span><span class="sxs-lookup"><span data-stu-id="42061-127">Apps that are created by using PowerApps can be embedded into the job template in Attract.</span></span>

<span data-ttu-id="42061-128">Voit ladata **Powerappsiin välitettyjen parametrien aloittaminen ja purkaminen** -mallin ja mukautetun yksikkörakenteen Microsoft Download Centerin kohdassa [Powerappsiin välitettyjen parametrien aloittaminen ja purkaminen](https://go.microsoft.com/fwlink/?linkid=2081991).</span><span class="sxs-lookup"><span data-stu-id="42061-128">To download the **Initiate and Extract Parameters Passed to Powerapps** template and Custom Entity Structure, go to [Initiate and Extract Parameters Passed to Powerapps](https://go.microsoft.com/fwlink/?linkid=2081991) on the Microsoft Download Center.</span></span>

## <a name="integration-with-office-365"></a><span data-ttu-id="42061-129">Integrointi Office 365:n kanssa</span><span class="sxs-lookup"><span data-stu-id="42061-129">Integration with Office 365</span></span>

<span data-ttu-id="42061-130">**Office 365 -integrointi** -sovelluksella voi purkaa kirjautuneiden käyttäjien tiimitiedot Microsoft Office 365:stä.</span><span class="sxs-lookup"><span data-stu-id="42061-130">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="42061-131">Se hakee työntekijäviitteet Talentissa ja purkaa saapumis- ja poistumisaikatiedot sekä poikkeustallenteet.</span><span class="sxs-lookup"><span data-stu-id="42061-131">It references workers in Talent to extract clock-in and clock-out details and exception recordings.</span></span> <span data-ttu-id="42061-132">Saapumis- ja poistumisaikatiedot tallennetaan mukautettuihin Common Data Service -yksiköihin.</span><span class="sxs-lookup"><span data-stu-id="42061-132">Clock-in and Clock-out details are stored in custom Common Data Service entities.</span></span> <span data-ttu-id="42061-133">Oletuksen on, että ulkopuoliset järjestelmät täyttävät nämä tiedot integroinnin kautta.</span><span class="sxs-lookup"><span data-stu-id="42061-133">The assumption is that these details are filled in from third-party systems via integration.</span></span>

<span data-ttu-id="42061-134">Sovellusta voidaan laajentaa siten, että sitä voidaan käyttää muissa skenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="42061-134">This app can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="42061-135">Sitä voidaan käyttää esimerkiksi näyttämään ryhmän lomatiedot, kalenteritapahtumat ja kaikki ryhmäkohtaiset tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="42061-135">For example, it can be used to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="42061-136">Voit ladata **Office 365 -integrointi** -sovelluksen ja mukautetun yksikkörakenteen Microsoft Download Centerin kohdassa [Office 365 -integrointi](https://go.microsoft.com/fwlink/?linkid=2081787).</span><span class="sxs-lookup"><span data-stu-id="42061-136">To download the **Integration with Office 365** app and Custome Entity Structure, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="flow--email-notification"></a><span data-ttu-id="42061-137">Työnkulku – sähköposti-ilmoitus</span><span class="sxs-lookup"><span data-stu-id="42061-137">Flow – Email Notification</span></span>

<span data-ttu-id="42061-138">**Työnkulku – sähköposti-ilmoitus** -mallia voi käyttää sähköposti-ilmoitusskenaarioissa.</span><span class="sxs-lookup"><span data-stu-id="42061-138">The **Flow – Email Notification** template can be used for email notification scenarios.</span></span> <span data-ttu-id="42061-139">Sen avulla voidaan käynnistää sähköposti-ilmoitukset niille ehdokkaille, jotka työhönottoryhmä hylkää rekrytointiprosessin jossain vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="42061-139">It can be used to trigger notification emails to candidates that the hiring team rejects during any stage of the recruiting process.</span></span>

<span data-ttu-id="42061-140">Tämä malli voidaan laajentaa seuraamaan ehdokasvaiheen muutoksia koko rekrytointiprosessin ajan sekä lähettämään ilmoitukset työhönottoryhmälle ja ehdokkaalle.</span><span class="sxs-lookup"><span data-stu-id="42061-140">This template can be extended to track changes to the candidate stage throughout the recruiting process, and to send notifications to the hiring team and candidate.</span></span>

<span data-ttu-id="42061-141">Yleisesti ottaen työnkulut voidaan määrittää lähettämään Common Data Serviceen tallennettuihin yksiköihin ilmoitukset Core HR:n, Attractin tai Dynamics 365 Talent: Onboardin tapahtumista.</span><span class="sxs-lookup"><span data-stu-id="42061-141">In general, for entities that are stored in Common Data Service, flows can be set up to send notifications for events that occur in Core HR, Attract, or Dynamics 365 Talent: Onboard.</span></span>

<span data-ttu-id="42061-142">Voit ladata **Työnkulku – sähköposti-ilmoitus** mallin Microsoft Download Centerin kohdassa [Työnkulku – sähköposti-ilmoitus](https://go.microsoft.com/fwlink/?linkid=2082103).</span><span class="sxs-lookup"><span data-stu-id="42061-142">To download the **Flow – Email Notification** template, go to [Flow – Email Notification](https://go.microsoft.com/fwlink/?linkid=2082103) on the Microsoft Download Center.</span></span>

## <a name="flow--sql-connect-and-execute"></a><span data-ttu-id="42061-143">Työnkulku – SQL-yhteys ja toteutus</span><span class="sxs-lookup"><span data-stu-id="42061-143">Flow – SQL Connect and execute</span></span>

<span data-ttu-id="42061-144">**Työnkulku – SQL-yhteys ja toteutus** -malli muodostaa yhteyden Microsoft SQL Serveriin ja mahdollistaa SQL-kyselyjen suorittamisen.</span><span class="sxs-lookup"><span data-stu-id="42061-144">The **Flow – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="42061-145">Vaikka tämä malli on suunniteltu lukemaan ja päivittämään SQL-taulukkoja, se voidaan laajentaa muissa skenaarioissa käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="42061-145">Although this template is designed to read and update SQL tables, it can be extended so that it can be used for other scenarios.</span></span> <span data-ttu-id="42061-146">Sen avulla voidaan esimerkiksi täyttää valmistelutaulu Common Data Servicessä SQL Serverin tietueilla sekä synkronoida valmistelutaulu säännöllisesti käyttämällä SQL Serverin lisäävää työntöä.</span><span class="sxs-lookup"><span data-stu-id="42061-146">For example, it can be used to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="42061-147">Voit ladata **Työnkulku – SQL-yhteys ja toteutus** -mallin Microsoft Download Centerin kohdassa [Työnkulku – SQL-yhteys ja toteutus](https://go.microsoft.com/fwlink/?linkid=2081789).</span><span class="sxs-lookup"><span data-stu-id="42061-147">To download the **Flow – SQL Connect and execute** template, go to [Flow – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="flow--sharepoint-integration"></a><span data-ttu-id="42061-148">Työnkulku – SharePoint-integrointi</span><span class="sxs-lookup"><span data-stu-id="42061-148">Flow – SharePoint Integration</span></span>

<span data-ttu-id="42061-149">**Työnkulku – SharePoint-integrointi** -mallin avulla voi lukea tietoja Microsoft SharePoint -luettelosta, verrata luetteloa Common Data Service -yksikön kenttien arvoihin ja lähettää vertailun tulokset ilmoitussähköpostina.</span><span class="sxs-lookup"><span data-stu-id="42061-149">The **Flow – SharePoint Integration** template can be used to read data from a Microsoft SharePoint list, compare the list with field values for any Common Data Service entity, and send the results of the comparison as a notification email.</span></span> 

<span data-ttu-id="42061-150">Organisaatio voi tarvita pikaisesti tiettyjä osaamisalueita.</span><span class="sxs-lookup"><span data-stu-id="42061-150">An organization might have a set of skills that it urgently requires.</span></span> <span data-ttu-id="42061-151">Nämä osaamisalueet voidaan tallentaa SharePointiin SharePoint-luettelona.</span><span class="sxs-lookup"><span data-stu-id="42061-151">These skills can be stored in SharePoint as a SharePoint list.</span></span> <span data-ttu-id="42061-152">Jos ehdokas hakee työtä, jossa on mainittu tarvittava osaamisaluejoukko, ja jos ehdokkaan osaamisalue ja SharePointiin tallennetut osaamisalueet vastaavat hyvin toisiaan, ilmoitussähköposti lähetetään.</span><span class="sxs-lookup"><span data-stu-id="42061-152">When a candidate applies for any job that a set of required skills is listed for, if there is a significant match between the candidate's skill and the skills that are stored in SharePoint, a notification email is sent.</span></span> <span data-ttu-id="42061-153">Tällä tavoin kiireellisesti täytettävä toimet voidaan täyttää nopeammin, sillä ilmoitukset auttavat työhönottajia tavoittelemaan ja palkkaamaan ehdokkaita koko organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="42061-153">In this way, positions that are urgently required are filled faster, because the notifications help recruiters reach out and cross-hire candidates throughout the organization.</span></span>

<span data-ttu-id="42061-154">Tämä malli voidaan laajentaa käytettäväksi missä tahansa SharePoint-integraation sisältävässä skenaariossa.</span><span class="sxs-lookup"><span data-stu-id="42061-154">This template can be extended so that it can be used for any scenario that involves SharePoint integration.</span></span>

<span data-ttu-id="42061-155">Voit ladata **Työnkulku – SharePoint-integrointi** -mallin Microsoft Download Centerin kohdassa [Työnkulku – SharePoint-integrointi](https://go.microsoft.com/fwlink/?linkid=2082109).</span><span class="sxs-lookup"><span data-stu-id="42061-155">To download the **Flow – SharePoint Integration** template, go to [Flow – SharePoint Integration](https://go.microsoft.com/fwlink/?linkid=2082109) on the Microsoft Download Center.</span></span>

## <a name="admin-console-to-manage-talent-pools"></a><span data-ttu-id="42061-156">Hallintakonsoli kykypoolien hallintaan</span><span class="sxs-lookup"><span data-stu-id="42061-156">Admin console to manage talent pools</span></span>

<span data-ttu-id="42061-157">Kun otat käyttöön LinkedIn-integroinnin, Attract luo automaattisesti LinkedIn-kykypoolin.</span><span class="sxs-lookup"><span data-stu-id="42061-157">When you enable integration with LinkedIn, Attract automatically createas a LinkedIn talent pool.</span></span> <span data-ttu-id="42061-158">Kun rekrytoija lähettää InMail-viestin rekrytoitavan kanssa LinkedIn kautta, Attract luo profiilin rekrytoitavalle ja rekrytoitava tulee jäsenenä LinkedIn-kykypooliin.</span><span class="sxs-lookup"><span data-stu-id="42061-158">When a recruiter exchanges InMail with a recruit through LinkedIn, Attract creates a profile for the recruit, and the recruit becomes a member of the LinkedIn talent pool.</span></span> <span data-ttu-id="42061-159">Tämä PowerApps-sovellus on hyödyllinen järjestettäessä ehdokkaita osaamisryhmiin taitojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="42061-159">This PowerApps app is useful for reorganizing candidates in talent pools based on skill.</span></span>

<span data-ttu-id="42061-160">Suorita tämä PowerApps-sovellus hallintakonsolina seuraavien tehtävien suorittamiseksi:</span><span class="sxs-lookup"><span data-stu-id="42061-160">Run this PowerApps app as an admin console to perform the following tasks:</span></span>

- <span data-ttu-id="42061-161">Listaa ehdokkaat kykypooliin</span><span class="sxs-lookup"><span data-stu-id="42061-161">List candidates in a talent pool</span></span>
- <span data-ttu-id="42061-162">Hakijoiden lisääminen ja poistaminen kykypoolista</span><span class="sxs-lookup"><span data-stu-id="42061-162">Add and remove candidates from a talent pool</span></span>
- <span data-ttu-id="42061-163">Siirrä ehdokkaita yhdestä kykypoolista toiseen</span><span class="sxs-lookup"><span data-stu-id="42061-163">Move candidates from one talent pool to another</span></span>
- <span data-ttu-id="42061-164">Päätä, ovatko ehdokkaat jo osa kykypoolia ennen niiden siirtämistä</span><span class="sxs-lookup"><span data-stu-id="42061-164">Determine whether candidates are already part of a talent pool before moving them</span></span>
- <span data-ttu-id="42061-165">Tarkista ehdokkaiden taidot ennen niiden siirtämistä muihin kykypooleihin</span><span class="sxs-lookup"><span data-stu-id="42061-165">Check the skills of candidates before moving them to other talent pools</span></span>

<span data-ttu-id="42061-166">Tämä PowerApps-sovellus käyttää monta-moneen-yhteyksiä, joten voit käyttää sitä mallina muille skenaarioille, joissa sinun täytyy poimia useita monta-moneen-yhteyksiä vaativia tietoja.</span><span class="sxs-lookup"><span data-stu-id="42061-166">This PowerApps app uses many-to-many relationships, so you can use it as a template for other scenarios where you need to extract records that have many-to-many relationships.</span></span>

<span data-ttu-id="42061-167">Voit ladata **Hallintakonsoli kykypoolien hallintaan** -mallin siirtymällä kohtaan [Hallintakonsoli kykypoolien hallintaan](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) Microsoft Download Centerissä.</span><span class="sxs-lookup"><span data-stu-id="42061-167">To download the **Admin console to manage talent pools** template,  go to [Admin console to manage talent pools](http://www.microsoft.com/downloads/details.aspx?FamilyID=780a5eee-0e2a-4159-9a83-009f9ccdc469) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42061-168">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="42061-168">Additional resources</span></span>

[<span data-ttu-id="42061-169">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="42061-169">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)

[<span data-ttu-id="42061-170">Sovelluksen siirtäminen vuokraajien ja ympäristöjen kesken</span><span class="sxs-lookup"><span data-stu-id="42061-170">Migrate app between tenants and environments</span></span>](https://docs.microsoft.com/en-us/power-platform/admin/environment-and-tenant-migration)
