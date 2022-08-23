---
title: Ongelmien vianmääritys alkumäärityksen aikana
description: Tässä artikkelissa on tietoja, joiden avulla voidaan korjata kaksoiskirjoituksen integroinnin alkuasennuksen aikana esiintyviä ongelmia.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289511"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Ongelmien vianmääritys alkumäärityksen aikana

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa on vianmääritystietoja kaksoiskirjoituksen integroinnista talous- ja toimintosovellusten sekä Dataversen välillä. Erityisesti se tarjoaa tietoa vianmääritystietoja, joiden avulla voit korjata ongelmat, joita voi ilmetä kaksoiskirjoituksen integroinnin alkuasennuksen aikana.

> [!IMPORTANT]
> Jotkin tämän artikkelin osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoft Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Talous- ja toimintosovellusta ei voi linkittää Dataverseen

**Kaksoiskirjoituksen asettamiseen vaadittava rooli:** Järjestelmän ylläpitäjä talous- ja toimintosovelluksissa ja Dataversessä.

**Asennuslinkki Dataverseen** -sivulla olevat virheet johtuvat yleensä puutteellisista määritys- tai käyttöoikeusongelmista. Varmista, että koko terveystarkistus siirtyy **Asennuslinkillä Dataverseen**, kuten seuraavasta kuvasta käy ilmi. Kaksoiskirjoittamista ei voi linkittää, ellei koko terveystarkistus ole ohi.

![Onnistunut kuntotarkistus.](media/health_check.png)

Sinulla on oltava Azure AD -vuokraajan järjestelmänvalvojan käyttöoikeudet talous- ja toimintosovellusympäristön sekä Dataverse-ympäristön linkittämiseen. Kun olet linkittänyt ympäristöt, käyttäjät voivat kirjautua sisään käyttämällä tilinsä tunnistetietoja ja päivittää aiemmin luotua taulujen yhdistämiskarttaa.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Kaksoiskirjoittamiseen liittyvien lakitaulujen tai yritysten määrän rajoittaminen

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität ottaa yhdistämismäärityksiä käyttöön:

