---
title: Luotonhallinnan parametrien määrittäminen
description: Tässä artikkelissa käsitellään asetuksia, joilla luotonhallinta voidaan määrittää vastaamaan yrityksen tarpeita.
author: JodiChristiansen
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ac5e0ba8c9279fc5f04a80d4444b11850e72d3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876351"
---
# <a name="credit-management-parameters-setup"></a>Luotonhallinnan parametrien määrittäminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään asetuksia, joilla luotonhallinta voidaan määrittää vastaamaan yrityksen tarpeita. Luotonhallinnan toimintojen käyttö aloitetaan määrittämällä parametrit **Luotonhallinta- ja perimisparametrit** -sivulla (**Luotonhallinta- ja perintä \> Asetukset \> Luotonhallinta- ja perintäparametrit**).

## <a name="credit-parameters"></a>Luottoparametrit

Luotonhallintaa ohjaavia parametreja voi muuttaa **Luotto**-osan neljässä pikavälilehdessä: **Luottorajapidot**, **Luotonhallinnan tarkistuspiste**, **Luotonhallinnan tilastot** ja **Luottorajat**. Seuraavissa osissa käsitellään kussakin pikavälilehdessä olevia asetuksia.

### <a name="credit-holds"></a>Luoton pidot

- Jos **Salli myyntitilausten arvon muokkaus sen jälkeen, kun tilaus on vapautettu pidosta** -asetuksena on **Ei**, kirjaussäännöt on tarkistettava uudelleen, jos myyntitilauksen arvo (laajennettu hinta) on noussut sen jälkeen, kun myyntitilaus vapautettiin pitoluettelosta.
- Valitse **Peruutettujen tilausten syyt** -kentässä vapautuksen syy, jotka käytetään oletusarvoisesti, kun luotonhallinnan pidossa ollut myyntitilaus peruutettiin.
- Jos **Tarkista asiakkaan luottoryhmän luottoraja** -asetuksena on **Kyllä**, asiakkaan luottoryhmän luottoraja tarkistetaan, kun myyntitilauksen asiakas kuuluu asiakkaan luottoryhmään. Ryhmän luottoraja tarkistetaan, minkä jälkeen tarkistetaan asiakkaan luottoraja, jos ryhmän luottoraja on riittävä.
- Jos **Tarkista luottoraja, kun maksuehtoja suurennetaan** -asetuksena on **Kyllä**, maksuehtojen sijoitus tarkistetaan ja sen perusteella määritetään, onko asiakkaan oletusmaksuehdoissa eroja. Jos uusien maksuehtojen sijoitus on korkeampi kuin alkuperäisten maksuehtojen sijoitus, tilaus asetetaan luotonvalvonnan pitoon.
- Jos **Tarkista luottoraja, kun tilitysalennus suurenee** -asetuksena on **Kyllä**, tilitysalennuksen sijoitus tarkistetaan ja sen perusteella määritetään, onko asiakkaan oletuskäteisalennuksissa eroja. Jos uuden käteisalennuksen sijoitus on korkeampi kuin alkuperäisen käteisalennuksen sijoitus, tilaus asetetaan luotonvalvonnan pitoon.
- Valitse **Muokattujen tilausten vapauttamisen syyt** -kentässä vapautuksen syy, jota käytetään oletusarvoisesti, kun muokatut tilaukset vapautetaan automaattisesti luotonvalvonnan pidosta.
- **Luottoraja vanhentunut** -säännön toimintaa voi hallita, jos **Ohita luottorajan vanhentumisen estosääntö, kun vanhentumispäivä on tyhjä** -asetuksena on **Kyllä**. Jos asetuksena **Ei**, tilaus estetään, kun vanhentumispäivä on tyhjä.
- Varastonhallinnassa voidaan luoda kuormia, kun myyntitilausta käsitellään. Jos **Poista estetyt kuormarivit** -asetuksena on **Ei**, myyntitilauksen rivit jätetään kuormaan, kun myyntitilaus on luottorajapidossa. Kuormaa ei voi käsitellä, kun myyntitilaus on pidossa. Jos asetuksena on **Kyllä**, myyntitilauksen rivit poistetaan kuormasta, kun myyntitilaus on luottorajapidossa. Kuorma voidaan sitten käsitellä.
- Myyntitilaukset voidaan vapauttaa automaattisesti luotonhallinnan tarkistuksesta. Valitse **Automaattisen vapautuksen syy** -kentässä vapautuksen syy, jota käytetään oletusarvoisesti, kun myyntitilauksen vapautetaan automaattisesti.
- Myyntitilaukset voidaan vapauttaa automaattisesti luotonhallinnan tarkistuksesta. Vapauta tilaus pidosta valitsemalla **Automaattinen vapautus** -kentässä **Kirjaamatta**. Tilauksen pitoon asettanut prosessi on suoritettava manuaalisesti. Valitse **Kirjataan**, jos kirjata tilauksen samalla kirjausprosessilla, jota suoritettiin, kun myyntitilaus asetettiin pitoon.

