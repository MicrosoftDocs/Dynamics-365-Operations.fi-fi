---
title: Miksi tapahtuman palauttaminen ei onnistu?
description: Tässä artikkelissa käsitellään syitä, miksi tapahtumien palauttaminen ei onnistu. Siinä käsitellään myös tämän ongelman ratkaisuja.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9a8b26584b1a9b82440583db693cd14daa580e22
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876179"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Miksi tapahtuman palauttaminen ei onnistu?

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään syitä, miksi tapahtumien palauttaminen ei onnistu. Siinä käsitellään myös tämän ongelman ratkaisuja.

## <a name="symptom"></a>Oire

Organisaatiot voivat kohdata tilanteita, joissa kirjattu tapahtuma on palautettava. Aina joskus järjestelmä ei salli kyseisten tapahtumien palauttamista. Tämän seurauksena esiin nousee kaksi kysymystä:

- Miksi tapahtumaa ei voi palauttaa?
- Miten joukkoperuutusominaisuus vaikuttaa tähän toimintaan?

## <a name="resolution"></a>Ratkaisu

Tiettyjen ehtojen on täytyttävä, ennen kuin tapahtumia voidaan palauttaa. Tämän artikkelin muissa osissa käsitellään kunkin moduulin vahvistusta. Vaikka tässä artikkelissa keskitytään Microsoft Dynamics 365 Financen tapahtumiin, jotkin käsitteet ja vahvistus koskevat myös muita sovelluksia,kuten Dynamics 365 Supply Chain Managementia.

Lisäksi kohta, jossa tapahtuma palautetaan, voi vaikuttaa siihen, onko tapahtuman palauttaminen mahdollista. Esimerkiksi sekkinä kirjattu toimittajamaksu voidaan palauttaa vain pankkitilien tapahtumasivun **Sekit**-osassa. Sitä ei voi palauttaa kirjanpidon **Tositetapahtumat**-sivulla.

Jos **Useiden asiakirjojen joukkoperuutus** -ominaisuus (jota kutsutaan myös joukkoperuutusominaisuudeksi) on otettu käyttöön **Ominaisuuksien hallinta** -työtilassa, se vaikuttaa siihen, kuinka monta tapahtumaa voidaan palauttaa ja missä ne voidaan palauttaa. Käyttöönotettuna ominaisuudella on kaksi etua:

- Joissakin tapahtumatyypeissä kerralla voidaan valita ja palauttaa useita tapahtumia siitä kirjauskansiosta, josta tapahtuma kirjattiin. Vaihtoehtoisesti voidaan käyttää **Tositetapahtumat**-sivua. Yksittäisten tapahtumien on kuitenkin oltava palautettavissa, ennen kuin ominaisuus otettiin käyttöön. Ennen tämän ominaisuuden käyttöönottoa, tapahtumat oli palautettava yksi kerrallaan.
- *Jotkin* alareskontran tapahtumat voidaan peruuttaa kirjauskansiosta tai **Tositetapahtumat**-sivulta. Niitä ei tarvitse palauttaa alareskontran sivulta. Esimerkiksi toimittajan laskukirjauskansio voitiin aiemmin palauttaa vain **Toimittajan tapahtumat** -sivulta. Tällainen lasku voidaan kuitenkin palauttaa nyt myös kirjanpidosta, kirjauskansiosta tai **Tositetapahtumat**-sivulta. Kussakin tämän artikkelin osassa käsitellään tapahtumatyypit, joissa tätä mahdollisuutta ei ole.

Joukkoperuuttamisominaisuus **ei** anna mahdollisuutta entistä useampien tapahtumatyyppien palauttamiseen. Jos tapahtumatyyppiä ei voitu aiemmin palauttaa, siltä ei voi edelleenkään palauttaa, vaikka ominaisuus olisi otettu käyttöön. Esimerkiksi ostotilauksen toimittajan laskuja ei voi palauttaa riippumatta siitä, onko joukkoperuuttamisominaisuus otettu käyttöön vai ei.

Lisätietoja joukkoperuuttamisominaisuudesta on kohdassa [Käänteinen kirjauskansion kirjaus](reverse-journal-posting.md).

## <a name="general-ledger"></a>Kirjanpito

Kirjanpidon oikaisut kirjataan vain kirjanpitotilejä käyttämällä. Tämän vuoksi ne päivittävät vain kirjanpidon.

