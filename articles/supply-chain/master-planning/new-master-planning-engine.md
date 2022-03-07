---
title: Siirtyminen suunnittelun optimointiin pääsuunnittelua varten
description: Tässä aiheessa on tietoja uudesta pääsuunnittelumoduulista eli suunnittelun optimoinnista ja siirtymisestä siihen nykyisestä moduulista.
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: e227cabdd205b7a0c1fe784fc719b538e6ea4443
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907688"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Siirtyminen suunnittelun optimointiin pääsuunnittelua varten

[!include [banner](../includes/banner.md)]

Sisäinen pääsuunnittelumoduuli on aikataulutettu vanhentumaan. Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin apuohjelma korvaa sen. Tässä aiheessa on tietoja vaikutuksista uusiin ja aiemmin luotuihin käyttöönottoihin. Siinä on tietoja pakollista toimenpiteistä.

Suunnittelun optimoinnin avulla pääsuunnittelulaskelmia voidaan Supply Chain Managementin ja sen Azure SQL -tietokannan ulkopuolella. Suunnittelun optimointitoimintoon liittyviä etuja ovat esimerkiksi suorituskyvyn parantuminen ja pääsuunnitteluajon vähäinen vaikutus SQL-tietokantaan. Koska nopeita suunnitteluajoja voidaan tehdä myös työaikana, suunnittelijat voivat reagoida heti kysynnän tai parametrin muutoksiin.

Lisätietoja suunnittelun optimoinnista on kohdassa [Suunnittelun optimoinnin yleiskatsaus](planning-optimization/planning-optimization-overview.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Nykyisen pääsuunnittelumoduulin vanhentuminen

Microsoft on parhaillaan poistamassa sisäistä suunnittelumoduulia käytöstä ja sen tilalle tulee suunnittelun optimointi. Tämä muutos vaikuttaa kaikkiin pilviympäristöihin. Sillä ei ole vaikutusta paikallisiin asennuksiin. Versiosta 10.0.16 alkaen virhesanoma avautuu, jos sisäinen pääsuunnittelu suoritetaan ilman suunniteltujen tuotantotilausten luontia. Pääsuunnittelun suorittaminen kuitenkin onnistuu virhesanomasta huolimatta.

Lisätietoja sisäisen suunnittelumoduulin vanhentumisesta on ilmoituksissa kohdassa [Dynamics 365 Supply Chain Managementin poistetut ja vanhentuneet ominaisuudet](../get-started/removed-deprecated-features-scm-updates.md).

## <a name="migration-messages-and-exceptions"></a>Siirto, sanomat ja poikkeukset

Aiemmin luotujen ympäristöjen omistajat, jotka käyttävät sisäistä pääsuunnittelumoduulia suunniteltuja tuotantotilauksia luomatta, saavat poikkeusprosessia koskevan sähköpostiviestin. Siirtyminen suunnittelun optimointiin kannattaa arvioida ja suunnitella yhteistyössä kumppanin kanssa.

Kuten edellä on todettu versiosta 10.0.16 alkaen virhesanoma avautuu, jos sisäinen pääsuunnittelu suoritetaan ilman suunniteltujen tuotantotilausten luontia. Tässä virhesanomassa on ohjeita siirtymistä ja poikkeuksen pyytämisestä.

### <a name="new-deployments"></a>Uudet käyttöönotot

Suunnittelun optimointi on kuin kaikkien uusien pilvikäyttöönottojen oletusarvoinen pääsuunnittelumoduuli. Suunnittelun optimointi on yleisesti ottaen käytettävä kaikissa uusissa käyttöönotoissa, joissa ei luoda suunniteltuja tuotantotilauksia pääsuunnittelun aikana. Jos uusi käyttöönotto on riippuvainen toiminnosta, jota suunnittelun optimointi ei tällä hetkellä tue, voit pyytää poikkeusta, jotta voit jatkaa sisäisen pääsuunnittelumoduulin käyttämistä.

### <a name="existing-deployments"></a>Aiemmin luodut käyttöönotot

Aiemmin luotujen pääsuunnittelu riippuvaisten pilvipohjaisten käyttöönottojen omistajien on suunniteltava suunnittelun optimointiin siirtyminen. Jos toteutus on riippuvainen toiminnosta, jota suunnittelun optimointi ei tällä hetkellä tue, voit pyytää poikkeusta, jotta voit jatkaa sisäisen pääsuunnittelumoduulin käyttämistä.

Microsoft lähettää niiden ympäristöjen järjestelmävalvojille sähköpostiviestin, joissa käytetään tällä hetkellä vanhentuvia pääsuunnitteluprosesseja. Tässä sähköpostiviestissä on tietoja toiminnoista, jotka on tehtävä siirtymistä tai poikkeuksen pyytämistä varten.

## <a name="the-exception-process"></a>Poikkeusprosessi

Voit pyytää poikkeusta, jos sisäisen pääsuunnittelumoduulin käyttöä on jatkettava, koska liiketoimintaprosessit ovat suuressa määrin riippuvaisia ainakin yhdestä toiminnosta, jota ei tällä hetkellä toteuteta suunnittelun optimoinnissa. Käytettävissä olevien ominaisuuksien luettelo on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization/planning-optimization-fit-analysis.md).

