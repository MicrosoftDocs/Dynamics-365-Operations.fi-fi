---
title: Lykkäysaikataulut tuoton ja kulujen lykkäyksissä
description: Tässä artikkelissa on tietoja lykkäysaikatauluista tuoton ja kulujen lykkäyksissä.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 093005f9b66d7ce741689b55612f006fa5123910
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903360"
---
# <a name="deferral-schedules"></a>Lykkäysaikataulut

Lykkäysaikataulut luodaan tapahtuman kirjaamisen jälkeen.

**Kaikki lykkäysaikataulut**- tai **Aktiiviset lykkäysaikataulut** -sivulla voit tarkastella yksityiskohtaisia tietoja lykkäysaikataulusta. Näkyvät tiedot määräytyvät ajoitustyypin (tasapoiston tai tapahtumapohjaisen) sekä tapahtumalajin mukaan. Siihen sisältyvät aikataulun lykkäysrivit ja lykkäysaikataulun kokonaissummat. Voit käyttää sivua muokataksesi lykkäysaikataulua.

## <a name="recognize-revenue"></a>Tuoton kirjaus

> [!NOTE]
> - Voit tunnistaa yhden lykkäysaikataulun tuoton aloittaen vaiheesta 1.
> - Voit tunnistaa useita lykkäysaikataulujen tuottoja aloittaen vaiheesta 2.

1. Valitse **Kaikki aikataulut** -sivun **Aikataulun rivit** -ruudukosta rivit, jotka haluat tunnistaa, ja valitse sitten **Tunnista**.
2. Määritä **Tunnistuskäsittely**-sivulla **Tunnistustoiminto**-kentän arvoksi **Luo tunnustuskirjauskansio**.
3. Valitse **Määräpäivä**-kentässä määräpäivä. Käsittely sisältää vain rivit, joilla päättymispäivä on aikaisempi tai sama kuin valittu määräpäivämäärä.
4. Valitse **Suodata** ja lisää tietosuodattimet siten, että luettelossa näkyvät vain haluamasi tietuealue.
5. Voit tarkastella rivejä valitsemalla **Näytä esiversio**.
6. Valitse rivien luettelosta rivit, joita et halua käsitellä, ja valitse sitten **Poista**.
7. Valitse, luodaanko kirjauskirjauskansion merkinnästä yhteenveto.
8. **Tapahtumapäivä**-osassa voit ohittaa tapahtumapäivämäärän tietyllä päivämäärällä ja käsitellä tapahtuman. Tapahtuman päivämäärä voidaan määrittää suljetuille kausille.
9. Voit tehdä käsittelyn osana erää valitsemalla **Erä**. Määritä eräkäsittelyn parametrit **Eräkäsittely**-valintaikkunassa ja palaa sitten **Tunnistuskäsittely**-sivulle valitsemalla **OK**. Tuottokirjauksen käsittely tapahtuu myöhemmin, kun erä käsitellään.
10. Valitse **Prosessi**. Jos sen ei tarvitse lisätä tapahtumaa erään, kaikki rivit käsitellään heti. Muussa tapauksessa rivit käsitellään eräkäsittelyn yhteydessä.

## <a name="modify-a-schedule"></a>Muokkaa aikataulua

Voit muokata lykkäysaikataulun seuraavien ohjeiden avulla.

1. Valitse **Kaikki lykkäysaikataulut** -sivulla lykkäysaikataulu ja valitse sitten **Kirjanpito \> Muokkaa aikataulua**.
2. **Muokkaa aikataulua** -sivulla asetuksia, joita haluat muuttaa. Lykkäysaikataulusta riippuen et voi muokata kaikkia vaihtoehtoja.
3. Valitse **Esiversio** tarkastellaksesi lykkäysaikataulun muutoksia.
4. Valitse **OK**.

### <a name="straight-line-deferral-schedules"></a>Suoraviivaiset lykkäysaikataulut

