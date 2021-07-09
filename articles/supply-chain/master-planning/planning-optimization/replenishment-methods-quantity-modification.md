---
title: Täydennysmenetelmät ja määrän muokkaus
description: Tässä ohjeaiheessa on tietoja täydennystavoista suunnittelun optimoinnissa. Osassa kerrotaan myös, miten tuotteen usean tilauksen määrä vaikuttaa tulokseen.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261693"
---
# <a name="replenishment-methods-and-quantity-modification"></a>Täydennysmenetelmät ja määrän muokkaus

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa on tietoja täydennystavoista suunnittelun optimoinnissa. Osassa kerrotaan myös, miten tuotteen usean tilauksen määrä vaikuttaa tulokseen.

Täydennysmenetelmiä kutsutaan myös kattavuusmenetelmiksi ja eräsyiden koon menetelmiksi.

## <a name="coverage-codes"></a>Kattavuuskoodit

Suunnittelun optimointi voidaan määrittää käyttämään erilaisia täydennysmenetelmiä. Täydennysmenetelmät ovat tekniikoita, joiden avulla järjestelmä laskee vaatimuksia tuotteelle. Täydennysmenetelmät määritetään kattavuuskoodien avulla, jotka voit määrittää joko kattavuusryhmälle tai tuotteelle.

Suunnittelun optimoinnissa voidaan käyttää seuraavia kattavuuskoodeja:

- **Kausi** – Täydennysmenetelmä, joka yhdistää kausikohtaisen kysynnän tuotteen yhteen tilaukseen. Tilaus suunnitellaan kauden ensimmäiselle päivälle, ja sen määrä täyttää määritetyn kauden nettotarpeet. Kausi alkaa tuotteen ensimmäisestä kysynnästä ja kattaa määritetyn ajanjakson. Seuraava kausi alkaa tuotteen seuraavista tarpeista. *Kauden* kattavuuskoodia käytetään usein ei-ennustettavissa olevan varaston asettaan, vuodenajan vaikutteille tai suurille kustannuksille. Seuraavassa kuvassa on esimerkki.

    ![Esimerkki kauden kattavuuskoodin käytöstä](./media/coverage-code-period.png "Esimerkki kauden kattavuuskoodin käytöstä")

- **Vaatimus** – Täydennysmenetelmä, jossa järjestelmä luo nimikkeelle tarpeen mukaan suunnitellun osto-, siirto- tai tuotantotilauksen. Tätä menetelmää käytetään kalliita tuotteita varten, joilla on ajoittainen kysyntä. *Vaatimuksen* kattavuuskoodia käytetään usein konfiguroitavissa tuotteissa tai valmistus tilattaessa -tapauksissa. Seuraavassa kuvassa on esimerkki.

    ![Esimerkki vaatimuksen kattavuuskoodin käytöstä](./media/coverage-code-requirement.png "Esimerkki vaatimuksen kattavuuskoodin käytöstä")

- **Min./Maks.** – Täydennysmenetelmä perustuu varastotasoon. Se määrittää varaston täydennyksen tietylle tasolle, kun arvioitu käytettävissä olevan varaston taso alittaa tietyn raja-arvon. Täydennysmäärä on enimmäistason ja ennustetun käytettävissä olevan tason välinen erotus. *Min./maks.* -kattavuuskoodia käytetään usein ennustettavissa olevan varaston laatimiseen, korkean tason tai vähemmän kalliiden tuotteiden osalta. Seuraavassa kuvassa on esimerkki.

    ![Esimerkki min.-/maks.-kattavuuskoodin käytöstä](./media/coverage-code-min-max.png "Esimerkki min.-/maks.-kattavuuskoodin käytöstä")

- **Manuaalinen** –Täydennysmenetelmä, jossa järjestelmä ei ehdota tuotteelle osto-, siirto- tai tuotantotilauksia. Sen sijaan tuotteen suunnittelu vastaa tarvittavien tilausten luomisesta tuotteen täydentämiseen. *Manuaalista* kattavuuskoodia käytetään usein niiden tuotteiden yhteydessä, joista järjestelmän luomia suunniteltuja tilauksia ei ole tarkoitus luoda.

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a>Tilauksen määrän vaikutus oletustilausasetuksista

Voit määrittää vapautetun tuotteen **oletustilausasetus**-sivulla **ostotilauksen**, **varaston** ja **myyntitilauksen** pikavälilehtien seuraavat määräasetukset. ( **Varasto**-pikavälilehtiä käytetään sekä siirtotilauksissa että tuotantotilauksissa.)

