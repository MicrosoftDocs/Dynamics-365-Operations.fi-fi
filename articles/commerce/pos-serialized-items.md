---
title: Sarjoitettujen nimikkeiden käyttäminen myyntipisteessä
description: Tässä ohjeaiheessa selitetään, kuinka sarjoitettuja nimikkeitä hallitaan myyntipisteen (POS) sovelluksessa.
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: b63ffc7921e37b0591c66a76d57214a5efe5a1ef
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761342"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Sarjoitettujen nimikkeiden käyttäminen myyntipisteessä

[!include [banner](includes/banner.md)]

Monet jälleenmyyjät myyvät tuotteita, jotka edellyttävät sarjavalvontaa. Näitä tuotteita kutsutaan *sarjoitetuiksi nimikkeiksi*. Jotkin vähittäismyyjät haluavat ehkä ylläpitää sarjanumeroita myymälässä tai varastossa seurantaa varten. Muut jälleenmyyjät saattavat haluta kaapata sarjanumeroita myyntiprosessin aikana huoltoa ja takuuta varten. Tässä ohjeaiheessa selitetään, kuinka voit hallita sarjoitettuja nimikkeitä Microsoft Dynamics 365 Commerce -myyntipisteen (POS) sovelluksessa.

## <a name="serial-number-configurations"></a>Sarjanumerokonfiguraatiot

Nimikettä pidetään sarjoitettuna nimikkeenä, jos sille on määritetty sarjanumeroiden sallimiseksi määritetty seurantadimensioryhmä. Valitse Commerce Headquarters -sovelluksen **Seurantadimensioryhmät**-sivulla **Aktiivinen**-vaihtoehto, jos haluat ottaa käyttöön sarjanumerot varastoprosessissa. Vaihtoehtoisesti voit valita **Aktiivinen myyntiprosessissa** -vaihtoehdon, jos haluat ottaa käyttöön sarjanumerot myyntiprosessissa.

Ota **Tyhjä kuitti sallittu** -vaihtoehto käyttöön **Seurantadimensiot**-pikavälilehdessä. Tällöin sarjanumero on valinnainen syöte sarjoitetun nimikkeen varaston vastaanottoprosessin aikana. Jos tämä parametri poistetaan käytöstä, sarjanumerolle on annettava syöte. Vastaavasti **Tyhjä varasto-otto sallitaan** -parametri ohjaa sarjanumeroiden määrittämistä pakolliseksi varaston lähetysprosessin aikana.

> [!NOTE]
> Jos haluat käyttää **Saapuva varasto**- ja **Lähtevä varasto** -myyntipistetoimintoja sarjanumeroiden rekisteröimisessä tai vahvistamisessa sarjoitetulle nimikkeelle, määritä kyseinen nimike seurantadimensioryhmää varten. Ryhmä on määritettävä sallimaan sarjanumerot **Aktiivinen**-vaihtoehdolle, ei **Aktiivinen myyntiprosessissa** -vaihtoehdolle.

## <a name="serial-number-management-page"></a>Sarjanumeroiden hallinta -sivu

Jos valittu, vastaanotettu tai lähetetty nimike on sarjoitettu nimike **Saapuva varasto**- ja **Lähtevä varasto** -myyntipistetoiminnoissa, **Tiedot**-ruutu sisältää **Hallinnoi sarjanumeroa** -vaihtoehdon, joka sisältää linkin **Sarjanumeroiden hallinta** -sivulle. Sivulla voit rekisteröidä nimikkeen sarjanumerot tai vahvistaa ne. Vaihtoehtoisesti voit avata **Sarjanumeroiden hallinta** -sivun joko valitsemalla tilaustietojen näkymän sovelluspalkin **Sarjanumero**-toiminnon tai valitsemalla **Hallitse sarjanumeroa** -vaihtoehdon valintaikkunassa, joka pyytää käyttäjää vastaamaan vastaanotto- tai lähetysprosessin aikana. 

**Sarjanumeroiden hallinta** -sivulla luetellaan kaikki avoimet sarjanumerorivit, jotka odottavat rekisteröintiä tai vahvistusta. Tällä sivulla voi olla seuraavat kaksi välilehteä: yksi nykyiselle nimikkeelle ja yksi tilauksen sarjoitettuja nimikkeitä varten.

