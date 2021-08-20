---
title: Aallon vaihekoodit
description: Tässä ohjeaiheessa on yleiskuvaus aallon vaihekoodeista ja niiden käytöstä.
author: josaw1
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 47ec1319c7d1dde151f63e7e37e86c0265d84089f4d0366dea9310bda49c859d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780431"
---
# <a name="wave-step-codes"></a>Aallon vaihekoodit

[!include [banner](../includes/banner.md)]

Aallon vaihekoodit ovat koodeja, joita käyttäjät voivat määrittää ja käyttää aaltomenetelmien tiettyjen esiintymien linkittämiseksi vastaavaan malliin. Mallit sisältävät malleja täydennykselle, konttijärjestelmälle, etikettien tulostamiselle, kuormituksen luonnille ja lajittelulle.

Kun aallon vaihekoodeja ei käytetä, käyttäjien on kirjoitettava vapaamuotoista tekstiä viitatakseen aaltomenetelmän esiintymän tiettyyn malliin. Vapaamuotoinen teksti on altis virheille, koska käyttäjien on varmistettava, että heidän aaltomalliin tiettyä aallon vaihemenetelmää varten syöttämänsä aallon vaiheen teksti vastaa kohdemallissa olevaa aallon vaiheen tekstiä tarkalleen.

Tietyn aallon vaihetyypin aallon vaihekoodit määritetään erillisellä sivulla. Aallon vaihekoodi on valittava avattavasta luettelosta jokaiselle aaltomallin aallon vaiheen menetelmän esiintymälle, joka edellyttää aallon vaihekoodia. Avattavasta luettelosta tehty valinta korvaa syötetyn vapaamuotoisen tekstin ja auttaa vähentämään inhimillisten virheiden riskiä ja vaikutusta. Asetuskoodeja käytetään aaltomallissa oleva aallon vaiheen menetelmän linkittämiseksi menetelmän kohdemalliin.

> [!NOTE]
> Aallon vaihekoodien käyttö on valinnaista. Se on käytössä koko organisaation laajuisesti kaikille yrityksille.

## <a name="setup-demo"></a>Asennuksen esittely 

Esittelytietojen on oltava asennettuna tätä esittelyä varten, ja sinun on käytettävä esittelytietojen **USMF**-yritystä.

### <a name="enable-wave-step-codes"></a>Ota käyttöön aallon vaihekoodit

Noudata seuraavia ohjeita ottaaksesi aallon vaihekoodien ominaisuuden käyttöön.

1. Mene **Toimintojen hallintaan**.
2. Valitsemalla tämän voit ottaa käyttöön **Organisaation laajuisen Wave Step-koodin**.

Kaikki olemassa olevat aallon vaiheiden vapaamuotoiset tekstit päivitetään uuteen rakenteeseen kaikissa yrityksissä. Kun tämä päivitys on valmis kaikille yrityksille, ominaisuus on käytössä. Jos toimintoa ei voi ottaa käyttöön yhdelle tai useammalle yritykselle, ominaisuus ei ole käytössä millekään yritykselle.

Käyttöönoton aikana validoinnit tehdään tietojen päivityksen aikana. Jos päivitys epäonnistuu, näyttöön tulee virhesanoma. Päivitys saattaa epäonnistua seuraavien ristiriitojen takia:

- Sinulla on identtisiä aallon vaiheiden vapaamuotoisia tekstejä.
- Sinulla on mukautuksia.
- Aallon vaiheen menetelmän esiintymään on liitetty aallon vaiheen vapaamuotoinen teksti, joka ei vastaa odotettua mallityyppiä.

Kun olet ratkaissut vahvistusten aikana havaitut ristiriidat, voit yrittää ottaa ominaisuuden uudelleen käyttöön.

Kun ominaisuus on otettu onnistuneesti käyttöön, **Aallon vaihekoodit** -sivu (**Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit**) tulee saataville. Tällä sivulla on luettelo aallon vaihekoodeista, jotka päivitettiin, kun organisaationlaajuinen aallon vaihekoodi -ominaisuus otettiin käyttöön.

### <a name="create-new-wave-step-codes"></a>Uusien aallon vaihekoodien luominen

Voit käyttää **Aallon vaihekoodit** -sivua luodaksesi ja poistaaksesi aallon vaihekoodeja.

Jokaisen uuden aallon vaihekoodin ja siihen liittyvän tunnuksen on oltava yksilöllisiä kaikkien aallon vaihetyyppien keskuudessa, ja ne on määritettävä tietylle aallon vaihetyypille.

### <a name="apply-wave-step-codes"></a>Aallon vaihekoodien soveltaminen

Kun olet määrittänyt sopivat aallon vaihekoodit, niitä voidaan soveltaa aallon käsittelymenetelmille.

Siirry asiaankuuluvaan kohdemalliin soveltaaksesi aallon vaihekoodeja. Alla on kohdemallit, joihin aallon vaihekoodit on määritetty osoittamaan:

- **Täydennysmallit:** Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit
- **Kuormituksen luonnin mallipohjat:** Varastonhallinta \> Asetukset \> Kuormitus \> Kuormituksen luonnin mallipohjat
- **Lajittelumallit:** Varastonhallinta \> Asetukset \> Pakkaus \> Lähtevät lajittelumallit
- **Konttijärjestelmän mallit:** Varastonhallinta \> Asetukset \> Kontit \> Kontin rakennusmallit
- **Etikettien tulostusmallit:** Varastonhallinta \> Asetukset \> Asiakirjan reititys \> Aallon etikettimallit

Tässä luettelossa olevia malleja käytetään, kun niihin viitataan aaltomallissa valitusta aallon käsittelymenetelmästä. Kun aaltomallissa olevan aallon käsittelymenetelmän aallon vaihekoodi vastaa jossakin mallityypissä olevaa aallon vaihekoodia, mallia käytetään.

### <a name="sample-scenario"></a>Esimerkkiskenaario

Seuraava toimenpide auttaa varmistamaan, että luomasi täydennysmalli otetaan käyttöön aaltomallille.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit** ja luo aiheen vaihekoodi **Täydennys**-tyypille.
2. Siirry kohtaan **Varastonhallinta \> Asetukset \> Täydennys \> Täydennysmallit** ja luo täydennysmalli.
3. Valitse täydennysmallista aallon vaihekoodi, jonka loit **Täydennys**-tyypille.
4. Siirry kohtaan **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit** ja valitse aaltomalli, jota haluat käyttää.
5. Valitse mallin **Menetelmät**-pikavälilehdestä **Täydennys**-menetelmä.
6. Valitse **Aallon vaihekoodi** -kentästä aallon vaihekoodi, jonka valitsit täydennysmallille.

Nämä vaiheet suoritetaan kullekin yritykselle.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]