---
title: Vuokrauksen kirjaustyypit
description: Tässä ohjeaiheessa kuvataan kirjaustyypit, joita käytetään resurssien vuokratapahtumissa.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b7d8c545c1addaa570d54855bbad6c576783007
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229499"
---
# <a name="lease-posting-types"></a>Vuokrauksen kirjaustyypit

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kuvataan kirjaustyypit, joita käytetään resurssien vuokratapahtumissa.

## <a name="lease-asset"></a>Vuokraresurssi

Tili liittyy käyttöoikeusomaisuuserään. Tätä tiliä veloitetaan, kun vuokra kirjataan alun perin uusien vuokrauksen tilinpäätösstandardien ASC 842:n (Accounting Standards Codification Topic 842) ja IFRS 16:n (International Financial Reporting Standard 16) mukaan. Jos kyseessä on muokattu vuokra, tätä tiliä voidaan veloittaa tai hyvittää sen mukaan, lisääkö muokkaus vuokravelkaa vai vähentääkö se sitä.

**Esimerkki kirjauskansiovienneistä:** Alkuperäinen kirjaus<br>
**Veloitus:** Vuokrasopimuksen resurssi XXX<br>
**Hyvitys:** Vuokrasopimusvelka XXX

## <a name="lease-liability"></a>Vuokrasopimusvelka

Tili liittyy vuokrasopimusvelkaan, joka toteutuu kun maksut diskontataan uusien IFRS 16- ja ASC 842 -standardien mukaan. Tätä tiliä hyvitetään, kun vuokra kirjataan alun perin uusien standardien mukaan. Vuokrat veloitetaan ja korkokertymät hyvitetään.

**Esimerkki kirjauskansiovienneistä:** Alkuperäinen kirjaus<br>
**Veloitus:** Vuokrasopimuksen resurssi XXX<br>
**Hyvitys:** Vuokrasopimusvelka XXX

**Esimerkki kirjauskansiovienneistä:** Korkokertymä<br>
**Veloitus:** Korkokustannus XXX<br>
**Hyvitys:** Vuokrasopimusvelka XXX

**Esimerkki kirjauskansiovienneistä:** Vuokra<br>
**Veloitus:** Vuokrasopimusvelka XXX<br>
**Hyvitys:** Toimittajan maksettava / maksu XXX

## <a name="short-term-lease-liability"></a>Lyhytaikainen vuokravelka

Tili liittyy lyhytaikaiseen vuokrasopimusvelkaan, kun lyhytaikaisen vuokrasopimusvelan uudelleenluokittelun kirjauskansiovienti kirjataan. Tälle tilille hyvitetään lyhytaikainen velka kuoletusaikataulusta kuukauden viimeisenä päivänä. Sama summa veloitetaan kuitenkin seuraavan kuukauden ensimmäisenä päivänä.

**Esimerkki kirjauskansiovienneistä:** Lyhytaikaisen vuokrasopimusvelan uudelleenluokittelu<br>
**Veloitus:** Vuokrasopimusvelka XXX<br>
**Hyvitys:** Lyhytaikainen vuokrasopimusvelka XXX<br>
**Veloitus:** Lyhytaikainen vuokrasopimusvelka XXX<br>
**Hyvitys:** Vuokrasopimusvelka XXX

## <a name="depreciation-expense"></a>Poistokulu

Tili liittyy kuluun, joka liittyy käyttöoikeusomaisuuserän poistoon IFRS 16-, ASC 842- ja rahoitusleasingsopimusstandardeihin IAS 17:n ja ASC 840:n mukaan. Tätä tiliä veloitetaan, kun käyttöoikeusomaisuuserä poistetaan kuukausittain.

**Esimerkki kirjauskansiovienneistä:** Poistokertymä<br>
**Veloitus:** Poistokulu XXX<br>
**Hyvitys:** Kumulatiivinen poisto XXX

## <a name="gainloss-on-lease-modification"></a>Vuokranmuokkauksen voitto/tappio

Tili on liitetty voittoihin tai tappioihin, jotka vuokrasopimuksen muokkauksista saadaan. Voitto saatetaan saada vuokrasopimuksen muokkauksen aikana, jos muokkaus vähentää vuokrasopimusvelkaa summalla, joka ylittää käyttöoikeusomaisuuserän kirjanpitoarvon.

Vuokrasopimuksen nykyinen kirjanpitoarvo on esimerkiksi 150 000 $ ja käyttöoikeusomaisuuserän 100 000 $. Vuokrasopimusta muokataan, ja muokkaus tuottaa tulevalle vähimmäisvuokralle (PVFMLP) uuden arvon 40 000 $. Tämän vuoksi vuokrasopimusvelkaa veloitetaan 110 000 $:n verran (150 000–40 000 $). Koska käyttöoikeusomaisuuserän arvo on vain 100 000 $, 110 000 $:n arvoisen vähennyksen vuoksi erän arvo on alle 0 (nolla). Kirjanpidon ohjeissa sanotaan, että jäljellä oleva arvo tulee kirjata voittotilille. Tässä tapauksessa lopullinen kirjauskansiovienti on vuokrasopimusvelan veloitus (110 000 $), vuokrasopimuksen resurssin hyvitys (100 000 $) ja voittotilin hyvitys (10 000 $).

**Esimerkki kirjauskansiovienneistä:** Vuokrasopimuksen muokkaus<br>
**Veloitus:** Vuokrasopimusvelka XXX<br>
**Hyvitys:** Vuokrasopimuksen resurssi XXX<br>
**Hyvitys:** Voitto XXX

## <a name="accumulated-depreciation"></a>Kertynyt poisto

Tili on liitetty käyttöoikeusomaisuuserän vastatilille. Tätä tiliä hyvitetään poistokulun kirjaamisen yhteydessä.

