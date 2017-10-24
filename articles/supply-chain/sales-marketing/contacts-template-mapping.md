---
title: "Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin"
description: "Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin yhteyshenkilöt (yhteyshenkilöt) ja yhteyshenkilöt (asiakkaat) synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="b0e1e-103">Salesin yhteyshenkilöiden synkronointi Finance and Operationsin yhteyshenkilöihin tai asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="b0e1e-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b0e1e-104">Tutustu [Dynamics 365:n tietojen integrointiin](/common-data-service/entity-reference/dynamics-365-integration), ennen kuin käytät ratkaisua, jolla prospekti muuttuu kannattavaksi asiakkaaksi.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="b0e1e-105">Ohjeaiheessa käsitellään malleja ja tehtäviä, joilla Microsoft Dynamics 365 for Salesin (Sales) Yhteyshenkilö (yhteyshenkilöt) -yksiköt ja yhteyshenkilöt (asiakkaat) synkronoidaan Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="b0e1e-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b0e1e-106">Mallit ja tehtävät</span><span class="sxs-lookup"><span data-stu-id="b0e1e-106">Templates and tasks</span></span>

<span data-ttu-id="b0e1e-107">Seuraavia malleja ja niiden taustalla olevia tehtäviä käytetään synkronoimaan Salesin yhteyshenkilö (yhteyshenkilöt) Finance and Operationsin yhteyshenkilöön (asiakkaat):</span><span class="sxs-lookup"><span data-stu-id="b0e1e-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="b0e1e-108">**Mallien nimi:**</span><span class="sxs-lookup"><span data-stu-id="b0e1e-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="b0e1e-109">Yhteyshenkilöt (Salesista Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="b0e1e-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="b0e1e-110">Yhteyshenkilöstä asiakkaaseen (Salesista Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="b0e1e-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="b0e1e-111">**Projektin tehtävien nimet:**</span><span class="sxs-lookup"><span data-stu-id="b0e1e-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="b0e1e-112">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="b0e1e-112">Contacts</span></span>
    - <span data-ttu-id="b0e1e-113">Yhteyshenkilö asiakkaaseen</span><span class="sxs-lookup"><span data-stu-id="b0e1e-113">ContactToCustomer</span></span>

<span data-ttu-id="b0e1e-114">Seuraava synkronointitehtävä on tehtävä ennen yhteyshenkilön synkronointia: tilit (Salesista Fin and Opsiin)</span><span class="sxs-lookup"><span data-stu-id="b0e1e-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="b0e1e-115">Yksikköjoukot</span><span class="sxs-lookup"><span data-stu-id="b0e1e-115">Entity sets</span></span>

| <span data-ttu-id="b0e1e-116">Myynti</span><span class="sxs-lookup"><span data-stu-id="b0e1e-116">Sales</span></span>    | <span data-ttu-id="b0e1e-117">CDS</span><span class="sxs-lookup"><span data-stu-id="b0e1e-117">CDS</span></span>     | <span data-ttu-id="b0e1e-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b0e1e-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="b0e1e-119">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="b0e1e-119">Contacts</span></span> | <span data-ttu-id="b0e1e-120">Kontakti</span><span class="sxs-lookup"><span data-stu-id="b0e1e-120">Contact</span></span> | <span data-ttu-id="b0e1e-121">CDS-yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="b0e1e-121">CDS Contacts</span></span>           |
| <span data-ttu-id="b0e1e-122">Yhteyshenkilöt</span><span class="sxs-lookup"><span data-stu-id="b0e1e-122">Contacts</span></span> | <span data-ttu-id="b0e1e-123">Tili</span><span class="sxs-lookup"><span data-stu-id="b0e1e-123">Account</span></span> | <span data-ttu-id="b0e1e-124">Asiakkaat V2</span><span class="sxs-lookup"><span data-stu-id="b0e1e-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="b0e1e-125">Yksikön työnkulku</span><span class="sxs-lookup"><span data-stu-id="b0e1e-125">Entity flow</span></span>

<span data-ttu-id="b0e1e-126">Yhteyshenkilöitä hallitaan Salesissa ja ne synkronoidaan Common Data Serviceen (CDS) ja Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="b0e1e-127">Salesin yhteyshenkilöstä voi tulla CDS:n ja Finance and Operationsin yhteyshenkilö.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="b0e1e-128">Vaihtoehtoisesti siitä voi olla CDS:n tili ja Finance and Operationsin asiakas.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-129">Järjestelmä määrittää seuraavien Salesin yhteyshenkilöiden ominaisuuksien perusteella, poimitaanko yhteyshenkilö Salesista CDS:ään ja Finance and Operationsiin synkronoitavaksi (kuten Yhteyshenkilöt Salesissa &gt; Yhteyshenkilö CDS:ssä &gt; Yhteyshenkilöt Finance and Operationsissa):</span><span class="sxs-lookup"><span data-stu-id="b0e1e-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="b0e1e-130">**Synkronoi tili CDS:ssä ja asiakas Finance and Operationsissa:** yhteyshenkilöt, kun **On aktiivinen asiakas** -asetuksena on **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="b0e1e-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="b0e1e-131">**Synkronoi yhteyshenkilö CDS:ssä ja yhteyshenkilö Finance and Operationsissa:** Yhteyshenkilöt, kun **On aktiivinen asiakas** -asetuksena on **Ei** ja **Yritys** (päätili tai asiakas) viittaa tiliin (eikä yhteyshenkilöön)</span><span class="sxs-lookup"><span data-stu-id="b0e1e-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b0e1e-132">Salesin ratkaisu prospektista käteiseksi</span><span class="sxs-lookup"><span data-stu-id="b0e1e-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="b0e1e-133">Uusi **On aktiivinen asiakas** -kenttä on lisätty yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="b0e1e-134">Tämän kentän avulla erotetaan yhteyshenkilöt, joilla on myyntitehtävä, ja ne, joilla ei sitä ole.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="b0e1e-135">**On aktiivinen asiakas** -asetuksena on **Kyllä** vain asiakkaille, joilla on liittyviä tarjouksia, tilauksia tai laskuja.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="b0e1e-136">Vain nämä yhteyshenkilöt synkronoidaan Finance and Operationsiin asiakkaina.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="b0e1e-137">Uusi **IsCompanyAnAccount**-kenttä on lisätty yhteyshenkilöön.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="b0e1e-138">Tämä kenttä osoittaa, onko yhteyshenkilö linkitetty **Tili**-tyypin yritykseen (päätili tai yhteyshenkilö).</span><span class="sxs-lookup"><span data-stu-id="b0e1e-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="b0e1e-139">Näillä tiedoilla tunnistetaan yhteystiedot, jotka on synkronoitava Finance and Operationsiin yhteyshenkilöinä.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="b0e1e-140">Uusi **Yhteyshenkilön numero** -kenttä on lisätty yhteyshenkilöön takaamaan integroinnin luonnollinen ja yksilöllinen avain.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="b0e1e-141">Kun uusi yhteyshenkilö luodaan, **Yhteyshenkilön numero** -arvo luodaan automaattisesti numerosarjan avulla.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="b0e1e-142">Arvossa on ensimmäisenä **CON**, sitten kasvava numerosarja ja lopuksi kuusimerkkinen loppuliite.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="b0e1e-143">Esimerkki: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="b0e1e-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="b0e1e-144">Kun Salesin integrointiratkaisu lisätään Salesiin, päivitetty komentosarja määrittää aiemmin luotujen yhteyshenkilöiden **Yhteyshenkilön numero** -kentän käyttämällä edellä mainittua numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="b0e1e-145">Päivityskomentosarja määrittää myös **On aktiivinen asiakas** -kentän arvoksi **Kyllä** kaikille yhteyshenkilöille, joilla on myyntitehtävä.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="b0e1e-146">Finance and Operationsissa</span><span class="sxs-lookup"><span data-stu-id="b0e1e-146">In Finance and Operations</span></span> 

<span data-ttu-id="b0e1e-147">Yhteyshenkilöt merkitään **IsContactPersonExternallyMaintained**-ominaisuudella.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="b0e1e-148">Tämä ominaisuus osoittaa, että kyseistä yhteyshenkilöä ylläpidetään ulkoisesti.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="b0e1e-149">Tässä tapauksessa ulkoisesti ylläpidettyjä yhteyshenkilöitä ylläpidetään Salesissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b0e1e-150">Edellytykset ja yhdistämismääritykset</span><span class="sxs-lookup"><span data-stu-id="b0e1e-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="b0e1e-151">Yhteyshenkilöstä yhteyshenkilöön</span><span class="sxs-lookup"><span data-stu-id="b0e1e-151">Contact to Contact</span></span>

- <span data-ttu-id="b0e1e-152">Päivitä **CDS-organisaation tunnus** **Lähde &gt; CDS** -yhdistämismääritykseksi.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="b0e1e-153">Mallin **Organization_OrganizationId [Organisaation tunnus]** oletusarvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="b0e1e-154">Mallin **PrimaryAccount_Organization_OrganizationId [Organisaation tunnus]** oletusarvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="b0e1e-155">**Osoitteen maa- tai aluekoodi** on pakollinen Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-156">Voit estää synkronointivirheet määrittämällä oletusarvon **CDS &gt; Operations** -yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="b0e1e-157">Oletusarvo käytetään, jos kenttä on tyhjä Salesissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="b0e1e-158">Mallin **PrimaryAddressCountryRegionISOCode** oletusarvo on **USA**.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="b0e1e-159">Varmista, että seuraavassa Finance and Operationsin kentässä on arvo.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-160">Jos tietoja ei tarvita Finance and Operationsissa, voit poistaa yhdistämismäärityksen **CDS &gt; Kohde** -määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="b0e1e-161">**Finance and Operationsin kentän nimi:** päätös</span><span class="sxs-lookup"><span data-stu-id="b0e1e-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="b0e1e-162">**Yhdistämismääritys:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="b0e1e-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="b0e1e-163">Yhteishenkilöstä asiakkaaseen</span><span class="sxs-lookup"><span data-stu-id="b0e1e-163">Contact to Customer</span></span>

- <span data-ttu-id="b0e1e-164">Päivitä **CDS-organisaation tunnus** **Lähde &gt; CDS** -yhdistämismääritykseksi.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="b0e1e-165">Mallin **Organization_OrganizationId [Organisaation tunnus]** oletusarvo on **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="b0e1e-166">**Osoitteen maa- tai aluekoodi** on pakollinen Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-167">Voit estää synkronointivirheet määrittämällä oletusarvon **CDS &gt; Kohde** -yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="b0e1e-168">Oletusarvo käytetään, jos kenttä on tyhjä Salesissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="b0e1e-169">Mallin **PrimaryAddressCountryRegionISOCode** oletusarvo on **USA**.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="b0e1e-170">**CustomerGroup** tarvitaan Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-171">Voit estää synkronointivirheet määrittämällä oletusarvon **CDS &gt; Kohde** -yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="b0e1e-172">Oletusarvo käytetään, jos kenttä on tyhjä Salesissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="b0e1e-173">Mallin **CustomerGroupId** oletusarvo on **10**.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="b0e1e-174">Kun seuraavat yhdistämismääritykset lisätään kohdasta **CDS &gt; Kohde**, Finance and Operationsissa tarvitaan vähemmän manuaalisia päivityksiä.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-175">Voit käyttää oletusarvoa tai arvomääritystä, kuten **Maa tai alue** tai **Paikkakunta**.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="b0e1e-176">**SiteId** – oletustoimipaikka voidaan määrittää myös Finance and Operationsin tuotteissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-177">Toimipaikka on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-178">Mallin **SiteId** arvoa ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="b0e1e-179">**WarehouseId** – oletusvarasto voidaan määrittää myös Finance and Operationsin tuotteissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-180">Varasto on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-181">Mallin **WarehouseId** arvoa ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="b0e1e-182">**LanguageId** – Kieli on pakollinen, jotta tarjoukset ja myyntitilaukset voidaan luoda Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="b0e1e-183">Mallin **LanguageId** oletusarvo on **en-us**.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="b0e1e-184">Mallin yhdistäminen tietojen integrointiohjelmassa</span><span class="sxs-lookup"><span data-stu-id="b0e1e-184">Template mapping in data integrator</span></span>

<span data-ttu-id="b0e1e-185">Seuraavissa kuvissa on esimerkki mallin yhdistämisestä tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="b0e1e-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="b0e1e-186">Yhteyshenkilöstä yhteyshenkilöön</span><span class="sxs-lookup"><span data-stu-id="b0e1e-186">Contact to Contact</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-template-mapping-data-integrator-1.png)

![Mallin yhdistäminen yhteyshenkilöitä varten tietojen integrointiohjelmassa](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="b0e1e-189">Yhteishenkilöstä asiakkaaseen</span><span class="sxs-lookup"><span data-stu-id="b0e1e-189">Contact to Customer</span></span>

![Mallin yhdistäminen tietojen integrointiohjelmassa](./media/contacts-template-mapping-data-integrator-3.png)

![Mallin yhdistäminen yhteyshenkilöitä varten tietojen integrointiohjelmassa](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="b0e1e-192">Liittyvät aiheet</span><span class="sxs-lookup"><span data-stu-id="b0e1e-192">Related topics</span></span>

[<span data-ttu-id="b0e1e-193">Finance and Operationsin tuotteiden synkronointi Salesin tuotteisiin</span><span class="sxs-lookup"><span data-stu-id="b0e1e-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="b0e1e-194">Salesin asiakkaiden synkronointi Finance and Operationsin asiakkaisiin</span><span class="sxs-lookup"><span data-stu-id="b0e1e-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="b0e1e-195">Myyntitarjouksien otsikoiden ja rivien synkronointi Salesista Finance and Operationsiin</span><span class="sxs-lookup"><span data-stu-id="b0e1e-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="b0e1e-196">Myyntitilauksien otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="b0e1e-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="b0e1e-197">Myyntilaskujen otsikoiden ja rivien synkronointi Finance and Operationsista Salesiin</span><span class="sxs-lookup"><span data-stu-id="b0e1e-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

