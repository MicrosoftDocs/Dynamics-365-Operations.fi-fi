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
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Ongelmien vianmääritys synkronoinnin aikana

[!include [banner](../../includes/banner.md)]



Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Common Data Servicen välillä. Erityisesti se tarjoaa tietoa, joiden avulla voit korjata virheitä, joita saattaa ilmetä alkuperäisen synkronoinnin aikana. 

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Finance and Operations -sovelluksen ensimmäisten synkronointivirheiden tarkistaminen

Kun otat yhdistämismallit käyttöön, karttojen tilan on oltava **Käytössä**. Jos tila on **ei käynnissä**, alkuperäisen synkronoinnin aikana ilmeni virheitä. Voit tarkastella virheitä valitsemalla **kaksoiskirjoitus**-sivun **ensimmäiset synkronointitiedot**-välilehden.

![Alkuperäisen synkronoinnin tiedot -välilehti](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Alkuperäistä synkronointia ei voi suorittaa loppuun: 400 virheellinen pyyntö

**Ongelman korjaamiseen tarvittava rooli:** Järjestelmänvalvoja

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität suorittaa yhdistämismääritystä ja alkuperäistä synkronointia:

*Etäpalvelin palautti virheen: (400) Virheellinen pyyntö.), AX-vienti kohtasi virheen*

Esimerkki täydestä virheviestistä.

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

Jos tämä virhe ilmenee jatkuvasti etkä voi suorittaa alkuperäistä synkronointia loppuun, korjaa ongelma noudattamalla seuraavia ohjeita.

1. Kirjaudu sisään virtuaalikone (VM) Finance and Operationsille -sovellukseen.
2. Avaa Microsoft Management Console. 
3. Varmista **Palvelut**-ruudussa, että Microsoft Dynamics 365 -tietojen tuonnin vientikehyspalvelu on käytössä. Käynnistä se uudelleen, jos se on pysäytetty, koska ensimmäinen synkronointi edellyttää sitä.

## <a name="initial-synchronization-error-403-forbidden"></a>Ensimmäinen synkronointivirhe: 403 kielletty

Seuraava virhesanoma saattaa tulla näyttöön alkuperäisen synkronoinnin aikana:

*(\[Kielletty\], Etäpalvelin palautti virheen: (403) Kielletty.), AX-vienti kohtasi virheen*

Korjaa ongelma seuraavien ohjeiden mukaisesti.

1. Kirjautuminen Finance and Operations -sovellukseen.
2. Poista **Azure Active Directory -sovellukset** -sivulla **DtAppID**-asiakasohjelma ja lisää se sitten uudelleen.

![Azure AD -sovellusluettelo](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a>Itseensä viittausvirheet alkuperäisen synkronoinnin aikana

Näyttöön saattaa tulla seuraavan kaltainen virhesanoma, jos jollakin yhdistämismäärityksistä on omat viittaukset:

*Toimittajat V2:ssa seuraava virhe: Tietueen tunnus: uusi tietue, ErrorMessage: Kentän GUID-tunnusta ei voitu ratkaista: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Hakuarvoa ei löytynyt: CN-001. Tarkista, onko viitetiedot olemassa, kokeilemalla näitä URL-osoitteita `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

Tämäntyyppinen virhe tapahtuu niiden yhdistämismääritysten alkuvaiheessa, joilla on itseensä viittauksia. Edeltävässä esimerkissä kentän laskutili viittaa toimittajayksikköön.

Jos haluat korjata ongelman, sinun on ehkä suoritettava yhdistämismääritys kaksi kertaa ennen kuin ensimmäinen synkronointi onnistuu.

