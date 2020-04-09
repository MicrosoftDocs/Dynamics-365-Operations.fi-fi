---
title: Finance and Operations -sovellusten päivityksiin liittyvien ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata Finance and Operations -sovellusten päivityksiin liittyviä ongelmia.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172874"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="ac4b7-103">Finance and Operations -sovellusten päivityksiin liittyvien ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="ac4b7-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="ac4b7-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="ac4b7-105">Erityisesti se tarjoaa tietoja, joiden avulla voit korjata Finance and Operations -sovellusten päivityksiin liittyviä ongelmia.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac4b7-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="ac4b7-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="ac4b7-108">Tietokannan synkronointivirheet</span><span class="sxs-lookup"><span data-stu-id="ac4b7-108">Database synchronization errors</span></span>

<span data-ttu-id="ac4b7-109">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="ac4b7-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="ac4b7-110">Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, kun yrität päivittää Finance and Operations -sovellusta Platform Update 30 -tietojärjestelmään käyttämällä **duowriteprojectconfiguration**-yksikköä.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="ac4b7-111">Korjaa ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="ac4b7-112">Kirjaudu sisään virtuaalikone (VM) Finance and Operationsille -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="ac4b7-113">Avaa Visual Studio ylläpitäjänä ja avaa sovellusobjektipuu (AOT).</span><span class="sxs-lookup"><span data-stu-id="ac4b7-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="ac4b7-114">Etsi **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="ac4b7-115">Napsauta sovellusobjektipuussa hiiren kakkospainikkeella **DualWriteProjectConfiguration**-kohtaa ja valitse **Lisää uuteen projektiin**.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="ac4b7-116">Luo oletusasetuksia käyttävä uusi projekti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="ac4b7-117">Napsauta Ratkaisunhallinnassa **Projektin ominaisuudet** hiiren kakkospainikkeella ja aseta **Synkronoi tietokanta koontiversioon** arvoksi **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="ac4b7-118">Rakenna projekti ja vahvista, että koontiversio onnistuu.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="ac4b7-119">Valitse **Dynamics 365** -valikosta **Synkronoi tietokanta**.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="ac4b7-120">Valitse **Synkronoi**, jos haluat tehdä täyden tietokannan synkronoinnin.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="ac4b7-121">Kun koko tietokannan synkronointi on onnistunut, suorita tietokannan synkronointivaihe uudelleen Microsoft Dynamics Lifecycle Servicesissä (LCS) ja käytä manuaalisia päivityskomentosarjoja, jotta voit jatkaa päivitystä.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="ac4b7-122">Puuttuvien yksikkökenttien ongelma kartoissa</span><span class="sxs-lookup"><span data-stu-id="ac4b7-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="ac4b7-123">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="ac4b7-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="ac4b7-124">**Kaksoiskirjoitussivulla** näyttöön saattaa tulla seuraavan kaltainen virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="ac4b7-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="ac4b7-125">*Puuttuva lähdekenttä \<kentän nimi\> rakenteessa.*</span><span class="sxs-lookup"><span data-stu-id="ac4b7-125">*Missing source field \<field name\> in the schema.*</span></span>

![Esimerkki puuttuva lähdekenttä -virhesanomasta](media/error_missing_field.png)

<span data-ttu-id="ac4b7-127">Voit korjata ongelman varmistamalla ensin seuraavien vaiheiden avulla, että kentät ovat yksikössä.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="ac4b7-128">Kirjaudu sisään virtuaalikone Finance and Operationsille -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="ac4b7-129">Siirry kohtaan **Työtilat \> Tietojen hallinta**, valitse **Kehysparametrit**-ruutu ja päivitä yksiköt valitsemalla **Yksikön asetukset** -välilehdessä **Päivitä yksikköluettelo**.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="ac4b7-130">Siirry kohtaan **Työtilat \> Tietojen hallinta**, valitse **Tietoyksiköt** -välilehti ja varmista, että yksikkö on luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="ac4b7-131">Jos yksikköä ei ole luettelossa, kirjaudu Finance and Operations -sovelluksen VM-kohtaan ja varmista, että yksikkö on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="ac4b7-132">Avaa **Yksikön yhdistämismääritys** -sivu **Kaksoiskirjoitussivulta** Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="ac4b7-133">Valitse **Päivitä yksikköluettelo**, jos haluat täyttää entiteettien yhdistämismääritysten kentät automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="ac4b7-134">Jos ongelma ei vieläkään korjaannu, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ac4b7-135">Näiden vaiheiden avulla voit poistaa yksikön ja lisätä sen sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="ac4b7-136">Voit välttää ongelmat noudattamalla tarkasti ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="ac4b7-137">Siirry Finance and Operations -sovelluksessa kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Tietoyksiköt**--ruutu.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="ac4b7-138">Etsi yksikkö, josta puuttuu kenttä.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-138">Find the entity that is missing the field.</span></span> <span data-ttu-id="ac4b7-139">Kirjoita kohdeyksikön, valmistelutaulun, yksikön nimen ja muiden sarakearvojen huomautus.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-139">Make a note of the target entity, staging table, entity name, and other column values.</span></span>
3. <span data-ttu-id="ac4b7-140">Jos jokin käsittelyryhmä on riippuvainen tästä yksiköstä, tee tarvittavat toimenpiteet käsittelyryhmille ennen yksikön poistamista.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-140">If any of your processing groups depend on this entity, take appropriate action for the processing groups before you delete the entity.</span></span>
4. <span data-ttu-id="ac4b7-141">Poista yksikkö, josta puuttuu kenttä.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-141">Delete the entity that is missing the field.</span></span>
5. <span data-ttu-id="ac4b7-142">Valitse **Uusi** ja lisää yksikkö takaisin.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-142">Select **New**, and add the entity back.</span></span> <span data-ttu-id="ac4b7-143">Määritä arvot, joista teit huomautuksen vaiheessa 2.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-143">Specify the values that you made a note of in step 2.</span></span>
6. <span data-ttu-id="ac4b7-144">Avaa **Yksikön yhdistämismääritys** -sivu **Kaksoiskirjoitussivulta** Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-144">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
7. <span data-ttu-id="ac4b7-145">Valitse **Päivitä yksikköluettelo**, jos haluat täyttää entiteettien yhdistämismääritysten kentät automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ac4b7-145">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>
