---
title: Pääsuunnittelun aloittaminen
description: Tässä artikkelissa käsitellään Dynamics 365 Supply Chain Managementin pääsuunnittelun ominaisuuden käytön aloittamista.
author: t-benebo
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4b986461e90b356580da8a136c1da95e7dc64696
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780408"
---
# <a name="get-started-with-master-planning"></a>Pääsuunnittelun aloittaminen

[!include [banner](../../includes/banner.md)]

Supply Chain Managementin pääsuunnittelun tarjoajana on ulkoinen palvelu, jota kutsutaan Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin lisäosaksi. Tässä aiheessa kuvataan, miten tämä palvelu hankitaan ja määritetään.

## <a name="availability"></a>Saatavuus

Suunnittelun optimointi on tällä hetkellä käytettävissä seuraavilla Azuren maantieteellisillä alueilla: Yhdysvallat, Kanada, Brasilia, Eurooppa, Ranska, Yhdistynyt kuningaskunta, Norja, Sveitsi, Australia, Tyynenmeren Aasia, Japani ja Intia. Jos yrität asentaa apuohjelman toiselta maantieteelliseltä alueelta, LCS näyttää sanoman, jonka mukaan tätä maantieteellistä aluetta ei tueta. Lisätietoja Azuren maantieteellisistä alueista ja niihin liittyvistä alueista on ohjeaiheessa [Azuren maantieteelliset alueet](https://azure.microsoft.com/global-infrastructure/geographies/#geographies).

Huomaa, että suunnittelun optimointi ei tue Dynamics 365 Supply Chain Management -järjestelmän paikallisia käyttöönottoja.

## <a name="licensing"></a>Käyttöoikeudet

Jos voit suorittaa pääsuunnittelua nykyisellä käyttöoikeudella, suunnittelun optimoinnin käytön aloittamista varten ei tarvitse ostaa käyttöoikeutta.

## <a name="install-and-enable-planning-optimization"></a>Suunnittelun optimoinnin asentaminen ja ottaminen käyttöön

Suunnittelun optimoinnin käyttö edellyttää, että edellytykset täyttyvät järjestelmässä. Sen jälkeen käyttöoikeusavain otetaan käyttöön ja Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin apuohjelma asennetaan.

### <a name="prerequisites"></a>Edellytykset

Ennen kuin suunnittelu optimoinnin apuohjelma voidaan asentaa, seuraavien edellytysten on toteuduttava:

- Supply Chain Managementia on käytettävä korkean käytettävyyden ympäristössä, jossa LCS on käytössä, taso 2 tai korkeampi (ei OneBox-ympäristö). Käytössä on Dynamics 365 Supply Chain Managementin versio 10.0.7 tai uudempi versio. Jos yrität asentaa apuohjelman OneBox-ympäristöön, asennus ei ole valmis ja sinun on peruutettava asennus.

- Järjestelmä on määritettävä Power Platform -integrointia varten. Lisätietoja on kohdassa [Microsoft Power Platformin sekä talous- ja toimintosovellusten integrointi](../../../fin-ops-core/dev-itpro/power-platform/overview.md).

### <a name="enable-the-planning-optimization-license"></a>Suunnittelun optimoinnin käyttöoikeuden ottaminen käyttöön

Suunnittelun optimoinnin käyttäminen edellyttää, että sen määritysavain otetaan käyttöön. Toimi seuraavasti:

1. Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.
1. Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.
1. Valitse **Määritysavain**-välilehdessä **Suunnittelun optimointi** -valintaruutu.
1. Poista järjestelmän ylläpitotila käytöstä kohdassa [Ylläpitotila](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.

### <a name="install-the-planning-optimization-add-in"></a>Suunnittelun optimoinnin apuohjelman asentaminen

LCS-projektin apuohjelma on asennettava ja suunnittelun optimointitoiminto on otettava sitten käyttöön Supply Chain Management -käyttöliittymässä.

Suunnittelun optimoinnin apuohjelman asentaminen:

1. Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.
1. Valitse **Kaikki tiedot**.
1. Vieritä alas **Ympäristön lisäosat** -pikavälilehteen.
1. Valitse **Asenna uusi lisäosa**.
1. Valitse **Suunnittelun optimointi**.
1. Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.
1. Valitse **Asenna**.
1. **Ympäristön lisäosat** -pikavälilehdessä pitäisi näkyä, että suunnittelun optimointia asennetaan.
1. Muutaman minuutin kuluttua arvon **Asennettaan** pitäisi muuttua arvoksi **Asennettu** (voi edellyttää sivun päivittämistä). Kun asennus on valmis, voit aktivoida suunnittelun optimoinnin Dynamics 365 Supply Chain Managementissa.

Suunnittelun optimoinnin apuohjelman asennuksen päätarkoitus on yhdistää palvelu ja ympäristö. Tämän vuoksi apuohjelma on asennettava erikseen jokaiseen ympäristöön, jossa suunnittelun optimointia käytetään, riippumatta ympäristöjen välillä siirrettävästä koodista riippumatta.

## <a name="integrate-planning-optimization-with-your-system"></a>Suunnittelun optimoinnin integrointi järjestelmään

Voit määrittää, käytetäänkö suunnittelun optimoinnin lisää pääsuunnittelussa valitsemalla **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin parametrit**.

### <a name="connection-status"></a>Yhteyden tila

Yhteyden tila ilmaisee Supply Chain Managementin ja suunnittelun optimointipalvelun välisen yhteyden nykyisen tilan. Mahdolliset arvot ovat seuraavassa taulukossa.

| Yhteyden tila | Kuvaus | Voiko suunnittelun optimointia käyttää? |
|---|---|---|
| Yhdistetty | Suunnittelun optimointipalvelun ja Supply Chain Managementin välille on muodostettu yhteys. | Kyllä |
| Otetaan yhteyttä käyttöön | Pyyntöä ottaa yhteys suunnittelun optimointipalveluun käsitellään. | Ei |
| Yhteys katkaistu | Suunnittelun optimointipalveluun ei ole yhteyttä. Yhteys voidaan ottaa käyttöön LCS:ssä aiemmin tässä artikkelissa kuvatulla tavalla. | En |
| Poistettaan yhteyttä käytöstä | Pyyntöä katkaista yhteys suunnittelun optimointipalveluun käsitellään. | Ei |
| Tilan saaminen | Järjestelmä odottaa tilatietoja suunnittelun optimointipalvelusta. | Ei |

### <a name="the-use-planning-optimization-option"></a>Käytä suunnittelun optimointia -vaihtoehto

**Käytä suunnittelun optimointia** -vaihtoehdossa valittu asetus määrittää, mitä suunnittelumoduulia pääsuunnittelussa käytetään:

- **Kyllä** – suunnittelun optimointia käytetään pääsuunnittelussa.
- **Ei** – Vanhentunutta pääsuunnittelumoduulia käytetään pääsuunnittelussa.

Tämä asetus koskee kaikkia yrityksiä (yrityksiä). Suunnittelun optimointia ei voida käyttää joissakin yrityksissä ja vanhentunutta pääsuunnittelumoduulia muissa yrityksissä.

> [!NOTE]
> Jos vanhentuneelle pääsuunnittelumoduulille aiemmin luodut suunnittelun erätyöt käynnistyvät, kun **Käytä suunnittelun optimointia** -asetuksena on **Kyllä**, kyseiset työt epäonnistuvat.

### <a name="integration-with-the-setup"></a>Integrointi määrityksiin

Jos suunnittelun optimointi on otettu käyttöön, suunnittelun optimoinnin apuohjelmaa käytetään pääsuunnittelussa. Tällä on vaikutusta pääsuunnittelun tuloksiin ja toimintoihin.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