*Kaksoiskirjoitusvirhe - Laajennuksen rekisteröiminen epäonnistui: [(Osiokarttaa ei voitu saada projektille DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Virhe ylittää DWM-määrityksen enimmäisosiot DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], tapahtui virheitä.*

Tämänhetkinen raja-arvo, kun linkität ympäristöjä, on noin 40 lakitaulua. Tämä virhe ilmenee, jos yrität ottaa käyttöön yhdistämisen ja yli 40 taulua linkitetään ympäristöjen välillä.

## <a name="connection-set-failed-while-linking-environment"></a>Yhteysjoukko epäonnistui ympäristöä linkitettäessä

Toiminto epäonnistuu kaksoiskirjoitusympäristöä linkitettäessä ja seuraava virhesanoma avautuu:

*Yhteysjoukon tallentaminen epäonnistui. Nimike, jolla on sama avain, on jo lisätty.*

Kaksoiskirjoitus ei tue useita samannimisiä yrityksiä/yhtiöitä. Tämä virhesanoma voidaan saada esimerkiksi silloin, jos Dataversessa on kaksi DAT-nimistä yritystä.

Asiakkaan esto poistetaan poistamalla tietueiden kaksoiskappaleet Dataversen **cdm_company**-taulukosta. Jos **cdm_company**-taulukossa on tietueita, joiden nimi on tyhjä, myös nämä tietueet on poistettava tai korjattava.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Virhe avattaessa kaksoiskirjoitussivua talous- ja toimintosovelluksissa

Seuraava virhesanoma voi avautua, kun Dataverse-ympäristö yritetään linkittää kaksoiskirjoittamista varten:

*Vastauksen tilakoodi ei tarkoita onnistumista: 404 (Ei löydetty).*

Tämä virhe tapahtuu, kun sovelluksen suostumusvaihetta ei ole valmis. Hyväksynnän antamisen voi tarkistaa kirjautumalla sivustoon `portal.azure.com` käyttämällä vuokraajan hallintatiliä ja tarkistamalla, näkyykö AAD:n yrityssovelluksessa kolmannen osapuolen sovellus, jolla on tunnus `33976c19-1db5-4c02-810e-c243db79efde`. Jos sitä ei ole, suorita seuraavassa osassa kuvattava hyväksymisvaihe uudelleen.

### <a name="providing-app-consent"></a>Sovelluksen hyväksymisen antaminen

+ Käynnistä seuraava URL-osoite järjestelmänvalvojan tunnistetietojen avulla.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Anna hyväksyntä valitsemalla **Hyväksy**. Hyväksyntä annetaan sovelluksen (jonka tunnus on `id=33976c19-1db5-4c02-810e-c243db79efde`) asentamiselle vuokraajaan.
+ Dataverse tarvitsee sovelluksen viestintään talous- ja toimintosovellusten kanssa.

    ![Ensimmäisen synkronoinnin määrityksen vianmääritys](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Jos tämä ei auta, käynnistä URL-osoite Microsoft Edgen yksityisessä tilassa tai Chromen incognito-tilassa.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Talous- ja toimintosovellusympäristö ei ole löydettävissä

Seuraava virhesanoma voi avautua:

*Talous- ja toimintosovellusympäristö \*\*\*.cloudax.dynamics.com ei ole löydettävissä.*

Kaksi seikkaa voi aiheuttaa ongelman, jos ympäristö ei ole löydettävissä:

+ Kirjautumiseen käytetty käyttäjä ei ole samassa vuokraajassa kuin talous- ja toimintosovellusesiintymä.
+ Joissakin vanhoissa Microsoftin isännöimissä talous- ja toimintosovellusesiintymissä oli löydettävyyteen liittyvä ongelma. Ongelma korjataan päivittämällä talous- ja toimintosovellusesiintymä. Ympäristöstä tulee löydettävä millä tahansa päivityksellä.

## <a name="403-forbidden-error-while-connections-are-being-created"></a>403 (Kielletty) -virhe yhteyksien luomisen aikana

Kaksoiskirjoituksen linkitysprosessin osana luodaan kaksi Power Apps -yhteyttä (tunnetaan myös *Apihub*-yhteyksinä), jotka ovat käyttäjän puolesta luotuja linkitetyssä Dataverse-ympäristössä. Jos asiakkaalla ei ole lisenssiä Power Apps -ympäristölle, ApiHub-yhteyksien luominen epäonnistuu ja näkyviin tulee 403 (Kielletty) -virhe. Esimerkki täydestä virheviestistä:

> MSG=\[Kaksoiskirjoitusympäristön asetus epäonnistui. Virhetiedot: Vastauksen tilakoodi ei tarkoita onnistumista: 403 (Kielletty). - Vastauksen tilakoodi ei tarkoita onnistumista: 403 (Kielletty).\] STACKTRACE=\[   kohteessa Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\>d\_\_29.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\DualWrite\\DualWriteConnectionSetProcessor.cs:line 297 --- Pinon jäljityksen lopetus aiemmassa sijainnissa, jossa poikkeus oli --- kohteessa System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() kohteessa System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task) kohteessa Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\>d\_\_34.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\Controllers\\DualWriteEnvironmentManagementController.cs:line 265\]

Tämä virhe johtuu Power Apps -käyttöoikeuden puutteesta. Määritä käyttäjälle asianmukainen lisenssi (esimerkiksi Power Apps -kokeiluversio 2), jotta käyttäjällä on käyttöoikeudet luoda yhteydet. Käyttöoikeuden tarkistamiseksi asiakas voi tarkastella käyttäjälle määritettyjä käyttöoikeuksia [Oman tili](https://portal.office.com/account/?ref=MeControl#subscriptions) -sivustossa.

Katso lisätietoja Power Apps -käyttöoikeudesta seuraavista artikkeleista:

- [Määritä käyttöoikeuksia käyttäjille](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [Osta Power Apps organisaatiollesi](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

