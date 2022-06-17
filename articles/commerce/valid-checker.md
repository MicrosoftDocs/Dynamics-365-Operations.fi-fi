---
title: Myymälän tapahtumien tarkistaminen tiliotteen laskemista varten
description: Tässä artikkelissa esitellään myymälän tapahtumien tarkistamisen toiminnot Microsoft Dynamics 365 Commercessa.
author: analpert
ms.date: 01/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4be40189777a37495f185467050b61af47b684d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890510"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Myymälän tapahtumien tarkistaminen tiliotteen laskemista varten

[!include [banner](includes/banner.md)]

Tässä artikkelissa esitellään myymälän tapahtumien tarkistamisen toiminnot Microsoft Dynamics 365 Commercessa. Tarkistusprosessi tunnistaa ja merkitsee kirjausvirheitä aiheuttavat tapahtumat, ennen kuin laskelmien kirjausprosessi valitsee ne.

Kun yrität kirjata laskelman, tarkistusprosessi voi epäonnistua kaupankäynnin tapahtumataulujen ristiriitaisten tietojen vuoksi. Seuraavassa on muutamia esimerkkejä tekijöistä, jotka voivat aiheuttaa näitä ristiriitoja:

- Tapahtuman kokonaissumma otsikkotaulussa ei vastaa riveillä olevaa tapahtuman kokonaissummaa.
- Otsikkotaulussa määritettyjen nimikkeiden määrä ei vastaa tapahtumataulun nimikkeiden määrää.
- Otsikkotaulussa olevat verot eivät vastaa riveillä olevaa veron määrää. 

Jos laskelmien kirjausprosessi havaitsee epäyhtenäisiä tapahtumia, luodut myyntilaskut ja maksukirjauskansiot voivat aiheuttaa laskelman kirjauksen epäonnistumisen. **Tarkista myymälän tapahtumat** -prosessi estää näiden ongelmien syntymisen varmistamalla, että vain tapahtuman tarkistussääntöjen hyväksymät tapahtumat välitetään tapahtumaraportin laskentaprosessiin.

Seuraavassa kuvassa ovat toistuvat päiväprosessit tapahtumien lataamista ja tarkistamista ja tapahtumaraporttien laskemista ja kirjaamista varten sekä tilinpäätöksen laskennan ja kirjauksen päivän lopussa suoritettavat prosessit.