Jos joukkopalautusominaisuus on poistettu käytöstä, useimmat kirjanpidon oikaisut voidaan palauttaa yksitellen kirjanpidon (**LedgerTransAccount**) **Kohteen \<main account\> tapahtumat** -sivulla . (Sivun tarkka otsikko vaihtelee valitun päätilin mukaan.) Sivulla näkyy jokainen päätilille kirjattu tapahtuma. Se avataan yleensä **Pääkirja**-luettelosivulta tai valitsemalla **Tapahtumat** **Tositetapahtumat**-sivulla.

Jos joukkopalautusominaisuus on otettu käyttöön, ainakin yksi kirjanpitotosite voidaan nyt palauttaa **Tositetapahtumat**-sivulta ja siitä kirjauskansiosta, josta tapahtuma kirjattiin. Poikkeuksia ovat kirjanpidon ulkomaanvaluutan uudelleenarvostus-, konsolidointi- ja tilinpäätöstapahtumat. Nämä tapahtumat palautetaan sivuilta, joilta tilinpäätös suoritettiin.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Tapahtumien palauttamisen estäviä syitä

Tapahtumia ei voi palauttaa seuraavien syiden vuoksi:

- Kirjauskansio:

    - Tilikausi on pidossa tai suljettu pysyvästi:

        - Jos palautuspäivämäärä on suljetulla tilikaudella, tapahtumaa ei voi palauttaa.
        - Jos tapahtuma tukee palautuspäivämäärän kirjausta, tapahtuma voi silti palauttaa muuttamalla palautuspäivämäärä avoimelle kaudelle.

    - Tilinpäätösprosessi on suoritettu:

        - Tapahtuman kirjauspäivä on tilikaudella, jolle on tehty tilinpäätös. Vaikka tilikauden kausi voi olla edelleen avoinna, tapahtumaa ei voi palauttaa, jos tilinpäätösprosessi on suoritettu tilikauden osalta. Tilikauden tila ei ole sama kuin siinä olevien kausien tila.
        - Tilinpäätös voidaan palauttaa, jonka jälkeen tapahtuma voidaan palauttaa. Tämän menetelmän käyttäminen ei ole ehkä mahdollista. Tilikauden lopetusprosessin tilan perusteella voikin olla kätevämpää kirjata manuaalinen palautustapahtuma joko suljetun tilikauden tai seuraavan tilikauden avoimella kaudella. Jos uusi tapahtuma kirjataan sellaisen tilikauden avoimeen kauteen, jossa tilinpäätösprosessi on tehty, tilinpäätös on suoritettava uudelleen.

    - Tapahtuman palautuksen käsittely on keskeneräinen:

        - Jos tapahtumaan ollaan jo palauttamassa, kyseinen prosessi on suoritettava loppuun. Erillistä palautusprosessia ei voida tehdä. 
        - Kun palautus on valmis, palautettu tapahtuma voidaan palauttaa uudelleen. (Palautus voidaan siis peruuttaa).

    - Tapahtuman selvitys:

        - Jos vähintään yhden tapahtumarivin tapahtuman selvitykseen on käytetty kausittaista **Tapahtuman selvitykset** -tapahtumaa (**Kirjanpito \> Kausittaiset tehtävät \> Tapahtuman selvitykset**) siten, että tietue sijaitsee LedgerTransSettlement-taulukossa, tapahtumaa ei voi palauttaa.
        - Tapahtuman selvitys voidaan palauttaa, jonka jälkeen voidaan palauttaa tosite.

    - Konsernin sisäinen:

        - Jos kyse on konsernin sisäisestä tapahtumasta, sitä ei voi palauttaa.
        - Tapahtuma **ei** ole konsernin sisäinen tapahtuma, mutta se on kirjattu maksun saajan tai maksun lähteen päätilille, joka määritettiin **Konserniasetukset**-sivulla.

    - Jaksotukset:

        - Jos jaksotettu kirjanpitotosite palautetaan, jaksotettu kirjaus ja kaikki vastaavat jaksotetut alitapahtumat palautetaan.
        - Yksittäisiä jaksotettuja alitapahtumia ei voi palauttaa.

