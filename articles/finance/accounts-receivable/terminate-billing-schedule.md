---
title: Laskutusaikataulujen lakkauttaminen
description: Tässä ohjeaiheessa on tietoja laskutusaikataulujen ja laskutusaikataulurivien lopettamisesta tilauslaskutuksen yhteydessä.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: df81cc888e893c6a4a127e1a43426a0a0b56f0d1
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8470452"
---
# <a name="terminate-billing-schedules"></a>Laskutusaikataulujen lakkauttaminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja laskutusaikataulujen ja laskutusaikataulurivien lopettamisesta tilauslaskutuksen yhteydessä. Kun laskutusaikataulu päätetään, sen tilana on oltava **Aktiivinen**. Sen tilana ei voi olla **Pidossa**. Samoin kun laskutusaikataulurivi päätetään, sen tilana on oltava **Aktiivinen**. Laskutusaikataulun otsikko-osaan ei vaikuta, kun laskutusaikataulun rivi päätetään.

Voit lopettaa laskutusaikataulun tai laskutusaikataulun rivin jossakin seuraavista paikoista:

- **Kaikki/aktiiviset laskutusaikataulut** -luettelosivu
- **Kaikki laskutusaikataulut** -sivulla tietty laskutusaikataulu
- **Kaikki laskutusaikataulut** -sivulla tietty laskutusaikataulurivi

> [!NOTE]
> Jos haluat lopettaa useita laskutusaikatauluja samanaikaisesti, käytä **useiden irtisanomisten käsittely** -sivua.

## <a name="terminate-a-billing-schedule-or-line"></a>Laskutusaikataulun tai -rivin lakkauttaminen

Voit lopettaa laskutusaikataulun tai laskutusaikataulun rivin seuraavien ohjeiden mukaan.

1. Valitse laskutusaikataulu tai laskutusaikataulun rivi ja valitse sitten **Lopeta**. 
2. Määritä **irtisanomispäivämäärä**-, **irtisanomistyyppi**- ja **syykoodi**-kentät.
3. Määritä **Hyvitysvaihtoehto**-kentän arvoksi **Hyvitys**.
4. Valitse **Lopeta**.

Laskutusaikataulun tila muuttuu valitsemasi irtisanomistyypin mukaan. Jos valitsit lopetustyypiksi **Jäljellä oleva lasku**, laskutusaikataulun kaikkien rivien tila on **Viimeinen laskutus**. Laskutusaikataulun tila on **aktiivinen**, kunnes viimeinen lasku käsitellään. Kun viimeinen lasku on käsitelty, tilaksi päivitetään **Päättynyt**. Jos valitsit lopetustyypiksi **Muokkaa aikataulua**, laskutusaikataulun tilaksi päivitetään välittömästi **Päättynyt**.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Laskutusaikataulun tai -rivin lopettaminen ja hyvityksen maksaminen

Voit lopettaa laskutusaikataulun tai laskutusaikataulun rivin ja maksaa hyvityksen seuraavien ohjeiden mukaan.

1. Valitse laskutusaikataulu tai laskutusaikataulun rivi ja valitse sitten **Lopeta**.
2. Määritä **Irtisanomispäivämäärä**-, **Irtisanomistyyppi**-, **Syykoodi**- ja **Hyvitysvaihtoehto**-kentät.
3. Valitse **Lopeta hyvityksen yhteydessä**. Näyttöön tulee **Joukkopäättämisen käsittely** -sivu, joka on suodatettu niin, että se näyttää laskutusaikataulun.
4. Valitse **Näytä esiversio** tarkastellaksesi laskutusaikataulun rivejä ja valitse sitten **Prosessi**.

Kun luotto on käsitelty, tarkista laskutusaikataulussa käytetty luotto avaamalla **Näytä laskutustiedot** -sivu. Jos hyvityssumma on suurempi kuin 0 (nolla), kaikki tulevat laskuttamattomat rivit poistetaan ja korvataan laskutustietoriveillä, jotka näyttävät laskutusaikatauluun kohdistetun luoton negatiiviset summat.

### <a name="view-example"></a>Näytä esimerkki

Laskutusaikataulussa on seuraavat tiedot:

- Aloituspäivä on 1.1.2020.
- Päättymispäivä on 31.12.2020.
- Laskutuskauden summa on 100,00 kuukaudessa.
- Laskutuskausille on luotu laskuja tammikuusta heinäkuuhun.
- Sopimuksen päättymispäivä on 15.6.2020.

Kun luotto-oikaisu käsitellään, kaikki tulevat laskutuskaudet (elokuu - joulukuu) poistetaan **Näytä laskutustiedot** -sivulta. Heinäkuun laskutuskauden jälkeen lisätään luotto-oikaisurivi:

- 16. kesäkuuta – 31. heinäkuuta, kredit-summa 150,00

