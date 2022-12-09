---
title: Kirjanpidon selvitykset
description: Tässä artikkelissa käsitellään tapaa, jolla Tapahtuman selvitykset -sivun avulla selvitetään kirjanpitotapahtumia ja tehdään käänteisiä tilityksiä.
author: kweekley
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6357629f83873437eb62a4839fafd8efd98fffc1
ms.sourcegitcommit: 9041fa6e00ecbdf1a1880659d9bdfff4d888f20e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/22/2022
ms.locfileid: "9800628"
---
# <a name="ledger-settlements"></a>Kirjanpidon selvitykset

[!include [banner](../includes/banner.md)]

Kirjanpidon tilitys on prosessi, jossa kirjanpidon debet- ja kredittapahtumat täsmäytetään. Debet- ja kreditsummien tilitystä käytetään kirjanpitotilin saldon täsmäytykseen saldon muodostavien yksityiskohtaisten tapahtumien kanssa.

Selvitetyt tapahtumat voidaan jättää pois kyselyistä ja raporteista. Näin on helpompi analysoida avoimia kirjanpitotapahtumia, jotka muodostavat kirjanpitotilin saldon.

> [!IMPORTANT] 
> Myyntireskontran ja ostoreskontran moduuleissa on myös laskujen ja maksujen täsmäytys. Kun selvitys tapahtuu myyntireskontran ja ostoreskontran alareskontrassa, vastaavia kirjanpitokirjauksia ei täsmäytetä automaattisesti.

## <a name="ledger-settlement-features"></a>Tapahtuman selvityksen ominaisuudet
Microsoft Dynamics 365 Finance -versiossa 10.0.21 **Ota käyttöön kirjanpidon lisäselvitysvaihtoehto** on poistettu **Kirjanpitoparametrit**-sivulta. Kirjanpidon lisäselvitys on nyt aina käytössä.
Finance-versiossa 10.0.25 on otettu käyttöön **Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä** -ominaisuus. Tämä ominaisuus muuttaa kirjanpidon tilityksen ja kirjanpidon tilinpäätöksen perustoimintoja. Ennen kuin otat tämän ominaisuuden käyttöön **Ominaisuuden hallinta** -työtilassa, katso [Tietoja kirjanpidon selvityksestä ja tilinpäätöksestä](awareness-between-ledger-settlement-year-end-close.md).

## <a name="set-up-ledger-settlement"></a>Määritä kirjanpidon tilitys
Päätilit, joista haluat tehdä tapahtumien selvityksen, on valittava. Nämä päätilit voidaan valita kahdella tavalla.

1. Valitse **Kirjanpito** > **Kirjanpidon asetukset** > **Kirjanpitoparametrit**.
2. Valitse **Kirjanpidon tilit** -välilehdessä tilikartat, joista haluat valita päätilit.
3. Valitse päätilit täsmäytystä varten. Koska tilikartat ovat yleisiä, kaikilla valitun tilikartan yrityksillä on samat päätilit valittuna tapahtumien selvitystä varten.

  -tai-

1. Valitse **Kirjanpito** > **Kausittaiset tehtävät** > **Tapahtuman selvitykset**.
2. Valitse **Kirjanpidon tilitystilit**.
3. Valitse valintaikkunassa tilikartat ja päätilit, joille tilitys tehdään. Tämä valintaikkuna on pikavalinta. Kaikki tähän lisätyt päätilit näkyvät myös **Kirjanpidon parametrit** -sivulla.

Samoja perusmenettelyjä voidaan käyttää päätilien poistamiseen kirjanpidon tilityksestä milloin tahansa. Päätilin poistaminen ei vaikuta aiempiin kirjanpitotilityksiin. Päätili ja tapahtumat eivät kuitenkaan enää näy **Kirjanpidon tilitys** -sivulla.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Selvitä tapahtumat
Voit selvittää kirjanpitotapahtumia seuraavien ohjeiden avulla.

1. Valitse **Kirjanpito** > **Kausittaiset tehtävät** > **Tapahtuman selvitykset**.
2. Määritä sivun yläosassa olevat suodattimet:

    - Valitse päivämääräväli. Valitse vaihtoehtoisesti päivämääräaluekoodi täyttääksesi automaattisesti päivämäärävälin. Kirjanpidon tilitys ei ole suositeltavaa, jos tapahtuma ylittää tilikaudet.
    - Muuta kirjanpitotasoa tarpeen mukaan. Et voi selvittää tapahtumia, jotka ovat eri kirjaustasoilla.
    - Jos haluat näyttää päätiliin ja dimensiot erikseen, valitse taloushallinnon dimensioyhdistelmä

