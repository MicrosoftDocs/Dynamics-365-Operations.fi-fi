---
title: Määritä Common Data Service -integraatio
description: Voit ottaa integroinnin Common Data Servicen ja Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä. Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida yksikön uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9ee4715526e18b33ae4b7e90b081ed5868bb19c
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527918"
---
# <a name="configure-common-data-service-integration"></a><span data-ttu-id="0ec05-104">Määritä Common Data Service -integraatio</span><span class="sxs-lookup"><span data-stu-id="0ec05-104">Configure Common Data Service integration</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0ec05-105">Voit ottaa integroinnin Common Data Servicen ja Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-105">You can turn integration between Common Data Service and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="0ec05-106">Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida yksikön uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-106">You can also view the synchronization details, clear tracking data, and resync an entity to help troubleshoot data issues between the two environments.</span></span>

<span data-ttu-id="0ec05-107">Kun poistat integroinnin käytöstä, käyttäjät voivat tehdä muutoksia Human Resourcesissa tai Common Data Servicessä, mutta näitä muutoksia ei synkronoida näiden kahden ympäristön välillä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-107">When you turn off integration, users can make changes in Human Resources or Common Data Service, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="0ec05-108">Oletusarvoisesti Human Resourcesin ja Common Data Servicen tietojen integrointi on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-108">By default, integration between Human Resources and Common Data Service is turned off.</span></span>

<span data-ttu-id="0ec05-109">Integrointi voi kannattaa poistaa käytöstä seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="0ec05-109">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="0ec05-110">Olet täyttämässä dataa tietojen hallintakehyksen kautta ja sinun on tuotava tiedot useita kertoja, jotta saat ne oikeaan tilaan.</span><span class="sxs-lookup"><span data-stu-id="0ec05-110">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="0ec05-111">Tietoihin liittyy ongelmia joko Human Resourcesissa tai Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-111">There are issues with data in either Human Resources or Common Data Service.</span></span> <span data-ttu-id="0ec05-112">Jos poistat integroinnin käytöstä, voit poistaa tietueen yhdestä ympäristöstä poistamatta sitä toisessa ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-112">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="0ec05-113">Kun otat integroinnin takaisin käyttöön, sen ympäristön tietue, josta sitä ei poistettu, synkronoidaan siihen ympäristöön, josta se poistettiin.</span><span class="sxs-lookup"><span data-stu-id="0ec05-113">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="0ec05-114">Synkronointi alkaa seuraavan kerran, kun **Common Data Servicen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="0ec05-114">Synchronization begins the next time the **Common Data Service integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="0ec05-115">Kun poistat tietojen integroinnin käytöstä, varmista, ettet muokkaa samaa tietuetta molemmissa ympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-115">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="0ec05-116">Kun otat integroinnin takaisin käyttöön, viimeksi muokattu tietue synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="0ec05-116">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="0ec05-117">Näin ollen, jos et tehnyt samoja muutoksia tietueeseen molemmissa ympäristöissä, tietoja voidaan menettää.</span><span class="sxs-lookup"><span data-stu-id="0ec05-117">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-common-data-service-integration-page"></a><span data-ttu-id="0ec05-118">Common Data Servicen integrointisivun käyttö</span><span class="sxs-lookup"><span data-stu-id="0ec05-118">Access the Common Data Service integration page</span></span>