Jos käytetään laskuttamaton tuotto -toimintoa, **laskuttamaton tuottokirjauskansion kirjauksen tarkistus** -sivu päivitetään irtisanomismerkinnän kanssa.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Laskutusaikataulun tai -rivin lopettaminen hyvitystä maksamatta

Voit lopettaa laskutusaikataulun tai laskutusaikataulun rivin ja ilman hyvityksen maksamista seuraavien ohjeiden mukaan.

1. Valitse laskutusaikataulu tai laskutusaikataulun rivi ja valitse sitten **Lopeta**.
2. Määritä **irtisanomispäivämäärä**-kenttä.
3. Määritä **Irtisanomistyyppi**-kentän arvoksi **Ei oikaisua**. **Hyvitysvaihtoehto**-kentän arvoksi määritetään automaattisesti **Ei hyvitystä**.
3. Määritä **Syykoodi**-kenttä.
4. Kirjoita **Irtisanomishuomautukset**-kenttään tarvittavat huomautukset.
5. Valitse **Lopeta**. 

Kun päättyminen käsitellään, kaikki irtisanomispäivämäärän jälkeiset laskutustietorivit poistetaan. (Nämä rivit sisältävät rivin, joka sisältää irtisanomispäivämäärän.) Laskuja ei voi luoda lopetetuille riveille. Jos työsuhteen päättyminen poistetaan, kaikki lopetetut rivit lisätään takaisin **Näytä laskutustiedot** -sivulle ja tulevat käyttöön laskutettavaksi.

## <a name="fields"></a>Kentät

**Näytä laskutustiedot** -sivu sisältää seuraavat kentät.

| Kenttä | Kuvaus |
|-------|-------------| 
| Työsuhteen loppumispäivämäärä | Valitse päivämäärä, jolloin haluat päättää laskutusaikataulun tai laskutusaikataulun rivin. |
| Irtisanomisen tyyppi | <p>Valitse päättämisen tyyppi:</p><ul><li>**Aikataulun oikaiseminen** – Voit poistaa rivin laskutuskaudet lopetuspäivänä ja muuttaa rivin tilaksi **Viimeinen laskutus**. Jos rivinimikkeelle on olemassa lykkäysaikataulu, se oikaistaan peruuttamalla summa, jota ei enää voida tunnistaa. Jos laskutuksen alkamispäivämäärä on päättymispäivän jälkeen, jäljellä olevat laskutuskaudet poistuvat.</li><li>**Jäljellä oleva lasku** – Lisää laskutuskauden jäljellä oleva summa irtisanomiskauteen ja muuta rivin tilaksi **Viimeinen laskutus**. Jos rivinimikkeelle on olemassa lykkäysaikataulu, myös lykkäyspäivämäärä päivitetään. Jos laskutuksen alkamispäivämäärä on päättymispäivämäärän jälkeen, kaikkien jäljellä olevien laskutuskausien kokonaissumma lisätään laskutuskauteen ja jäljellä olevat laskutuskaudet poistetaan.</li><li>**Ei oikaisua** – Voit lopettaa rivin laskutuskaudet määritettynä päättymispäivänä. Oikaisuja ei tehdä. Kun tämä irtisanomistyyppi on valittuna, **Hyvitysvaihtoehto**-kentän arvoksi määritetään **Ei hyvittämistä** ja **Suhteutetaan päivittäin** -kentän arvoksi määritetään **Ei**. Molemmista kentistä tulee vain luku -kenttiä, eikä niitä voi muuttaa.</li></ul> |
| Luottovaihtoehto | <p>Valitse, miten luottoa käytetään, kun laskutusaikataulun rivi päätetään:</p><ul><li>**Luotto-oikaisu** – Luo luotto-oikaisu laskutusaikataulua varten, kun rivi on päättynyt. Luotto-oikaisu näkyy laskutusaikataulun tulevalla laskutuskaudella. Oikaisu säätää automaattisesti myös seuraavan laskutuskauden laskun summaa, kunnes hyvitys on otettu laskutusaikatauluun.</li><li>**Myönnä hyvitys** – Luo hyvityslasku, kun laskutusaikataulu- tai laskutusaikataulurivi on päättynyt.</li><li>**Ei hyvitystä** – Älä luo luotto-oikaisua, kun laskutusaikataulu- tai laskutusaikataulurivi on päättynyt. Tämä vaihtoehto on käytettävissä vain, kun käytät **Ei oikaisua** -tyypin irtisanomista laskutusaikataulun päättämiseen.</li></ul><p>Oletusvaihtoehto on **Toistuvan sopimuslaskutuksen parametrit** -sivulla.</p> |
| Syykoodi | Valitse päättämisen syykoodi. |
| Syyn kuvaus | Syykoodin kuvaus. |
| Irtisanomisilmoitukset | Kirjoita mitä tahansa lopetukseen liittyviä huomautuksia. |

<!--## Additional information-->
