---
title: Common Data Service-integroinnin määritys
description: Voit ottaa integroinnin Common Data Servicen ja Microsoft Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä. Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida yksikön uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008856"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="c3cb9-104">Common Data Service-integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="c3cb9-104">Configure Common Data Service integration</span></span>

<span data-ttu-id="c3cb9-105">Voit ottaa integroinnin Common Data Servicen ja Microsoft Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-105">You can turn integration between Common Data Service and an instance of Microsoft Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="c3cb9-106">Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida yksikön uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="c3cb9-107">Kun poistat integroinnin käytöstä, käyttäjät voivat tehdä muutoksia Human Resourcesissa tai Common Data Servicessä, mutta näitä muutoksia ei synkronoida näiden kahden ympäristön välillä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="c3cb9-108">Oletusarvoisesti integrointi Human Resourcesin ja Common Data Servicen välillä on joko käytössä tai pois käytöstä sen mukaan, onko ympäristössä demotietoja:</span><span class="sxs-lookup"><span data-stu-id="c3cb9-108">By default, integration between Human Resources and Common Data Service is turned either off or on, depending on the presence of demo data in the environments:</span></span>

- <span data-ttu-id="c3cb9-109">**Pois** sellaisten uusien ympäristöjen osalta, joissa ei ole demotietoja</span><span class="sxs-lookup"><span data-stu-id="c3cb9-109">**Off** for new environments that don't include demo data</span></span>
- <span data-ttu-id="c3cb9-110">**Käytössä** sellaisten uusien ympäristöjen osalta, joissa on demotietoja</span><span class="sxs-lookup"><span data-stu-id="c3cb9-110">**On** for new environments that include demo data</span></span>

<span data-ttu-id="c3cb9-111">Uudet ympäristöt, joissa on demotietoja, alkavat synkronoida tietoja, kun ne valmistellaan.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-111">New environments that include demo data will start to sync data when they are provisioned.</span></span>