- Tuottokirjauskansio:

    - Tuottokirjaustapahtumia ei voi palauttaa.
    - Kun tuotto kirjataan tuottokirjauskansion kautta, tosite kirjataan vain kirjanpitotileille. Tämän vuoksi tosite näkyy **Tositetapahtumat** ja muilla vastaavilla sivuilla aivan kuin olisivat vain kirjanpitotapahtumia.

- Ulkomaanvaluutan uudelleenarvostus:

    - Vaikka ulkomaanvaluutan uudelleenarvostustapahtumat voidaan palauttaa, se on mahdollista vain siltä kirjanpidon **Ulkomaanvaluutan uudelleenarvostus** -sivulta, jolta uudelleenarvostus suoritettiin.
    - Palautus voi valmistua vain, jos se kirjattiin avoimeen tilikauteen.

- Konsolidointi:

    - Konsolidointitapahtumat voidaan palauttaa vain **Konsolidointitapahtumat**-sivulla.
    - Palautus voi valmistua vain, jos se kirjattiin avoimeen tilikauteen.

- Tilinpäätös:

    - Tilinpäätöstapahtumat (sekä sulkemis- että avaustapahtumat) voidaan palauttaa seuraavasti:

        - Jos kirjanpidon tilinpäätöksen parannusominaisuus on poistettu käytöstä, valitse **Kumoa edellinen sulkeminen** -vaihtoehto **Tilinpäätös**-valintaikkunassa.
        - Jos kirjanpidon tilinpäätöksen parannusominaisuus on otettu käyttöön, valitse yrityksen ja tilikauden tietueet, jotka luotiin tilinpäätöstä varten **Tilinpäätös**-sivulla ja valitse **Palauta tilinpäätös**.

    - Huomaa, että tilinpäätöksen palauttaminen poistaa sulkemis- ja avaustapahtumat. Palautustositetta ei kirjata koskaan.

## <a name="accounts-payable"></a>Ostoreskontra

Useat tapahtumatyypit päivittävät ostoreskontran. Näitä tapahtumia ovat esimerkiksi toimittajan laskut, toimittajan laskukirjauskansiot ja kuluraportit.

Jos joukkopalautusominaisuus on poistettu käytöstä, tapahtumat voidaan palauttaa yksittäisinä laskujen osalta **Toimittajan tapahtumat** -sivulta tai sekkimaksujen osalta **Pankkitili**-sivulta.

Jos joukkopalautusominaisuus on otettu käyttöön, yksi tai usea ostoreskontratapahtuma voidaan palauttaa myös **Tositetapahtumat**-sivulta ja siitä kirjauskansiosta, josta tapahtuma kirjattiin. Toimittajan maksut voidaan silti palauttaa vain pankkitililtä. Toimittajan tapahtumia ei myöskään voida palauttaa kirjanpidon **Kohteen \<main account\> tapahtumat** -sivulta. Ne voidaan palauttaa vain **Tositetapahtumat**-sivulta.

Huomaa, että joitakin tapahtumia ei voi palauttaa lainkaan. Sellaisia ovat esimerkiksi ostotilauksen toimittajan laskut ja sähköiset toimittajan maksut.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Tositteiden palauttamisen estäviä syitä

Tositteita ei voi palauttaa seuraavien syiden vuoksi:

- Tilikausi on pidossa tai suljettu:

    - Jos palautuspäivämäärä on suljetulla tilikaudella, tapahtumaa ei voi palauttaa.
    - Jos tapahtuma tukee palautuspäivämäärän kirjausta, tapahtuma voi silti palauttaa muuttamalla palautuspäivämäärä avoimelle kaudelle.

- Kirjanpidon tilinpäätösprosessi on suoritettu:

    - Tapahtuman kirjauspäivä on tilikaudella, joka on suljettu kirjanpidossa. Vaikka tilikauden kausi voi olla edelleen avoinna, tapahtumaa ei voi palauttaa, jos tilinpäätösprosessi on suoritettu tilikauden osalta. Tilikauden tila ei ole sama kuin siinä olevien kausien tila.
    - Tilinpäätös voidaan palauttaa, jonka jälkeen tapahtuma voidaan palauttaa. Tämän menetelmän käyttäminen ei ole ehkä mahdollista. Tilikauden lopetusprosessin tilan perusteella voikin olla kätevämpää kirjata manuaalinen palautustapahtuma joko suljetun tilikauden tai seuraavan tilikauden avoimella kaudella. Jos uusi tapahtuma kirjataan sellaisen tilikauden avoimeen kauteen, jossa tilinpäätösprosessi on tehty, tilinpäätös on suoritettava uudelleen.

