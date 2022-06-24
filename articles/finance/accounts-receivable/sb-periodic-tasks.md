---
title: Toistuvan sopimuksen laskutuksen kausittaiset tehtävät
description: Tässä artikkelissa käsitellään toistuvan sopimuksen laskutuksen kausittaiset tehtävät.
author: JodiChristiansen
ms.date: 04/29/2022
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
ms.openlocfilehash: d834d1d7aa34448b4ef21606974538eb294b5d7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904785"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>Toistuvan sopimuksen laskutuksen kausittaiset tehtävät

Tässä artikkelissa käsitellään toistuvan sopimuksen laskutuksen kausittaiset tehtävät.

## <a name="generate-invoice"></a>Luo lasku

Käytä **Luo lasku** -sivua luodaksesi toistuvat kuukausittaiset massalaskut tiedoista, jotka määritit **Kaikki laskutusaikataulut** -kohdassa ja **Näytä laskutustiedot** -sivuilla. Kun lasku luodaan, myyntitilauksen käsittelyrivin nimikkeen kuvaukseen päivitetään nimikkeen kuvaus sekä laskutettavan aikataulurivin laskutuksen alkamis- ja päättymispäivämäärät.

## <a name="generate-invoice-batch-processing"></a>Luo laskun erätöiden käsittely

Käytä **Luo laskun erätöiden käsittely** -sivua luodaksesi toistuvat laskut toistuvien erätöiden käsittelyn avulla. Käytössä olevat parametrit ovat samat kuin parametrit **Luo lasku** -sivulla, mutta ne voi tallentaa erätöiden käsittelyssä, jonka voi suorittaa useita kertoja.

## <a name="price-update"></a>Hinnanpäivitys

Käytä Hinnan päivitys -toimintoa päivittääksesi yhdellä toiminnolla useiden nimikkeiden hinnat useissa laskutusaikatauluissa. Hinnat voidaan päivittää joko määritetyn prosenttiosuuden tai määritetyn summan perusteella. Rivien luettelossa näkyvät vain nimikkeiden nykyiset yksikköhinnat. Hinnat eivät näy sen jälkeen, kun hinta on päivitetty.

Ota huomioon seuraavat Hinnan päivitys -työkaluun liittyvät seikat:

- Jos tietyn vuoden myyntitilaus on jo luotu (eli nimikkeet on laskutettu), rivinimikkeiden hintaan ei ole vaikutusta.
- Hinnan päivitys -toimintoa voidaan käyttää rivinimikkeisiin, joiden tila on **Aktiivinen** tai **Pidossa**. Jos nimike on pidossa, **Säädä aikataulua** -vaihtoehdon on oltava tilassa **Ei** pidon asettamisen aikana.
- Hinnan päivitys -työkalua ei voi käyttää rivinimikkeissä, jotka ovat käyttönimikkeitä tai jotka käyttävät eskalointia, tavoitteisiin perustuvaa laskutusta tai tuottojen jakoa.

### <a name="price-update-example"></a>Hinnan päivityksen esimerkki

Laskutusaikataulu luodaan ja uusittava nimike lisätään. Yksikköhinta on 750 dollaria. Nimikkeen ensimmäinen vuosi maksetaan 15. joulukuuta 2021. Laskutusaikataulu luodaan ajanjaksolle 1.1.–31.12.2022.

Uusinta-ajankohtana **Luo lasku** -prosessi luo myyntitilauksen vuodelle 2022. Kun hinnan päivitys suoritetaan, hinta päivitetään 750 dollarista 800 dollariin.

Vuoden 2022 myyntitilaukseen ja laskutusaikatauluun ei ole vaikutusta, ja yksikköhinnaksi jää 750 dollaria, koska vuoden 2022 laskutusaikataulu on jo laskutettu. Vuoden 2023 laskutusaikataulun rivi ja rivitiedot päivitetään 800 dollariin, koska vuoden 2023 laskutusaikataulua ei ole vielä laskutettu.

### <a name="update-prices--flat-pricing-method"></a>Hintojen päivittäminen – Kiinteä hinnoittelumenetelmä

Kun päivität hintoja nimikkeille, jotka käyttävät kiinteää hinnoittelumenetelmää, voit määrittää hinnan korotusprosentin tai summan.

Kun haluat suorittaa kiinteän hinnoittelumenetelmän nimikkeille hinnan päivityksen, noudata seuraavia ohjeita.