### <a name="credit-management-checkpoint"></a>Luotonhallinnan tarkistuspiste

Voit määrittää ajoituksen, jolla tarkistetaan myyntitilausten luotto-ongelmat. **Luotonhallinnan tarkistuspiste** -pikavälilehti määrittää asiakirjan kirjausprosessit, mukaan lukien luotonhallintasääntöjen käsittelyn. Voit tarkistaa luottosäännöt myös joko myyntitilauksen proformakirjauksen tai täydellisen kirjauksen yhteydessä. Määritä valintaruutuja valitsemalla kirjausprosessit, jotka asettavat tilauksen pitoon, jos ongelma löytyy luotonhallinnan estosääntöjen käsittelyn jälkeen.

Voit myös määrittää kuinka monta ylimääräistä päivää odotetaan, ennen kuin luottosäännöt tarkistetaan uudelleen. Vaikka voit määrittää, että luotonhallintasäännöt tarkistetaan kirjauksen yhteydessä, sääntöjen tarkistamista odotetaan määritetty määrä ylimääräisiä päiviä. Myyntitilaus esimerkiksi vahvistetaan 1. päivänä ja vahvistusvaihetta määritetään odottamaan kaksi ylimääräistä päivää. Tässä tapauksessa luottosääntöjä ei tarkisteta seuraavassa kirjausvaiheessa (esimerkiksi pakkausluetteloa luotaessa tai tilausta laskutettaessa), ennen kuin 4. päivänä. 4. päivänä tai sen jälkeen säännöt tarkistetaan uudelleen kirjausta tehtäessä, ja odotettavien ylimääräisten päivien määrä muutetaan arvoksi, joka on määritetty seuraavaan kirjauksen tarkistuspisteeseen.

Jos odotettavia ylimääräisiä päiviä ei määritetä, luottosäännöt tarkistetaan jokaisessa kirjausvaiheessa, joka määritetty suorittamaan luotonhallintasäännöt. Jos vapautat myyntitilauksen kirjaamatta ja suoritat saman tilauksen käsittelyvaiheen uudelleen, luottosäännöt tarkistetaan uudelleen. Tilaus voidaan esimerkiksi asettaan pitoon vahvistuksen jälkeen, ja se vapautetaan joko tekemällä kirjaus tai kirjaamatta: Tässä tapauksessa tilaus asetetaan uudelleen pitoon, jos vahvistat sen uudelleen. Tilauksessa kannattaa käyttää ylimääräisiä odottavia päiviä, jos tilauksen on siirryttävä seuraavaan käsittelyvaiheeseen ilman, että asetetaan uudelleen pitoon.

> [!Note]
> Jos yhdelle kirjauksen tarkistuspisteelle on määritetty ylimääräisiä päiviä, kaikilla kirjattavaksi merkityissä tarkistuspisteillä on oltava ylimääräisiä päiviä.