1. <span data-ttu-id="0ec05-119">Valitse siinä Human Resources -esiintymässä, jossa haluat tarkastella tai määrittää Common Data Servicen kanssa integroinnin asetuksia, **Järjestelmän hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="0ec05-119">In the Human Resources instance where you want to view or configure settings for the integration with Common Data Service, select the **System administration** tile.</span></span>

    <span data-ttu-id="0ec05-120">[![Järjestelmän hallinta -ruutu](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="0ec05-120">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="0ec05-121">Valitse **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="0ec05-121">Select the **Links** tab.</span></span>

    <span data-ttu-id="0ec05-122">[![Linkit-välilehti](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="0ec05-122">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="0ec05-123">Valitse **Integroinnit**-kohdassa **Common Data Servicen määritys**.</span><span class="sxs-lookup"><span data-stu-id="0ec05-123">Under **Integrations**, select **Common Data Service configuration**.</span></span>

    <span data-ttu-id="0ec05-124">[![Common Data Servicen määrityslinkki](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span><span class="sxs-lookup"><span data-stu-id="0ec05-124">[![Common Data Service configuration link](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a><span data-ttu-id="0ec05-125">Human Resourcesin ja Common Data Servicen tietojen integroinnin käyttöönotto ja käytöstä poistaminen</span><span class="sxs-lookup"><span data-stu-id="0ec05-125">Turn data integration between Human Resources and Common Data Service on or off</span></span>

- <span data-ttu-id="0ec05-126">Ota integrointi käyttöön asettamalla **Ota integrointi Common Data Serviceeen** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0ec05-126">To turn on integration, set the **Enable the integration to the Common Data Service** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ec05-127">Kun otat integroinnin käyttöön, tiedot synkronoidaan seuraavan kerran, kun **Common Data Servicen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="0ec05-127">When you turn on integration, data will be synced the next time that the **Common Data Service integration missed request sync** batch job runs.</span></span> <span data-ttu-id="0ec05-128">Kaikkien tietojen pitäisi olla käytettävissä, kun erätyö on valmis.</span><span class="sxs-lookup"><span data-stu-id="0ec05-128">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="0ec05-129">Voit poistaa integroinnin käytöstä määrittämällä asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="0ec05-129">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="0ec05-130">[![Common Data Service -integroinnin käyttöönotto tai käytöstä poisto](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="0ec05-130">[![Turning the Common Data Service integration on or off](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)</span></span>

> [!WARNING]
> <span data-ttu-id="0ec05-131">On suositeltavaa, että Common Data Service -integrointi poistetaan käytöstä, kun tiedonsiirtotehtäviä suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="0ec05-131">We strongly recommend turning off Common Data Service integration while performing data migration tasks.</span></span> <span data-ttu-id="0ec05-132">Suurten tietomäärien lataaminen voi vaikuttaa suorituskykyyn paljon.</span><span class="sxs-lookup"><span data-stu-id="0ec05-132">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="0ec05-133">Esimerkiksi 2 000 työntekijän tietojen lataaminen voi kestää useita tunteja, jos integrointi on käytössä. Jos se ei ole käytössä, aikaa voi kulua alle tunti.</span><span class="sxs-lookup"><span data-stu-id="0ec05-133">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="0ec05-134">Tässä esimerkissä annetut numerot ovat vain esittelytarkoituksia varten.</span><span class="sxs-lookup"><span data-stu-id="0ec05-134">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="0ec05-135">Tietojen tuomiseen kuluvat tarkka aikamäärä voi vaihdella paljon. Se riippuu useista tekijöistä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-135">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="0ec05-136">Integrointitietojen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="0ec05-136">View data integration details</span></span>

<span data-ttu-id="0ec05-137">**Common Data Service** -integroinnin -sivun **Ylläpito**-pikavälilehdessä voit nähdä, miten tietueet linkittyvät yhteen Human Resourcesin ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-137">On the **Administration** FastTab of the **Common Data Service integration** page, you can see how records are linked together between Human Resources and Common Data Service.</span></span>

- <span data-ttu-id="0ec05-138">Jos haluat tarkastella yksikön tietueita, valitse yksikkö **CDS-yksikön nimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-138">To view the records for an entity, select the entity in the **CDS entity name** field.</span></span> <span data-ttu-id="0ec05-139">Ruudukossa näkyvät kaikki valittuun yksikköön linkitetyt tietueet.</span><span class="sxs-lookup"><span data-stu-id="0ec05-139">The grid shows all the records that are linked to the selected entity.</span></span>

<span data-ttu-id="0ec05-140">[![Yksikön tietueen tarkasteleminen](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span><span class="sxs-lookup"><span data-stu-id="0ec05-140">[![Viewing the records for an entity](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)</span></span>

> [!NOTE]
> <span data-ttu-id="0ec05-141">Kaikkia Common Data Service -yksikköjä ei tällä hetkellä ole luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0ec05-141">Not all Common Data Service entities are currently listed.</span></span> <span data-ttu-id="0ec05-142">Ruudukossa näkyvät vain ne yksiköt, jotka tukevat mukautettujen kenttien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-142">Only entities that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="0ec05-143">Uusia yksikköjä tulee saataville jatkuvien Human Resources -julkaisujen myötä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-143">New entities become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="0ec05-144">Ruudukko sisältää seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="0ec05-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="0ec05-145">**CDS-yksikön nimi** – Yksikön nimi Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-145">**CDS entity name** – The name of the entity in Common Data Service.</span></span>
- <span data-ttu-id="0ec05-146">**CDS-yksikköviite** – Tunnus, jota Common Data Service käyttää yksikön tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="0ec05-146">**CDS entity reference** – The identifier that Common Data Service uses to identify a record.</span></span> <span data-ttu-id="0ec05-147">Tämä arvo vastaa Human Resourcesin **RecId**-arvoa.</span><span class="sxs-lookup"><span data-stu-id="0ec05-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="0ec05-148">Löydät tunnuksen, kun avaat Common Data Service -yksikön Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-148">You can find the identifier when you open the Common Data Service entity in Microsoft Excel.</span></span>
- <span data-ttu-id="0ec05-149">**Human Resources -yksikön nimi** – Yksikkö, joka viimeksi synkronoi tietoja Common Data Serviceen.</span><span class="sxs-lookup"><span data-stu-id="0ec05-149">**Human Resources entity name** – The entity that last synced data to Common Data Service.</span></span> <span data-ttu-id="0ec05-150">Yksiköllä voi olla joko Common Data Service -etuliite tai muu etuliite.</span><span class="sxs-lookup"><span data-stu-id="0ec05-150">The entity can have either the Common Data Service prefix or another prefix.</span></span>
- <span data-ttu-id="0ec05-151">**Human Resources -viite** – **RecId**-arvo, joka tietueelle on määritetty Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="0ec05-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="0ec05-152">**Poistettiin CDS:stä** – Arvo, joka ilmaisee, onko tietue poistettu Common Data Servicestä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-152">**Was deleted from CDS** – A value that indicates whether the record was deleted from Common Data Service.</span></span>

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a><span data-ttu-id="0ec05-153">Poista Human Resourcesissa olevan tietueen liitos Common Data Servicestä</span><span class="sxs-lookup"><span data-stu-id="0ec05-153">Remove the association of a record in Human Resources from Common Data Service</span></span>

<span data-ttu-id="0ec05-154">Jos kohtaat ongelmia Human Resourcesin ja Common Data Servicen välisen tietojen synkronoinnin aikana, voit ehkä ratkaista ne tyhjentämällä seurannan ja sallimalla seurantataulukon uudelleensynkronoinnin.</span><span class="sxs-lookup"><span data-stu-id="0ec05-154">If you experience issues during data synchronization between Human Resources and Common Data Service, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="0ec05-155">Jos poistat liitoksen ja muutat tai poistat tietueen Common Data Servicessä, muutoksia ei synkronoida Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="0ec05-155">If you remove the association, and then change or delete a record in Common Data Service, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="0ec05-156">Jos teet muutoksia Human Resourcesissa, uusi seurantatietue luodaan ja päivitetään Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-156">If you make changes in Human Resources, a new tracking record is created, and the record is updated in Common Data Service.</span></span>

- <span data-ttu-id="0ec05-157">Jos haluat poistaa tietueen liitoksen Human Resourcesin ja Common Data Servicen väliltä, valitse yksikkö **CDS-yksikön nimi** -kentästä ja valitse sitten **Tyhjennä seurantatiedot**.</span><span class="sxs-lookup"><span data-stu-id="0ec05-157">To remove the association of a record between Human Resources and Common Data Service, select the entity in the **CDS entity name** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="0ec05-158">[![Seurantatietojen tyhjennys](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="0ec05-158">[![Clearing tracking information](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)</span></span>

<span data-ttu-id="0ec05-159">Katso seuraava menettely, jos haluat suorittaa yksikölle täydellisen synkronoinnin seurannan tyhjentämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="0ec05-159">To run a full synchronization on the entity after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a><span data-ttu-id="0ec05-160">Synkronoi yksikkö Human Resourcesin ja Common Data Servicen välillä</span><span class="sxs-lookup"><span data-stu-id="0ec05-160">Sync an entity between Human Resources and Common Data Service</span></span>

<span data-ttu-id="0ec05-161">Käytä tätä menetelmää seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="0ec05-161">Use this procedure when:</span></span>

- <span data-ttu-id="0ec05-162">Common Data Servicen muutokset näkyvät liian hitaasti henkilöstöhallinnossa.</span><span class="sxs-lookup"><span data-stu-id="0ec05-162">Changes from Common Data Service take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="0ec05-163">Seurantataulukko on päivitettävä seurannan poistamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="0ec05-163">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="0ec05-164">Voit suorittaa täyden synkronoinnin yksikölle henkilöstöhallinnon ja Common Data Servicen välillä:</span><span class="sxs-lookup"><span data-stu-id="0ec05-164">To run a full synchronization on an entity between Human Resources and Common Data Service:</span></span>

1. <span data-ttu-id="0ec05-165">Valitse yksikkö **CDS-yksikkönimi** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="0ec05-165">Select the entity in the **CDS entity name** field.</span></span>

2. <span data-ttu-id="0ec05-166">Valitse **Synkronoi nyt**.</span><span class="sxs-lookup"><span data-stu-id="0ec05-166">Select **Sync now**.</span></span>

<span data-ttu-id="0ec05-167">[![Täyden synkronoinnin suoritus](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="0ec05-167">[![Running a full synchronization](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)</span></span>


