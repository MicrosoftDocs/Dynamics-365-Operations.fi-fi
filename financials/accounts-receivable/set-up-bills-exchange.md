---
title: "Tuoterakenteen määrittäminen"
description: "Tässä aiheessa kuvataan ohjeita vekseleiden määrittämisestä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Tuoterakenteen määrittäminen

Tässä aiheessa kuvataan ohjeita vekseleiden määrittämisestä.

Vekseli on Paperimuotoinen tai sähköinen kuninkaasta, joka määrittää, että toisen osapuolen, yleensä pankin, on maksettava ilmoitettua summaa yrityksen asiakkaalle. Kun vekseliä käytetään myyntitilauslaskujen tai vapaatekstilaskujen maksuna, asiakastiliä hyvitetään. Vekseli toimii hyvityksen vakuutena, kunnes asiakas maksaa vekselin pankkiin. Yleensä sinun lasku selvitetään vekselin kanssa eräpäivänä. Kun saat pankista ilmoituksen, että vekseli on maksettu, voit sulkea vekselin. Voit piirtää vekselin kautta pankin seuraavina ajankohtina:

-   Eräpäivänä. Tätä lähestymistapaa käytetään nimitystä perittäväksi.
-   Ennen eräpäivää, alennuksen päivämäärää, joka on määritetty maksuehdot, jotka on määritetty asiakkaan käyttöön yleensä. Kun tapahtuma kirjataan, alennuksen summa kirjataan kulutilille. Jäljellä oleva summa jäädään velkaa, kunnes pankki saa maksun asiakkaalta. Tätä lähestymistapaa käytetään nimitystä alennusmaksusuoritus.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Vekselien kirjausprofiilien määrittäminen
Käytä **asiakkaan kirjausprofiileille** sivulla voit määrittää kirjausprofiilit, joita voit käyttää vekselien, protestoitujen vekselien, perittäviksi ja alennusmaksusuoritus. - **Reskontratili** -kentässä, valitse reskontratili, johon vekselin summat kirjataan. Tätä tiliä veloitetaan tai hyvitetään vekselitapahtuman tyypin mukaan:
-   Vekseli tätä tiliä veloitetaan vekselin kirjaamisen yhteydessä ja hyvitetään alennusmaksusuorituksen tai perittäväksi kirjaamisen yhteydessä.
-   Kun kyseessä on protestoitu vekseli, tätä tiliä veloitetaan protestoidun vekselin kirjaamisen yhteydessä.
-   Kun kyseessä on perittäväksi palautettu vekseli, tätä tiliä veloitetaan perittäväksi palautetun vekselin kirjaamisen yhteydessä.
-   Kun kyseessä on alennusmaksusuoritus, tätä tiliä veloitetaan alennusmaksusuorituksen kirjaamisen yhteydessä.

- **Selvitystili** -kentässä, valitse käteistili, johon vekselin summat kirjataan. Tätä tiliä veloitetaan vekselin selvittämisen yhteydessä. - **Arvonlisäveron ennakkomaksut** yhteenveto kirjataan, kun vekseleitä käytetään ennakkomaksuissa arvonlisäverosummat tili-kenttään. - **Alennustili** alennusmaksusuoritus johon alennussumma kirjataan tili-kenttään. Tätä tiliä hyvitetään alennusmaksusuorituksen kirjaamisen yhteydessä.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Vekselien myyntireskontran parametrien määrittäminen
- **Myyntireskontran parametrit** sivun oletusarvo varten syötetään vekselien kirjausprofiilien **Kirjanpito- ja** välilehti. Numerosarjat on määritetty **Number sequences** välilehti.
Vekselikirjauskansioiden nimien määrittäminen
------------------------------------------

- **Nimet** vähintään viisi kirjauskansioiden nimeä vekselien Luo-sivulla. Kirjauskansioiden tyypit ovat tässä:
-   **Asiakkaan asettama vekseli** – Luo vekselin asettamisen kirjauskansion Kirjauskansionimi.
-   **Asiakkaan protestoitu vekseli** – Luo vekselin protestoinnin kirjauskansion Kirjauskansionimi.
-   **Asiakkaan tarkistaman vekselin** – Luo Kirjauskansionimen tarkastettujen vekselien kirjauskansioon.
-   **Asiakkaan pankkisiirtomääräys** – Luo Maksusuoritusten kirjauskansio-Kirjauskansionimi.
-   **Asiakkaan selvittämän vekselin** – Luo vekselin selvityskirjauskansion Kirjauskansionimi.

Vekselikirjauskansio kullekin kirjauskansion tosite sivulla, kirjoita tiedot vekseli **vekselin** välilehti. Kun vekselin kirjauskansioiden rivit on kirjattu, voit tarkastella niitä **vekselin kirjauskansioiden kyselyn** sivun ja **Vekselitilasto** sivulla.
Vekselien maksutapojen määrittäminen
-----------------------------------------------

- **Maksutavat** sivun, Määritä vähintään yksi maksutapa vekselien. Jos asioit usean pankin kanssa, Määritä maksutapa, joka vastaa, jotka kukin pankki edellyttää vekselin Maksusuorituksen muoto.
Vekselien toimitusmaksujen määrittäminen
-----------------------------------------

Toimitusmaksu liittyy prosessiin, jolla peritään maksuja asiakkailta. Jokaiseen toimitusmaksuun liittyviä useita toimitusmaksun asetukset voi saada. Miten lasketaan toimitusmaksut asetusrivejä voit rivit. Voit esimerkiksi luoda asetusrivit maksulle, maksumäärittelyille, valuutoille ja ajanjaksoille. Voit myös luoda asetusrivit prosenttiosuus tai summa, joka perustuu päivän välein. Voit esimerkiksi määrittää korko-osuus, joka perustuu aika maksu on erääntynyt. Jos pankki veloittaa maksuja eri erilaisia **kokoelman** tai **alennus**, maksu myöhästyy erillisen maksurivi määrittää.
Suoritusmaksujen määrittäminen pankkisiirtomääräystiedostoja varten
------------------------------------------------

- **Pankki** -sivulla voit määrittää suoritusmaksuja, jotka pankki veloittaa jokaisesta muodostetusta, joka luodaan kulut. Suoritusmaksut kirjataan, kun maksusuoritus on vahvistettu ja realisoituneet palkkiosummat ovat tiedossa. Suoritusmaksut eroavat toimitusmaksut, jotka kerätä asiakkailta ja liitetään kirjauskansiorivit.
Vekselien asettelujen määrittäminen
---------------------------------------------

- **Pankkitilit** -sivulla **määrittäminen**, ja määritä asiakirja-asettelu, jota tarvitaan, jotta jokaiselle pankkitilille, että olet luonut tulostettavan vekselien asiakirjoja varten.
Asiakkaiden vekselimääritysten tekeminen
--------------------------------------

- **Asiakkaiden** -jokaiselle asiakkaalle, joka on sopinut vekselin avulla voit määrittää oletusarvoinen maksutapa vekselien sivulla **maksun oletukset** välilehti.