![Kuvassa ovat toistuvat päiväprosessit tapahtumien lataamista ja tarkistamista ja tapahtumaraporttien laskemista ja kirjaamista varten sekä tilinpäätöksen laskennan ja kirjauksen päivän lopussa suoritettavat prosessit](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Myymälän tapahtuman tarkistussäännöt

**Tarkista myymälän tapahtumat** -eräprosessi tarkistaa kaupankäynnin tapahtumataulujen yhdenmukaisuuden seuraavien tarkistussääntöjen perusteella.

> [!NOTE]
> Tarkistussäännöt lisätään myös seuraaviin versioihin.

### <a name="transaction-header-validation-rules"></a>Tapahtuman otsikon tarkistussäännöt

Seuraavassa taulussa ovat tapahtuman otsikon tarkistussäännöt, joita verrataan vähittäismyyntitapahtumien otsikkoon ennen tapahtumien välittämistä laskelman kirjaukseen.

| Sääntö | Kuvaus |
|-------|-------------|
| Liiketoimintapäivämäärä | Tämä sääntö tarkistaa, että tapahtuman liiketoimintapäivämäärä liittyy kirjanpidon avoimeen kauteen. |
| Valuutan pyöristys | Tämä sääntö tarkistaa, että tapahtuman summat pyöristetään valuutan pyöristyssäännön mukaan. |
| Asiakastili | Tämä sääntö tarkistaa, että tapahtumassa käytettävä asiakas on tietokannassa. |
| Alennussumma | Tämä sääntö tarkistaa, että otsikon alennussumma on yhtä suuri kuin rivien alennussummat yhteensä. |
| Veroasiakirjan kirjauksen tila (Brasilia) | Tämä sääntö tarkistaa, että veroasiakirjan kirjaus onnistuu. |
| Bruttosumma | Tämä sääntö tarkistaa, että tapahtuman otsikon bruttosumma vastaa tapahtumarivien ja kulujen nettosummaa ja veroja. |
| Netto | Tämä sääntö tarkistaa, että tapahtuman otsikon nettosumma vastaa tapahtumarivien ja kulujen nettosummaa ilman veroja. |
| Netto + vero | Tämä sääntö tarkistaa, että tapahtuman otsikon bruttosumma vastaa tapahtumarivien ja kaikkien verojen ja kulujen nettosummaa ilman veroja. |
| Nimikkeiden määrä | Tämä sääntö tarkistaa, että tapahtuman otsikossa määritettyjen nimikkeiden määrä vastaa tapahtumarivien määrien summaa. |
| Maksun summa | Tämä sääntö tarkistaa, että tapahtuman otsikon maksun summa vastaa kaikkien maksutapahtumien summaa. |
| Verovapauden laskenta | Tämä sääntö tarkistaa, että laskettu summa ja kulurivien verovapaa summa yhteensä on yhtä suuri kuin alkuperäinen laskettu summa. |
| Vero sisältyy hinnoitteluun | Tämä sääntö tarkistaa, että **Vero sisältyy hintaan** -merkintä on yhdenmukainen tapahtuman otsikossa ja verotapahtumissa. |
| Tapahtuma ei ole tyhjä | Tämä sääntö tarkistaa, että tapahtuma sisältää rivejä ja että vähintään yhtä riviä ei ole mitätöity. |
| Ali-/liikamaksu | Tämä sääntö tarkistaa, että brutto- ja maksusumman välinen ero ei ole suurempi kuin ali- tai liikamaksun määrityksen enimmäismäärä. |

### <a name="transaction-line-validation-rules"></a>Tapahtumarivin tarkistussäännöt

Seuraavassa taulussa ovat tapahtumarivin tarkistussäännöt, joita verrataan vähittäismyyntitapahtumien rivitietoihin ennen tapahtumien välittämistä laskelman kirjaukseen.

| Sääntö | Kuvaus |
|-------|-------------|
| Viivakoodi | Tämä sääntö tarkistaa, että kaikki tapahtumariveillä käytettävät nimikkeen viivakoodit ovat tietokannassa. |
| Kulurivit | Tämä sääntö tarkistaa, että laskettu summa ja kulurivien verovapaa summa yhteensä on yhtä suuri kuin alkuperäinen laskettu summa. |
| Lahjakorttien palautukset | Tämä sääntö tarkistaa, että tapahtumassa ei ole lahjakorttien palautuksia. |
| Nimikevariantti | Tämä sääntö tarkistaa, että kaikki tapahtumariveillä käytettävät nimikkeet ja kaikki variantit ovat tietokannassa. |
| Rivialennus | Tämä sääntö tarkistaa, että rivin alennussumma vastaa alennustapahtumien summaa. |
| Rivin vero | Tämä sääntö tarkistaa, että rivin verosumma vastaa verotapahtumien summaa. |
| Negatiivinen hinta | Tämä sääntö tarkistaa, että tapahtumariveillä ei ole käytetty negatiivisia hintoja. |
| Sarjanumeroseurannassa | Tämä sääntö tarkistaa, että tapahtumarivillä on sarjanumero sarjanumeroseurannassa olevien nimikkeitä varten. |
| Sarjanumeron dimensio | Tämä sääntö tarkistaa, että sarjanumeroa ei ole annettu, jos nimikkeen sarjanumeron dimensio ei ole käytössä. |
| Merkkiristiriita | Tämä sääntö tarkistaa, että määrän ja nettosumman merkit ovat samat kaikilla tapahtumariveillä. |
| Verovapaa | Tämä sääntö tarkistaa, että rivinimikkeen hinta ja verovapaa summa yhteensä on yhtä suuri kuin alkuperäinen hinta. |
| Veroryhmän määritys | Tämä sääntö tarkistaa, että arvonlisäveroryhmän ja nimikkeen veroryhmän yhdistelmä tuottaa sallitun verojen leikkauskohdan. |
| Mittayksikkömuunnokset | Tämä sääntö tarkistaa, että kaikkien rivien mittayksiköillä on sallittu varaston mittayksikön muunnos. |

## <a name="enable-the-store-transaction-validation-process"></a>Myymälän tapahtumien tarkistusprosessin käyttöönotto

Määritä **Tarkista myymälän tapahtumat** -työ Commerce-pääkonttorisovelluksen kausittaisille suorituksille (**Retail ja Commerce \> Retailin ja Commercen IT \> Myyntipistekirjaus**). Erätyö ajoitetaan myymälän organisaatiohierarkian perusteella. Tämä eräprosessi kannattaa määrittää suoritettavaksi samalla toistovälillä kuin **noutotyö** ja **Tapahtumaraportin laskenta** -erätyö.

## <a name="results-of-the-validation-process"></a>Tarkistusprosessin tulokset

**Tarkista myymälän tapahtumat** -eräprosessin tulosta voi tarkastella kussakin vähittäismyyntitapahtumassa. Tapahtumatietueen **Tarkistuksen tila** -kentän arvoksi on määritetty **Onnistui**, **Virhe** tai **Ei mitään**. **Edellisen tarkistuksen aika** -kentässä on edellisen tarkistusajon päivämäärä.

Seuraavassa taulussa on kukin tarkistuksen tila.

| Tarkistuksen tila | Kuvaus |
|-------------------|-------------|
| Onnistui | Kaikki käytössä olevat tarkistussäännöt hyväksyttiin. |
| Virhe | Käyttöönotettu tarkistussääntö löysi virheen. Voit tarkastella virheen lisätietoja valitsemalla toimintoruudussa **Tarkistusvirheet**. |
| Ei mitään | Tapahtumatyyppi ei vaadi tarkistussääntöjen kohdistamista. |

![Myymälän tapahtumat -sivulla on Tarkistuksen tila -kenttä ja Tarkistusvirheet-painike.](./media/valid-checker-validation-status-errors.png)

Vain tapahtumat, joiden tarkistuksen tila on **Onnistui**, noudetaan tapahtumaraportteihin. Jos haluat tarkastella tapahtumia, joiden tila on **Virhe**, tarkista **Itsepalvelun tarkistusvirheet** -ruutu **Myymälän myyntitiedot** -työtilassa.

![Myymälän myyntitiedot -työtilan ruudut.](./media/valid-checker-cash-carry-validation-failures.png)

Lisätietoja itsepalvelun tarkistusvirheiden korjaamisesta on kohdassa [Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen](edit-cash-trans.md).

## <a name="additional-resources"></a>Lisäresurssit

[Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
