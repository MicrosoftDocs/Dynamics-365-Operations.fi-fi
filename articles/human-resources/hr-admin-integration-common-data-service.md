---
title: Määritä Dataverse -integraatio
description: Voit ottaa integroinnin Microsoft Dataversen ja Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä. Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida taulukon uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
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
ms.openlocfilehash: 38c42469e62bf5457d0281540325a6c56a5f930f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112418"
---
# <a name="configure-dataverse-integration"></a><span data-ttu-id="d627c-104">Määritä Dataverse -integraatio</span><span class="sxs-lookup"><span data-stu-id="d627c-104">Configure Dataverse integration</span></span>

<span data-ttu-id="d627c-105">Voit ottaa integroinnin Microsoft Dataversen ja Dynamics 365 Human Resourcesin välillä käyttöön tai poistaa sen käytöstä.</span><span class="sxs-lookup"><span data-stu-id="d627c-105">You can turn integration between Microsoft Dataverse and Dynamics 365 Human Resources on or off.</span></span> <span data-ttu-id="d627c-106">Voit myös tarkastella synkronointitietoja, tyhjentää seurantatiedot ja synkronoida taulukon uudelleen, mikä helpottaa näiden kahden ympäristön välisten tieto-ongelmien vianmääritystä.</span><span class="sxs-lookup"><span data-stu-id="d627c-106">You can also view the synchronization details, clear tracking data, and resync a table to help troubleshoot data issues between the two environments.</span></span>

