---
title: Sarjoitettujen nimikkeiden käyttäminen myyntipisteessä
description: Tässä ohjeaiheessa selitetään, kuinka sarjoitettuja nimikkeitä hallitaan myyntipisteen (POS) sovelluksessa.
author: boycezhu
manager: annbe
ms.date: 05/27/2020
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
ms.openlocfilehash: eedb64ae04345cb94bdd8cc68de833cfcfd40119
ms.sourcegitcommit: 39981582778b0a62567324452485a6721ca18284
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2020
ms.locfileid: "3407495"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Sarjoitettujen nimikkeiden käyttäminen myyntipisteessä

[!include [banner](includes/banner.md)]

Monet jälleenmyyjät myyvät tuotteita, jotka edellyttävät sarjavalvontaa. Näitä nimikkeitä kutsutaan *sarjoitetuiksi nimikkeiksi*. Jotkin vähittäismyyjät haluavat ehkä ylläpitää sarjanumeroita seurantaa varten. Muut jälleenmyyjät saattavat haluta kaapata sarjanumeroita myyntiprosessin aikana huoltoa ja takuuta varten. Tässä ohjeaiheessa selitetään, kuinka voit hallita sarjoitettuja nimikkeitä Microsoft Dynamics 365 Commerce -myyntipisteen (POS) sovelluksessa.

## <a name="serial-number-configurations"></a>Sarjanumerokonfiguraatiot

Nimikettä pidetään sarjoitettuna nimikkeenä, jos sille on määritetty sarjanumeroiden sallimiseksi määritetty seurantadimensioryhmä. Valitse Commercen pääkonttorin **Seurantadimensioryhmät**-sivulla **Aktiivinen**-valintaruutu ottaaksesi käyttöön varastoprosessin sarjanumerot. Voit ottaa myyntiprosessin sarjanumerot käyttöön valitsemalla **myyntiprosessi käytössä** -vaihto ehdon.

Jos **tyhjä kuitti sallittu** -vaihtoehto on käytössä **seurantadimensiot**-pikavälilehdessä, sarjanumero on valinnainen syöte varaston vastaanottoprosessin aikana. Jos vaihtoehto on poistettu käytöstä, sarjanumero on pakollinen.

Jos **sarjanumeroiden hallinta** -vaihtoehto on käytössä **sarjanumerot**-pikavälilehdessä, sarjanumeron on oltava yksilöivä yksikköä kohden. Toisin sanoen sarjanumeroiden kaksoiskappaleita ei sallita.

## <a name="serialized-items-in-the-receiving-process"></a>Sarjoitetut nimikkeet vastaanottavassa prosessissa

Myyntipistesovelluksen **saapuva varasto** -toiminto antaa käyttäjien suorittaa seuraavat sarjoitetuille kohteille tehtävät toimet:

- Rekisteröi sarjanumerot sarjasarjoitettuja nimikkeitä vastaan, kun nimikkeet vastaanotetaan myymälässä ostotilauksen kautta.
- Vahvista ennalta rekisteröidyt sarjanumerot sarjasarjoitettuja nimikkeitä vastaan, kun nimikkeet vastaanotetaan myymälässä ostotilauksen kautta tai siirrä tilaus.

> [!NOTE]
> Jotta voit käyttää **saapuvien nimikkeiden varasto** -toimintoa sarjoitetun nimikkeen rekisteröimiseen tai vahvistamiseen, nimikkeelle on määritettävä seurantadimensioryhmä, joka on määritetty sallimaan sarjanumerot **aktiivisessa** vaihtoehdossa, ei **aktiivinen myyntiprosessi** -vaihtoehdossa.

Kun haluat aloittaa vastaanottoprosessin, voit aloittaa **saapuvan varaston** työvaiheen **vastaanotto nyt** -näkymässä skannaamalla nimikkeen viivakoodin tai syöttämällä nimiketunnuksen. Vaihtoehtoisesti voit aloittaa **koko tilausluettelo** -näkymästä valitsemalla nimikkeen manuaalisesti.

Jos valittu tai vastaanotettu nimike on sarjoitettu nimike, nimikkeen **tieto**-ruudussa on **Hallitse sarjanumeroa** -linkki, joka avaa **sarjanumeroiden hallinta** -sivun. Vaihtoehtoisesti voit avata **sarjanumeroiden hallinta** -sivun joko valitsemalla tilaustiedot-näkymän sovelluspalkissa **sarjanumero** tai valitsemalla **Hallitse sarjanumeroa** -valintaikkunassa, joka kysyy sinulta vastaanottavan prosessin aikana. **Sarjanumeroiden hallinta** -sivulla luetellaan kaikki avoimet sarjanumerorivit, jotka odottavat rekisteröintiä tai vahvistusta. Tällä sivulla voi olla kaksi välilehteä: yksi nykyiselle nimikkeelle ja yksi tilauksen sarjoitettuja nimikkeitä varten.