Jos lykkäysaikataulussa ei ole hyväksyttyjä tai ulkoisesti kirjattuja rivejä, voit muokata koko lykkäysaikataulua aloituspäivämäärä mukaan lukien.

Jos lykkäysaikataulussa on hyväksyttyjä tai ulkoisesti kirjattuja rivejä ja muokkaat lykkäysaikataulua, lykkäysaikataulun tuloksena oleva toimintatapa määräytyy uudelleenlaskentapäivämäärän ja tunnistettujen rivien jäljellä olevan lopetuspäivämäärän mukaan. Lykkäyspäivämäärä määrittää oletusarvon mukaan ensimmäisen kauden, jota ei ole tunnistettu.

Jos haluat käyttää tunnistuspäivää, valitse **Ajoitus alkaa** -kentästä jokin seuraavista arvoista: 
- **Täydennys** – Summa, kun kaikki tunnustetut rivit on laskettu uudelleen.
- **Peruutus** – Uudelleenlaskennan päivämäärän jälkeiset rivit palautetaan käyttämällä määritettyä kirjauskansion nimeä ja kirjauspäivämäärää. Uudelleenlaskennan päivämäärän jälkeen oleva summa lasketaan sitten uudelleen.

Jos mallia käytetään, ohitettuja kausia ei käytetä ja mallia käytetään vain päättymispäivän laskemiseen.

### <a name="event-based-deferral-schedules"></a>Tapahtumaan perustuvat lykkäysaikataulut

Tapahtumaperusteisen lykkäysaikataulun yhteydessä voit muokata kaikkia toteutumattomia rivejä.

Jos lykkäysaikataulussa on hyväksyttyjä tai ulkoisesti kirjattuja rivejä, et voi muokata lykkäysaikataulun mallia ja varaustyyppiä. Kun muokkaat aiemmin luotua lykkäysaikataulua, et voi muuttaa **Yksikkökohtaisten tapahtumien luominen** -kentän arvoa.

Jos rivi tunnistetaan tai kirjataan ulkoisesti, **Hyväksytty**-valintaruutu on valittuna.

## <a name="modify-a-deferral-or-recognition-account"></a>Lykkäys- tai hyväksymistilin muokkaaminen

Jos haluat muokata lykkäysaikataulun lykkäys- tai hyväksymistiliä, noudata seuraavia ohjeita.

1. Valitse **Kaikki lykkäysaikataulut** -sivulla lykkäysaikataulu ja valitse sitten **Kirjanpito \> Muokkaa tiliä**.
2. Valitse **Muokkaa tiliä** -sivulla tili, jota haluat muuttaa (lykkäys, lyhytaikainen tai hyväksyntä).
3. Valitse **Uusi tili** -kentässä uusi tili.
4. Valitse, luovatko tilin muutokset oikaisukirjauskansiomerkintöjä.
5. Jos määrität edellisessä vaiheessa, että asetus on **Kyllä**, valitse kirjauskansion nimi **Kirjauskansion nimi** -kentästä ja määritä tapahtuman päivämäärä **Tapahtumapäivä**-kenttään.
6. Valitse **OK**.

## <a name="put-a-deferral-schedule-on-hold"></a>Lykkäysaikataulun laittaminen pitoon

Voit laittaa lykkäysaikataulun pitoon seuraavien ohjeiden avulla.

1. Valitse **Kaikki lykkäysaikataulut** -sivulla lykkäysaikataulu ja valitse sitten **Pito \> Laita pitoon**.
2. Valitse **Laita pitoon** -sivulla, haluatko siirtää saldon lykkäystililtä vai pitotililtä.
3. Jos valitsit saldon siirron, valitse päiväkirjan nimi kentässä **Kirjauskansion nimi**, valitse lykkäystili **Pidossa oleva tili** -kentässä ja määritä tapahtumapäivä **Tapahtumapäivä**-kenttään.
4. Valitse **OK**.

## <a name="remove-a-hold-from-a-deferral-schedule"></a>Pidosta poistaminen lykkäysaikataulusta