- Alareskontran kirjauskansiovientiä ei ole siirretty kirjanpitoon:

    - Tämä syy koskee vain muiden kuin ostotilauksen toimittajan laskuja.
    - Kyseinen vienti voidaan siirtää kirjanpitoon **Alareskontran kirjauskansioviennit, joita ei ole vielä siirretty** -sivulla. Muun kuin ostotilauksen toimittajan lasku voidaan palauttaa **Toimittajan tapahtumat** -sivulla.

- Tilitys:

    - Tapahtuma (kuten lasku tai maksu) on tilitetty tai merkitty tilitettäväksi.

        - Tapahtuman tilityksen tai tilitettäväksi merkitseminen voi tarkistaa valitsemalla **Toimittajan tapahtumat** -sivulla **Näytä tilitykset** tai **Tilitys \> Tilityshistoria**.
        - Tilityksen voi myös palauttaa **Toimittajan tapahtumat** -sivulla (**Tilitys \> Kumoa tilitys**), jos jokin tapahtumista on palautettava.

- Tositteessa on useampi kuin yksi alareskontratapahtuma, joka kirjattiin käyttämällä samaa tositenumeroa (yhden tositteen ongelma).
- Laskua ei ole hyväksytty:

    - Jos laskun **Hyväksyminen**-valintaruutua ei ole valittu, laskua ei voi palauttaa.

        - Tässä tapauksessa hyväksyminen ei viittaa työnkulkuprosessin hyväksymiseen vaan laskun **Hyväksyminen**-vaihtoehtoon. Tämän vaihtoehdon avulla voidaan estää laskun maksaminen. Sitä käytetään yleensä toimittajan laskurekisterin laskuissa.

- Tapahtuma on laskupoolissa:

    - Poolissa olevaa laskua ei voi palauttaa suoraan **Toimittajan tapahtumat** -sivulta. Se on palautettava sen sijaan peruutusprosessin avulla **Hyväksyttyjen laskujen kirjauskansio** -sivulla.

- Tapahtumalla on oikaistu päälasku (Intian lokalisointi).
- Tapahtuman velan tila on **Lasku maksettu**.
- Tapahtumaa käytetään veron osittaisessa tilityksessä.
- Vaikka tapahtuma sisältää toimittajan tilin, se palautetaan virheelliseltä sivulta, kuten **Kohteen \<main account\> tapahtumat** -sivulta:

    - Niin kuin tästä syystä voi päätellä osa alareskontratapahtumista voidaan palauttaa vain tietyiltä sivuilta, vaikka joukkopalautusominaisuus olisi otettu käyttöön.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Tapahtumatyypit, joita ei voi palauttaa

Seuraavia tapahtumatyyppejä ei voi palauttaa:

- Ulkomaanvaluutan uudelleenarvostus:

    - Kirjanpidon ulkomaanvaluutan uudelleenarvostuksesta poiketen myyntireskontran ja ostoreskontran ulkomaanvaluutan uudelleenarvostusta ei voi palauttaa. Uudelleenarvostus on sijaan suoritettava uudelleen käyttämällä laskun päivämäärää. Tässä tapauksessa uudelleenarvostus käyttää laskun päivämäärän vaihtokurssia ja käytännössä tuo toteutumattoman voiton tai tappion nollaan (0). Tämän vuoksi tulos muistuttaa edellisen uudelleenarvostuksen palauttamisen tulosta. On kuitenkin huomattava, että samaa summaa ei palauteta, jos laskun oletusvaihtokurssi on vaihdettu.

- Ostotilauksen toimittajan lasku:

    - Toimittajan laskun palauttamista varten on luotava hyvityslasku. Lisätietoja palautustapahtuman luomisesta on kohdassa [Ostopalautustilauksen luominen](../../supply-chain/procurement/tasks/create-purchase-return-order.md).

- Velkakirja
- Pankkiremburssin viennin lähetys

## <a name="accounts-receivable"></a>Myyntireskontra

Monet tapahtumatyypit päivittävät myyntireskontrat. Näitä tapahtumia ovat esimerkiksi myyntitilausten myyntilaskut, kirjanpidon kautta kirjatut myyntilaskut, vapaatekstilaskut, asiakkaan maksut ja poistot.

