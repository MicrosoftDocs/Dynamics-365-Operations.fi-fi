---
title: Päivämäärän ja ajan käyttäminen Microsoft Dynamics 365 Talentissa
description: Tietoja siitä, mitä tapahtuu, kun Päivämäärä- ja Aika-kenttiä käytetään Microsoft Dynamics 365 Talentissa. Saat tietää, mitä on odotettavissa, kun päivämäärä- ja aikatietoja käytetään Talentin lomakkeessa, ulkoisessa lähteessä tai Common Data Servicessä.
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
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
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a1d1a47bfe6bd58b1e1a0d4d46c2133f3bf48ad
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2019
ms.locfileid: "2007964"
---
# <a name="date-and-time-fields-in-talent"></a><span data-ttu-id="e715a-104">Talentin päivämäärä- ja kellonaikakentät</span><span class="sxs-lookup"><span data-stu-id="e715a-104">Date and Time fields in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e715a-105">**Päivämäärä- ja Aika-** kentät ovat Dynamics 365 Talentin peruskäsitteitä.</span><span class="sxs-lookup"><span data-stu-id="e715a-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Talent.</span></span> <span data-ttu-id="e715a-106">On tärkeää ymmärtää, miten **Päivämäärä ja aika** -tietoja käytetään Dynamics 365 -lomakkeessa, Common Data Servicessä ja ulkoisissa lähteissä.</span><span class="sxs-lookup"><span data-stu-id="e715a-106">It's important to understand how to work with **Date and Time** data in a Dynamics 365 form, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="e715a-107">Tietoja Päivämäärä- ja Päivämäärä ja aika -tietotyyppien eroista</span><span class="sxs-lookup"><span data-stu-id="e715a-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="e715a-108">**Päivämäärä ja aika** -kentissä on aikavyöhyketietoja, joita ei ole **Päivämäärä**-kentissä.</span><span class="sxs-lookup"><span data-stu-id="e715a-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="e715a-109">**Päivämäärä**-kentät näyttävät samat tiedot kaikissa sijainneissa.</span><span class="sxs-lookup"><span data-stu-id="e715a-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="e715a-110">Kun **Päivämäärä**-kenttään annetaan tietoja, Talent kirjoittaa saman päivämäärän tietokantaan.</span><span class="sxs-lookup"><span data-stu-id="e715a-110">When you enter a date into a **Date** field, Talent writes that same date to the database.</span></span>