Voit poistaa lykkäysaikataulu pidosta seuraavien ohjeiden avulla.

1. Valitse **Kaikki lykkäysaikataulut** -luettelossa lykkäysaikataulu ja valitse sitten **Pito \> Poista pito**.
2. Valitse **Kirjauskansion nimi** -kentästä kirjauskansion nimi.
3. Määritä **Tapahtuman päivämäärä** -kentässä tapahtuman päivämäärä.
4. Valitse **OK**.

## <a name="cancel-unrecognized-amounts"></a>Peruuta tulouttamattomat summat

> [!NOTE]
> Kaikki jo hyväksytyt tai ulkoisesti kirjatut rivit eivät sisälly tähän prosessiin.

Voit peruuttaa lykkäysaikataulun hyväksymättömiä määriä seuraavien ohjeiden avulla.

1. Valitse **Kaikki lykkäysaikataulut** -sivulla lykkäysaikataulu ja valitse sitten **Peruuta \> Hyväksymättömät määrät**.
2. Valitse **Peruuta hyväksymätön summa** -sivulla, haluatko luoda peruutusmerkintöjä.
3. Jos valitsit peruutuskirjausten luonnin, valitse päiväkirjan nimi kentässä **Kirjauskansion nimi**, valitse peruutustili **Peruutustili**-kentässä ja määritä tapahtumapäivä **Tapahtumapäivä**-kenttään.
4. Valitse **OK**.

## <a name="cancel-a-completed-schedule"></a>Valmiin aikataulun peruuttaminen

**Kaikki lykkäysaikataulut** -sivulla voit palauttaa tunnistetut tai ulkoisesti kirjatut summat ja peruuttaa lykkäysaikataulun, jotta lisäkirjaukset voidaan estää.

Voit peruuttaa koko lykkäysaikataulun seuraavien ohjeiden avulla.

1. Valitse **Kaikki lykkäysaikataulut** -sivulla lykkäysaikataulu ja valitse sitten **Peruuta \> Koko aikataulu**.
2. Valitse **Peruuta koko aikataulu** -sivulla, haluatko luoda peruutusmerkintöjä.
3. Jos valitsit peruutuskirjausten luonnin, valitse päiväkirjan nimi kentässä **Kirjauskansion nimi**, valitse tili **Peruutustili**-kentässä ja määritä tapahtumapäivä **Tapahtumapäivä**-kenttään.
4. Valitse **OK**.

## <a name="reverse-transactions"></a>Palauta tapahtumat

> [!NOTE]
> - Voit peruuttaa yhden lykkäysaikataulun hyväksynnän aloittaen vaiheesta 1.
> - Voit peruuttaa useiden lykkäysaikataulujen hyväksynnän aloittaen vaiheesta 2.

1. Valitse **Kaikki aikataulut** -sivun **Aikataulun rivit** -ruudukosta rivit, joiden hyväksynnän haluat perua, ja valitse sitten **Peruuta**.
2. Määritä **Tunnistuskäsittely**-sivulla **Tunnistustoiminto**-kentän arvoksi **Peruuta hyväksyntäkirjauskansio**.
3. Valitse **Määräpäivä**-kentässä määräpäivä. Käsittely sisältää vain rivit, joilla päättymispäivä on aikaisempi tai sama kuin määritetty määräpäivämäärä.
4. Valitse **Suodata** ja lisää tietosuodattimet siten, että luettelossa näkyvät vain haluamasi tietuealue.
5. Voit tarkastella rivejä valitsemalla **Näytä esiversio**.
6. Valitse rivien luettelosta rivit, joita et halua käsitellä, ja valitse sitten **Poista**.
7. **Nimi**- ja **kuvaus**-kenttiin päivitetään automaattisesti oletuskirjauskansion nimi ja kuvaus. Voit muuttaa arvoja tarpeen mukaan. Voit myös valita, luodaanko kirjauskirjauskansion merkinnästä yhteenveto.
8. **Tapahtumapäivä**-osassa voit ohittaa tapahtumapäivämäärän tietyllä päivämäärällä ja käsitellä tapahtuman. Tapahtuman päivämäärä voidaan määrittää suljetuille kausille.
9. Voit tehdä käsittelyn osana erää valitsemalla **Erä**. Määritä eräkäsittelyn parametrit **Eräkäsittely**-valintaikkunassa ja palaa sitten **Tunnistuskäsittely**-sivulle valitsemalla **OK**. Tuottokirjauksen käsittelyn peruuttaminen tapahtuu myöhemmin, kun erä käsitellään.
10. Valitse **OK**. Jos sen ei tarvitse lisätä tapahtumaa erään, kaikki rivit käsitellään heti. Muussa tapauksessa rivit käsitellään eräkäsittelyn yhteydessä.