**Sarjanumeroiden hallinta** -sivun **tila**-kentässä on tietoja nykyisestä vaiheesta, jossa kukin sarjanumero on:

- **Ei rekisteröity** – Sarjanumeroa ei ole annettu tai esirekisteröityä sarjanumeroa ei ole vielä vahvistettu (vastaanottoprosessissa).
- **Rekisteröityminen** – Sarjanumero on rekisteröity ja tallennettu paikallisesti myymälän kanavatietokantaan tai esirekisteröity sarjanumero on vahvistettu. Vain sarjanumerot, joiden tila on **Rekisteröityminen**, lähetetään Commerce Headquarters -sovellukseen, kun vastaanotto tai täytäntöönpano on valmis.

## <a name="receive-serialized-items"></a>Sarjoitettujen nimikkeiden vastaanottaminen

**Saapuva varasto** -myyntipistetoiminto antaa käyttäjien suorittaa seuraavat sarjoitetuille kohteille tehtävät toimet:

- Rekisteröi sarjanumerot sarjasarjoitettuja nimikkeitä vastaan, kun nimikkeet vastaanotetaan myymälässä ostotilauksen kautta.
- Vahvista ennalta rekisteröidyt sarjanumerot sarjasarjoitettuja nimikkeitä vastaan, kun nimikkeet vastaanotetaan myymälässä ostotilauksen kautta tai siirrä tilaus.

### <a name="register-serial-numbers-against-serialized-items"></a>Sarjanumeroiden rekisteröiminen sarjoitettuja nimikkeitä vasten

Jos kyseessä on ostotilaus, käyttäjälle näytetään valintaikkuna, joka sisältää **Hallinnoi sarjanumeroa** -vaihtoehdon sarjoitetun nimikkeen vastaanottoprosessin aikana. Voit valita tämän vaihtoehdon, kun haluat avata **sarjanumeroiden hallinta** -sivun ja alkaa rekisteröidä sarjanumeroita. Voit myös ohittaa tämän vaiheen vastaanottoprosessin aikana ja antaa syötteen myöhemmin ennen vastaanoton kirjaamista.

Oletusarvon mukaan näytetään nykyisen nimikkeen välilehti. Kaikilla sarjanumeroriveillä on tyhjä sarjanumeroarvo ja tila, jota **ei ole rekisteröity**. Voit skannata sarjanumeroviivakoodeja tai voit määrittää **sarjanumerot** jatkuvasti valitsemalla sarjanumeron sovelluspalkista. Syöttämäsi sarjanumerot näkyvät luettelossa, ja niiden tilaksi tulee **Rekisteröinti**. Luettelossa rekisteröitävien sarjanumeroiden enimmäismäärä on sama kuin vastaanottava määrä. Jos teet virheen, voit tehdä muutoksia syöttämääsi sarjanumeroon valitsemalla **Muokkaa** tai **Tyhjennä** **Tieto**-ruudusta.

Sarjanumerot voi rekisteröidä myös **sarjanumeroiden hallinta** -sivun **kaikki sarjoitetut nimikkeet** -välilehdessä. Valitse luettelosta nimike, jota vastaan haluat rekisteröidä sarjanumerot.

### <a name="validate-serial-numbers-on-serialized-items"></a>Sarjoitetussa nimikkeissä olevien sarjanumeroiden vahvistaminen

Siirtotilauksen lähtevän puolen on suoritettava sarjanumerot sarjoitetussa nimikkeissä lähetysprosessin aikana. Jos kyseessä on ostotilaus, toimittaja voi antaa sarjanumerotiedot ennakkolähetysilmoituksen (ASN) kautta, ja voit määrittää toimitettavien nimikkeiden numerot. Molemmissa tapauksissa sarjanumerot ovat tiedossa ennen vastaanottoa. Siksi saapuvien puolella, sinun täytyy vain vahvistaa, että olet saanut mitä oli tarkoitus saada.

