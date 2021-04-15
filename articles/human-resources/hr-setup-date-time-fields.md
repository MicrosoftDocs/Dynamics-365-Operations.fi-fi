---
title: Ymmärrä päivämäärä- ja kellonaikakentät
description: Tietoja siitä, mitä tapahtuu, kun Päivämäärä- ja Aika-kenttiä käytetään Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efda2b54f9228ac539e6ba2d18f85bf3ad15a6ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802428"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="f91a4-103">Ymmärrä päivämäärä- ja kellonaikakenttiä</span><span class="sxs-lookup"><span data-stu-id="f91a4-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f91a4-104">**Päivämäärä- ja Aika-** kentät ovat Dynamics 365 Human Resourcesin peruskäsitteitä.</span><span class="sxs-lookup"><span data-stu-id="f91a4-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f91a4-105">On tärkeää ymmärtää, miten **Päivämäärä ja aika** -tietoja käytetään lomakkeissa, Dataversessä ja ulkoisissa lähteissä.</span><span class="sxs-lookup"><span data-stu-id="f91a4-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="f91a4-106">Tietoja Päivämäärä- ja Päivämäärä ja aika -tietotyyppien eroista</span><span class="sxs-lookup"><span data-stu-id="f91a4-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="f91a4-107">**Päivämäärä ja aika** -kentissä on aikavyöhyketietoja, joita ei ole **Päivämäärä**-kentissä.</span><span class="sxs-lookup"><span data-stu-id="f91a4-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="f91a4-108">**Päivämäärä**-kentät näyttävät samat tiedot kaikissa sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="f91a4-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="f91a4-109">Kun **Päivämäärä**-kenttään annetaan tietoja, henkilöstöhallinto kirjoittaa saman päivämäärän tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="f91a4-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="f91a4-110">Kun tiedot näytetään **Päivämäärä ja aika** -kentässä, henkilöstöhallinto mukauttaa päivämäärää ja aikaa **Käyttäjän asetukset** -lomakkeessa (**Yleinen > Asetukset > Käyttäjän asetukset**) määritettyjen käyttäjän aikavyöhykkeen perusteella.</span><span class="sxs-lookup"><span data-stu-id="f91a4-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="f91a4-111">Kenttään annetut päivämäärä- ja aikatiedot eivät välttämättä ole samat kuin tietokantaan kirjoitettavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="f91a4-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="f91a4-112">[![Käyttäjän asetukset -lomake](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="f91a4-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="f91a4-113">Tietoja lomakkeiden Päivämäärä ja aika -kentistä</span><span class="sxs-lookup"><span data-stu-id="f91a4-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="f91a4-114">Näytössä näkyvät **Päivämäärä ja aika** -tiedot eivät ole samoja kuin tietokantaan tallennetut tiedot, jos käyttäjän vyöhykkeeksi ei ole määritetty UTC (Coordinated Universal Time) -aika.</span><span class="sxs-lookup"><span data-stu-id="f91a4-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="f91a4-115">**Päivämäärä ja aika** -kenttien tiedot tallennetaan aina UTC-aikana.</span><span class="sxs-lookup"><span data-stu-id="f91a4-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="f91a4-116">[![Työntekijä-lomake – UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="f91a4-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="f91a4-117">Tietoja tietokannan Päivämäärä ja aika -kentistä</span><span class="sxs-lookup"><span data-stu-id="f91a4-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="f91a4-118">Kun henkilöstöhallinto kirjoittaa **Päivämäärä ja aika** -arvon tietokannan, se tallentaa tiedot UTC-ajassa.</span><span class="sxs-lookup"><span data-stu-id="f91a4-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="f91a4-119">Tällä tavoin käyttäjät näkevät **Päivämäärä ja aika** -tiedot suhteessa käyttäjän asetuksissa määritettyyn aikavyöhykkeeseen.</span><span class="sxs-lookup"><span data-stu-id="f91a4-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="f91a4-120">Edellä olevassa esimerkissä aloitusaika on ajankohta, ei tietty päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="f91a4-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="f91a4-121">Kun kirjautuneen käyttäjän aikavyöhyke muutetaan siten, että GMT +12:00 on nyt GMT UTC, samassa tietueessa näkyy 04/30/2019 12:00:00 eikä 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="f91a4-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="f91a4-122">Jäljempänä olevassa esimerkissä työntekijän 000724 työsuhde aktivoituu samaan aikaan aikavyöhykkeestä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="f91a4-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="f91a4-123">Työntekijä aktivoituu 04/30/2019 GMT-aikavyöhykkeellä, mikä on sama kuin 05/01/2019 GMT+12:00 -aikavyöhykkeellä.</span><span class="sxs-lookup"><span data-stu-id="f91a4-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="f91a4-124">Kumpikin viittaa samaan ajankohtaan eikä tiettyyn päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="f91a4-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="f91a4-125">[![Työntekijä-lomake – GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="f91a4-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="f91a4-126">Data Management Frameworkin, Excelin, Dataversen ja Power BI:n päivämäärä ja aikatiedot</span><span class="sxs-lookup"><span data-stu-id="f91a4-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="f91a4-127">Data Management Framework, Excel-lisäosa, Dataverse ja Power BI -raportointi on suunniteltu käyttämään tietoja suoraan tietokantatasolla.</span><span class="sxs-lookup"><span data-stu-id="f91a4-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="f91a4-128">Koska mikään asiakas ei muuta **Päivämäärä ja aika** -tietoja käyttäjän aikavyöhykkeen mukaiseksi, kaikki **Päivämäärä ja aika** -tiedot ilmoitetaan UTC-aikoina, mikä voi saada aikaan virheellisiä olettamuksia tietoja annettaessa tai tarkasteltaessa.</span><span class="sxs-lookup"><span data-stu-id="f91a4-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="f91a4-129">Tietokanta olettaa, että DMF:n, Excelin tai Dataversen kautta lähetettävien **Päivämäärä ja aika** -tiedot ovat UTC-aikoja.</span><span class="sxs-lookup"><span data-stu-id="f91a4-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="f91a4-130">Tämä voi aiheuttaa sekaannusta, kun lähetetty **Päivämäärä ja aika** -arvo ei näy odotetusti, koska tietoja tarkastelevan käyttäjän aikavyöhykkeeksi ei ole määritetty UTC-aikaa.</span><span class="sxs-lookup"><span data-stu-id="f91a4-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="f91a4-131">Näin voi käydä (käänteisesti) myös tietoja vietäessä.</span><span class="sxs-lookup"><span data-stu-id="f91a4-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="f91a4-132">Viedyn DMF-yksikön **Päivämäärä ja aika** -tiedot voivat olla erilaiset kuin Dynamics-asiakasohjelmassa näkyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="f91a4-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="f91a4-133">Kun tietojen katsomiseen ja luomiseen käytetään ulkoisia lähteitä, kuten DMF:tä, kannattaa muistaa, että **Päivämäärä ja aika** -arvojen oletetaan olevan oletusarvoisesti UTC-arvoja riippumatta siitä, mikä on käyttäjän tietokoneen aikavyöhyke tai mitkä ovat nykyisen käyttäjän aikavyöhykeasetukset.</span><span class="sxs-lookup"><span data-stu-id="f91a4-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="f91a4-134">Esimerkkejä saman tietueen näkymisestä eri tuotantoalueilla</span><span class="sxs-lookup"><span data-stu-id="f91a4-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="f91a4-135">**Henkilöstöhallinto, kun käyttäjän aikavyöhykkeeksi on määritetty UTC**</span><span class="sxs-lookup"><span data-stu-id="f91a4-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="f91a4-136">[![Työntekijä-lomake, jonka ajaksi on määritetty UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="f91a4-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="f91a4-137">**Henkilöstöhallinto, kun käyttäjän aikavyöhykkeeksi on määritetty GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="f91a4-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="f91a4-138">[![Työntekijä-lomake, jonka ajaksi on määritetty GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="f91a4-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="f91a4-139">**Excel ODatan kautta**</span><span class="sxs-lookup"><span data-stu-id="f91a4-139">**Excel Via OData**</span></span>

<span data-ttu-id="f91a4-140">[![Excel ODatan kautta](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="f91a4-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="f91a4-141">**DMF-vaiheet**</span><span class="sxs-lookup"><span data-stu-id="f91a4-141">**DMF Staging**</span></span>

<span data-ttu-id="f91a4-142">[![DMF-vaiheet](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="f91a4-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="f91a4-143">**DMF-vienti**</span><span class="sxs-lookup"><span data-stu-id="f91a4-143">**DMF Export**</span></span>

<span data-ttu-id="f91a4-144">[![DMF-vienti](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="f91a4-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="f91a4-145">**Excel Dataversen kautta**</span><span class="sxs-lookup"><span data-stu-id="f91a4-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="f91a4-146">[![Excel Dataversen kautta](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="f91a4-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="f91a4-147">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f91a4-147">See also</span></span>

[<span data-ttu-id="f91a4-148">Päivämäärä ja aikatiedot</span><span class="sxs-lookup"><span data-stu-id="f91a4-148">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="f91a4-149">Käyttäjän ensisijaiset aikavyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="f91a4-149">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]