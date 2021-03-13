---
title: Myyntipisteen Peruuta tilaus -toiminto
description: Tässä ohjeaiheessa käsitellään myyntipisteen parannetulla tilausten peruutussivuilla olevia ominaisuuksia.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010071"
---
# <a name="recall-order-operation-in-pos"></a>Myyntipisteen Peruuta tilaus -toiminto

[!include [banner](includes/banner.md)]

Commercen myyntipisteen **Peruuta tilaus** -toiminnossa on päivitetyt tilauksen haku- ja suodatusominaisuudet ja tilauskohtaiset tiedot. Tämä ominaisuus on käytettävissä Commercen versiossa 10.0.15 ja sitä uudemmissa versioissa.

Ota tämä toiminto käyttöön ottamalla **Parannettu tilauksen peruutustoiminto myyntipisteessä** -ominaisuus käyttöön Commercen pääkonttorin **Ominaisuuksien hallinta** -työtilassa. Kun ominaisuus on otettu käyttöön, harkitse myyntipisteen [näytön asettelujen](pos-screen-layouts.md) päivittämistä, jotta voit käyttää muutettuja ominaisuuksia.

**Peruuta tilaus** -toimintopainikkeen määritys antaa organisaatioille mahdollisuuden ottaa toiminnon käyttöön siten, että näyttö määritetty valmiiksi.

![Painikeruudukon määritykset](media/recallorderbuttongrid.png)

Näyttöasetukset:
- **Ei mitään** – Tällä asetuksella toiminto otetaan käyttöön ilman tiettyä näyttöä. Kun käyttäjä avaa toiminnon tällä määrityksellä, häntä pyydetään hakemaan tilaukset tai tekemään valinnan esimääritetystä tilaussuodattimesta.
- **Täytettävät tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka myymälän on täytettävä. Nämä tilaukset määritetään myymälästä noudatettavaksi tai lähetettäväksi eikä näiden tilausten rivejä ole vielä poimittu tai pakattu.
- **Poimittavat tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka on määritetty myymälästä poimittavaksi käyttäjän nykyisestä myymälästä.
- **Lähetettävät tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka on määritetty lähetettäväksi käyttäjän nykyisestä myymälästä.

Jos **Peruuta tilaus** -toiminto käynnistetään myyntipisteessä ja jos näytön määrityksenä on **Ei mitään**, käyttäjä voi hakea ja noutaa tilauksia jollakin seuraavista tavoista.
- Skannaa tilauksen viivakoodit. Tällä tavoin haetaan vastaavuuksien tilauksen numeron, kanavaviitteen ja vastaanottotunnuksen kentät.
- Valitse sovelluspalkissa **Hae tilaukset**- tai **Hae ja suodata** -kuvake. Tällä tavoin voit käyttää suodatusmekanismia suodatusehtoja vastaavien tilausten paikantamiseen.
- Valitse jokin esimääritetty suodatin avattavassa **Näytä tilaukset** -valikossa (täytettävät tilaukset, poimittavat tilaukset tai lähetettävät tilaukset).

![RecallOrderMainMenu](media/recallordermain.png)

Kun ehtojen mukainen haku on tehty, sovellus näyttää vastaavien myyntitilausten luettelon.

![RecallOrderDetail](media/orderrecalldetail.png)

Käyttäjä voi valita luettelossa tilauksen ja katsoa lisätietoja. Näytön oikealla puolella on tietopaneeli, jossa on tietoja valitusta tilauksesta, kuten tilausrivin tiedot, toimituksen tiedot ja täyttämistiedot.

Valitse toiminto sovelluspalkissa. Tilauksen tilan mukaan määräytyy, voidaanko tietyt toiminnot ottaa käyttää.

- **Palautus** – palauttaa vähintään yhden valittuun myyntilaskuun liittyvän laskun.

- **Peruuta** – myöntää valitun myyntitilauksen täyden peruutuksen.

- **Täytä** – Siirtää käyttäjän tilauksen täyttämissivulle, joka esisuodatetaan valittuun tilaukseen. Näkyvissä on vain ne valitun tilauksen tilausrivit, jotka ovat avoimia täytettäväksi käyttäjän myymälässä.

- **Muokkaa** – käyttäjät saavat tehdä muutoksia valittuun asiakastilaukseen.

- **Keräile** – käynnistää keräilytyönkulun, jossa käyttäjä voi valita kerättävät tuotteet ja joka luo myynnin keräilytapahtuman.