Tällä hetkellä suunnittelun optimointiin siirtymisen poikkeuksilla on merkitystä vain, jos pääsuunnitteluprosessi ei sisällä tuotantoa (eli pääsuunnittelun luomia suunniteltuja tuotantotilauksia) ja sisäistä pääsuunnittelumoduulia tarvitaan version 10.0.15 jälkeen.

Kun tarvittavat toiminnot ovat käytettävissä, Microsoft antaa lisäaikaa poikkeuksen päättymiseen saakka. Ympäristön järjestelmänvalvojalla ilmoitetaan, kun tarvittavat toiminnot ovat käytettävissä ja lisäaika on alkanut.

Seuraavassa vuokaaviossa on yhteenveto tämän ohjeaiheen tiedoista, jotta voit nopeasti selvittää, haluatko pyytää poikkeusta. Jos haluat pyytää poikkeusta, täytä ja lähetä [Suunnittelun optimointi -siirto ja poikkeuslomake](https://go.microsoft.com/fwlink/?linkid=2144962).

![Poikkeuskaavio](media/exception-diagram.png "Poikkeuskaavio")

> [!NOTE]
> Voit pyytää poikkeusta vain vuokraajille, jotka sisältävät tai sisällyttävät tuotantoympäristön– ei vain vuokralaisia, joilla on vain eri ympäristöjä. Jos suunnittelun optimoinnin poikkeusvirhe on poistettava käytöstä IaaS (infrastruktuuri palveluna) -eristysympäristössä, suorita [eristysympäristöissä](#faq-sandbox) oleva SQL-kysely.

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Eristysympäristöt

Voiko sisäistä pääsuunnittelua käyttää omassa eristysympäristössä? Tarvitaanko sitä varten poikkeus?

**Vastaus:** Poikkeukset eivät yleensä koske eristysympäristöjä, koska suunnittelun optimoinnin poikkeusvirhe ei estä sisäisen pääsuunnittelumoduulin suorittamista. Jos virhesanoma on kuitenkin häiritsevä, se voidaan poistaa käytöstä IaaS- (ei Service Fabric) -eristysympäristössä suorittamalla seuraava kysely tietokannassa:

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

**Vastaus:** Ei. Poikkeusta ei tarvita paikallisissa ympäristöissä. Sisäisen pääsuunnittelun käyttöä voidaan jatkaa. Ympäristön järjestelmänvalvojalle ilmoitetaan, jos jotakin on tehtävä.

### <a name="production-scenarios"></a>Tuotantoskenaariot

Käytämme suunniteltuja tuotantotilauksia, mutta mitä tapahtuu päivitettäessä versioon 10.0.16. Onko jotakin tehtävä?

**Vastaus:** Syytä huoleen ei ole. Sisäisen pääsuunnittelun käyttöä voidaan jatkaa versiossa 10.0.16. Kannattaa kuitenkin arvioida, voiko suunnittelun optimointiin siirtymisen aloittaa nykyisillä toiminnoilla. Lisäksi kannattaa pysyä ajan tasalla uusien toimintojen osalta.

### <a name="email-from-microsoft"></a>Microsoftin lähettämä sähköposti

Ympäristön järjestelmänvalvoja sai sähköpostia Microsoftilta. Tämän sähköpostin mukaan meidän pitäisi siirtyä suunnittelun optimointiin tai pyytää poikkeusta. Onko jotakin tehtävä?

**Vastaus:** Kyllä. Sähköpostin ohjeiden noudattamatta jättäminen vaikuttaa ympäristöön. Vaihtoehtoina on joko suunnittelun optimointiin siirtyminen määritettyyn päivämäärään mennessä tai pyytämällä poikkeusta sähköpostin linkkiä käyttämällä. Tämä linkki avaa kyselylomakkeen. Kun tämä kyselylomake on täytetty ja lähetetty, vastaus lähetetään sähköpostitse. Vaikka tämä prosessi on manuaalinen, Microsoft yrittää vastata viikon kuluessa siitä, kun kyselylomake on lähetetty.

### <a name="error-messages"></a>Virheilmoitukset

Käytössä on versio 10.0.16 tai sitä uudempi versio ja seuraava virhesanoma avautuu pääsuunnittelua suoritettaessa. Onko pääsuunnittelu estetty?

> Tämä virhesanoma avautuu, koska sisäistä suunnittelumoduulia käytettiin suunnittelun optimoinnin tukemissa skenaarioissa. Suunnittelun optimointiin kannattaa siirtyä nyt, sillä nykyinen sisäinen pääsuunnittelu vanhentuu. Huomaa, että pääsuunnittelun suorittaminen onnistui.
>
> Jos siirrossa on vahvat riippuvuudet odottaviin toimintoihin, voidaan pyytää poikkeusta sisäisen pääsuunnittelumoduulin käytön jatkamista varten.
>
> Aloita täyttämällä seuraava kyselylomake ja pyydä tarvittaessa poikkeus suunnittelun optimointiin siirtymisessä.

**Vastaus:** Ei, pääsuunnittelua ei ole estetty. Pääsuunnitteluajo onnistui ja tuloksia voi käyttää tavalliseen tapaan. Tämän virhesanoman avautuminen voidaan kuitenkin estää tulevissa pääsuunnitteluajoissa joko siirtymällä heti suunnittelun optimointiin tai pyytämällä poikkeusta käyttämällä virhesanomassa olevaa linkkiä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