## <a name="apply-or-unapply-a-credit-note"></a>Hyvityslaskun kohdistaminen tai sen poistaminen

Voit ottaa hyvityslaskun käyttöön seuraavien ohjeiden avulla.

> [!NOTE]
> Kun luot hyvityslaskun **Myyntitilauksen tapahtuman lykkäys** -sivulta ja asetat **Muokkaa nykyistä aikataulua** -asetukseksi **Kyllä**, hyvityslasku otetaan automaattisesti käyttöön aikataulussa, kun hyvitys huomautus on lähetetty.

1. Valitse **Kaikki lykkäysaikataulut** -sivulla lykkäysaikataulu.
2. Valitse **Hyvitysoikaisut**-luettelosta rivi ja valitse sitten **Käytä**.
3. Määritä **Käytä hyvityslaskua (lykkäykset)** -sivulla **Uudelleenlaskennan päivämäärä** -kentässä Uudelleenlaskennan päivämäärä ja päättymispäivä **Päättymispäivä**-kenttään.
4. Valitse **Otsikko**-luettelosta **myyntitilaus**, jossa on hyvityslaskuja.
5. Valitse rivi **Rivit**-luettelosta.
6. Valitse **OK**.
7. Valitse **Kyllä**.

> [!NOTE]
> Voit kohdistaa hyvityslaskun useisiin eri laskujen yksittäisiin nimikkeisiin toistamalla nämä vaiheet.

Voit poistaa hyvityslaskun käytöstä seuraavien ohjeiden avulla.

1. Valitse **Kaikki lykkäysaikataulut** -sivulla lykkäysaikataulu.
2. Valitse **Hyvitysoikaisut**-luettelosta lasku ja valitse sitten **Poista käytöstä**.
3. Valitse **Kyllä**.

## <a name="fields"></a>Kentät

**Kaikki lykkäysaikataulut** -sivu sisältää seuraavat kentät.

