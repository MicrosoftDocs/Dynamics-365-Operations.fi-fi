---
title: Ongelmien vianmääritys synkronoinnin aikana
description: Tässä ohjeaiheessa on vianmääritys tietoja, joiden avulla voit korjata, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.
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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172711"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a><span data-ttu-id="8ddff-103">Ongelmien vianmääritys synkronoinnin aikana</span><span class="sxs-lookup"><span data-stu-id="8ddff-103">Troubleshoot issues during initial synchronization</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="8ddff-104">Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä.</span><span class="sxs-lookup"><span data-stu-id="8ddff-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="8ddff-105">Erityisesti se tarjoaa tietoa, joiden avulla voit korjata virheitä, joita saattaa ilmetä alkuperäisen synkronoinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="8ddff-105">Specifically, it provides information that can help you fix issues that might occur during initial synchronization.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="8ddff-106">Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia.</span><span class="sxs-lookup"><span data-stu-id="8ddff-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="8ddff-107">Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="8ddff-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a><span data-ttu-id="8ddff-108">Finance and Operations -sovelluksen ensimmäisten synkronointivirheiden tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="8ddff-108">Check for initial synchronization errors in a Finance and Operations app</span></span>

<span data-ttu-id="8ddff-109">Kun otat yhdistämismallit käyttöön, karttojen tilan on oltava **Käytössä**.</span><span class="sxs-lookup"><span data-stu-id="8ddff-109">After you enable the mapping templates, the status of the maps should be **Running**.</span></span> <span data-ttu-id="8ddff-110">Jos tila on **ei käynnissä**, alkuperäisen synkronoinnin aikana ilmeni virheitä.</span><span class="sxs-lookup"><span data-stu-id="8ddff-110">If the status is **Not running**, errors occurred during initial synchronization.</span></span> <span data-ttu-id="8ddff-111">Voit tarkastella virheitä valitsemalla **kaksoiskirjoitus**-sivun **ensimmäiset synkronointitiedot**-välilehden.</span><span class="sxs-lookup"><span data-stu-id="8ddff-111">To view the errors, select the **Initial sync details** tab on the **Dual-write** page.</span></span>

![Alkuperäisen synkronoinnin tiedot -välilehti](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a><span data-ttu-id="8ddff-113">Alkuperäistä synkronointia ei voi suorittaa loppuun: 400 virheellinen pyyntö</span><span class="sxs-lookup"><span data-stu-id="8ddff-113">You can't complete initial synchronization: 400 Bad Request</span></span>

<span data-ttu-id="8ddff-114">**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="8ddff-114">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="8ddff-115">Näyttöön saattaa tulla seuraava virhesanoma, kun yrität suorittaa yhdistämismääritystä ja alkuperäistä synkronointia:</span><span class="sxs-lookup"><span data-stu-id="8ddff-115">You might receive the following error message when you try to run the mapping and initial synchronization:</span></span>

<span data-ttu-id="8ddff-116">*Etäpalvelin palautti virheen: (400) Virheellinen pyyntö.), AX-vienti kohtasi virheen*</span><span class="sxs-lookup"><span data-stu-id="8ddff-116">*The remote server returned an error: (400) Bad Request.), AX export encountered an error*</span></span>

<span data-ttu-id="8ddff-117">Esimerkki täydestä virheviestistä.</span><span class="sxs-lookup"><span data-stu-id="8ddff-117">Here is an example of the full error message.</span></span>

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

<span data-ttu-id="8ddff-118">Jos tämä virhe ilmenee jatkuvasti etkä voi suorittaa alkuperäistä synkronointia loppuun, korjaa ongelma noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="8ddff-118">If this error occurs consistently, and you can't complete the initial synchronization, follow these steps to fix the issue.</span></span>