**Sarjanumeroiden hallinta** -sivun **tila**-kentässä on tietoja nykyisestä vaiheesta, jossa kukin sarjanumero on:

- **Ei rekisteröity** – Sarjanumeroa ei ole annettu tai esirekisteröityä sarjanumeroa ei ole vielä vahvistettu.
- **Rekisteröityminen** – Sarjanumero on rekisteröity ja tallennettu paikallisesti myymälän kanavatietokantaan tai esirekisteröity sarjanumero on vahvistettu. Vain sarjanumerot, joiden tila on **Rekisteröityminen**, lähetetään Commercen pääkonttori -sovellukseen, kun vastaanotto on valmis.

### <a name="register-serial-numbers-against-serialized-items"></a>Sarjanumeroiden rekisteröiminen sarjoitettuja nimikkeitä vasten

Jos kyseessä on ostotilaus, valintaikkuna, jossa kysytään sarjoitetun nimikkeen vastaanottavan prosessin aikana, tarjoaa **sarjanumeron hallinta** -vaihtoehdon. Voit valita tämän vaihtoehdon, kun haluat avata **sarjanumeroiden hallinta** -sivun ja alkaa rekisteröidä sarjanumeroita. Voit myös ohittaa tämän vaiheen vastaanottoprosessin aikana ja antaa syötteen myöhemmin ennen vastaanoton kirjaamista.

Oletusarvon mukaan näytetään nykyisen nimikkeen välilehti. Kaikilla sarjanumeroriveillä on tyhjä sarjanumeroarvo ja tila, jota **ei ole rekisteröity**. Voit skannata sarjanumeroviivakoodeja tai voit määrittää **sarjanumerot** jatkuvasti valintaikkunassa valitsemalla sarjanumeron sovelluspalkista. Syöttämäsi sarjanumerot näkyvät luettelossa, ja sarjanumerorivien tilaksi tulee **rekisteröinti**. Luettelossa rekisteröitävien sarjanumeroiden enimmäismäärä on sama kuin vastaanottava määrä. Jos teet virheen, voit tehdä muutoksia syöttämääsi sarjanumeroon valitsemalla **Muokkaa** tai **Tyhjennä** **Tieto**-ruudusta.

Sarjanumerot voi rekisteröidä myös **sarjanumeroiden hallinta** -sivun **kaikki sarjoitetut nimikkeet** -välilehdessä. Valitse luettelosta nimike, jota vastaan haluat rekisteröidä sarjanumerot.

Tämän sivun sarjanumeron rekisteröinnissä tapahtuu kaksoisarvojen oikeellisuustarkistus. Jos yrität kirjoittaa monistetun sarjanumeron nimikkeeseen, jolle sarjanumero-ohjaus on otettu käyttöön, näyttöön tulee virhesanoma ja sen on annettava eri numero.

### <a name="validate-serial-numbers-on-serialized-items"></a>Sarjoitetussa nimikkeissä olevien sarjanumeroiden vahvistaminen

Siirtotilauksen lähtevän puolen on suoritettava sarjanumerot sarjoitetussa nimikkeissä lähetysprosessin aikana. Jos kyseessä on ostotilaus, toimittaja voi antaa sarjanumerotiedot ennakkolähetysilmoituksen (ASN) kautta, ja voit määrittää toimitettavien nimikkeiden numerot. Molemmissa tapauksissa sarjanumerot ovat tiedossa ennen vastaanottoa. Siksi saapuvien puolella, sinun täytyy vain vahvistaa, että olet saanut mitä oli tarkoitus saada.

Voit vahvistaa sarjanumerot avaamalla **Sarjanumeroiden hallinta** -sivun joko vastaanottavan prosessin aikana tai milloin tahansa ennen vastaanoton kirjaamista. Kaikille sarjanumeroille määritetään automaattisesti alkutila, jota **ei ole rekisteröity** tällä sivulla, kullekin sarjoitetun nimikkeen sarjanumerolle. Voit tarkistaa sarjanumerot skannaamalla tai kirjoittamalla ne. Kun sarjanumero on määritetty, sovellus tarkistaa, vastaavatko ne ennalta rekisteröityjä sarjanumeroita. Jos ne täsmäävät, niiden tilaksi muutetaan **Rekisteröityminen**. Muussa tapauksessa näyttöön avautuu virhesanoma. Luettelossa vahvistettavien sarjanumeroiden enimmäismäärä on sama kuin vastaanottava määrä.

Sarjanumerot voi vahvistaa myös **sarjanumeroiden hallinta** -sivun **kaikki sarjoitetut nimikkeet** -välilehdessä. Valitse luettelosta nimike, jota vastaan haluat vahvistaa sarjanumerot.

## <a name="additional-resources"></a>Lisäresurssit

[Myyntipisteen saapuva varastotoiminto](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
