---
title: Suunnittelun optimoinnin aloittaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoiminnon käytön aloittamisesta.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2020
ms.locfileid: "4427519"
---
# <a name="get-started-with-planning-optimization"></a>Suunnittelun optimoinnin aloittaminen

[!include [banner](../../includes/banner.md)]

Kuten [aiemmin ilmoitettiin](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), suunnittelun optimointi on aikataulutettu korvaamaan nykyinen sisäinen pääsuunnittelumoduuli.

Jos sisäinen pääsuunnittelumoduuli on tällä hetkellä käytössä, suunnittelun optimointiin siirtymisen suunnittelu on syytä aloittaa nyt. Siirtoprosessi on tärkeää aloittaa heti, koska toiminnot voivat häiriintyä, kun vanhentumista ei voi estää. Siirtyminen kannattaa toteuttaa 1. joulukuuta 2020 mennessä, jotta vanhentumisesta aiheutuvat viime hetken ongelmat voidaan välttää. 

Suunnittelun optimointitoiminto ei tällä hetkellä tue kaikki niitä toimintoja, joita on Supply Chain Managementin sisäisessä suunnittelumoduulissa. Tämän vuoksi on tärkeää arvioida, vastaako suunnittelun optimoinnissa tällä hetkellä käytössä oleva toimintojoukko tarpeitasi. Suunnittelun optimointi ei ole tällä hetkellä oletusarvoisesti otettuna käyttöön Dynamics Lifecycle Servicesissä (LCS), joten arvionti on mahdollista tehdä ennen ominaisuuden ottamista käyttöön.

> [!NOTE]
> Poikkeusta suunnittelun optimointiin siirtymiseen on pyydettävä, jos pääsuunnitteluprosessi ei sisällä tuotantoa (pääsuunnittelun luomia suunniteltuja tuotantotilauksia) ja tarvitset sisäistä pääsuunnittelumoduulia version 10.0.15 jälkeen. Versiosta 10.0.16 alkaen ympäristöissä näytetään virhe, jos sisäinen pääsuunnittelu suoritetaan ilman suunniteltujen tuotantotilausten luontia. Suunnittelun optimointia on käytettävä kaikissa uusissa käyttöönotoissa, joissa ei luoda suunniteltuja tuotantotilauksia pääsuunnittelun aikana. Aiemmin luotujen ympäristöjen omistajat, jotka käyttävät sisäistä pääsuunnittelumoduulia suunniteltuja tuotantotilauksia luomatta, saavat poikkeusprosessia koskevan sähköpostin. Siirtyminen suunnittelun optimointiin kannattaa arvioida ja suunnitella yhteistyössä kumppanin kanssa.

Ennen suunnittelun optimoinnin ottamista käyttöön on syytä arvioida suunnittelun optimoinnin sopivuusanalyysin tulokset. Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).

### <a name="availability"></a>Saatavuus
Suunnittelun optimointi on tällä hetkellä käytettävissä seuraavilla Azure-maantieteellisillä alueilla: Yhdysvallat, Kanada, Eurooppa, Iso-Britannia ja Australia. Jos yrität asentaa apuohjelman toiselta maantieteelliseltä alueelta, LCS näyttää sanoman, jonka mukaan tätä maantieteellistä aluetta ei tueta.

Huomaa, että suunnittelun optimointi ei tue Dynamics 365 Supply Chain Management -järjestelmän paikallisia käyttöönottoja.

### <a name="licensing"></a>Käyttöoikeudet

Jos voit suorittaa pääsuunnittelua nykyisellä käyttöoikeudella, suunnittelun optimoinnin käytön aloittamista varten ei tarvitse ostaa käyttöoikeutta.

### <a name="install-the-add-in"></a>Lisäosan asentaminen

Suunnittelun optimoinnin käyttöä varten on asennettava Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin lisäosa. Voit käyttää lisäosaa LCS-projektista ja ottaa suunnittelun optimointitoiminnon käyttöön Supply Chain Management -käyttöliittymässä.

