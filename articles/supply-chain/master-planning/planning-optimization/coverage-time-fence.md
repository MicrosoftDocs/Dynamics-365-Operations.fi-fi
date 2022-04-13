---
title: Kattavuuden aikarajat
description: Tässä aiheessa käsitellään kattavuuden aikarajojen määrittämistä suunnittelun optimointia käytettäessä. Kattavuuden aikaraja ilmaiseen suunnitteluhorisontin ja -rajoituksen.
author: t-benebo
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 12deca22fd6ff3cb4556e0525ab831e1aea0ee33
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468913"
---
# <a name="coverage-time-fences"></a>Kattavuuden aikarajat

[!include [banner](../../includes/banner.md)]

Tässä aiheessa käsitellään *kattavuuden aikarajojen* määrittämistä suunnittelun optimointia käytettäessä. Suunnittelijat voiva määrittää suunnitteluhorisontin (kattavuuden aikarajan päivinä) sekä jättää pois kyseisen horisontin ulkopuolella olevan kysynnän ja tarjonnan. Niinpä kattavuuden aikarajat auttavat estämään sellaiset sekaannusta aiheuttavat toimitusehdotukset, joihin ei tarvitse reagoida kuin vasta kuukausien kuluttua. Esimerkkejä ovat esimerkiksi seuraavan vuoden ennuste ja asiakastilaukset, joiden läpimenoaika ylittää selvästi normaalin.

Kattavuuden aikaraja on päivien määrä kuluvan päivän jälkeen (tai tarkemmin sanottuna päivän, jolloin suunnitteluajo tehdään), jolloin toimitus ja kysyntä suljetaan pois. Viiveiden estämiseksi on varmistettava, että kattavuuden aikaraja on pidempi kuin kokonaisläpimenoaika. Järjestelmän oletusarvo on 100 päivää.

Kattavuuden aikaraja voidaan määrittää kullekin seuraavalle tasolle:

- **Kattavuusryhmä** – kattavuuden oletusaikaraja voidaan määrittää kullekin kattavuusryhmälle.
- **Nimikekattavuus** – nimikkeelle määritystä kattavuusryhmästä peritty kattavuuden aikaraja voidaan ohittaa.
- **Pääsuunnitelma** – kattavuusryhmä- ja nimikkeen kattavuusasetuksista perityt kattavuuden aikarajat voidaan ohittaa.

Seuraavissa osissa käsitellään kattavuudenryhmän määrittämistä kullakin tasolla.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Kattavuusryhmän kattavuuden aikarajan määrittäminen

Kun kattavuusryhmälle määritetään kattavuuden aikaraja, asetus koskee kaikki kyseiseen ryhmään kuuluvia nimikkeitä (tuotteita). Tiettyjen nimikkeiden tai tiettyjen pääsuunnitelmien asetus voidaan kuitenkin ohittaa.

Kattavuusryhmän kattavuuden aikaraja määritetään seuraavasti:

1. Siirry kohtaan **Pääsuunnittelu \> Määritys \> Kattavuus \> Kattavuusryhmät**.
1. Valitse luettelossa aiemmin luotu kattavuusryhmä tai luo uusi kattavuusryhmä.
1. Määritä **Yleiset**-pikavälilehden **Kattavuuden aikaraja (päivää)** -kenttään se päivien lukumäärä, jota haluat käyttää kattavuusryhmän kattavuuden aikarajana.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Tietyn nimikkeen kattavuuden aikarajan määrittäminen

Jokainen nimike (tuote) kuuluu kattavuusryhmään. Jos nimikkeelle ei ole nimenomaisesti määritetty kattavuusryhmää, oletuskattavuusryhmää käytetään. Jokainen nimike perii kattavuusryhmän kattavuuden aikarajan. Tämä aikaraja voidaan kuitenkin tarvittaessa ohittaa tiettyjen nimikkeiden kohdalla.

Tietyn nimikkeen kattavuuden aikaraja määritetään seuraavasti:

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Valitse tuote ruudukossa.
1. Valitse toimintoruudun **Suunnitelma**-välilehden **Kattavuus**-ryhmässä **Nimikkeen kattavuus**.
1. Valitse tai luo **Nimikkeen kattavuus** -sivun **Yleiskatsaus**-välilehdessä sen toimipaikan rivi, jolle kattavuuden aikaraja halutaan määrittää.
1. Avaa valitun toimipaikan asetukset valitsemalla **Yleiset**-välilehti.
1. Valitse **Korvaa kattavuusryhmän asetukset** -valintaruutu.
1. Määritä **Kattavuuden aikaraja (päivää)** -kenttään se päivien lukumäärä, jota haluat käyttää nimikkeen kattavuuden aikarajana.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Tietyn pääsuunnitelman kattavuuden aikarajan määrittäminen

