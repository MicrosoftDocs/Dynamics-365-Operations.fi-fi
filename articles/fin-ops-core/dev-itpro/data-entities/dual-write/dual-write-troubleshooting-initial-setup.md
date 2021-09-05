---
title: Ongelmien vianmääritys alkumäärityksen aikana
description: Tässä ohjeaiheessa on tietoja, joiden avulla voidaan korjata kaksoiskirjoituksen integroinnin alkuasennuksen aikana esiintyviä ongelmia.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2b75155aac12d79b9d68cce3e066acaaf80d6764
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380185"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Ongelmien vianmääritys alkumäärityksen aikana

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tässä artikkelissa on vianetsintätietoja kaksoiskirjoituksen integroinnista Finance and Operations -sovellusten ja Dataversen välillä. Erityisesti se tarjoaa tietoa vianmääritystietoja, joiden avulla voit korjata ongelmat, joita voi ilmetä kaksoiskirjoituksen integroinnin alkuasennuksen aikana.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Et voi linkittää Finance and Operations -sovellusta Dataverseen

**Kaksoiskirjoituksen asettamiseen vaadittava rooli:** Järjestelmän ylläpitäjä Finance and Operations -sovelluksissa ja Dataversessä.

**Asennuslinkki Dataverseen** -sivulla olevat virheet johtuvat yleensä puutteellisista määritys- tai käyttöoikeusongelmista. Varmista, että koko terveystarkistus siirtyy **Asennuslinkillä Dataverseen**, kuten seuraavasta kuvasta käy ilmi. Kaksoiskirjoittamista ei voi linkittää, ellei koko terveystarkistus ole ohi.

![Onnistunut kuntotarkistus.](media/health_check.png)

Sinulla on oltava Azure AD -vuokralaisen järjestelmänvalvojan käyttöoikeudet Finance and Operations- ja Dataverse -ympäristöjen linkittämiseen. Kun olet linkittänyt ympäristöt, käyttäjät voivat kirjautua sisään käyttämällä tilinsä tunnistetietoja ja päivittää aiemmin luotua taulujen yhdistämiskarttaa.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Kaksoiskirjoittamiseen liittyvien lakitaulujen tai yritysten määrän rajoittaminen

Näyttöön saattaa tulla seuraava virhesanoma, kun yrität ottaa yhdistämismäärityksiä käyttöön:

*Kaksoiskirjoitusvirhe - Laajennuksen rekisteröiminen epäonnistui: [(Osiokarttaa ei voitu saada projektille DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Virhe ylittää DWM-määrityksen enimmäisosiot DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], tapahtui virheitä.*

Tämänhetkinen raja-arvo, kun linkität ympäristöjä, on noin 40 lakitaulua. Tämä virhe ilmenee, jos yrität ottaa käyttöön yhdistämisen ja yli 40 taulua linkitetään ympäristöjen välillä.

## <a name="connection-set-failed-while-linking-environment"></a>Yhteysjoukko epäonnistui ympäristöä linkitettäessä

Toiminto epäonnistuu kaksoiskirjoitusympäristöä linkitettäessä ja seuraava virhesanoma avautuu:

*Yhteysjoukon tallentaminen epäonnistui. Nimike, jolla on sama avain, on jo lisätty.*

Kaksoiskirjoitus ei tue useita samannimisiä yrityksiä/yhtiöitä. Tämä virhesanoma voidaan saada esimerkiksi silloin, jos Dataversessa on kaksi DAT-nimistä yritystä.

Asiakkaan esto poistetaan poistamalla tietueiden kaksoiskappaleet Dataversen **cdm_company**-taulukosta. Jos **cdm_company**-taulukossa on tietueita, joiden nimi on tyhjä, myös nämä tietueet on poistettava tai korjattava.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Virhe avattaessa kaksoiskirjoitussivua Finance and Operations -sovelluksessa

Seuraava virhesanoma voi avautua, kun Dataverse-ympäristö yritetään linkittää kaksoiskirjoittamista varten:

*Vastauksen tilakoodi ei tarkoita onnistumista: 404 (Ei löydetty).*

Tämä virhe tapahtuu, kun sovelluksen suostumusvaihetta ei ole valmis. Hyväksynnän antamisen voi tarkistaa kirjautumalla sivustoon `portal.azure.com` käyttämällä vuokraajan hallintatiliä ja tarkistamalla, näkyykö AAD:n yrityssovelluksessa kolmannen osapuolen sovellus, jolla on tunnus `33976c19-1db5-4c02-810e-c243db79efde`. Jos sitä ei ole, suorita seuraavassa osassa kuvattava hyväksymisvaihe uudelleen.

### <a name="providing-app-consent"></a>Sovelluksen hyväksymisen antaminen

+ Käynnistä seuraava URL-osoite järjestelmänvalvojan tunnistetietojen avulla.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Anna hyväksyntä valitsemalla **Hyväksy**. Hyväksyntä annetaan sovelluksen (jonka tunnus on `id=33976c19-1db5-4c02-810e-c243db79efde`) asentamiselle vuokraajaan.
+ Dataverse tarvitsee sovelluksen viestintään Finance and Operations -sovellusten kanssa.

    ![Ensimmäisen synkronoinnin määrityksen vianmääritys](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Jos tämä ei auta, käynnistä URL-osoite Microsoft Edgen yksityisessä tilassa tai Chromen incognito-tilassa.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finance and Operations -ympäristöä ei havaita

Seuraava virhesanoma voi avautua:

*Finance and Operations -sovellusympäristö \*\*\*.cloudax.dynamics.com ei ole löydettävissä.*

Kaksi seikkaa voi aiheuttaa ongelman, jos ympäristö ei ole löydettävissä:

+ Kirjautumiseen käytetty käyttäjä ei ole samassa vuokraajassa kuin Finance and Operations -esiintymä.
+ Joissakin vanhoissa Microsoftin isännöimissä Finance and Operations -esiintymissä oli löydettävyyteen liittyvä ongelma. Ongelma korjataan päivittämällä Finance and Operations -esiintymä. Ympäristöstä tulee löydettävä millä tahansa päivityksellä.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