> [!NOTE]
> Suunnittelun optimoinnin vaatimus on korkean käytettävyyden ympäristö, jossa LCS on käytössä, taso 2 tai korkeampi (ei OneBox-ympäristö). Käytössä on Dynamics 365 Supply Chain Management -sovelluksen versio 10.0.7 tai uudempi versio. Jos yrität asentaa apuohjelman OneBox-ympäristöön, asennus ei ole valmis ja sinun on peruutettava asennus.

1. Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.
1. Valitse **Kaikki tiedot**.
1. Vieritä alas **Ympäristön lisäosat** -pikavälilehteen.
1. Valitse **Asenna uusi lisäosa**.
1. Valitse **Suunnittelun optimointi**.
1. Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.
1. Valitse **Asenna**.
1. **Ympäristön lisäosat** -pikavälilehdessä pitäisi näkyä, että suunnittelun optimointia asennetaan.
1. Muutaman minuutin kuluttua arvon **Asennettaan** pitäisi muuttua arvoksi **Asennettu** (voi vaatia sivun päivityksen). Kun asennus on valmis, voit aktivoida suunnittelun optimoinnin Dynamics 365 Supply Chain Managementissa.

Suunnittelun optimoinnin apuohjelman asennuksen päätarkoitus on yhdistää palvelu ja ympäristö. Tämän vuoksi apuohjelma on asennettava erikseen jokaiseen ympäristöön, jossa suunnittelun optimointia käytetään, riippumatta ympäristöjen välillä siirrettävästä koodista riippumatta.

### <a name="planning-optimization-integration"></a>Suunnittelun optimoinnin integrointi

Voit määrittää, käytetäänkö suunnittelun optimoinnin lisää pääsuunnittelussa valitsemalla **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin parametrit**.

#### <a name="connection-status"></a>Yhteyden tila

Yhteyden tila ilmaisee Supply Chain Managementin ja suunnittelun optimointipalvelun välisen yhteyden nykyisen tilan. Mahdolliset arvot ovat seuraavassa taulukossa.

| Yhteyden tila | Kuvaus | Voiko suunnittelun optimointia käyttää? |
|---|---|---|
| Yhdistetty | Suunnittelun optimointipalvelun ja Supply Chain Managementin välille on muodostettu yhteys. | Kyllä |
| Otetaan yhteyttä käyttöön | Pyyntöä ottaa yhteys suunnittelun optimointipalveluun käsitellään. | Ei |
| Yhteys katkaistu | Suunnittelun optimointipalveluun ei ole yhteyttä. Yhteys voidaan ottaa käyttöön LCS:ssä aiemmin tässä ohjeaiheessa kuvatulla tavalla. | Ei |
| Poistettaan yhteyttä käytöstä | Pyyntöä katkaista yhteys suunnittelun optimointipalveluun käsitellään. | Ei |
| Tilan saaminen | Järjestelmä odottaa tilatietoja suunnittelun optimointipalvelusta. | Ei |

#### <a name="the-use-planning-optimization-option"></a>Käytä suunnittelun optimointia -vaihtoehto

**Käytä suunnittelun optimointia** -vaihtoehdossa valittu asetus määrittää, mitä suunnittelumoduulia pääsuunnittelussa käytetään:

- **Kyllä** – suunnittelun optimointia käytetään pääsuunnittelussa.
- **Ei** – Supply Chain Managementin sisäistä suunnittelumoduulia käytetään pääsuunnittelussa.

> [!NOTE]
> Jos Supply Chain Managementin sisäiselle suunnittelumoduulille aiemmin luodut suunnittelun erätyöt käynnistyvät, kun **Käytä suunnittelun optimointia** -asetuksena on **Kyllä**, kyseiset työt epäonnistuvat.

### <a name="integration-with-the-setup"></a>Integrointi määrityksiin

Jos suunnittelun optimointi on otettu käyttöön, suunnittelun optimoinnin apuohjelmaa käytetään pääsuunnittelussa. Tällä on vaikutusta pääsuunnittelun tuloksiin ja toimintoihin.

## <a name="additional-resources"></a>Lisäresurssit

[Esiversion ehdot](https://go.microsoft.com/fwlink/?linkid=2015274)

[Suunnittelun optimoinnin yleiskatsaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suodattimien käyttäminen suunnitelmaan](plan-filters.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]