---
title: Finance and Operations -sovellusten päivitysten ongelmien vianmääritys
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata Finance and Operations -sovellusten päivityksiin liittyviä ongelmia.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: ae54ffc9f7a97793dfaddc29f5aae66e5b06c931
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561199"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="b0236-103">Finance and Operations -sovellusten päivitysten ongelmien vianmääritys</span><span class="sxs-lookup"><span data-stu-id="b0236-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="b0236-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä.</span><span class="sxs-lookup"><span data-stu-id="b0236-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="b0236-105">Erityisesti se tarjoaa tietoja, joiden avulla voit korjata Finance and Operations -sovellusten päivityksiin liittyviä ongelmia.</span><span class="sxs-lookup"><span data-stu-id="b0236-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0236-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="b0236-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b0236-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="b0236-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="b0236-108">Tietokannan synkronointivirheet</span><span class="sxs-lookup"><span data-stu-id="b0236-108">Database synchronization errors</span></span>

<span data-ttu-id="b0236-109">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="b0236-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b0236-110">Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, kun yrität päivittää Finance and Operations -sovellusta Platform Update 30 -tietojärjestelmään käyttämällä **duowriteprojectconfiguration**-taulukkoa.</span><span class="sxs-lookup"><span data-stu-id="b0236-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="b0236-111">Korjaa ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="b0236-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="b0236-112">Kirjaudu sisään virtuaalikone (VM) Finance and Operationsille -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="b0236-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="b0236-113">Avaa Visual Studio ylläpitäjänä ja avaa sovellusobjektipuu (AOT).</span><span class="sxs-lookup"><span data-stu-id="b0236-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="b0236-114">Etsi **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="b0236-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="b0236-115">Napsauta sovellusobjektipuussa hiiren kakkospainikkeella **DualWriteProjectConfiguration**-kohtaa ja valitse **Lisää uuteen projektiin**.</span><span class="sxs-lookup"><span data-stu-id="b0236-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="b0236-116">Luo oletusasetuksia käyttävä uusi projekti valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b0236-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="b0236-117">Napsauta Ratkaisunhallinnassa **Projektin ominaisuudet** hiiren kakkospainikkeella ja aseta **Synkronoi tietokanta koontiversioon** arvoksi **Tosi**.</span><span class="sxs-lookup"><span data-stu-id="b0236-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="b0236-118">Rakenna projekti ja vahvista, että koontiversio onnistuu.</span><span class="sxs-lookup"><span data-stu-id="b0236-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="b0236-119">Valitse **Dynamics 365** -valikosta **Synkronoi tietokanta**.</span><span class="sxs-lookup"><span data-stu-id="b0236-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="b0236-120">Valitse **Synkronoi**, jos haluat tehdä täyden tietokannan synkronoinnin.</span><span class="sxs-lookup"><span data-stu-id="b0236-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="b0236-121">Kun koko tietokannan synkronointi on onnistunut, suorita tietokannan synkronointivaihe uudelleen Microsoft Dynamics Lifecycle Servicesissä (LCS) ja käytä manuaalisia päivityskomentosarjoja, jotta voit jatkaa päivitystä.</span><span class="sxs-lookup"><span data-stu-id="b0236-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="b0236-122">Taulukon puuttuvien sarakkeiden ongelmia yhdistämismäärityksissä</span><span class="sxs-lookup"><span data-stu-id="b0236-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="b0236-123">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="b0236-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b0236-124">**Kaksoiskirjoitussivulla** näyttöön saattaa tulla seuraavan kaltainen virhesanoma:</span><span class="sxs-lookup"><span data-stu-id="b0236-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="b0236-125">*Rakenteesta puuttuu lähdekenttä \<field name\>.*</span><span class="sxs-lookup"><span data-stu-id="b0236-125">*Missing source field \<field name\> in the schema.*</span></span>

![Esimerkki puuttuvan lähdesarakkeen virhesanomasta](media/error_missing_field.png)

<span data-ttu-id="b0236-127">Voit korjata ongelman varmistamalla ensin seuraavien vaiheiden avulla, että sarakkeet ovat taulukossa.</span><span class="sxs-lookup"><span data-stu-id="b0236-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="b0236-128">Kirjaudu sisään virtuaalikone Finance and Operationsille -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="b0236-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="b0236-129">Valitse **Työtilat \> Tietojen hallinta**, valitse **Kehysparametrit**-ruutu ja päivitä taulut valitsemalla **Taulun asetukset** -välilehdessä **Päivitä taululuettelo**.</span><span class="sxs-lookup"><span data-stu-id="b0236-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="b0236-130">Valitse **Työtilat \> Tietojen hallinta**, valitse **Tietotaulut** -välilehti ja varmista, että taulu on luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b0236-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="b0236-131">Jos taulua ei ole luettelossa, kirjaudu Finance and Operations -sovelluksen VM-kohtaan ja varmista, että taulu on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="b0236-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="b0236-132">Avaa **Taulujen yhdistämismääritys** -sivu **Kaksoiskirjoitussivulta** Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="b0236-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="b0236-133">Valitse **Päivitä taululuettelo**, jos haluat täyttää taulujen yhdistämismääritysten sarakkeet automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="b0236-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="b0236-134">Jos ongelma ei vieläkään korjaannu, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="b0236-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0236-135">Näiden vaiheiden avulla voit poistaa taulun ja lisätä sen sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="b0236-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="b0236-136">Voit välttää ongelmat noudattamalla tarkasti ohjeita.</span><span class="sxs-lookup"><span data-stu-id="b0236-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="b0236-137">Siirry Finance and Operations -sovelluksessa kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Tietotaulut**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="b0236-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="b0236-138">Etsi taulu, josta puuttuu määrite.</span><span class="sxs-lookup"><span data-stu-id="b0236-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="b0236-139">Valitse työkaluriviltä **Muokkaa kohteen yhdistämismääritystä**.</span><span class="sxs-lookup"><span data-stu-id="b0236-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="b0236-140">Valitse **Yhdistä väliaikainen alue kohteeseen** -ruudusta **Luo yhdistämismääritys**.</span><span class="sxs-lookup"><span data-stu-id="b0236-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="b0236-141">Avaa **Taulujen yhdistämismääritys** -sivu **Kaksoiskirjoitussivulta** Finance and Operations -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="b0236-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="b0236-142">Jos määritettä ei täytetä automaattisesti kartalla, lisää se manuaalisesti valitsemalla **Lisää määrite** -painike ja valitsemalla sitten **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b0236-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="b0236-143">Valitse kartta ja valitse **Suorita**.</span><span class="sxs-lookup"><span data-stu-id="b0236-143">Select the map and click **Run**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]