Kattavuuden aikaraja voidaan määrittää pääsuunnitelmatasolla. Tällä tavoin määritetään niiden päivien lukumäärä, jonka pääsuunnittelun laskenta kattaa pääsuunnittelussa. Tämä asetus ohittaa kaikki kattavuuden aika-asetukset, jotka on määritetty kullekin liittyvälle nimikkeelle ja kattavuusryhmälle.

Tietyn pääsuunnitelman kattavuuden aikaraja määritetään seuraavasti:

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse aiemmin luotu pääsuunnitelma luettelossa tai luo uusi pääsuunnitelma.
1. Määritä **Aikarajat päivissä** -pikavälilehden **Kattavuus**-asetukseksi *Kyllä*. Määritä sitten asetuksessa olevaan kenttään se päivien lukumäärä, jota haluat käyttää pääsuunnitelman kattavuuden aikarajana.

## <a name="considerations-for-coverage-time-fences"></a>Kattavuuden aikarajoissa huomioon otettavia seikkoja

Seuraavat seikat kannattaa ottaa huomioon kattavuuden aikarajoja määritettäessä:

- Kattavuuden aikarajat vaikuttavat vain pääsuunnittelun syöttötietoihin. Viivästysten tapahtuessa tuloksena olevissa suunnitelluissa tilauksissa saattaa olla kuluvan päivän jälkeinen päivämäärä, johon on lisätty kattavuuden aikaraja.
- Kattavuuden aikarajat määritetään kalenteripäivinä. Arkipäiviä käyttävät kalenterit eivät vaikuta aikarajan laskentaan. Esimerkiksi viikossa katsotaan aina olevan seitsemän päivää myös silloin, kun viikonloput on määritetty työaikakalenterissa suljetuiksi päiviksi.
- Tarvetapahtumia ei voi luoda millekään kattavuuden aikarajan ulkopuoliselle tarjonnalle ja kysynnälle.
- Jos hyväksytty tarjonta ja kysyntä sijoittuu kattavuuden aikarajan ulkopuolelle, sitä ei ladata moduuliin. Niinpä ei käynnistä täydennystä eikä viiveitä lasketa. Tätä tarjontaa ja kysyntää ei kuitenkaan kannata poistaa järjestelmästä.
- Varmuusvarastomäärien vaihtelut (minimitunnisteista) ohitetaan, jos ne ovat kattavuuden aikarajan ulkopuolella.
- Konsernin sisäinen kysyntä ohitetaan, jos laskettu pyydetty lähetyspäivämäärä on kattavuuden aikarajan ulkopuolella. Huomaa, että sisäisessä pääsuunnittelussa kattavuuden aikaraja ei rajoita konsernin sisäistä kysyntää.
- Kysynnän ennusteet ohitetaan, jos budjettipäivämäärä on kattavuuden aikarajan ulkopuolella. Huomaa, että sisäisessä pääsuunnittelussa kattavuuden aikaraja ei rajoita kysynnän ennusteita.
- Suunnittelun optimointi ottaa aikavyöhykkeet huomioon. Se ottaa huomioon tarjonnan ja kysynnän toimipaikan aikavyöhykkeen ja suunnitteluajon ajankohdan. Esimerkki: Pääsuunnittelu käynnistetään 15. lokakuuta klo 11 Tanskassa sijaitsevassa toimipaikassa (GMT+1 aikavyöhyke), ja kattavuuden aikarajana käytetään 10 päivää. Tässä tapauksessa tarjonta ja kysyntä Seattlen toimipaikassa (GMT-8 aikavyöhyke) otetaan huomioon 25. lokakuuta klo 2.00 saakka (= kymmenen 24 tunnin päivää pääsuunnittelun käynnistymisen jälkeen, josta on vähennetty aikavyöhyke-eron vuoksi 9 tuntia). Huomaa, että sisäinen pääsuunnittelumoduuli ottaa huomioon vain aikarajan päivämäärän. Tämän vuoksi tuloksissa voi olla eroja.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]