1. Valitse **Hinnan päivitys** -sivulla **Kiinteä** hinnoittelumenetelmä.
2. Valitse **Lisäysmenetelmä**-kentässä lisäysmenetelmä, jota käytetään nimikkeiden hinnan päivityksessä.
3. Määritä valitsemasi lisäysmenetelmän mukaan prosentti **Prosentti**-kenttään tai määrä **Määrä**-kenttään.
4. Käytä **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**-painiketta lisätäksesi suodattimia.
5. Voit tarkastella tietuealuetta valitsemalla **Näytä esiversio**.
6. Valitse rivien luettelosta rivit, joita et halua käsitellä, ja valitse sitten **Poista**.
7. Valitse **OK**.

### <a name="update-prices--standard-pricing-method"></a>Hintojen päivittäminen – Vakiohintamenetelmä

Jos nimikkeen hinta on muuttunut nimiketietueessa, se voidaan päivittää kaikille laskutusaikatauluriveille, jos nimike käyttää vakiohintamenetelmää.

1. Valitse **Hinnan päivitys** -sivulla **Vakio**-hinnoittelumenetelmä.
2. Käytä **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**-painiketta lisätäksesi suodattimia.
3. Voit tarkastella tietuealuetta valitsemalla **Näytä esiversio**.
4. Valitse rivien luettelosta rivit, joita et halua käsitellä, ja valitse sitten **Poista**.
5. Valitse **OK**.

## <a name="mass-hold-processing"></a>Joukkopitokäsittely

Käytä **Joukkopito**-sivua soveltaaksesi pitoasetuksia useille laskutusaikatauluille samanaikaisesti.

Voit asettaa vain yhden laskutusaikataulun tai yhden laskutusaikataulurivin pitoon avaamalla **Kaikki laskutusaikataulut** -sivun ja valitsemalla **Aseta pitoon**. Käytä **Poista pito** -sivua poistaaksesi pidon.

### <a name="put-billing-schedules-on-hold"></a>Aseta laskutusaikataulut pitoon

Voit asettaa useita laskutusaikatauluja pitoon seuraavien ohjeiden avulla.

1. Määritä **Joukkopito**-sivulla **Prosessiasetus**-kenttä arvoon **Käytä pitoa**.
2. Valitse uusi syykoodi **Syykoodi** -kentässä.
3. Määritä **Säädä aikataulua** -asetus:

    - **Kyllä** – Jos määrität tämän asetuksen arvoon **Kyllä**, määritä pidon päivämäärä **Pidon päivämäärä** -kentässä. Kaikki pidon päivämäärän jälkeiset laskutusaikataulun rivit poistetaan.
    - **Ei** – Laskutusaikataulun rivejä ei muuteta. Vain tilaa muutetaan. Se päivitetään arvoon **Pidossa**.

4. Käytä **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**-painiketta lisätäksesi suodattimia.
5. Voit tarkastella tietuealuetta valitsemalla **Näytä esiversio**.
6. Valitse rivien luettelosta rivit, joita et halua käsitellä, ja valitse sitten **Poista**.
7. Valitse **OK**.

Kun palaat laskutusaikataulujen luetteloon, sinun tulisi nähdä, että laskutusaikataulujen tilaksi on muutettu **Pidossa**.

### <a name="remove-a-hold-from-several-billing-schedules"></a>Pidon poistaminen useista laskutusaikatauluista

1. Määritä **Joukkopito**-sivulla **Prosessiasetus**-kenttä arvoon **Poista pito**.
2. Syötä syykoodi **Syykoodi** -kentässä.
3. Valitse **Poistopäivämäärä**-kenttään päivämäärä, jona pito tulisi poistaa.
4. Määritä **Jatkamispäivä**- ja **Lykkäyspäivä**-kentät tarpeittesi mukaan. Lykkäyspäivä lisätään kaikille riveille, jotka ovat lykättäviä.
5. Käytä **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**-painiketta lisätäksesi suodattimia.
6. Voit tarkastella tietuealuetta valitsemalla **Näytä esiversio**.
7. Valitse rivien luettelosta rivit, joita et halua käsitellä, ja valitse sitten **Poista**.
8. Valitse **OK**.

> [!NOTE]
> Jos haluat poistaa pidon, sinun on määritettävä **Poista käyttäjäryhmältä pidon ohitus** -arvo **Toistuvan sopimuksen laskutusparametrit** -sivulla.

