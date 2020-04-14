---
title: Luotonhallinnan parametrien määrittäminen
description: Tässä ohjeaiheessa käsitellään asetuksia, joilla luotonhallinta voidaan määrittää vastaamaan yrityksen tarpeita.
author: mikefalkner
manager: AnnBe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6d4ced14e51dd28d51d2081d8e92891e31eea49d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154525"
---
# <a name="credit-management-parameters-setup"></a>Luotonhallinnan parametrien määrittäminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään asetuksia, joilla luotonhallinta voidaan määrittää vastaamaan yrityksen tarpeita. Luotonhallinnan toimintojen käyttö aloitetaan määrittämällä parametrit **Luotonhallinta- ja perimisparametrit** -sivulla (**Luotonhallinta- ja perintä \> Asetukset \> Luotonhallinta- ja perintäparametrit**).

## <a name="credit-parameters"></a>Luottoparametrit

Luotonhallintaa ohjaavia parametreja voi muuttaa **Luotto**-osan neljässä pikavälilehdessä: **Luottorajapidot**, **Luotonhallinnan tarkistuspiste**, **Luotonhallinnan tilastot** ja **Luottorajat**. Seuraavissa osissa käsitellään kussakin pikavälilehdessä olevia asetuksia.

### <a name="credit-holds"></a>Luoton pidot

- Jos **Salli myyntitilausten arvon muokkaus sen jälkeen, kun tilaus on vapautettu pidosta** -asetuksena on **Kyllä**, kirjaussäännöt on tarkistettava uudelleen, jos myyntitilauksen arvo (laajennettu hinta) on muuttunut sen jälkeen, kun myyntitilaus vapautettiin pitoluettelosta. .
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

Odottavia ylimääräisiä päiviä ei voi määrittää joihinkin kirjauksen tarkistuspisteisiin muttei toisiin. Kaikki kirjauksen tarkistuspisteet on määritettävä siten, että niissä joko on ylimääräisiä odottavia päiviä tai niitä ei ole.

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

### <a name="number-sequences-and-shared-number-sequence-parameters"></a>Numerosarjat ja jaetut numerosarjaparametrit

Luottorajaoikaisujen käsittelemiseen tarvitaan kirjauskansion tunnus. Kirjauskansion tunnukseen käytettävä luottorajan oikaisun numero on lisättävä.