> [!NOTE]
> <span data-ttu-id="d627c-107">Lisätietoja Dataversesta (aiemmin Common Data Service) ja terminologiapäivityksistä on kohdassa [Mikä on Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="d627c-107">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="d627c-108">Kun poistat integroinnin käytöstä, käyttäjät voivat tehdä muutoksia Human Resourcesissa tai Dataversessä, mutta näitä muutoksia ei synkronoida näiden kahden ympäristön välillä.</span><span class="sxs-lookup"><span data-stu-id="d627c-108">When you turn off integration, users can make changes in Human Resources or Dataverse, but those changes aren't synced between the two environments.</span></span>

<span data-ttu-id="d627c-109">Oletusarvoisesti Human Resourcesin ja Dataversen tietojen integrointi on poistettu käytöstä.</span><span class="sxs-lookup"><span data-stu-id="d627c-109">By default, integration between Human Resources and Dataverse is turned off.</span></span>

<span data-ttu-id="d627c-110">Integrointi voi kannattaa poistaa käytöstä seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="d627c-110">You might want to turn off integration in these situations:</span></span>

- <span data-ttu-id="d627c-111">Olet täyttämässä dataa tietojen hallintakehyksen kautta ja sinun on tuotava tiedot useita kertoja, jotta saat ne oikeaan tilaan.</span><span class="sxs-lookup"><span data-stu-id="d627c-111">You're filling in data through the Data Management Framework and must import the data multiple times to get it into a correct state.</span></span>

- <span data-ttu-id="d627c-112">Tietoihin liittyy ongelmia joko Human Resourcesissa tai Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="d627c-112">There are issues with data in either Human Resources or Dataverse.</span></span> <span data-ttu-id="d627c-113">Jos poistat integroinnin käytöstä, voit poistaa tietueen yhdestä ympäristöstä poistamatta sitä toisessa ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="d627c-113">If you turn off integration, you can delete a record in one environment without deleting it in the other.</span></span> <span data-ttu-id="d627c-114">Kun otat integroinnin takaisin käyttöön, sen ympäristön tietue, josta sitä ei poistettu, synkronoidaan siihen ympäristöön, josta se poistettiin.</span><span class="sxs-lookup"><span data-stu-id="d627c-114">When you turn integration back on, the record in the environment where it wasn't deleted sync to the environment where it was deleted.</span></span> <span data-ttu-id="d627c-115">Synkronointi alkaa seuraavan kerran, kun **Dataversen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="d627c-115">Synchronization begins the next time the **Dataverse integration missed request sync** batch job runs.</span></span>

> [!WARNING]
> <span data-ttu-id="d627c-116">Kun poistat tietojen integroinnin käytöstä, varmista, ettet muokkaa samaa tietuetta molemmissa ympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="d627c-116">When you turn off data integration, make sure that you don't edit the same record in both environments.</span></span> <span data-ttu-id="d627c-117">Kun otat integroinnin takaisin käyttöön, viimeksi muokattu tietue synkronoidaan.</span><span class="sxs-lookup"><span data-stu-id="d627c-117">When you turn integration back on, the record that you last edited will be synced.</span></span> <span data-ttu-id="d627c-118">Näin ollen, jos et tehnyt samoja muutoksia tietueeseen molemmissa ympäristöissä, tietoja voidaan menettää.</span><span class="sxs-lookup"><span data-stu-id="d627c-118">Therefore, if you didn't make the same changes to the record in both environments, data loss can occur.</span></span>

## <a name="access-the-dataverse-integration-page"></a><span data-ttu-id="d627c-119">Dataversen integrointisivun käyttö</span><span class="sxs-lookup"><span data-stu-id="d627c-119">Access the Dataverse integration page</span></span>

1. <span data-ttu-id="d627c-120">Valitse siinä Human Resources -esiintymässä, jossa haluat tarkastella tai määrittää Dataversen kanssa integroinnin asetuksia, **Järjestelmän hallinta** -ruutu.</span><span class="sxs-lookup"><span data-stu-id="d627c-120">In the Human Resources instance where you want to view or configure settings for the integration with Dataverse, select the **System administration** tile.</span></span>

    <span data-ttu-id="d627c-121">[![Järjestelmän hallinta -ruutu](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span><span class="sxs-lookup"><span data-stu-id="d627c-121">[![System administration tile](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)</span></span>

2. <span data-ttu-id="d627c-122">Valitse **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="d627c-122">Select the **Links** tab.</span></span>

    <span data-ttu-id="d627c-123">[![Linkit-välilehti](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span><span class="sxs-lookup"><span data-stu-id="d627c-123">[![Links tab](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)</span></span>

3. <span data-ttu-id="d627c-124">Valitse **Integroinnit**-kohdassa **Dataversen määritys**.</span><span class="sxs-lookup"><span data-stu-id="d627c-124">Under **Integrations**, select **Dataverse configuration**.</span></span>

    <span data-ttu-id="d627c-125">[![Dataversen määrityslinkki](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span><span class="sxs-lookup"><span data-stu-id="d627c-125">[![Dataverse configuration link](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)</span></span>

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a><span data-ttu-id="d627c-126">Human Resourcesin ja Dataversen tietojen integroinnin käyttöönotto ja käytöstä poistaminen</span><span class="sxs-lookup"><span data-stu-id="d627c-126">Turn data integration between Human Resources and Dataverse on or off</span></span>

- <span data-ttu-id="d627c-127">Ota integrointi käyttöön asettamalla **Ota Dataverse -integrointi käyttöön** -asetuksen arvoksi **Kyllä** **Microsoft Dataverse -integrointi** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="d627c-127">To turn on integration, set the **Enable Dataverse integration** option to **Yes** on the **Microsoft Dataverse integration** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d627c-128">Kun otat integroinnin käyttöön, tiedot synkronoidaan seuraavan kerran, kun **Dataversen integroinnin toteutumattoman pyynnön synkronointi** -erätyö suoritetaan seuraavan kerran.</span><span class="sxs-lookup"><span data-stu-id="d627c-128">When you turn on integration, data will be synced the next time that the **Dataverse integration missed request sync** batch job runs.</span></span> <span data-ttu-id="d627c-129">Kaikkien tietojen pitäisi olla käytettävissä, kun erätyö on valmis.</span><span class="sxs-lookup"><span data-stu-id="d627c-129">All data should be available after the batch job is completed.</span></span>

- <span data-ttu-id="d627c-130">Voit poistaa integroinnin käytöstä määrittämällä asetukseksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="d627c-130">To turn off integration, set the option to **No**.</span></span>

<span data-ttu-id="d627c-131">[![Dataverse -integroinnin käyttöönotto tai käytöstä poisto](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span><span class="sxs-lookup"><span data-stu-id="d627c-131">[![Turning the Dataverse integration on or off](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)</span></span>

> [!WARNING]
> <span data-ttu-id="d627c-132">On suositeltavaa, että Dataverse -integrointi poistetaan käytöstä, kun tiedonsiirtotehtäviä suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="d627c-132">We strongly recommend turning off Dataverse integration while performing data migration tasks.</span></span> <span data-ttu-id="d627c-133">Suurten tietomäärien lataaminen voi vaikuttaa suorituskykyyn paljon.</span><span class="sxs-lookup"><span data-stu-id="d627c-133">Large data uploads can significantly impact performance.</span></span> <span data-ttu-id="d627c-134">Esimerkiksi 2 000 työntekijän tietojen lataaminen voi kestää useita tunteja, jos integrointi on käytössä. Jos se ei ole käytössä, aikaa voi kulua alle tunti.</span><span class="sxs-lookup"><span data-stu-id="d627c-134">For example, uploading 2000 workers can take several hours when integration is enabled, and less than one hour when it's disabled.</span></span> <span data-ttu-id="d627c-135">Tässä esimerkissä annetut numerot ovat vain esittelytarkoituksia varten.</span><span class="sxs-lookup"><span data-stu-id="d627c-135">The numbers provided in this example are for demonstration purposes only.</span></span> <span data-ttu-id="d627c-136">Tietojen tuomiseen kuluvat tarkka aikamäärä voi vaihdella paljon. Se riippuu useista tekijöistä.</span><span class="sxs-lookup"><span data-stu-id="d627c-136">The exact amount of time it takes to import records can vary greatly based on many factors.</span></span>

## <a name="view-data-integration-details"></a><span data-ttu-id="d627c-137">Integrointitietojen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="d627c-137">View data integration details</span></span>

<span data-ttu-id="d627c-138">**Microsoft Dataverse** -integroinnin -sivun **Ylläpito**-pikavälilehdessä voit nähdä, miten rivit linkittyvät yhteen Human Resourcesin ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="d627c-138">On the **Administration** FastTab of the **Microsoft Dataverse integration** page, you can see how rows are linked together between Human Resources and Dataverse.</span></span>

- <span data-ttu-id="d627c-139">Voit tarkastella taulun rivejä valitsemalla taulun **Dataverse-taulu** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="d627c-139">To view the rows for a table, select the table in the **Dataverse table** field.</span></span> <span data-ttu-id="d627c-140">Ruudukossa näkyvät kaikki valittuun taulukkoon linkitetyt rivit.</span><span class="sxs-lookup"><span data-stu-id="d627c-140">The grid shows all the rows that are linked to the selected table.</span></span>

> [!NOTE]
> <span data-ttu-id="d627c-141">Kaikkia Dataverse-taulukoita ei tällä hetkellä ole luettelossa.</span><span class="sxs-lookup"><span data-stu-id="d627c-141">Not all Dataverse tables are currently listed.</span></span> <span data-ttu-id="d627c-142">Ruudukossa näkyvät vain ne taulukot, jotka tukevat mukautettujen kenttien käyttöä.</span><span class="sxs-lookup"><span data-stu-id="d627c-142">Only tables that support the use of custom fields appear in the grid.</span></span> <span data-ttu-id="d627c-143">Uusia taulukoita tulee saataville jatkuvien Human Resources -julkaisujen myötä.</span><span class="sxs-lookup"><span data-stu-id="d627c-143">New tables become available through continuous releases of Human Resources.</span></span>

<span data-ttu-id="d627c-144">Ruudukko sisältää seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="d627c-144">The grid includes the following fields:</span></span>

- <span data-ttu-id="d627c-145">**Dataverse-taulukko** – Dataverse-taulukon nimi.</span><span class="sxs-lookup"><span data-stu-id="d627c-145">**Dataverse table** – The name of the table in Dataverse.</span></span>
- <span data-ttu-id="d627c-146">**Dataverse-taulukkoviite** – Tunnus, jota Dataverse käyttää tietueen tunnistamiseen.</span><span class="sxs-lookup"><span data-stu-id="d627c-146">**Dataverse table reference** – The identifier that Dataverse uses to identify a record.</span></span> <span data-ttu-id="d627c-147">Tämä arvo vastaa Human Resourcesin **RecId**-arvoa.</span><span class="sxs-lookup"><span data-stu-id="d627c-147">This value is equivalent to a Human Resources **RecId** value.</span></span> <span data-ttu-id="d627c-148">Löydät tunnuksen, kun avaat Dataverse-taulukon Microsoft Excelissä.</span><span class="sxs-lookup"><span data-stu-id="d627c-148">You can find the identifier when you open the Dataverse table in Microsoft Excel.</span></span>
- <span data-ttu-id="d627c-149">**Human Resources -yksikön nimi** – Human Resources -yksikkö, joka viimeksi synkronoi tietoja Dataverseen.</span><span class="sxs-lookup"><span data-stu-id="d627c-149">**Human Resources entity name** – The Human Resources entity that last synced data to Dataverse.</span></span> <span data-ttu-id="d627c-150">Yksiköllä voi olla joko Dataverse -etuliite tai muu etuliite.</span><span class="sxs-lookup"><span data-stu-id="d627c-150">The entity can have either the Dataverse prefix or another prefix.</span></span>
- <span data-ttu-id="d627c-151">**Human Resources -viite** – **RecId**-arvo, joka tietueelle on määritetty Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="d627c-151">**Human Resources reference** – The **RecId** value that is associated with the record in Human Resources.</span></span>
- <span data-ttu-id="d627c-152">**Poistettu Dataversestä** – Arvo, joka ilmaisee, onko rivi poistettu Dataversestä.</span><span class="sxs-lookup"><span data-stu-id="d627c-152">**Deleted from Dataverse** – A value that indicates whether the row was deleted from Dataverse.</span></span>

> [!NOTE]
> <span data-ttu-id="d627c-153">Human Resources -tietueet vastaavat rivejä Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="d627c-153">Records in Human Resources correspond to rows in Dataverse.</span></span>

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a><span data-ttu-id="d627c-154">Poista Human Resources -tietueen liitos Dataverse-rivistä</span><span class="sxs-lookup"><span data-stu-id="d627c-154">Remove the association of a Human Resources record from a Dataverse row</span></span>

<span data-ttu-id="d627c-155">Jos kohtaat ongelmia Human Resourcesin ja Dataversen välisen tietojen synkronoinnin aikana, voit ehkä ratkaista ne tyhjentämällä seurannan ja sallimalla seurantataulukon uudelleensynkronoinnin.</span><span class="sxs-lookup"><span data-stu-id="d627c-155">If you experience issues during data synchronization between Human Resources and Dataverse, you might be able to resolve them by clearing the tracking and letting the tracking table be resynced.</span></span> <span data-ttu-id="d627c-156">Jos poistat liitoksen ja muutat tai poistat rivin Dataversessä, muutoksia ei synkronoida Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="d627c-156">If you remove the association, and then change or delete a row in Dataverse, the changes won't be synced to Human Resources.</span></span> <span data-ttu-id="d627c-157">Jos teet muutoksia Human Resourcesissa, uusi seurantatietue luodaan ja rivi päivitetään Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="d627c-157">If you make changes in Human Resources, a new tracking record is created, and the row is updated in Dataverse.</span></span>

- <span data-ttu-id="d627c-158">Jos haluat poistaa liitoksen Human Resources -tietueen ja Dataverse-rivin väliltä, valitse taulukko **Dataverse-taulukko** -kentästä ja valitse sitten **Tyhjennä seurantatiedot**.</span><span class="sxs-lookup"><span data-stu-id="d627c-158">To remove the association of a Human Resources record and a Dataverse row, select the table in the **Dataverse table** field, and then select **Clear tracking information**.</span></span>

<span data-ttu-id="d627c-159">[![Seurantatietojen tyhjennys](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span><span class="sxs-lookup"><span data-stu-id="d627c-159">[![Clearing tracking information](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)</span></span>

<span data-ttu-id="d627c-160">Katso seuraava menettely, jos haluat suorittaa taulukolle täydellisen synkronoinnin seurannan tyhjentämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="d627c-160">To run a full synchronization on the table after you clear the tracking, see the next procedure.</span></span>

## <a name="sync-a-table-between-human-resources-and-dataverse"></a><span data-ttu-id="d627c-161">Synkronoi taulukko Human Resourcesin ja Dataversen välillä</span><span class="sxs-lookup"><span data-stu-id="d627c-161">Sync a table between Human Resources and Dataverse</span></span>

<span data-ttu-id="d627c-162">Käytä tätä menetelmää seuraavissa tilanteissa:</span><span class="sxs-lookup"><span data-stu-id="d627c-162">Use this procedure when:</span></span>

- <span data-ttu-id="d627c-163">Dataversen muutokset näkyvät liian hitaasti henkilöstöhallinnossa.</span><span class="sxs-lookup"><span data-stu-id="d627c-163">Changes from Dataverse take too long to appear in Human Resources.</span></span>

- <span data-ttu-id="d627c-164">Seurantataulukko on päivitettävä seurannan poistamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="d627c-164">You must refresh the tracking table after clearing the tracking.</span></span>

<span data-ttu-id="d627c-165">Voit suorittaa täyden synkronoinnin taulukolle Human Resourcesin ja Dataversen välillä:</span><span class="sxs-lookup"><span data-stu-id="d627c-165">To run a full synchronization on a table between Human Resources and Dataverse:</span></span>

1. <span data-ttu-id="d627c-166">Valitse taulukko **Dataverse-taulukko** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="d627c-166">Select the table in the **Dataverse table** field.</span></span>

2. <span data-ttu-id="d627c-167">Valitse **Synkronoi nyt**.</span><span class="sxs-lookup"><span data-stu-id="d627c-167">Select **Sync now**.</span></span>

<span data-ttu-id="d627c-168">[![Täyden synkronoinnin suoritus](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span><span class="sxs-lookup"><span data-stu-id="d627c-168">[![Running a full synchronization](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="d627c-169">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="d627c-169">See also</span></span>

[<span data-ttu-id="d627c-170">Dataverse-taulut</span><span class="sxs-lookup"><span data-stu-id="d627c-170">Dataverse tables</span></span>](hr-developer-entities.md)<br>
[<span data-ttu-id="d627c-171">Määritä Dataverse -virtuaalitaulukot</span><span class="sxs-lookup"><span data-stu-id="d627c-171">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="d627c-172">Human Resourcesin virtuaalitaulut – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="d627c-172">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="d627c-173">Mikä on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="d627c-173">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="d627c-174">Terminologiapäivitykset</span><span class="sxs-lookup"><span data-stu-id="d627c-174">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