- Valitsemalla **Kirjaus**-valintaruudun voit suorittaa luotonhallintasäännöt, kun rivillä näkyvä kirjauksen tarkistuspiste suoritetaan. Jos valintaruutua ei valita, säännöt tarkistetaan vain kerran koko kirjausprosessin aikana.
- Jos valitset **Kirjaus**-valintaruudun, voit määrittää, kuinka monta ylimääräistä päivää odotetaan, ennen kuin estosäännöt tarkistetaan uudelleen. Ylimääräisiä odottavia päiviä ei voi lisätä, jos **Kirjaus**-valintaruudun valinta on poistettu.
- Valitsemalla **Proforma**-valintaruudun voit suorittaa luotonhallintasäännöt, kun rivillä näkyvä proformakirjauksen tarkistuspiste suoritetaan. Useimmissa tapauksissa **Kirjaus**-kentän arvona on **Ei** siinä valintaikkunassa, joka avautuu, kun myyntitilaus kirjataan.
- Jos valitset **Kirjaus**-valintaruudun, voit määrittää, kuinka monta ylimääräistä päivää odotetaan, ennen kuin estosäännöt tarkistetaan uudelleen. Ylimääräisiä odottavia päiviä ei voi lisätä, jos **Kirjaus**-valintaruudun valinta on poistettu.

### <a name="credit-management-statistics"></a>Luotonhallinnan tilastot

**Asiakas**-sivun **Asiakkaan luotonhallinnan tilastot** -tietoruudussa on useita luotonhallinnan tilastoja. Kyseisten tilastojen laskemiseen tarvittavat arvot on määritettävä. Ilmoita, kuinka monen kuukauden perusteella lasketaan seuraavat **Asiakkaan luotonhallinnan tilastot** -tietoruudun arvot:

1. Selvittämätön päivämyynti 1
2. Selvittämätön päivämyynti 2
3. Keskimääräinen saldo 1
4. Keskimääräinen saldo 2
5. Keskimääräinen luottoraja %
6. Keskimääräinen alttius-%

### <a name="credit-limits"></a>Luottorajat

- Asiakkaan luottoraja näytetään luotonhallinnassa asiakkaan valuuttana. Luottorajan vaihtokurssin tyyppi on määritettävä asiakkaan valuuttana. Valitse **Luottorajan vaihtokurssin tyyppi** -kentässä vaihtokurssin tyyppi, jota käytetään muuntamaan ensisijainen luottoraja asiakkaan luottorajaksi.
- Kun **Salli luottorajojen manuaalinen muokkaus** -asetuksena on **Ei**, käyttäjät eivät voi muokata luottorajoja **Asiakkaat**-sivulla. Jos tässä asetuksessa on valittu **Ei**, asiakkaan luottorajaa voi muuttaa vain kirjaamalla luottorajan oikaisutapahtumia.
- Määritä **Ohita varaston varaukset** -asetukseksi **Kyllä**, jos haluat ohittaa varastovaraukset, kun luotonhallinnan estosäännöt tarkistetaan. Tässä tapauksessa järjestelmä tarkistaa täydet rivimäärät ja ottaa käyttöön tarkistuspisteiden jatkoajat varastovarausmäärästä riippumatta.
- Kun luotonhallinta on käytössä, **Sanoma luottorajan ylittyessä** -kentän asetusta käytetään vain vapaatekstilaskujen käsittelemiseen. Vaikka sanomat lisätään edelleen myyntitilauksiin, kun asiakkaat ovat ylittäneet luottorajansa, näiden sanomien näyttäminen ei estä vahvistusta, keräysluetteloiden ja pakkausluetteloiden tulostamista tai laskujen kirjaamista.

    Luotonhallinta on oletusarvoisesti käytössä, mutta sen voi poistaa käytöstä. Jos se on käytössä, tunnistat luottorajan ylittäneet asiakkaat hyvityshallinnan estosääntöjen ja tarkistuspisteiden avulla. Jos se ei ole käytössä, myyntitilauksiin lisätyt sanomat, jotka perustuvat **Sanoma luottorajakentän ylittyessä** -kentän asetukseen, voivat auttaa tunnistamaan, milloin asiakkaat ovat ylittäneet luottorajansa.

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Numerosarjat ja jaetut numerosarjaparametrit

Luottorajaoikaisujen käsittelemiseen tarvitaan kirjauskansion tunnus. Kirjauskansion tunnukseen käytettävä luottorajan oikaisun numero on lisättävä.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