Jos joukkopalautusominaisuus on poistettu käytöstä, tapahtumat voidaan palauttaa yksittäisinä laskujen osalta **Asiakkaan tapahtumat** -sivulta tai talletusten osalta **Pankkitili**-sivulta. Lisätietoja maksun peruuttamisesta on jäljempänä tämän artikkelin [Maksuliikenteen hallinta](cant-reverse-transctns.md#cash-and-bank-management) -osassa.

Jos joukkopalautusominaisuus on otettu käyttöön, yksi tai usea myyntireskontratapahtuma voidaan palauttaa myös **Tositetapahtumat**-sivulta ja siitä kirjauskansiosta, josta tapahtuma kirjattiin. Talletukset voidaan kuitenkin edelleen palauttaa vain pankkitililtä ja vapaatekstilaskut vain alkuperäiseltä sivulta (jos oikaisut salliva ominaisuus on otettu käyttöön). Asiakkaan tapahtumia ei myöskään voida edelleenkään palauttaa kirjanpidon **Kohteen \<main account\> tapahtumat** -sivulta. Ne voidaan kuitenkin palauttaa **Tositetapahtumat**-sivulta.

Huomaa, että joitakin tapahtumia ei voida palauttaa. Tällaisia tapahtuvia ovat esimerkiksi myyntitilauksen myyntilaskut ja poistot.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Tapahtumien palauttamisen estäviä syitä

Tapahtumia ei voi palauttaa seuraavien syiden vuoksi:

- Tilikausi on pidossa tai suljettu pysyvästi:

    - Jos palautuspäivämäärä on suljetulla tilikaudella, tapahtumaa ei voi palauttaa.
    - Jos tapahtuma tukee palautuspäivämäärän kirjausta, tapahtuma voi silti palauttaa muuttamalla palautuspäivämäärä avoimelle kaudelle.

- Kirjanpidon tilinpäätösprosessi on suoritettu:

    - Tapahtuman kirjauspäivä on tilikaudella, jolle on tehty kirjanpidossa tilinpäätös. Vaikka tilikauden kausi voi olla edelleen avoinna, tapahtumaa ei voi palauttaa, jos tilinpäätösprosessi on suoritettu tilikauden osalta. Tilikauden tila ei ole sama kuin siinä olevien kausien tila.
    - Tilinpäätös voidaan palauttaa, jonka jälkeen tapahtuma voidaan palauttaa. Tämän menetelmän käyttäminen ei ole ehkä mahdollista. Tilikauden lopetusprosessin tilan perusteella voikin olla kätevämpää kirjata manuaalinen palautustapahtuma joko suljetun tilikauden tai seuraavan tilikauden avoimella kaudella. Jos uusi tapahtuma kirjataan sellaisen tilikauden avoimeen kauteen, jossa tilinpäätösprosessi on tehty, tilinpäätös on suoritettava uudelleen.

- Alareskontran kirjauskansiovientiä ei ole siirretty kirjanpitoon:

    - Tämä syy koskee vain vapaatekstilaskuja.
    - Kyseinen vienti voidaan siirtää kirjanpitoon **Alareskontran kirjauskansioviennit, joita ei ole vielä siirretty** -sivulla. Vapaatekstilaskut voidaan sitten palauttaa tai ne voidaan korjata, jos korjaustoiminto on otettu käyttöön.

- Tilitys:

    - Tapahtuma (kuten lasku tai maksu) on tilitetty tai merkitty tilitettäväksi.

        - Tapahtuman tilityksen tai tilitettäväksi merkitseminen voi tarkistaa valitsemalla **Asiakkaan tapahtumat** -sivulla **Näytä tilitykset** tai **Tilitys \> Tilityshistoria**.
        - Tilityksen voi myös palauttaa **Asiakkaan tapahtumat** -sivulla (**Tilitys \> Kumoa tilitys**), jos jokin tapahtumista on palautettava.

- Tapahtumassa on useampi kuin yksi alareskontratapahtuma, joka kirjattiin käyttämällä samaa tositenumeroa (yhden tositteen ongelma).
- Laskua ei ole hyväksytty:

    - Jos laskun **Hyväksyminen**-valintaruutua ei ole valittu, laskua ei voi palauttaa.

        - Tässä tapauksessa hyväksyminen ei viittaa työnkulkuprosessin hyväksymiseen vaan tositerivien **Hyväksyminen**-vaihtoehtoon. Tämän vaihtoehdon avulla voidaan estää laskun maksaminen. Vaikka tätä vaihtoehtoa käytetään yleensä ostoreskontrassa, sitä voi käyttää myös myyntireskontran kirjauskansion kautta kirjatuissa laskuissa.

- Tapahtumalla on oikaistu päälasku (Intian lokalisointi).
- Vaikka tapahtuma sisältää asiakkaan tilin, se palautetaan virheelliseltä sivulta, kuten **Kohteen \<main account\> tapahtumat** -sivulta:

    - Niin kuin tästä syystä voi päätellä osa alareskontratapahtumista voidaan palauttaa vain tietyiltä sivuilta, vaikka joukkopalautusominaisuus olisi otettu käyttöön.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Tapahtumatyypit, joita ei voi palauttaa

Seuraavia tapahtumatyyppejä ei voi palauttaa:

- Ulkomaanvaluutan uudelleenarvostus:

    - Kirjanpidon ulkomaanvaluutan uudelleenarvostuksesta poiketen myyntireskontran ja ostoreskontran ulkomaanvaluutan uudelleenarvostusta ei voi palauttaa. Uudelleenarvostus on sijaan suoritettava uudelleen käyttämällä laskun päivämäärää. Tässä tapauksessa uudelleenarvostus käyttää laskun päivämäärän vaihtokurssia ja käytännössä tuo toteutumattoman voiton tai tappion nollaan (0). Tämän vuoksi tulos muistuttaa edellisen uudelleenarvostuksen palauttamisen tulosta. On kuitenkin huomattava, että samaa summaa ei palauteta, jos laskun oletusvaihtokurssi on vaihdettu.

- Tapahtumassa on oikaistu ennakonpidätys
- Myyntitilauksen myyntilasku:

    - Tapahtuman palauttamista varten on luotava hyvityslasku tai palautus. Lisätietoja palautustapahtuman luonnista on kohdassa [Myyntipalautukset](../../supply-chain/warehousing/sales-returns.md).

- Vekseli
- Kassapäätetapahtumat
- Edistynyt oikaisu
- Korkolasku
- Maksukehotus
- Pankkiremburssi
- Vientilähetys
- Tuottokirjauskansio:

    - Kun tuotto kirjataan tuottokirjauskansion kautta, tositteet kirjataan kirjanpitotileille. Tämän vuoksi ne näyttävät vain kirjanpitovienneiltä. Näitä vientejä ei voi palauttaa, koska tuottoaikataulua ei avata tuoton uudelleenkirjaamista varten.

## <a name="cash-and-bank-management"></a>Maksuliikenteen hallinta

Useat tapahtumatyypit päivittävät pankin alareskontran kirjanpidon kautta. Tällaisia tapahtumia ovat esimerkiksi toimittajan maksut, asiakkaan maksut ja pankkisiirrot.

Jos joukkopalautusominaisuus on poistettu käytöstä, tapahtumat voidaan palauttaa yksittäisinä sekkien ja talletusten osalta **Pankkitilit**-sivulta tai asiakkaan maksujen osalta **Asiakkaan tapahtumat** -sivulta.

Jos joukkopalautusominaisuus on otettu käyttöön, yksi tai usea maksutapahtuma voidaan palauttaa myös **Tositetapahtumat**-sivulta ja siitä kirjauskansiosta, josta tapahtuma kirjattiin. Talletukset maksut voidaan edelleenkin palauttaa vain pankkitililtä. Pankkitapahtumia ei myöskään voida edelleenkään palauttaa kirjanpidon **Kohteen \<main account\> tapahtumat** -sivulta. Ne voidaan kuitenkin palauttaa **Tositetapahtumat**-sivulta.

Huomaa, että joitakin tapahtumia ei voida palauttaa. Tällaisia tapahtumia ovat esimerkiksi sähköiset toimittajan maksut.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Tapahtumien palauttamisen estäviä syitä

Tapahtumia ei voi palauttaa seuraavien syiden vuoksi:

- Tilikausi on pidossa tai suljettu pysyvästi:

    - Jos palautuspäivämäärä on suljetulla tilikaudella, tapahtumaa ei voi palauttaa.
    - Jos tapahtuma tukee palautuspäivämäärän kirjausta, tapahtuma voi silti palauttaa muuttamalla palautuspäivämäärä avoimelle kaudelle.

- Kirjanpidon tilinpäätösprosessi on suoritettu:

    - Tapahtuman kirjauspäivä on tilikaudella, jolle on tehty kirjanpidossa tilinpäätös. Vaikka tilikauden kausi voi olla edelleen avoinna, tapahtumaa ei voi palauttaa, jos tilinpäätösprosessi on suoritettu tilikauden osalta. Tilikauden tila ei ole sama kuin siinä olevien kausien tila.
    - Tilinpäätös voidaan palauttaa, jonka jälkeen tapahtuma voidaan palauttaa. Tämän menetelmän käyttäminen ei ole ehkä mahdollista. Tilikauden lopetusprosessin tilan perusteella voikin olla kätevämpää kirjata manuaalinen palautustapahtuma joko suljetun tilikauden tai seuraavan tilikauden avoimella kaudella. Jos uusi tapahtuma kirjataan sellaisen tilikauden avoimeen kauteen, jossa tilinpäätösprosessi on tehty, tilinpäätös on suoritettava uudelleen.

- Tilitys:

    - Tapahtuma (maksu) on tilitetty tai merkitty tilitettäväksi.

        - Tapahtuman tilityksen tai tilitettäväksi merkitseminen voi tarkistaa valitsemalla **Toimittajan tapahtumat** tai **Asiakkaan tapahtumat** -sivulla **Näytä tilitykset** tai **Tilitys \> Tilityshistoria**.
        - Tilityksen voi myös palauttaa **Toimittajan tapahtumat**- tai **Asiakkaan tapahtumat** -sivulla (**Tilitys \> Kumoa tilitys**), jos jokin tapahtumista on palautettava.

- Tapahtumassa on useampi kuin yksi alareskontratapahtuma, joka kirjattiin käyttämällä samaa tositenumeroa (yhden tositteen ongelma).
- Välitilitapahtumat:

    - Jos tapahtuma liittyy välitiliöintimaksuun, sitä ei voi palauttaa.
    - Jos välitiliöintimaksu on palautettava, maksu on selvitettävä ensin välitililtä pankkiin. Maksu voidaan sitten palauttaa, jos se täyttää muut vahvistusehdot.

- Tapahtuma sisältää pankkitilin mutta palautetaan **Kohteen \<main account\> tapahtumat** -sivulta tai virheellisestä alareskontrasta, kuten ostoreskontrasta tai myyntireskontrasta:

    - Niin kuin tästä syystä voi päätellä osa alareskontratapahtumista voidaan palauttaa vain tietyiltä sivuilta, vaikka joukkopalautusominaisuus olisi otettu käyttöön.

- Pankin ulkomaanvaluutan uudelleenarvostus:

    - Pankin ulkomaanvaluutan uudelleenarvostus voidaan palauttaa. Palautus voidaan kuitenkin estää, jos palautusvaiheita ei tehdä oikeassa aikajärjestyksessä. Jos uudelleenarvostus esimerkiksi suoritettiin maaliskuussa ja huhtikuussa, maaliskuun uudelleenarvostusta ei palauttaa, ennen kuin huhtikuun uudelleenarvostus on palautettu.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Tapahtumatyypit, joita ei voi palauttaa

Seuraavia tapahtumatyyppejä ei voi palauttaa:

- Sähköisenä rahansiirtona (EFT-siirtona) suoritetut toimittajan maksut
- Velkakirjat
- Vekseli

## <a name="fixed-assets"></a>Käyttöomaisuus

Useat tapahtumatyypit päivittävät käyttöomaisuuden alareskontran. Näitä tapahtumia ovat esimerkiksi hankinnat ja poisto.

Jos joukkopalautusominaisuus on poistettu käytöstä, tapahtumat voidaan palauttaa yksittäin **Toimittajan tapahtumat** -sivulta, **Käyttöomaisuustapahtumat**-sivulta tai resurssin vuokrauksesta sen perusteella, mistä tapahtumatyypistä on kyse.

Jos joukkopalautusominaisuus on otettu käyttöön, yksi tai usea käyttöomaisuustapahtuma voidaan palauttaa myös **Tositetapahtumat**-sivulta siinä kirjauskansiossa, josta tapahtuma kirjattiin.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Tapahtumien palauttamisen estäviä syitä

Tapahtumia ei voi palauttaa seuraavien syiden vuoksi:

- Tilikausi on pidossa tai suljettu pysyvästi:

    - Jos palautuspäivämäärä on suljetulla tilikaudella, tapahtumaa ei voi palauttaa.
    - Jos tapahtuma tukee palautuspäivämäärän kirjausta, tapahtuma voi silti palauttaa muuttamalla palautuspäivämäärä avoimelle kaudelle.

- Kirjanpidon tilinpäätösprosessi on suoritettu:

    - Tapahtuman kirjauspäivä on tilikaudella, joka on suljettu kirjanpidossa. Vaikka tilikauden kausi voi olla edelleen avoinna, tapahtumaa ei voi palauttaa, jos tilinpäätösprosessi on suoritettu tilikauden osalta. Tilikauden tila ei ole sama kuin siinä olevien kausien tila.
    - Tilinpäätös voidaan palauttaa, jonka jälkeen tapahtuma voidaan palauttaa. Tämän menetelmän käyttäminen ei ole ehkä mahdollista. Tilikauden lopetusprosessin tilan perusteella voikin olla kätevämpää kirjata manuaalinen palautustapahtuma joko suljetun tilikauden tai seuraavan tilikauden avoimella kaudella. Jos uusi tapahtuma kirjataan sellaisen tilikauden avoimeen kauteen, jossa tilinpäätösprosessi on tehty, tilinpäätös on suoritettava uudelleen.

- Hankinnat:

    - Jos hankinta tapahtui ostotilauksen toimittajan laskussa, palautus on tehtävä kirjaamalla toimittajan hyvityslasku. Lisätietoja palautustapahtuman kirjaamisesta on kohdassa [Ostopalautustilauksen luominen](../../supply-chain/procurement/tasks/create-purchase-return-order.md).
    - Hankinta tehtiin projektitapahtumassa.
    - Hankintaa ei voi palauttaa sen jälkeen, kun resurssin poisto on kirjattu. Ennen kuin hankinta voidaan palauttaa, poisto on palautettava.
    - Jos käyttöomaisuuden arvomallin tai poistokirjan tila ei ole avoin, tapahtumaa ei voi palauttaa.

- Luovutukset:

    - Luovutus tehdään vapaatekstilaskuna:

        - Vapaatekstilaskun korjaus estetään, jos se sisältää käyttöomaisuuserän. Jos käyttöomaisuuserä kuitenkin luovutetaan kirjauskansion kautta, vapaatekstilasku voidaan palauttaa käyttöomaisuustietueesta.

    - Jos käyttöomaisuuden arvomallin tai poistokirjan tila ei ole avoin, tapahtumaa ei voi palauttaa.

- Poisto:

    - Poisto **voidaan** palauttaa, jos myös seuraava poisto on kirjattu. Tästä kuitenkin annetaan varoitus, sillä menetelmä ei ole parhaan käytännön mukainen.
    - Jos käyttöomaisuuden arvomallin tai poistokirjan tila ei ole avoin, tapahtumaa ei voi palauttaa.

- Tositteen tapahtumapäivällä tai sitä myöhemmin on tietyn käyttöomaisuuserän tai käyttöomaisuuskirjan tapahtumia (tai palautustapahtumia).
- Tapahtuma sisältää käyttöomaisuuserän tilin mutta palautetaan **Kohteen \<main account\> tapahtumat** -sivulta tai virheellisestä alareskontrasta, kuten ostoreskontrasta tai myyntireskontrasta:

    - Niin kuin tästä syystä voi päätellä osa alareskontratapahtumista voidaan palauttaa vain tietyiltä sivuilta, vaikka joukkopalautusominaisuus olisi otettu käyttöön.
    - Jos hankinta tapahtuu muussa kuin ostotilauksen toimittajan laskussa tai toimittajan laskukirjauskansiossa, se voidaan palauttaa vain ostoreskontran **Toimittajan tapahtumat** -sivulla.
    - Jos käyttöomaisuuserä hankitaan resurssin vuokrauksesta, se voidaan palauttaa resurssin vuokrauksen **Velkatapahtumat**-sivulta.