| Kentät | Kuvaus |
|--------|-------------|
| **Otsikko** | |
| **Aikatauluta** | |
| Kohdistustyyppi | Tapahtumaan perustuvien lykkäyksien kohdistustyyppi: **prosentti** tai **summa**. |
| Uudelleenluokittelupäivä | <p>Viimeisin päivämäärä, jolloin lykkäysaikataulun lyhyt uudelleenluokittelu on käsitelty. Tämä päivämäärä päivitetään aina, kun lykkäysaikataulussa käytetään **tapahtuman lyhyttä uudelleenluokittelua**.</p>Tämä kenttä on käytettävissä vain, kun käytössä on liukuva kausi tai kiinteä lyhytkestoinen lykkäysmenetelmä. |
| **Tili** | |
| Lykkäystili | Lykkäyssummalle käytettävä tili. |
| Tuloutustili | Hyväksyntäsummalle käytettävä tili. |
| Tuloutustyyppi | Hyväksyntätyyppi. |
| Jaon tyyppi | Jaon tyyppi. |
| **Tapahtuma** | |
| Luontilähde | Lähde, josta tapahtuma luotiin. |
| Tapahtumatyyppi | Tapahtumatyyppi. |
| Myyntitilaus | Myyntitilausnumero. |
| Lasku | Laskunumero. |
| Nimike | Nimikkeen numero. |
| **Laskutusaikataulu** | |
| Laskutusaikataulun numero | Vastaavan laskutusaikataulun numero. |
| Laskutusrivin tila | Vastaavan laskutusaikataulurivinimikkeen tila. |
| Ulkoiset viittaukset | Tietoja laskutusaikataulun ulkoisista viitteistä: **ulkoinen viite** ja **rivinumero**. |
| Summat | <p>Lykkäysaikataulun summat:</p><ul><li>**Pitkäaikainen** – Pitkäaikaisten lykättyjen määrien summa. Tämä arvo on käytettävissä vain , kun **lyhytkestoinen lykkäysmenetelmä** -kentän arvoksi on määritetty **Ei mitään** **tuotto- ja kulujen lykkäysparametrit** -sivulla tai kun lyhytaikainen summa on suurempi kuin 0 (nolla).</li><li>**Lyhytaikainen** – Lyhytaikaisten lykättyjen määrien summa. Tämä arvo on käytettävissä vain , kun **lyhytkestoinen lykkäysmenetelmä** -kentän arvoksi on määritetty **Ei mitään** **tuotto- ja kulujen lykkäysparametrit** -sivulla tai kun lyhytaikainen summa on suurempi kuin 0 (nolla).</li><li>**Hyväksymätön** – Kaikkien rivien hyväksymättömät summat yhteensä.</li><li>**Typistetty** – Kaikkien rivien ulkoisesti kirjatut summat yhteensä.</li><li>**Hyväksytyt** – Kaikkien rivien hyväksytyt summat yhteensä.</li><li>**Ulkoisesti kirjattu ja hyväksytty** – Ulkoisesti kirjattujen ja hyväksyttyjen määrien summa kaikilla riveillä.</li><li>**Summa yhteensä** – Määrien summa kaikilla riveillä.</li></ul> |
| **Aikataulurivit** | |
| Rivi | Rivin luonnin järjestysnumero. |
| Lykkäyksen alkamispäivä | Lykkäysaikataulun alkamispäivä. |
| Lykkäyksen päättymispäivä | Lykkäysaikataulun päättymispäivä. |
| Määrä | Hyväksynnän summa. |
| Kirjattu ulkoisesti | Tämä arvo ilmaisee, onko rivi kirjattu ulkoisesti. |
| Tuloutettu | Tämä arvo ilmaisee, onko rivi hyväksytty. |
| Kirjauskansion eränumero | Eränumero, jossa summa tunnistettiin. |
| Tapahtuman kuvaus | Tapahtuman kuvaus. Tämä kenttä on käytettävissä vain tapahtumaan perustuvia lykkäysaikatauluja varten. |
| **Luoton oikaisut** | |
| Lasku | <p>Laskunumero.</p><p>Arvo ilmaisee hyvityslaskun oikaisun laskun, joka on jo otettu käyttöön lykkäysaikataulussa.</p> |
| Määritetty summa | Lykkäysaikatauluun jo kohdistettu luotto-oikaisusumma. |
| Kohdistuksen päivämäärä | Päivämäärä, jolloin hyvitysoikaisua on käytetty. |
| **Oikaisu** | Oikaisuarvot näkyvät vain, jos lykkäysaikataulua varten on käsitelty hyvityslaskua. Jos hyvityslaskua ei ole käsitelty, arvot piilotetaan. |
| Oikaisusumma | Oikaisun kokonaissumma, joka lasketaan käyttäen *alkuperäistä summaa* – *ajoitettua summaa*. |
| Alkuperäinen päättymispäivämäärä | Alkuperäinen lykkäysaikataulun päättymispäivä. |
| Alkuperäinen aikataulun summa | Koko alkuperäinen lykkäysaikataulu. |