<span data-ttu-id="e715a-111">Kun tiedot näytetään **Päivämäärä ja aika** -kentässä, Talent mukauttaa päivämäärää ja aikaa **Käyttäjän asetukset** -lomakkeessa (**Yleinen > Asetukset > Käyttäjän asetukset**) määritettyjen käyttäjän aikavyöhykkeen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e715a-111">When displaying data in a **Date and Time** field, Talent adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="e715a-112">Kenttään annetut päivämäärä- ja aikatiedot eivät välttämättä ole samat kuin tietokantaan kirjoitettavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="e715a-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="e715a-113">[![Käyttäjän asetukset -lomake](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="e715a-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="e715a-114">Tietoja lomakkeiden Päivämäärä ja aika -kentistä</span><span class="sxs-lookup"><span data-stu-id="e715a-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="e715a-115">Kun tietoja annetaan **Päivämäärä ja aika** -kentässä, näytössä näkyvät tiedot eivät ole samoja kuin tietokantaan tallennetut tiedot, jos käyttäjän vyöhykkeeksi ei ole määritetty UTC (Coordinated Universal Time) -aika.</span><span class="sxs-lookup"><span data-stu-id="e715a-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="e715a-116">**Päivämäärä ja aika** -kenttien tiedot tallennetaan aina UTC-aikana.</span><span class="sxs-lookup"><span data-stu-id="e715a-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="e715a-117">[![Työntekijä-lomake](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="e715a-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="e715a-118">Tietoja tietokannan Päivämäärä ja aika -kentistä</span><span class="sxs-lookup"><span data-stu-id="e715a-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="e715a-119">Kun Talent kirjoittaa **Päivämäärä ja aika** -arvon tietokannan, se tallentaa tiedot UTC-ajassa.</span><span class="sxs-lookup"><span data-stu-id="e715a-119">When Talent writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="e715a-120">Tällä tavoin käyttäjät näkevät **Päivämäärä ja aika** -tiedot suhteessa käyttäjän asetuksissa määritettyyn aikavyöhykkeeseen.</span><span class="sxs-lookup"><span data-stu-id="e715a-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="e715a-121">Edellä olevassa esimerkissä aloitusaika on ajankohta, ei tietty päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="e715a-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="e715a-122">Kun kirjautuneen käyttäjän aikavyöhyke muutetaan siten, että GMT +12:00 on nyt GMT UTC, samassa juuri luodussa tietueessa näkyy 04/30/2019 12:00:00 eikä 05/01/2019 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="e715a-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="e715a-123">Jäljempänä olevassa esimerkissä työntekijän 000724 työsuhde aktivoituu samaan aikaan aikavyöhykkeestä riippumatta.</span><span class="sxs-lookup"><span data-stu-id="e715a-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="e715a-124">Työntekijä aktivoituu 04/30/2019 GMT-aikavyöhykkeellä, mikä on sama kuin 05/01/2019 GMT+12:00 -aikavyöhykkeellä.</span><span class="sxs-lookup"><span data-stu-id="e715a-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="e715a-125">Kumpikin viittaa samaan ajankohtaan eikä tiettyyn päivämäärään.</span><span class="sxs-lookup"><span data-stu-id="e715a-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="e715a-126">[![Työntekijä-lomake](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="e715a-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="e715a-127">Data Management Frameworkin, Excelin, Common Data Servicen ja Power BI:n päivämäärä ja aikatiedot</span><span class="sxs-lookup"><span data-stu-id="e715a-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="e715a-128">Data Management Framework, Excel-lisäosa, Common Data Service ja Power BI -raportointi on suunniteltu käyttämään tietoja suoraan tietokantatasolla.</span><span class="sxs-lookup"><span data-stu-id="e715a-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="e715a-129">Koska mikään asiakas ei muuta **Päivämäärä ja aika** -tietoja käyttäjän aikavyöhykkeen mukaiseksi, kaikki **Päivämäärä ja aika** -tiedot ilmoitetaan UTC-aikoina, mikä voi saada aikaan virheellisiä olettamuksia tietoja annettaessa tai tarkasteltaessa.</span><span class="sxs-lookup"><span data-stu-id="e715a-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="e715a-130">Tietokanta olettaa, että DMF:n, Excelin tai Common Data Servicen kautta lähetettävien **Päivämäärä ja aika** -tiedot ovat UTC-aikoja.</span><span class="sxs-lookup"><span data-stu-id="e715a-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="e715a-131">Tämä voi aiheuttaa sekaannusta, kun lähetetty **Päivämäärä ja aika** -arvo ei näy odotetusti, koska tietoja tarkastelevan käyttäjän aikavyöhykkeeksi ei ole määritetty UTC-aikaa.</span><span class="sxs-lookup"><span data-stu-id="e715a-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="e715a-132">Näin voi käydä (käänteisesti) myös tietoja vietäessä.</span><span class="sxs-lookup"><span data-stu-id="e715a-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="e715a-133">Viedyn DMF-yksikön **Päivämäärä ja aika** -tiedot voivat olla erilaiset kuin Dynamics-asiakasohjelmassa näkyvät tiedot.</span><span class="sxs-lookup"><span data-stu-id="e715a-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="e715a-134">Kun tietojen katsomiseen ja luomiseen käytetään ulkoisia lähteitä, kuten DMF:tä, on tärkeää muistaa, että **Päivämäärä ja aika** -arvojen oletetaan olevan oletusarvoisesti UTC-arvoja riippumatta siitä, mikä on käyttäjän tietokoneen aikavyöhyke tai mitkä ovat nykyisen käyttäjän aikavyöhykeasetukset.</span><span class="sxs-lookup"><span data-stu-id="e715a-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="e715a-135">Esimerkkejä saman tietueen näkymisestä eri tuotantoalueilla</span><span class="sxs-lookup"><span data-stu-id="e715a-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="e715a-136">**Talent, kun käyttäjän aikavyöhykkeeksi on määritetty UTC**</span><span class="sxs-lookup"><span data-stu-id="e715a-136">**Talent with user time zone set to UTC**</span></span>

<span data-ttu-id="e715a-137">[![Työntekijä-lomake](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="e715a-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="e715a-138">**Talent, kun käyttäjän aikavyöhykkeeksi on määritetty GMT +12:00**</span><span class="sxs-lookup"><span data-stu-id="e715a-138">**Talent with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="e715a-139">[![Työntekijä-lomake](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="e715a-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="e715a-140">**Excel ODatan kautta**</span><span class="sxs-lookup"><span data-stu-id="e715a-140">**Excel Via OData**</span></span>

<span data-ttu-id="e715a-141">[![Excel ODatan kautta](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="e715a-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="e715a-142">**DMF-vaiheet**</span><span class="sxs-lookup"><span data-stu-id="e715a-142">**DMF Staging**</span></span>

<span data-ttu-id="e715a-143">[![DMF-vaiheet](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="e715a-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="e715a-144">**DMF-vienti**</span><span class="sxs-lookup"><span data-stu-id="e715a-144">**DMF Export**</span></span>

<span data-ttu-id="e715a-145">[![DMF-vaiheet](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="e715a-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="e715a-146">**Excel Common Data Servicen kautta**</span><span class="sxs-lookup"><span data-stu-id="e715a-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="e715a-147">[![Excel Common Data Servicen kautta](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="e715a-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

### <a name="see-also"></a><span data-ttu-id="e715a-148">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="e715a-148">See also</span></span>

[<span data-ttu-id="e715a-149">Päivämäärä ja aikatiedot</span><span class="sxs-lookup"><span data-stu-id="e715a-149">Date and time data</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="e715a-150">Käyttäjän ensisijaiset aikavyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="e715a-150">User preferred time zones</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