Laskutusrivin alkamispäivämäärä on esimerkiksi 1.2.2022 ja päättymispäivä 28.2.2022. Laskutussumma on 200 dollaria. **Pidon päivämäärä** -kenttään on määritetty 10.2.2022. Siksi helmikuun jaksoa oikaistaan siten, että pois jätetään kaikki 10. helmikuuta jälkeiset päivät. Uusi kausi on 1.–9.2. ja määrä 64,29 dollaria (päivittäisen suhteellisen jaon kautta). Kaikki laskutusaikataulurivit päivältä 10.2. ja sen jälkeen poistetaan.

Jos **Poista pito** -prosessi on valmis ja **Poistopäivämäärä**-kenttään on määritetty 10.2.2022, laskutuskausia tulee kaksi. Ensimmäinen laskutuskausi on 1.–9.2. ja määrä 64,29 dollaria. Toinen laskutuskausi on 10.–28.2. ja määrä 135,71 dollaria.

## <a name="mass-termination-processing"></a>Joukkoirtisanomiskäsittely

Käytä **Joukkoirtisanominen**-sivua irtisanoaksesi laskutusaikataulurivit, jotka näytetään määrittämällä irtisanomispäivämäärä.

Jos käytät tuotto- ja kululykkäyksiä, laskutusaikataulut, joissa **Irtisanomispäivämäärä**-kenttä on määritetty arvoon **Säädä aikataulua** **Kaikki laskutusaikataulut** -sivulla, ovat oikeutettuja hyvitykseen.

Laskutusaikataulut, jotka käyttävät usean elementin kohdistustoimintoa (multiple element allocation, MEA), eivät näy **Joukkoirtisanominen**-sivulla. Voit silti irtisanoa yksittäisen laskutusaikataulun käyttämällä laskutusaikataulun irtisanomistoimintoa.

> [!NOTE]
> Laskutusaikataulurivit, jotka kuuluvat **Luo lasku** -erään, eivät ole tämän prosessin käytettävissä.

Tietoja prosessista ja kaikista kentistä: [Laskutusaikataulujen lakkauttaminen](terminate-billing-schedule.md).

## <a name="mass-archive-process"></a>Joukkoarkistointiprosessi

Käytä **Joukkoarkisto**-sivua useiden laskutusaikataulujen arkistoimiseksi. Vain lakkautetut laskutusaikataulut voidaan arkistoida.

Kun laskutusaikataulu on arkistoitu, tapahtuu seuraavaa:

- Tilaksi muuttuu **Arkistoitu**.
- Laskutusaikataulut on lukittu pysyvästi.
- Laskutusaikataulurivit eivät ole enää käytettävissä kyselysivuilla.

> [!NOTE]
> Laskutusaikataulun arkistointi on pysyvä toimenpide, eikä sitä voi peruuttaa.

Voit arkistoida laskutusaikataulun seuraavien ohjeiden avulla.

1. Määritä **Joukkoarkisto**-sivulla, **Laskutuksen päättymispäivä** kentässä, laskutuksen päättymispäivämäärä. Jos haluat tarkastella kaikkia lakkautettuja laskutusaikatauluja, jätä tämä kenttä tyhjäksi.
2. Käytä **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**-painiketta rajoittaaksesi näytettäviä tietueita.
3. Valitse **Näytä esiversio**.
4. Valitse rivien luettelosta tietueet, joita et halua arkistoida, ja valitse sitten **Poista**.
5. Arkistoi tietueet sivulle valitsemalla **OK**.

## <a name="mass-stubbing-process"></a>Kannaksi muuttamisen joukkoprosessi

Käytä **Kannaksi muuttamisen joukkoprosessi** -sivua merkitäksesi valitut laskutusaikataulurivit laskutetuiksi (kannaksi muuttaminen) tai laskuttamattomiksi (kannaksi muuttamisen peruuttaminen). Kannaksi muuttaminen ja kannaksi muuttamisen peruuttaminen tehdään useimmiten tuoduille laskutusaikatauluriveille, jotka laskutettiin aiemmin muussa järjestelmässä. Kannaksi muutetut laskutusaikataulurivit näkyvät kannaksi muutettuina, eivätkä ne luo laskua asiakkaalle.

### <a name="stub-records"></a>Tietueen muuttaminen kannaksi