- **Kerrannainen**– Suunnitelluista tilauksista tulee tämän määrän kerrannainen.

    Jos esimerkiksi **kerrannainen**-kentän arvo on *5*, tilauksen määrä voi olla 5, 10, 15, 20 ja niin edelleen.

- **Tilauksen vähimmäismäärä** – Suunniteltujen tilausten määrä ei ole pienempi kuin määritetty arvo.

    Jos tilauksen **vähimmäistilausmäärä**-kentän arvoksi määritetään esimerkiksi *10*, luodaan 10:n määrän suunniteltu tilaus, vaikka kysynnän täyttämiseen tarvitaan vain neljä.

- **Tilauksen enimmäismäärä** – Suunniteltujen tilausten määrä ei ylitä määritettyä arvoa. Jos kysyntä on suurempi kuin **Tilauksen enimmäismäärä** -arvo, luodaan useita suunniteltuja tilauksia sen kattamiseksi.

    Jos esimerkiksi **Tilauksen enimmäismäärä** -kentän arvoksi määritetään *100* ja kysyntä on 450, ohjelma luo neljä suunniteltua tilausta määrälle 100 ja yhden suunnitellun tilauksen määräksi 50.

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a>Esimerkkejä täydennyksestä, jotka käyttävät min./maks.-kohdetta. kattavuuskoodi

Jos tuotteen **Kerrannais**-kentässä ei ole arvoa **oletustilausasetus** sivulla ja jos käytössä on *minimi-/maksimiarvo*. täydennysmenetelmä, suunnittelun optimointi täydentää varaston, kun arvioitu käytettävissä olevan varaston taso alittaa tietyn raja-arvon.

Jos määrität tuotteelle useita määriä, *minimi-/maksimimäärä* täydennysmenetelmä muuttaa toimintatapaansa ja ottaa **kerrannais**-arvon huomioon.

Toisin sanoen suunnittelun optimointi täydentää varastoa määritetylle maksimitasolle, kun käytettävissä olevan varaston arvioitu taso on pienempi kuin määritetty minimitaso. Täydennysmäärän on kuitenkin oltava **Kerrannainen**-arvon kerrannainen.

Jos täydennysmäärä (maksimitason ja arvioidun varastotason välinen ero) ei ole määritetyn usean määrän kerrannainen, suunnittelun optimointi käyttää ensimmäistä mahdollista arvoa, joka yhdessä arvioidun käytettävissä olevan tason kanssa alittaa maksimitason. Jos summa on pienempi kuin vähimmäistaso, suunnittelun optimointi käyttää ensimmäistä arvoa, joka yhdessä arvioidun varastoarvon kanssa on maksimitasoa suurempi.

Seuraavissa osa-alueen esimerkeissä on esimerkkejä, jotka osoittavat, miten tuotteen usean tilauksen määrä vaikuttaa *minimi-/maksimi*-kentän tulokseen. täydennysmenetelmä.

### <a name="example-1"></a>Esimerkki 1

Tuotteella on seuraava konfiguraatio:

- **Kattavuuskoodi:** *Min./Maks.*
- **Minimi:** *15*
- **Maksimi:** *22*
- **Kerrannainen:** *0*

Tuotteella on 10 kappaletta käyttövarastoa, eikä siinä ole muuta kysyntää tai toimitusta.

Pääsuunnittelun ajon yhteydessä luodaan suunniteltu 12 kappaleen tilaus, joka täydentää varastoa maksimimäärään.

### <a name="example-2"></a>Esimerkki 2

Tuotteella on seuraava konfiguraatio:

- **Kattavuuskoodi:** *Min./Maks.*
- **Minimi:** *15*
- **Maksimi:** *22*
- **Kerrannainen:** *5*

Tuotteella on 10 kappaletta käyttövarastoa, eikä siinä ole muuta kysyntää tai toimitusta.

Kun pääsuunnittelu suoritetaan, luodaan suunniteltu 10 kappaleen tilaus (koska 15 kappaletta täydennystä sekä 10 käytettävissä olevan varaston kappaletta ylittävät enimmäismäärän).

### <a name="example-3"></a>Esimerkki 3

Tuotteella on seuraava konfiguraatio:

- **Kattavuuskoodi:** *Min./Maks.*
- **Minimi:** *21*
- **Maksimi:** *24*
- **Kerrannainen:** *5*

Tuotteella on 10 kappaletta käyttövarastoa, eikä siinä ole muuta kysyntää tai toimitusta.

Kun pääsuunnittelu suoritetaan, luodaan suunniteltu 15 kappaleen tilaus (koska 10 kappaletta täydennystä sekä 10 käytettävissä olevan varaston kappaletta alittavat vähimmäismäärän).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
