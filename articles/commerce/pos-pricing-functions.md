---
title: Myyntipisteen hinnoittelutoiminnot
description: Tässä artikkelissa kuvataan Microsoft Dynamics 365 Commercen myyntipistesovelluksen (POS) eri hinta- ja alennustoiminnot.
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 210798ac192ee251594ec8ff9d23dab31ec2043e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473684"
---
# <a name="pricing-functions-in-pos"></a>Myyntipisteen hinnoittelutoiminnot

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan Microsoft Dynamics 365 Commercen myyntipistesovelluksen (POS) eri hinta- ja alennustoiminnot.

Dynamics 365 Commercen myyntipistesovellus sisältää useita monipuolisia ominaisuuksia, joiden avulla eturivin työntekijät voivat suorittaa Store Commercen toimintoja. Seuraava taulukko esittää hinta- ja alennustoiminnot, jotka ovat käytettävissä sovelluksessa tällä hetkellä.

| Toiminto                       | Myyntipisteen toiminnot |
|--------------------------------|----------------|
| Näytä hinnat                    | [Hinnantarkistus](#price-check) |
| Näytä alennukset                 | [Näytä kaikki alennukset](#view-all-discounts)<br>[Näytä käytettävissä olevat alennukset](#view-available-discounts) |
| Ohita hinnat                | [Hinnan ohitus](#price-override) |
| Lisää tai poista alennuksia      | [Rivialennuksen summa](#line-discount-amount)<br>[Rivialennusprosentti](#line-discount-percent)<br>[Alennuksen kokonaissumma](#total-discount-amount)<br>[Kokonaisalennusprosentti](#total-discount-percent)<br>[Poista järjestelmäalennukset tapahtumasta](#remove-system-discounts-from-transaction)<br>[Kohdista järjestelmäalennukset uudelleen](#reapply-system-discounts) |
| Lisää tai poista kuponkeja        | [Lisää kuponkikoodi](#add-coupon-code)<br>[Poista kuponkikoodi](#remove-coupon-code) |
| Laske hinnat ja alennukset | [Laske uudelleen](#recalculate) |

Lisätietoja siitä, kuinka nämä toiminnot voidaan määrittää myyntipistesovelluksessa ja tukevatko ne offline-tilaa, on kohdassa [Myyntipisteen toiminnot (POS) verkossa ja paikallisesti](pos-operations.md).

## <a name="price-check"></a>Hinnantarkistus

**Hinnantarkistus**-toiminto sallii myyntipisteen käyttäjiä hakea valmiiksi määritettyjä hintoja tietylle tuotteelle.

## <a name="view-all-discounts"></a>Näytä kaikki alennukset

**Näytä kaikki alennukset** -toiminto sallii myyntipisteen käyttäjiä hakea kaikkia tällä hetkellä kauppakanavalle voimassa olevia kampanjoita. Tarkalleen ottaen tämä toiminto näyttää luettelon alennuksista, jotka vastaavat jotakin seuraavista ehdoista:

- Alennuksen hintaryhmä vastaa myymälän hintaryhmää.
- Alennuksen hintaryhmä yhdistetään liitokseen tai kanta-asiakasohjelmaan.
- Alennuksen hintaryhmä on liitetty myymälään liittyvään luetteloon.

**Näytä kaikki alennukset** -toiminto näyttää vain alennukset, jotka eivät kilpaile minkään jo lisätyn alennuksen kanssa. Näin varmistetaan, että jos myyjä kertoo asiakkaalle alennuksesta ja asiakas tekee vaaditun toiminnon (esimerkiksi ostaa yhden lisänimikkeen ja saa 10 prosenttia alennusta), alennus kohdistetaan tapahtumaan. Kuponkiin perustuvat alennukset näytetään vain, jos **Käytä ilman kuponkikoodia** -parametri on käytössä.

Myyntipistekäyttäjät voivat hakea alennuksia nimen ja kuvauksen perusteella **Näytä kaikki alennukset** -toiminnolla ja suodattaa alennuksia sen mukaan, edellyttävätkö ne kuponkia.

## <a name="view-available-discounts"></a>Näytä käytettävissä olevat alennukset

**Näytä käytettävissä olevat alennukset** -toiminto sallii myyntipisteen käyttäjien tarkastella kaikkia alennuksia, jotka koskevat tapahtuman valittua riviä tai koko tapahtumaa. Valittua riviä koskevat alennukset sisältävät jo lisätyt alennukset sekä alennukset, joita ei ole vielä lisätty, mutta jotka voidaan lisätä (esimerkiksi lisää nimikkeitä vaativat yhdistelmäalennukset). Jos sovellettava alennus on linkitetty kuponkeihin, joissa on **Käytä ilman kuponkikoodia** -parametri käytössä, myyntipisteen käyttäjä voi käyttää tämän toiminnon sisäistä **Käytä kuponkia** -toimintoa lunastaakseen kupongin suoraan syöttämättä tai skannaamatta kuponkikoodeja tai kuponkien viivakoodeja.

## <a name="price-override"></a>Hinnan ohitus

**Hinnan ohitus** -toiminto sallii myyntipisteen käyttäjien korvata tuotteen myyntihinnan tapahtumassa. Tämä toiminto toimii vain tuotteille, jotka on määritetty sallimaan hinnan ohitukset.

## <a name="line-discount-amount"></a>Rivialennuksen summa

**Rivialennuksen summa** -toiminto sallii myyntipisteen käyttäjien syöttää tapahtumassa olevalle rivinimikkeelle alennussumman. Tämä toiminto koskee vain alennuskelpoisia nimikkeitä ja noudattaa **Suurin rivialennussumma** -arvoa, joka on määritetty käyttäjälle myyntipisteen käyttöoikeusryhmässä.

## <a name="line-discount-percent"></a>Rivialennusprosentti

**Rivialennusprosentti**-toiminto sallii myyntipisteen käyttäjien syöttää tapahtumassa olevalle rivinimikkeelle alennusprosentin. Tämä toiminto koskee vain alennuskelpoisia nimikkeitä ja noudattaa **Suurin sallittu rivialennusprosentti** -arvoa, joka on määritetty käyttäjälle myyntipisteen käyttöoikeusryhmässä.

## <a name="total-discount-amount"></a>Alennuksen kokonaissumma

**Alennuksen kokonaissumma** -toiminto sallii myyntipisteen käyttäjien syöttää tapahtumalle alennussumman. Tämä toiminto koskee vain alennuskelpoisia nimikkeitä ja noudattaa **Suurin kokonaisalennussumma** -arvoa, joka on määritetty käyttäjälle myyntipisteen käyttöoikeusryhmässä. Jos syötetty alennussumma ylittää suurimman sallitun kokonaisalennussumman, toiminto estetään eikä käyttöoikeuksien ohituksen työnkulkua käynnistetä. Tällä hetkellä kokonaisalennussummaa ei voi käyttää ostoskorissa, jossa on myyntinimikkeiden ja palautusnimikkeiden yhdistelmä.

## <a name="total-discount-percent"></a>Kokonaisalennusprosentti

**Kokonaisalennusprosentti**-toiminto sallii myyntipisteen käyttäjien syöttää tapahtumalle alennusprosentin. Tämä toiminto koskee vain alennuskelpoisia nimikkeitä ja noudattaa **Suurin sallittu kokonaisalennusprosentti** -arvoa, joka on määritetty käyttäjälle myyntipisteen käyttöoikeusryhmässä. Jos syötetty alennusprosentti ylittää suurimman sallitun kokonaisalennusprosentin, toiminto estetään eikä käyttöoikeuksien ohituksen työnkulkua käynnistetä. Tällä hetkellä kokonaisalennusprosenttia ei voi käyttää ostoskorissa, jossa on myyntinimikkeiden ja palautusnimikkeiden yhdistelmä.

## <a name="remove-system-discounts-from-transaction"></a>Poista järjestelmäalennukset tapahtumasta

**Poista järjestelmäalennukset tapahtumasta** -toiminto sallii myyntipisteen käyttäjien tyhjentää kaikki lisätyt järjestelmäasetukset (mukaan lukien kuponkeihin perustuvat alennukset) tapahtumasta. Kun tämä toiminto on suoritettu, hinnoittelumoduuli jättää järjestelmäalennukset vastaedes pois alennusten laskutoimista. **Poista järjestelmäalennukset tapahtumasta** -toiminto ei poista manuaalisia alennuksia.

## <a name="reapply-system-discounts"></a>Kohdista järjestelmäalennukset uudelleen

**Kohdista järjestelmäalennukset uudelleen** -toiminto sallii myyntipisteen käyttäjien lisätä järjestelmän laskemat alennukset uudelleen tapahtumaan, jos alennukset poistettiin **Poista järjestelmäalennukset tapahtumasta** -toiminnolla. Kun tämä toiminto on suoritettu, hinnoittelumoduuli laskee järjestelmäalennukset vastaedes mukaan alennusten laskutoimiin.

## <a name="add-coupon-code"></a>Lisää kuponkikoodi

**Lisää kuponkikoodi** -toiminto sallii myyntipisteen käyttäjien lisätä tapahtumaan kupongin syöttämällä kuponkikoodin. Myyntipisteen käyttäjät voivat myös skannata kupongin viivakoodin tai syöttää sen numeronäppäimistön avulla **Tapahtumat**-ruudussa.

## <a name="remove-coupon-code"></a>Poista kuponkikoodi

**Poista kuponkikoodi** -toiminto sallii myyntipisteen käyttäjien valita tai poistaa kuponkeja, jotka ovat tällä hetkellä voimassa tapahtumassa.

## <a name="recalculate"></a>Laske uudelleen

**Laske uudelleen** -toiminto sallii myyntipisteen käyttäjien käynnistää hinnoittelun laskennan tarvittaessa. Tämä toiminto on pakollinen, kun hinnan lukitus ja/tai viivytetty hinnan laskenta on käytössä ja myyntipisteen käyttäjä haluaa laskea hinnat ja alennukset uudelleen ostoskoriin tai tilaukseen tehtyjen muutosten jälkeen. **Laske uudelleen** -toiminto laskee aina koko tilauksen uudelleen. Sitä ei voi käyttää valittujen myyntirivien laskemiseksi uudelleen. Jotta myyntipisteen käyttäjät voisivat lisätä manuaalisia alennuksia lukitulle myyntiriville myyntipisteessä, heidän täytyy käyttää ensin **Laske uudelleen** -toimintoa avatakseen kaikkien myyntirivien lukituksen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