1. Valitse **Kannaksi muuttamisen joukkoprosessi** -sivulla, **Prosessin asetukset** -kentässä, **Muuta kannaksi**.
2. Määritä **Katkaisupäivä**-kentässä katkaisupäivä, jotta voit määrittää rivit, joihin haluat soveltaa prosessia. Näytetään vain tietueet, joiden laskutuksen alkamispäivämäärä on sama tai aikaisempi kuin määritetty katkaisupäivä.
3. Valitse **Näytä esiversio**, niin näet, mitkä rivit haluat muuttaa kannaksi.
4. Jos haluat poistaa rivin prosessista, merkitse se ja valitse sitten **Poista**.
5. Valitse **Käsittele** muuttaaksesi rivit kannaksi.

### <a name="reverse-stub-records"></a>Kumoa kannan tietueet

1. Valitse **Kannaksi muuttamisen joukkoprosessi** -sivulla, **Prosessin asetukset** -kentässä, **Kumoa kanta**.
2. Määritä **Katkaisupäivä**-kentässä katkaisupäivä, jotta voit määrittää rivit, joihin haluat soveltaa prosessia. Näytetään vain tietueet, joiden laskutuksen alkamispäivämäärä on sama tai aikaisempi kuin määritetty katkaisupäivä.
3. Valitse **Näytä esiversio**, niin näet, mihin riveihin haluat käyttää kannan kumoamista.
4. Jos haluat poistaa rivin prosessista, merkitse se ja valitse sitten **Poista**.
5. Valitse **Käsittele** käyttääksesi riveihin kannan kumoamista.

## <a name="update-completion-date-process"></a>Päivitä valmistumispäivä -prosessi

Käytä **Päivitä valmistumispäivä** -sivua päivittääksesi valmistumispäivän tietyille tavoitenimikkeille, useille laskutusaikatauluille tai käyttäjille. Voit myös päivittää prosenttia valmiina -arvon tavoitemallien nimikkeille, jotka käyttävät **Prosenttia valmiina** -menetelmää.

1. Siirry **Päivitä valmistumispäivä** -sivulla kohtaan **Välitavoitteen käsittely** ja valitse **Päivityksen valmistumisprosentti**.
2. Syötä **Prosenttimäärä**-kenttään valmistumisprosentti.
3. Valitse nimikenumero, joka liittyy tavoitemalliin.
4. Valitse **Sisällytettävät tietueet** -pikavälilehdessä **Suodatin**, niin voit valita tietyn **Loppukäyttäjän tilin**, **Laskutusaikataulun numeron** tai **Nimikenumerot** suodatinehdoksi.
5. Käsittele muutos valitsemalla **OK**. Kun käsittely on valmis, tavoitekohdistukseen lisätään uusi rivi. Tämä rivi ilmaisee prosenttiosuuden, joka on valmiina tavoitemallille.

## <a name="unbilled-revenue-mass-processing"></a>Laskuttamattoman tuoton joukkokäsittely

Käytä **Laskuttamattoman tuoton joukkokäsittely** -sivua luodaksesi laskuttamattoman tuoton kirjauskansioviennin tai muuttaaksesi valitun laskutusaikataulun tai laskutustietorivin kirjauskansioviennin kannaksi.

- **Luo kirjauskansiovienti** – Luo laskuttamattomia tuottojen kirjauskansiovientejä useiden laskutusaikataulurivien osalta. Käytä **Suodatin**-painiketta **Sisällytettävät tietueet** -pikavälilehdessä valitaksesi luettelossa näkyvän tietuealueen. Luettelossa näkyvät vain laskutusaikataulurivit, joille ei ole luotu laskuttamattomia tuottojen kirjauskansiovientejä. Ensimmäiset kirjauskansioviennit luodaan. Lykkäysnimikkeille luodaan myös lykkäysaikataulut.
- **Kirjauskansioviennin muuttaminen kannaksi** – Merkitse laskutusaikataulurivit, joille on jo luotu laskuttamattomat kirjauskansioviennit. Tätä vaihtoehtoa käytetään, jos laskuttamaton kirjauskansiovienti on jo kirjattu toiseen järjestelmään. Laskuttamattoman tuoton kirjauskansio merkitään muutetuksi kannaksi, ja transaktiota ei kirjata kirjanpitoon.
- **Kumottu kantakirjauskansiovienti** – Kumotut kantakirjauskansioviennit, jotka on käsitelty. Jos **Kantakirjauskansioviennin** käsittelyn yhteydessä tuli virhe, tämä asetus tyhjentää laskutusaikataulurivin **Muutettu kannaksi** -valintaruudun.
- **Muuta laskutuksen tietorivi kannaksi** – Käytä tätä prosessia, jos laskuttamaton tuotto käsiteltiin ulkoisessa järjestelmässä ja tietyt laskutustietorivit on jo laskutettu. Tämän prosessin avulla voit varmistaa, että laskuttamattoman tuoton tileillä näkyy oikea summa.
- **Kumoa kantalaskutuksen tietorivi** – Kumoa mitä tahansa **Muuta laskutuksen tietorivi kannaksi** -toimintoja.

