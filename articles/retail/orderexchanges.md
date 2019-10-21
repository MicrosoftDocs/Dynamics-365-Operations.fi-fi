---
title: Palautustilauksen vaihdon määritys ja käsittely
description: Tässä ohjeaiheessa kerrotaan, miten vaihto palautuksen yhteydessä konfiguroidaan ohjelmassa Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3ce327a918159771df0acab276b1169d2ad77825
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025376"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Palautustilaukseen liittyvän vaihdon määritys ja käsittely

[!include [banner](includes/banner.md)]

Dynamics 365 Retailin aiemmissa versioissa asiakastilausten palautukset käsiteltiin käyttämällä palautustilauksen asiakirjaa Retail Headquarters -ohjelmassa. Palautustilauksen asiakirjaa voidaan kuitenkin käyttää vain palautettavien tuotteiden käsittelyyn. Palautetut tuotteet on merkitty palautustilauksen riveille negatiivisena määränä. Sen sijaan myynti on merkitty on positiivisena määränä. Palautustilauksen asiakirja ei kuitenkaan tue positiivisia määriä. Tämän rajoituksen vuoksi Retailin aiemmat versiot eivät tukeneet tilanteita, joissa tuotteita vaihdettiin käyttämällä palautustilauksen asiakirjaa.

Toiminto on nyt lisätty tukemaan tilanteita, joissa palautustilauksiin liittyy tuotteiden vaihto. Nyt Retail käyttää palautustilauksen asiakirjan sijaan myyntitilauksen asiakirjaa käsittelemään tämäntyyppisiä tapahtumia.

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a>Retailin määrittäminen tukemaan tuotteiden vaihtoa palautustilauksissa

Voit määrittää järjestelmän tukemaan vaihtoa palautustilauksissa seuraavasti.

1. Valitse **Vähittäismyynti \> Pääkonttorin asetukset \> Parametrit \> Vähittäismyynnin parametrit**. Määritä **Asiakastilaukset**-pikavälilehdessä **Käsittele palautustilauksia myyntitilauksina** -asetukseksi **Kyllä**.
2. Suorita **Yleinen määritysjakelun aikataulu** -työ (**1110**).

## <a name="make-an-exchange"></a>Vaihdon tekeminen

Kun järjestelmä on määritetty edellä kuvatulla tavalla, myyntipisteen käyttäjä edelleen valitsee palautuksen käsittelyyn myyntitilauksen tai myyntilaskun, kuten aiemmissa Retail-versioissakin. Kun palautetut nimikkeet on lisätty ostoskoriin, käyttäjä voi kuitenkin lisätä myös uusia myyntirivejä ostoskoriin.

Näille uusille myyntiriveille käyttäjän on määritettävä kaikki määritteet, jotka tarvitaan asiakastilauksen rivin käsittelyyn. Näihin määritteisiin kuuluvat toimitustapa sekä täyttämissijainti. Tapahtuman maksettava summa on palautustilauksen rivien ja myyntitilausrivien nettosumma. Kun tapahtuman maksu maksetaan, palautustilaus kirjataan myyntitilausasiakirjana Retail Headquarters -sovelluksessa ja järjestelmä laskuttaa palautusrivit välittömästi.

Ostoskoriin on lisätty kolme uutta summakenttää, jotta ostoskorin eri summat erottuisivat selkeästi. Näytön suunnitteluohjelmassa voit lisätä nämä uudet kentät myyntipisteen käyttöliittymään.

- **Käytetty talletus** – Tallennussumma, jota käytetään tapahtumassa, kun käyttäjä suorittaa asiakastilauksen noudon. Jos talletuksen ohitus ei ole käytössä ja määritetään 10 prosentin talletus, tähän kenttään tulee 90 prosenttia asiakastilauksen kokonaissummasta.
- **Suoritussumma** – Niiden rivien kokonaissumma, joiden toimitustavaksi oli määritetty **Suoritus** asiakastilausta luotaessa tai muokattaessa tai asiakastilaukseen liittyvän vaihdon yhteydessä. Tämän kentän summa sisältää verot ja maksut.
- **Palautussumma** – Niiden rivien kokonaissumma, joilla on negatiiviset määrät asiakastilauksen vaihdon aikana. Tämän kentän summa sisältää verot ja maksut.