1. <span data-ttu-id="8ddff-119">Kirjaudu sisään virtuaalikone (VM) Finance and Operationsille -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="8ddff-119">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="8ddff-120">Avaa Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="8ddff-120">Open Microsoft Management Console.</span></span> 
3. <span data-ttu-id="8ddff-121">Varmista **Palvelut**-ruudussa, että Microsoft Dynamics 365 -tietojen tuonnin vientikehyspalvelu on käytössä.</span><span class="sxs-lookup"><span data-stu-id="8ddff-121">In the **Services** pane, make sure that the Microsoft Dynamics 365 Data import export framework service is running.</span></span> <span data-ttu-id="8ddff-122">Käynnistä se uudelleen, jos se on pysäytetty, koska ensimmäinen synkronointi edellyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="8ddff-122">Restart it if it has been stopped, because the initial synchronization requires it.</span></span>

## <a name="initial-synchronization-error-403-forbidden"></a><span data-ttu-id="8ddff-123">Ensimmäinen synkronointivirhe: 403 kielletty</span><span class="sxs-lookup"><span data-stu-id="8ddff-123">Initial synchronization error: 403 Forbidden</span></span>

<span data-ttu-id="8ddff-124">Seuraava virhesanoma saattaa tulla näyttöön alkuperäisen synkronoinnin aikana:</span><span class="sxs-lookup"><span data-stu-id="8ddff-124">You might receive the following error message during initial synchronization:</span></span>

<span data-ttu-id="8ddff-125">*(\[Kielletty\], Etäpalvelin palautti virheen: (403) Kielletty.), AX-vienti kohtasi virheen*</span><span class="sxs-lookup"><span data-stu-id="8ddff-125">*(\[Forbidden\], The remote server returned an error: (403) Forbidden.), AX export encountered an error*</span></span>

<span data-ttu-id="8ddff-126">Korjaa ongelma seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8ddff-126">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="8ddff-127">Kirjautuminen Finance and Operations -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="8ddff-127">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="8ddff-128">Poista **Azure Active Directory -sovellukset** -sivulla **DtAppID**-asiakasohjelma ja lisää se sitten uudelleen.</span><span class="sxs-lookup"><span data-stu-id="8ddff-128">On the **Azure Active Directory applications** page, delete the **DtAppID** client, and then add it again.</span></span>

![Azure AD -sovellusluettelo](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a><span data-ttu-id="8ddff-130">Itseensä viittausvirheet alkuperäisen synkronoinnin aikana</span><span class="sxs-lookup"><span data-stu-id="8ddff-130">Self-reference failures during initial synchronization</span></span>

<span data-ttu-id="8ddff-131">Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, jos jollakin yhdistämismäärityksistä on omat viittaukset:</span><span class="sxs-lookup"><span data-stu-id="8ddff-131">You might receive an error message that resembles the following example if any of your mappings have self-references:</span></span>

<span data-ttu-id="8ddff-132">*Toimittajat V2:ssa seuraava virhe: Tietueen tunnus: uusi tietue, ErrorMessage: Kentän GUID-tunnusta ei voitu ratkaista: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Hakuarvoa ei löytynyt: CN-001. Tarkista, onko viitetiedot olemassa, kokeilemalla näitä URL-osoitteita `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span><span class="sxs-lookup"><span data-stu-id="8ddff-132">*On the Vendors V2, the following error: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Try this URL(s) to check if the reference data exists: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*</span></span>

<span data-ttu-id="8ddff-133">Tämäntyyppinen virhe tapahtuu niiden yhdistämismääritysten alkuvaiheessa, joilla on itseensä viittauksia.</span><span class="sxs-lookup"><span data-stu-id="8ddff-133">This type of error occurs during initial synchronization of mappings that have self-references.</span></span> <span data-ttu-id="8ddff-134">Edeltävässä esimerkissä kentän laskutili viittaa toimittajayksikköön.</span><span class="sxs-lookup"><span data-stu-id="8ddff-134">In the preceding example, the field invoice account references the vendor entity.</span></span>

<span data-ttu-id="8ddff-135">Jos haluat korjata ongelman, sinun on ehkä suoritettava yhdistämismääritys kaksi kertaa ennen kuin ensimmäinen synkronointi onnistuu.</span><span class="sxs-lookup"><span data-stu-id="8ddff-135">To fix the issue, you might have to run the mapping two times before the initial synchronization is successful.</span></span>

