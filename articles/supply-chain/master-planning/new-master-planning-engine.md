---
title: Siirtyminen suunnittelun optimointiin pääsuunnittelua varten
description: Tässä artikkelissa on tietoja uudesta pääsuunnittelumoduulista eli suunnittelun optimoinnista ja siirtymisestä siihen nykyisestä moduulista.
author: t-benebo
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: dbbc58f0dcd833f63e84a73ac68ada60bd0c291d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739948"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Siirtyminen suunnittelun optimointiin pääsuunnittelua varten

[!include [banner](../includes/banner.md)]

Sisäinen pääsuunnittelumoduuli on aikataulutettu vanhentumaan. Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin apuohjelma korvaa sen. Tässä artikkelissa on tietoja vaikutuksista uusiin ja aiemmin luotuihin käyttöönottoihin. Siinä on tietoja pakollista toimenpiteistä.

Suunnittelun optimoinnin avulla pääsuunnittelulaskelmia voidaan Supply Chain Managementin ja sen Azure SQL -tietokannan ulkopuolella. Suunnittelun optimointitoimintoon liittyviä etuja ovat esimerkiksi suorituskyvyn parantuminen ja pääsuunnitteluajon vähäinen vaikutus SQL-tietokantaan. Koska nopeita suunnitteluajoja voidaan tehdä myös työaikana, suunnittelijat voivat reagoida heti kysynnän tai parametrin muutoksiin.