<span data-ttu-id="c3cb9-112">Integrointi voi kannattaa poistaa käytöstä seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="c3cb9-112">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="c3cb9-113">Olet täyttämässä dataa tietojen hallintakehyksen kautta ja sinun on tuotava tiedot useita kertoja, jotta saat ne oikeaan tilaan.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-113">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="c3cb9-114">Tietoihin liittyy ongelmia joko Human Resourcesissa tai Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-114">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="c3cb9-115">Jos poistat integroinnin käytöstä, voit poistaa tietueen yhdestä ympäristöstä poistamatta sitä toisessa ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-115">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="c3cb9-116">Kun otat integroinnin takaisin käyttöön, sen ympäristön tietue, jossa sitä ei poistettu, synkronoidaan takaisin siihen ympäristöön, jossa se poistettiin.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-116">When you turn integration back on, the record in the environment where it wasn't deleted will be synced back to the environment where it was deleted.</span></span> <span data-ttu-id="c3cb9-117">Synkronointi alkaa seuraavan kerran, kun **Common Data Servicen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-117">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="c3cb9-118">Kun poistat tietojen integroinnin käytöstä, varmista, ettet muokkaa samaa tietuetta molemmissa ympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-118">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="c3cb9-119">Kun otat integroinnin takaisin käyttöön, viimeksi muokattu tietue synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-119">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="c3cb9-120">Näin ollen, jos et tehnyt samoja muutoksia tietueeseen molemmissa ympäristöissä, tietoja voidaan menettää.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-120">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="c3cb9-121">Common Data Servicen integrointisivun käyttö</span><span class="sxs-lookup"><span data-stu-id="c3cb9-121">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="c3cb9-122">Valitse siinä Human Resources -esiintymässä, jossa haluat tarkastella tai määrittää Common Data Servicen kanssa integroinnin asetuksia, **Järjestelmän hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-122">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="c3cb9-123">[![Järjestelmän hallinta -ruutu](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="c3cb9-123">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="c3cb9-124">Valitse **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-124">Select the **Links** tab.</span></span>

    <span data-ttu-id="c3cb9-125">[![Linkit-välilehti](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="c3cb9-125">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="c3cb9-126">Valitse **Integroinnit**-kohdassa **Common Data Servicen määritys**.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-126">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="c3cb9-127">[![Common Data Servicen määrityslinkki](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="c3cb9-127">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="c3cb9-128">Human Resourcesin ja Common Data Servicen tietojen integroinnin käyttöönotto ja käytöstä poistaminen</span><span class="sxs-lookup"><span data-stu-id="c3cb9-128">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="c3cb9-129">Ota integrointi käyttöön asettamalla **Ota integrointi Common Data Serviceeen** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-129">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c3cb9-130">Kun otat integroinnin käyttöön, tiedot synkronoidaan seuraavan kerran, kun **Common Data Servicen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-130">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="c3cb9-131">Kaikkien tietojen pitäisi olla käytettävissä, kun erätyö on valmis.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-131">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="c3cb9-132">Voit poistaa integroinnin käytöstä määrittämällä asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-132">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="c3cb9-133">[![Common Data Service -integroinnin käyttöönotto tai käytöstä poisto](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="c3cb9-133">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="c3cb9-134">Integrointitietojen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="c3cb9-134">View data integration details</span></span>

<span data-ttu-id="c3cb9-135">**Common Data Service** -integroinnin -sivun **Ylläpito**-pikavälilehdessä voit nähdä, miten tietueet linkittyvät yhteen Human Resourcesin ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-135">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="c3cb9-136">Jos haluat tarkastella yksikön tietueita, valitse yksikkö **CDS-yksikön nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-136">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="c3cb9-137">Ruudukossa näkyvät kaikki valittuun yksikköön linkitetyt tietueet.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-137">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="c3cb9-138">[![Yksikön tietueen tarkasteleminen](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="c3cb9-138">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="c3cb9-139">Kaikkia Common Data Service -yksikköjä ei tällä hetkellä ole luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-139">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="c3cb9-140">Ruudukossa näkyvät vain ne yksiköt, jotka tukevat mukautettujen kenttien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-140">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="c3cb9-141">Uusia yksikköjä tulee saataville jatkuvien Human Resources -julkaisujen myötä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-141">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="c3cb9-142">Ruudukko sisältää seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="c3cb9-142">The grid includes the following fields:</span></span>

- <span data-ttu-id="c3cb9-143">**CDS-yksikön nimi** – Yksikön nimi Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-143">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="c3cb9-144">**CDS-yksikköviite** – Tunnus, jota Common Data Service käyttää yksikön tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-144">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="c3cb9-145">Tämä arvo vastaa Human Resourcesin **RecId**-arvoa.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-145">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="c3cb9-146">Löydät tunnuksen, kun avaat Common Data Service -yksikön Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-146">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="c3cb9-147">**Human Resources -yksikön nimi** – Yksikkö, joka viimeksi synkronoi tietoja Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-147">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="c3cb9-148">Yksiköllä voi olla joko Common Data Service -etuliite tai muu etuliite.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-148">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="c3cb9-149">**Human Resources -viite** – **RecId**-arvo, joka tietueelle on määritetty Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-149">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="c3cb9-150">**Poistettiin CDS:stä** – Arvo, joka ilmaisee, onko tietue poistettu Common Data Servicestä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-150">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="c3cb9-151">Poista Human Resourcesissa olevan tietueen liitos Common Data Servicestä</span><span class="sxs-lookup"><span data-stu-id="c3cb9-151">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="c3cb9-152">Jos kohtaat ongelmia Human Resourcesin ja Common Data Servicen välisen tietojen synkronoinnin aikana, voit ehkä ratkaista ne tyhjentämällä seurannan ja sallimalla seurantataulukon uudelleensynkronoinnin.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-152">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="c3cb9-153">Jos poistat liitoksen ja muutat tai poistat tietueen Common Data Servicessä, muutoksia ei synkronoida Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-153">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="c3cb9-154">Jos teet muutoksia Human Resourcesissa, uusi seurantatietue luodaan ja päivitetään Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-154">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="c3cb9-155">Jos haluat poistaa tietueen liitoksen Human Resourcesin ja Common Data Servicen väliltä, valitse yksikkö **CDS-yksikön nimi** -kentästä ja valitse sitten **Tyhjennä seurantatiedot**.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-155">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="c3cb9-156">[![Seurantatietojen tyhjennys](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="c3cb9-156">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="c3cb9-157">Katso seuraava menettely, jos haluat suorittaa yksikölle täydellisen synkronoinnin seurannan tyhjentämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-157">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="c3cb9-158">Synkronoi yksikkö Human Resourcesin ja Common Data Servicen välillä</span><span class="sxs-lookup"><span data-stu-id="c3cb9-158">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="c3cb9-159">Käytä tätä menettelyä, jos Common Data Servicestä peräisin olevien muutosten näkyminen Human Resourcesissa kestää liian kauan tai jaos sinun on päivitettävä seurantataulukko seurannan tyhjentämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-159">Use this procedure if changes from Common Data Service are taking too long to appear in Human Resources, or if you must refresh the tracking table after you clear the tracking.</span></span>

- <span data-ttu-id="c3cb9-160">Suorittaaksesi yksikölle täydellisen synkronoinnin Human Resourcesin ja Common Data Servicen välillä valitse yksikkö **CDS-yksikön nimi** -kentässä ja valitse sitten **Synkronoi nyt**.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-160">To run a full synchronization on an entity between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Sync now**.</span></span>

<span data-ttu-id="c3cb9-161">[![Täyden synkronoinnin suoritus](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="c3cb9-161">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


