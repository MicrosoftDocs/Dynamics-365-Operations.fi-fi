---
title: Myyntipisteen Peruuta tilaus -toiminto
description: Tässä ohjeaiheessa käsitellään myyntipisteen parannetulla tilausten peruutussivuilla olevia ominaisuuksia.
author: hhainesms
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2f7ad4f53917bb607afe84a2c457518c3f8f7a08
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799103"
---
# <a name="recall-order-operation-in-pos"></a>Myyntipisteen Peruuta tilaus -toiminto

[!include [banner](includes/banner.md)]

Commercen myyntipisteen **Peruuta tilaus** -toiminnossa on päivitetyt tilauksen haku- ja suodatusominaisuudet ja tilauskohtaiset tiedot. Tämä ominaisuus on käytettävissä Commercen versiossa 10.0.15 ja sitä uudemmissa versioissa.

Ota tämä toiminto käyttöön ottamalla **Parannettu tilauksen peruutustoiminto myyntipisteessä** -ominaisuus käyttöön Commercen pääkonttorin **Ominaisuuksien hallinta** -työtilassa. Kun ominaisuus on otettu käyttöön, harkitse myyntipisteen [näytön asettelujen](pos-screen-layouts.md) päivittämistä, jotta voit käyttää muutettuja ominaisuuksia.

**Peruuta tilaus** -toimintopainikkeen määritys antaa organisaatioille mahdollisuuden ottaa toiminnon käyttöön siten, että näyttö määritetty valmiiksi.

![Painikeruudukon määritykset](media/recallorderbuttongrid.png)

Näyttöasetukset:
- **Ei mitään** – Tällä asetuksella toiminto otetaan käyttöön ilman tiettyä näyttöä. Kun käyttäjä avaa toiminnon tällä määrityksellä, häntä pyydetään hakemaan tilaukset tai tekemään valinnan esimääritetystä tilaussuodattimesta.
- **Täytettävät tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka käyttäjän nykyisen myymälän on täytettävä. Nämä tilaukset määritetään myymälästä noudatettavaksi tai lähetettäväksi eikä näiden tilausten rivejä ole vielä poimittu tai pakattu.
- **Poimittavat tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka on määritetty myymälästä poimittavaksi käyttäjän nykyisestä myymälästä.
- **Lähetettävät tilaukset** – Kun käyttäjä käynnistää toiminnon, automaattisesti suoritettava kysely tekee haun ja luettelon tilauksista, jotka on määritetty lähetettäväksi käyttäjän nykyisestä myymälästä.

Jos **Peruuta tilaus** -toiminto käynnistetään myyntipisteessä ja jos näytön määrityksenä on **Ei mitään**, käyttäjä voi hakea ja noutaa tilauksia jollakin seuraavista tavoista.
- Skannaa tilauksen viivakoodit. Tällä tavoin haetaan vastaavuuksien tilauksen numeron, kanavaviitteen ja vastaanottotunnuksen kentät.
- Valitse sovelluspalkissa **Hae tilaukset**- tai **Hae ja suodata** -kuvake. Tällä tavoin voit käyttää suodatusmekanismia suodatusehtoja vastaavien tilausten paikantamiseen.
- Valitse jokin esimääritetty suodatin avattavassa **Näytä tilaukset** -valikossa (täytettävät tilaukset, poimittavat tilaukset tai lähetettävät tilaukset).

![RecallOrderMainMenu](media/recallordermain.png)

Kun ehtojen mukainen haku on tehty, sovellus näyttää vastaavien myyntitilausten luettelon. Haku- tai suodatusasetuksia käytettäessä on tärkeää muistaa, että haettujen tilausten ei tarvitse olla käyttäjän nykyiseen myymälään linkitettyjä tilauksia. Tämä hakuprosessi hakee ja näyttää kaikki hakuehtoja vastaavat asiakastilaukset, vaikka tilaus olisi luotu tai määritetty toisen myymälän/kanavan tai varaston sijainnin avulla.

![RecallOrderDetail](media/orderrecalldetail.png)

Käyttäjä voi valita luettelossa tilauksen ja katsoa lisätietoja. Näytön oikealla puolella on tietopaneeli, jossa on tietoja valitusta tilauksesta, kuten tilausrivin tiedot, toimituksen tiedot ja täyttämistiedot.

Valitse toiminto sovelluspalkissa. Tilauksen tilan mukaan määräytyy, voidaanko tietyt toiminnot ottaa käyttää.

- **Palauta** – Aloittaa prosessin, joka luo palautuksen valitun asiakastilauksen laskutetuille tuotteille.

- **Peruuta** – myöntää valitun myyntitilauksen täyden peruutuksen. Tämä vaihtoehto ei ole käytettävissä puhelinkeskuksen kanavan kautta käynnistettaville tilauksille, eikä sitä voi käyttää tilauksen osittaista peruuttamista varten.

- **Täytä** – Siirtää käyttäjän tilauksen täyttämissivulle, joka esisuodatetaan valittuun tilaukseen. Näkyvissä on vain ne valitun tilauksen tilausrivit, jotka ovat avoimia täytettäväksi käyttäjän myymälässä.

- **Muokkaa** – käyttäjät saavat tehdä muutoksia valittuun asiakastilaukseen. Tilauksia voi muokata vain [tietyissä tilanteissa](customer-orders-overview.md#edit-an-existing-customer-order).

- **Nouto** – Tämä vaihtoehto on käytettävissä, jos tilauksessa on vähintään yksi rivi, joka on määritetty noudettavaksi käyttäjän nykyisessä myymälässä. Tämä toiminto käynnistää keräilytyönkulun, jossa käyttäjä voi valita kerättävät tuotteet ja joka luo myynnin keräilytapahtuman.

## <a name="add-notifications-to-the-recall-order-operation"></a>Ilmoitusten lisääminen palautustilauksen toimintoon

Versiossa 10.0.18 ja sitä myöhemmässä versiossa voit tarvittaessa määrittää **Tilauksen palautus** -toiminnolle myyntipisteilmoitukset ja live- ruutuhälytykset. Lisätietoja on kohdassa [Tilausilmoitusten näyttäminen myyntipisteessä](notifications-pos.md).  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