Lisätietoja suunnittelun optimoinnista on kohdassa [Pääsuunnittelujärjestelmän arkkitehtuuri](master-planning-architecture.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Nykyisen pääsuunnittelumoduulin vanhentuminen

Microsoft on parhaillaan poistamassa vanhentunutta suunnittelumoduulia käytöstä, ja sen tilalle tulee suunnittelun optimointi. Tämä muutos vaikuttaa kaikkiin pilviympäristöihin. Sillä ei ole vaikutusta paikallisiin asennuksiin. Versiosta 10.0.16 alkaen näet virhesanoman, jos suoritat vanhentuneen pääsuunnittelumoduulin luomatta suunniteltuja tuotantotilauksia. Pääsuunnittelun suorittaminen kuitenkin onnistuu virhesanomasta huolimatta.

Lisätietoja vanhentuneesta suunnittelumoduulista on ilmoituksissa kohdassa [Dynamics 365 Supply Chain Managementin poistetut ja vanhentuneet ominaisuudet](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Siirto, sanomat ja poikkeukset

Aiemmin luotujen ympäristöjen omistajat, jotka käyttävät vanhentunutta pääsuunnittelumoduulia luomatta suunniteltuja tuotantotilauksia, saavat poikkeusprosessia koskevan sähköpostiviestin. Siirtyminen suunnittelun optimointiin kannattaa arvioida ja suunnitella yhteistyössä kumppanin kanssa.

Kuten edellä on todettu, näet versiosta 10.0.16 alkaen virhesanoman, jos suoritat vanhentuneen pääsuunnittelumoduulin luomatta suunniteltuja tuotantotilauksia. Tässä virhesanomassa on ohjeita siirtymistä ja poikkeuksen pyytämisestä.

### <a name="new-deployments"></a>Uudet käyttöönotot

Suunnittelun optimointi on kuin kaikkien uusien pilvikäyttöönottojen oletusarvoinen pääsuunnittelumoduuli. Suunnittelun optimointi on yleisesti ottaen käytettävä kaikissa uusissa käyttöönotoissa, joissa ei luoda suunniteltuja tuotantotilauksia pääsuunnittelun aikana. Jos uusi käyttöönotto on riippuvainen toiminnosta, jota suunnittelun optimointi ei tällä hetkellä tue, voit pyytää poikkeusta, jotta voit jatkaa vanhentuneen pääsuunnittelumoduulin käyttämistä.

### <a name="existing-deployments"></a>Aiemmin luodut käyttöönotot

Aiemmin luotujen pääsuunnittelu riippuvaisten pilvipohjaisten käyttöönottojen omistajien on suunniteltava suunnittelun optimointiin siirtyminen. Jos toteutus on riippuvainen toiminnosta, jota suunnittelun optimointi ei tällä hetkellä tue, voit pyytää poikkeusta, jotta voit jatkaa vanhentuneen pääsuunnittelumoduulin käyttämistä.

Microsoft lähettää niiden ympäristöjen järjestelmävalvojille sähköpostiviestin, joissa käytetään tällä hetkellä vanhentuvia pääsuunnitteluprosesseja. Tässä sähköpostiviestissä on tietoja toiminnoista, jotka on tehtävä siirtymistä tai poikkeuksen pyytämistä varten.

## <a name="the-exception-process"></a>Poikkeusprosessi

Voit pyytää poikkeusta, jos sinun täytyy jatkaa vanhentuneen pääsuunnittelumoduulin käyttöä, koska liiketoimintaprosessisi ovat suuressa määrin riippuvaisia ainakin yhdestä toiminnosta, jota ei ole tällä hetkellä toteutettu suunnittelun optimoinnissa. Käytettävissä olevien ominaisuuksien luettelo on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization/planning-optimization-fit-analysis.md).

Tällä hetkellä suunnittelun optimointiin siirtymisen poikkeuksilla on merkitystä vain, jos pääsuunnitteluprosessisi ei sisällä tuotantoa (eli pääsuunnittelun luomia suunniteltuja tuotantotilauksia) ja tarvitset vanhentunutta pääsuunnittelumoduulia version 10.0.15 jälkeenkin.

Kun tarvittavat toiminnot ovat käytettävissä, Microsoft antaa lisäaikaa poikkeuksen päättymiseen saakka. Ympäristön järjestelmänvalvojalla ilmoitetaan, kun tarvittavat toiminnot ovat käytettävissä ja lisäaika on alkanut.

Seuraavassa vuokaaviossa on yhteenveto tämän artikkelin tiedoista, jotta voit nopeasti selvittää, haluatko pyytää poikkeusta. Jos haluat pyytää poikkeusta, täytä ja lähetä [Suunnittelun optimointi -siirto ja poikkeuslomake](https://go.microsoft.com/fwlink/?linkid=2144962). Tuoteryhmä vastaa kunkin poikkeuspyynnön arvioinnista ja hyväksymisestä, joten lähetä pyyntösi suoraan tuoteryhmään linkin avulla, älä luo tukipalvelupyyntöä sitä varten. Jos pyyntösi hylätään, älä luo tukipalvelupyyntöä, koska Microsoftin tuki ei voi arvioida uudelleen tai myöntää poikkeuksia.

![Poikkeuskaavio.](media/exception-diagram.png "Poikkeuskaavio")

> [!NOTE]
> Voit pyytää poikkeusta vain vuokraajille, jotka sisältävät tai sisällyttävät tuotantoympäristön– ei vain vuokralaisia, joilla on vain eri ympäristöjä. Jos suunnittelun optimoinnin poikkeusvirhe on poistettava käytöstä IaaS (infrastruktuuri palveluna) -eristysympäristössä, suorita [eristysympäristöissä](#faq-sandbox) oleva SQL-kysely.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Eristysympäristöt

Voinko käyttää vanhentunutta pääsuunnittelumoduulia omassa eristysympäristössäni? Tarvitaanko sitä varten poikkeus?

**Vastaus:** Poikkeukset eivät tavallisesti koske eristysympäristöjä, koska suunnittelun optimoinnin poikkeusvirhe ei estä vanhentuneen pääsuunnittelumoduulin suorittamista. Jos virhesanoma on kuitenkin häiritsevä, se voidaan poistaa käytöstä IaaS- (ei Service Fabric) -eristysympäristössä suorittamalla seuraava kysely tietokannassa:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Paikalliset ympäristöt

Oma ympäristön on paikallinen ympäristö. Tarvitaanko sitä varten poikkeus?

**Vastaus:** Ei. Poikkeusta ei tarvita paikallisissa ympäristöissä. Voit jatkaa vanhentuneen pääsuunnittelumoduulin käyttämistä. Ympäristön järjestelmänvalvojalle ilmoitetaan, jos jotakin on tehtävä.

### <a name="production-scenarios"></a>Tuotantoskenaariot

Käytämme suunniteltuja tuotantotilauksia, mutta mitä tapahtuu päivitettäessä versioon 10.0.16. Onko jotakin tehtävä?

**Vastaus:** Syytä huoleen ei ole. Voit jatkaa vanhentuneen pääsuunnittelumoduulin käyttämistä versiossa 10.0.16. Kannattaa kuitenkin arvioida, voiko suunnittelun optimointiin siirtymisen aloittaa nykyisillä toiminnoilla. Lisäksi kannattaa pysyä ajan tasalla uusien toimintojen osalta.

### <a name="email-from-microsoft"></a>Microsoftin lähettämä sähköposti

Ympäristön järjestelmänvalvoja sai sähköpostia Microsoftilta. Tämän sähköpostin mukaan meidän pitäisi siirtyä suunnittelun optimointiin tai pyytää poikkeusta. Onko jotakin tehtävä?

**Vastaus:** Kyllä. Sähköpostin ohjeiden noudattamatta jättäminen vaikuttaa ympäristöön. Vaihtoehtoina on joko suunnittelun optimointiin siirtyminen määritettyyn päivämäärään mennessä tai pyytämällä poikkeusta sähköpostin linkkiä käyttämällä. Tämä linkki avaa kyselylomakkeen. Kun tämä kyselylomake on täytetty ja lähetetty, vastaus lähetetään sähköpostitse. Vaikka tämä prosessi on manuaalinen, Microsoft yrittää vastata viikon kuluessa siitä, kun kyselylomake on lähetetty.

### <a name="error-messages"></a>Virheilmoitukset

Käytössä on versio 10.0.16 tai sitä uudempi versio ja seuraava virhesanoma avautuu pääsuunnittelua suoritettaessa. Onko pääsuunnittelu estetty?

> Näet tämän virhesanoman, koska vanhentunutta pääsuunnittelumoduulia käytettiin suunnittelun optimoinnin tukemissa skenaarioissa. Sinun tulisi siirtyä suunnittelun optimointiin nyt, sillä sisäinen pääsuunnittelumoduuli on poistettu käytöstä. Huomaa, että pääsuunnittelun suorittaminen onnistui.
>
> Jos siirtosi on vahvasti riippuvainen tulevista ominaisuuksista, voit pyytää poikkeusta vanhentuneen pääsuunnittelumoduulin käytön jatkamista varten.
>
> Aloita täyttämällä seuraava kyselylomake ja pyydä tarvittaessa poikkeus suunnittelun optimointiin siirtymisessä.

**Vastaus:** Ei, pääsuunnittelua ei ole estetty. Pääsuunnitteluajo onnistui ja tuloksia voi käyttää tavalliseen tapaan. Tämän virhesanoman avautuminen voidaan kuitenkin estää tulevissa pääsuunnitteluajoissa joko siirtymällä heti suunnittelun optimointiin tai pyytämällä poikkeusta käyttämällä virhesanomassa olevaa linkkiä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