3. Valitse **Näytä tapahtumat**, jos haluat näyttää kaikki määritettyjä suodattimia vastaavat tapahtumat ja tililuettelon, jonka määritit, kun määritit tilikarttaluettelon edellisessä osassa.

    - Jos muutat suodattimia tai dimensioyhdistelmiä, sinun on valittava uudelleen **Näytä tapahtumat**.
    - Voit suodattaa tapahtumat yksittäiselle päätilille käyttämällä **Kirjanpitotili**-kentän suodatinta. Ei ole suositeltavaa, että eri päätileille kirjattavat tapahtumat tilitetään.

4. Valitse rivit tilitykseen. Sivun yläosassa olevan **Valittu summa** -kentän arvo suurenee tai pienenee valittujen rivien kokonaissumman mukaan.
5. Kun olet valinnut tapahtumat, valitse **Merkitse valitut**. Kunkin valitun tapahtuman **Merkitty**-sarakkeeseen tulee valintamerkki. Lisäksi ruudukon yläpuolella olevan **Merkitty summa** -kentän arvo suurenee tai pienenee merkittyjen rivien kokonaissumman mukaan.
6. Kun **Merkitty summa** -kentän arvo on **0** (nolla), valitse **Selvitä merkityt tapahtumat**. Merkittyjen tapahtumien tilaksi päivitetään **Selvitetty**.

    > [!IMPORTANT]
    > Kaikki aktiiviselle yritykselle selvitettäviksi merkityt tapahtumat selvitetään, vaikka ne eivät näkyisi kirjanpidon tilityssivulla suodattimen vuoksi.

## <a name="make-transactions-easier-to-find"></a>Tapahtumien löytämisen helpottaminen
**Tapahtuman selvitykset** -sivulla on toimintoja, jotka helpottavat selvitettävän tapahtuman näkemistä.

- **Merkitty**-suodattimella voi suodataa tapahtumia sen perusteella, onko tapahtumien **Merkitty**-valintaruutu valittu.
- Käytä **Tila**-suodatinta, kun haluat suodattaa tapahtumia niiden tilan mukaan.
- Lajittele summat absoluuttisen summan mukaan valitsemalla **Lajittelu absoluuttisen arvon mukaan**. Näin voit ryhmitellä debet- ja kredit-merkinnät, joissa on sama summa.

## <a name="reverse-a-settlement"></a>Käänteinen tilitys
Voit tehdä tarvittaessa käänteisen tilityksen.

1. Voit tarkastella haluamiasi tapahtumia noudattamalla [Tilitä tapahtumat](#settle-transactions) -osan vaiheita 1–3.
2. Valitse **Tila**-suodattimessa **Selvitetty**.
3. Valitse peruutettavat rivit.
4. Valitse **Peruuta merkityt tapahtumat**. Kaikkien niiden tapahtumien tilaksi päivitetään **Ei selvitetty**, joiden tilityksen tunnus on sama.

    > [!IMPORTANT]
    > Kaikki tapahtumat, joilla on sama tilitystunnus, palautetaan, vaikka niitä ei olisi merkitty. Esimerkiksi neljä riviä on merkitty ja selvitetty. Kaikilla neljällä rivillä on sama tilitystunnus. Jos merkitset jo jonkin näistä neljästä rivistä ja valitset sitten **Palauta merkityt tapahtumat**, kaikki neljä riviä palautetaan.

## <a name="unmark-for-selected-users"></a>Merkinnän poistaminen valituille käyttäjille
Valitse **Merkinnän poistaminen valituille käyttäjille** poistaaksesi kirjanpitoon täsmäytettyjen tapahtumien merkinnän kaikkien yritysten osalta käyttäjätunnuksen mukaan. Tämän avulla esimerkiksi laskentapäällikkö voi poistaa tapahtuman merkinnän lomalle lähteneen ja täsmäytyksen kesken jättäneen käyttäjän osalta tai organisaatiosta lähteneen käyttäjän osalta. Tämän toiminnon avulla toinen käyttäjä voi merkitä tapahtuman selvitettäväksi.


## <a name="unmark-all-transactions"></a>Poista kaikkien tapahtumien merkinnät
Valitse **Poista kaikkien tapahtumien merkinnät** poistaaksesi kaikkien kirjanpitoon täsmäytettyjen tapahtumien merkinnät kaikkien käyttäjien ja yritysten osalta käyttäjätunnuksen mukaan. Tämä toiminto on käytössä järjestelmänvalvojan roolille.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