**Esimerkki kirjauskansiovienneistä:** Poistokertymä<br>
**Veloitus:** Poistokulu XXX<br>
**Hyvitys:** Kumulatiivinen poisto XXX

## <a name="retained-earnings"></a>Jakamaton voitto

Kertyneisiin tuottoihin liittyvä tili. Tätä tiliä veloitetaan tai hyvitetään siirtymäoikaisun kirjauskansioviennissä käyttämällä kokonaan takautuvaa menetelmää tai päivittävää kumulatiivista vaihtoehto A -menetelmää. Alkuperäisen käyttöoikeusomaisuuserän ja vuokrasopimusvelan välinen ero kirjataan kertyneisiin tuottoihin. Harvoissa tapauksissa myös vuokrasopimuksen muokkaus vaikuttaa kertyneisiin tuottoihin, jos vuokrasopimuksen luokittelu muutetaan rahoitusleasingsopimuksesta käyttöleasingsopimukseksi ja käyttöoikeusomaisuuserä korotetaan tai alennetaan niin, että se vastaa vuokrasopimusvelkaa.

**Esimerkki kirjauskansiovienneistä:** Siirtymän oikaisu (kokonaan takautuva menetelmä tai päivittävä kumulatiivinen vaihtoehto A -menetelmä)<br>
**Veloitus:** Vuokrasopimusvelka XXX<br>
**Hyvitys:** Vuokrasopimuksen resurssi XXX<br>
**Hyvitys:** Kertynyt tuotto XXX

## <a name="variable-payment"></a>Muuttuva maksu

Tämä tili liittyy muuttuviin vuoksiin, jotka indeksin uudelleenarviointi luo ASC 842-, ASC 840- ja IAS 17 -vuokrasopimusten avulla. Vuokra-aikataulussa muuttuvat maksut sisältyvät **Muuttuva maksu** -sarakkeeseen. Tätä tiliä veloitetaan, kun lasku luodaan muuttuvan maksun sisältävälle maksuaikatauluriville.

**Esimerkki kirjauskansiovienneistä:** Vuokra<br>
**Veloitus:** Vuokrasopimusvelka XXX<br>
**Veloitus:** Muuttuva maksu XXX<br>
**Hyvitys:** Toimittajan maksettava / maksu XXX

## <a name="deferred-rent-asset-liability"></a>Toteutumaton vuokrauksen resurssi (velka)

Tili liitetään toteutumattomaan vuokrauksen resurssiin tai velkaan, jonka toteutumattoman vuokran käsittelyn vuokrasopimus luo. Tätä tiliä veloitetaan, kun lasku kirjataan toteutumattoman vuokran käsittelyn vuokrasopimuksen mukaan, jos vuokrasumma on enemmän kuin kauden suora vuokrakulu. Se hyvitetään, jos vuokra on vähemmän kuin kauden suora vuokrakulu.

**Esimerkki kirjauskansiovienneistä:** Vuokra (toteutumattoman vuokran käsittelyn vuokrasopimus)<br>
**Veloitus:** Vuokran kulu XXX<br>
**Hyvitys:** Toteutumattoman vuokran velka XXX<br>
**Hyvitys:** Toimittajan maksettava / maksu XXX

## <a name="lease-expense"></a>Vuokran kulu

Tili liittyy vuokran kuluun, jos vuokra luokitellaan toteutumattoman vuokran käsittelyn vuokrasopimukseksi. Tätä tiliä veloitetaan, kun lasku kirjataan toteutumattoman vuokran käsittelyn vuokrasopimuksen mukaan.

**Esimerkki kirjauskansiovienneistä:** Vuokra (toteutumattoman vuokran käsittelyn vuokrasopimus)<br>
**Veloitus:** Vuokran kulu XXX<br>
**Hyvitys:** Toteutumattoman vuokran velka XXX<br>
**Hyvitys:** Toimittajan maksettava / maksu XXX

## <a name="impairment-expense"></a>Arvonalennuksen kulu

Tilille kirjataan, kun vuokran arvoa alennetaan. Tätä tiliä veloitetaan, kun taas käyttöoikeusomaisuuserän tiliä hyvitetään suoraan.

**Esimerkki kirjauskansiovienneistä:** Vuokra<br>
**Veloitus:** Arvonalennuksen kulu XXX<br>
**Hyvitys:** Käyttöoikeusomaisuuserä XXX

## <a name="lease-payment"></a>Vuokra

Tilille kirjataan, jos **Maksu toimittajalle** -parametri on poistettu käytöstä. Tiliä hyvitetään toimittajan maksettavan sijaan, jos parametri on poistettu käytöstä.

**Esimerkki kirjauskansiovienneistä:** Vuokra<br>
**Veloitus:** Vuokrasopimusvelka XXX<br>
**Hyvitys:** Vuokra XXX

## <a name="expense-type-postings"></a>Kulutyypin kirjaukset

Kullekin kulutyypille valittua tiliä veloitetaan, kun luodaan maksu, jonka tyyppi on Kulu. Jos tilin kulutyypiksi on määritetty esimerkiksi **Vakuutus**, tiliä veloitetaan aina, kun lasku tai maksukirjauskansiovienti luodaan vakuutuskulun toimeenpanokustannusaikataulusta.

**Esimerkki kirjauskansiovienneistä:** Vakuutusmaksu<br>
**Veloitus:** Vakuutuskulutyypin tili XXX<br>
**Hyvitys:** Vastatili XXX

> [!NOTE]
> Vastatili valitaan toimeenpanokustannuksen maksuaikataulun rivien vuokratasolla. Tämä vastatili voidaan liittää toimittajaan tai kirjanpitotiliin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]