Voit vahvistaa sarjanumerot avaamalla **Sarjanumeroiden hallinta** -sivun joko vastaanottavan prosessin aikana tai milloin tahansa ennen vastaanoton kirjaamista. Kaikille sarjanumeroille määritetään automaattisesti alkutila, jota **ei ole rekisteröity** tällä sivulla, kullekin sarjoitetun nimikkeen sarjanumerolle. Voit tarkistaa sarjanumerot skannaamalla tai kirjoittamalla ne. Kun sarjanumero on määritetty, sovellus tarkistaa, vastaavatko ne ennalta rekisteröityjä sarjanumeroita. Jos ne täsmäävät, niiden tilaksi muutetaan **Rekisteröityminen**. Muussa tapauksessa näyttöön avautuu virhesanoma. Vaihtoehtoisesti voit valita sarjanumeron suoraan ja valita sitten **Vahvista sarjanumero** -vaihtoehdon **Tiedot**-ruudussa. Näin voit merkitä sarjanumeron nopeasti vahvistetuksi. Luettelossa vahvistettavien sarjanumeroiden enimmäismäärä on sama kuin vastaanottava määrä.

Sarjanumerot voi vahvistaa myös **sarjanumeroiden hallinta** -sivun **kaikki sarjoitetut nimikkeet** -välilehdessä. Valitse luettelosta nimike, jota vastaan haluat vahvistaa sarjanumerot.

## <a name="ship-serialized-items"></a>Sarjoitettujen nimikkeiden lähettäminen

**Lähtevä varasto** -myyntipistetoiminnon avulla käyttäjä voi rekisteröidä sarjanumeroita sarjoitetuille nimikkeille, kun niitä lähetetään nykyisestä myymälästä siirtotilauksen kautta.

### <a name="register-serial-numbers-against-serialized-items"></a>Sarjanumeroiden rekisteröiminen sarjoitettuja nimikkeitä vasten

Jos kyseessä on siirtotilaus, käyttäjälle näytetään valintaikkuna, joka sisältää **Hallinnoi sarjanumeroa** -vaihtoehdon sarjoitetun nimikkeen lähetysprosessin aikana. Voit valita vaihtoehdon, kun haluat avata **Sarjanumeroiden hallinta** -sivun ja alkaa rekisteröidä sarjanumeroita. Voit myös ohittaa tämän vaiheen lähetysprosessin aikana ja antaa syötteen myöhemmin ennen lähetyksen kirjaamista.

Oletusarvon mukaan näytetään nykyisen nimikkeen välilehti. Kaikilla sarjanumeroriveillä on tyhjä sarjanumeroarvo ja tila, jota **ei ole rekisteröity**. Voit skannata sarjanumeroviivakoodeja tai voit määrittää **sarjanumerot** jatkuvasti valitsemalla sarjanumeron sovelluspalkista. Syöttämäsi sarjanumerot näkyvät luettelossa, ja niiden tilaksi tulee **Rekisteröinti**. Luettelossa rekisteröitävien sarjanumeroiden enimmäismäärä on sama kuin lähetysmäärä. Jos teet virheen, voit tehdä muutoksia syöttämääsi sarjanumeroon valitsemalla **Muokkaa** tai **Tyhjennä** **Tieto**-ruudusta.

Sarjanumerot voi rekisteröidä myös **Sarjanumeroiden hallinta** -sivun **Kaikki sarjoitetut nimikkeet** -välilehdessä. Valitse luettelosta nimike, jota vastaan haluat rekisteröidä sarjanumerot.

Vaihtoehtoisesti voit ottaa sarjanumeroiden käytettävyyden vahvistuksen käyttöön sarjanumeroiden rekisteröinnissä lähtevälle siirtotilaukselle. Kun tämä tarkistus on käytössä ja yrität lähettää sarjanumeron, joka ei ole käytettävissä lähettävän myymälän varastossa, näyttöön tulee virhesanoma. Anna tämän jälkeen toinen numero.

Jotta tämä vahvistus voidaan ottaa käyttöön edellytyksenä, seuraavat työt on aikataulutettava suoritettavaksi toistuvasti:

- **Vähittäismyynti ja kauppa** > **Vähittäismyynnin ja kaupan IT** > **Tuotteet ja varasto** > **Tuotteiden saatavuus ja seurantadimensiot**
- **Vähittäismyynti ja kauppa** > **Jakeluaikataulut** > **1130** (**Tuotteen saatavuus**)

## <a name="additional-resources"></a>Lisäresurssit

[Myyntipisteen saapuva varastotoiminto](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Myyntipisteen lähtevä varastotoiminto](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)