**Kirjauskansion nimi** -kenttää käytetään **Luo kirjauskansiovienti** -toiminnon kirjaamiseksi kirjanpitoon.

> [!NOTE]
> Kannaksi muuttamisen prosessi ei kirjaa määriä kirjanpitoon. **Kirjauskansion nimi** -kenttä ei ole käytettävissä kaikille kannaksi muuttamisen ja kannan kumoamisen prosesseille.

### <a name="unbilled-revenue-stub-example"></a>Laskuttamattoman tuottokannan esimerkki

Laskutusaikataulu määritetään yhdelle vuodelle (vuoden 2021 lokakuusta syyskuuhun 2022). Laskuttamaton tuotto on jo käsitelty ulkoisessa järjestelmässä. Laskutusaikataulusta on jo laskutettu yhdeksän kuukautta. Laskutuskauden summa on 250 dollaria. Vuoden alussa laskuttamattomaan tuottoon kirjattu kokonaissumma on 3 000 dollaria. Yhdeksän kuukauden kuluttua 2 250 dollaria on jo laskutettu, ja laskuttamatonta tuottoa on jäljellä 750 dollaria.

Noudattamalla näitä ohjeita voit määrittää laskutusaikataulun, jossa laskuttamatonta tuottoa on jäljellä vain kolmelta kuukaudelta.

1. Luo **Näytä laskutustiedot** -sivulla laskutusaikataulu jaksolle lokakuu 2021 - syyskuu 2022, nimikenumero S0001 ja kuukausittainen summa 250 dollaria.
2. Valitse laskutusaikataulua varten **Luo kirjauskansiovienti**. Summa 3 000 dollaria kirjataan laskuttamattomaan tuottoon.
3. Valitse **Muuta laskutuksen tietorivi kannaksi** ja määritä transaktiopäivämääräksi kesäkuu 2022 (yhdeksän kuukautta). Laskutusaikataulun rivit eivät näy esiversiossa. Rivit, joihin toimenpide vaikuttaa, perustuvat transaktiopäivämäärään.
4. Valitse **OK**.

Ensimmäiset yhdeksän laskutettua kuukautta on muutettu kannaksi.

[![Tarkastele laskutustietorivien kantaa.](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

3 000 dollaria palautetaan laskuttamattomista tuotoista, ja jäljellä oleva 750 dollarin laskuttamaton tuotto kirjataan. Jos haluat tarkastella laskuttamattoman tuoton kirjauksia, valitse **Laskuttamattoman tuoton kirjauskansioviennin tarkistus** rivitietojen sivun **Uusimiset**-välilehdessä.

[![Laskuttamattoman tuoton kirjauskansioviennin tarkistus.](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> Voit luoda laskuttamattoman tuoton kirjauskansioviennin mille tahansa uusimiskaudelle, jos kaikki edellisen kauden laskutustietorivit on laskutettu. Esimerkiksi laskutusaikataulun rivin laskutustiheys on kuukausi 12 kuukauden jaksolla, tammikuusta joulukuuhun 2021. Rivillä on kolme kautta: alkuperäinen kausi, toinen kausi (tammikuu - joulukuu 2022) ja kolmas kausi (tammikuu - joulukuu 2023). Kun lasku on luotu kaikille laskutustietojen riveille 12 kuukaudelta vuodelta 2021, laskuttamattoman tuoton kirjauskansioviennin voi luoda toista kautta varten.
>
> Lykkäysnimikkeille, jotka käyttävät laskuttamattoman tuoton ominaisuutta, käsitellään laskutusrivi ja alennusrivit. Näille nimikkeille luodaan laskuttamattoman tuoton kirjauskansiovienti, laskutusrivin lykkäysaikataulu ja alennusrivi.
>
> Kirjauskansioviennit, jotka on luotu ei-lykättäviä nimikkeitä ja lykkäysnimikkeitä varten, kirjaavat hyvityksen eri tuottotileille.
