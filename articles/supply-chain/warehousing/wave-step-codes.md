---
title: Aallon vaihekoodit
description: Tässä ohjeaiheessa on yleiskuvaus aallon vaihekoodeista ja niiden käytöstä.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992354"
---
# <a name="wave-step-codes"></a>Aallon vaihekoodit

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a>Tietoja aallon vaihekoodeista

Aallon vaihekoodit ovat koodeja, joita käyttäjät voivat määrittää ja käyttää aaltomenetelmien tiettyjen esiintymien linkittämiseksi vastaavaan malliin. Mallit sisältävät malleja täydennykselle, konttijärjestelmälle, etikettien tulostamiselle, kuormituksen luonnille ja lajittelulle.

Kun aallon vaihekoodeja ei käytetä, käyttäjien on kirjoitettava vapaamuotoista tekstiä viitatakseen aaltomenetelmän esiintymän tiettyyn malliin. Vapaamuotoinen teksti on altis virheille, koska käyttäjien on varmistettava, että heidän aaltomalliin tiettyä aallon vaihemenetelmää varten syöttämänsä aallon vaiheen teksti vastaa kohdemallissa olevaa aallon vaiheen tekstiä tarkalleen.

Tietyn aallon vaihetyypin aallon vaihekoodit määritetään erillisellä sivulla. Aallon vaihekoodi on valittava avattavasta luettelosta jokaiselle aaltomallin aallon vaiheen menetelmän esiintymälle, joka edellyttää aallon vaihekoodia. Avattavasta luettelosta tehty valinta korvaa syötetyn vapaamuotoisen tekstin ja auttaa vähentämään inhimillisten virheiden riskiä ja vaikutusta. Asetuskoodeja käytetään aaltomallissa oleva aallon vaiheen menetelmän linkittämiseksi menetelmän kohdemalliin.

> [!NOTE]
> Aallon vaihekoodien ominaisuuden käyttäminen on valinnaista, ja käyttö tapahtuu yrityskohtaisesti. Jos siis tietty yritys käyttää tätä ominaisuutta, kaikki kyseisen yrityksen olemassa olevat aallon vaihekoodit päivitetään uuteen rakenteeseen.

## <a name="setup-demo"></a>Asennuksen esittely 

Esittelytietojen on oltava asennettuna tätä esittelyä varten, ja sinun on käytettävä esittelytietojen **USMF**-yritystä.

### <a name="enable-wave-step-codes"></a>Ota käyttöön aallon vaihekoodit

Noudata seuraavia ohjeita ottaaksesi aallon vaihekoodien ominaisuuden käyttöön.

1. Siirry kohtaan **Varastonhallinta \> Asetukset \> Varastonhallinnan parametrit**.
2. Määritä **Yleinen**-välilehden **Aallon käsittely** -pikavälilehdessä **Ota käyttöön aallon vaihekoodit** -asetukseksi **Kyllä**.

Kaikki olemassa olevat aallon vaiheiden vapaamuotoiset tekstit päivitetään uuteen rakenteeseen. Kun tämä päivitys on suoritettu yritykselle, **Ota käyttöön aallon vaihekoodit** -asetus ei ole enää käytettävissä **Varastonhallinnan parametrit** -sivulla.

Vahvistukset tehdään päivityksen aikana, ja jos päivitys epäonnistuu, näet virhesanoman. Päivitys saattaa epäonnistua seuraavien ristiriitojen takia:

- Sinulla on identtisiä aallon vaiheiden vapaamuotoisia tekstejä.
- Sinulla on mukautuksia.
- Aallon vaiheen menetelmän esiintymään on liitetty aallon vaiheen vapaamuotoinen teksti, joka ei vastaa odotettua mallityyppiä.

Kun olet ratkaissut vahvistusten aikana havaitut ristiriidat, voit suorittaa päivitysprosessin uudelleen.

Kun päivitys on suoritettu onnistuneesti, **Aallon vaihekoodit** -sivu (**Varastonhallinta \> Asetukset \> Aallot \> Aallon vaihekoodit**) tulee saataville. Tällä sivulla on luettelo aallon vaihekoodeista, jotka päivitettiin, kun aallon vaiheenkoodien ominaisuus otettiin käyttöön.

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
