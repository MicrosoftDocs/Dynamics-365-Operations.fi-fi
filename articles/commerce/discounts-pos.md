---
title: Alennusten näyttäminen myyntipisteessä
description: Tässä ohjeaiheessa kerrotaan, miten myyjät saavat Microsoft Dynamics 365 Commercesta tietoja kampanjoista ja niiden käyttämisestä ristiinmyynti- ja lisämahdollisuuksista.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 89f7b79733f01c089a16c507b127b23ada5df1a6
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265577"
---
# <a name="show-discounts-in-pos"></a>Alennusten näyttäminen myyntipisteessä

[!include [banner](includes/banner.md)]

Kampanjat ovat tärkeä osa ostopäätöksiä tekevien asiakkaiden motivoinnissa. Esimerkiksi lomat voivat tuottaa vähittäismyyjille suurimman myyntimäärän, koska vähittäismyyntimarkkinat ovat täynnä houkuttelevia kampanjoita ja alennuksia. Jos myyjät tietävät käytettävissä olevista kampanjoista ja ymmärtävät niitä, he voivat helposti hyödyntää niitä ristiin- ja lisämyynnissä. Tässä ohjeaiheessa kerrotaan, miten myyjät saavat Microsoft Dynamics 365 Commercesta tietoja kampanjoista ja niiden käyttämisestä ristiinmyynti- ja lisämahdollisuuksista.

## <a name="learn-about-store-discounts"></a>Lisätietoja myymälän alennuksista

Commerce sisältää toiminnon, jonka nimi on Näytä kaikki alennukset. Tämä toiminto näyttää kaikki myymälässä parhaillaan suoritettavat alennukset. Näytä kaikki alennukset -toiminto voidaan yhdistää painikkeeseen myyntipisteessä. Tämä painike voidaan lisätä **aloitussivulle** tai **Tapahtuma**-sivulle. Seuraavassa kuvassa on esimerkki avoinna olevasta **Kaikki alennukset** -sivusta.

![Kaikki alennukset -sivu](./media/View_all_discounts.png "Kaikki alennukset -sivu")

Jos haluat näyttää alennukset, järjestelmä etsii kaikki alennukset, jotka vastaavat yhtä tai useampaa seuraavista ehdoista:

- Alennuksen hintaryhmä vastaa myymälän hintaryhmää.
- Alennuksen hintaryhmä yhdistetään liitokseen tai kanta-asiakasohjelmaan.
- Alennuksen hintaryhmä on liitetty myymälään liittyvään luetteloon.

**Kaikki alennukset** -sivulla on vain osa kuponkeihin perustuvia alennuksia, koska vähittäismyyjät yleensä luovat tuhansia kuponkeja ja vastaavia alennuksia yksittäisille asiakkaille. Tämä sivu ei ole tarkoitettu asiakaskohtaisille alennuksille. Kuponkiin perustuvat alennukset näytetään vain, jos **Käytä ilman kuponkikoodia** -vaihtoehto on otettu käyttöön kussakin kupongin otsikossa. Tällöin kassat voivat käyttää kuponkia ilman kuponkikoodin syöttämistä tai viivakoodin skannaamista.

Kun **Käytä ilman kuponkikoodia** -asetus on käytössä, käytettävissä on erilaisia skenaarioita. Kassat voivat esimerkiksi antaa asiakkaille lisäalennuksia asiakkaiden lepyttelytarkoituksissa tai tuotevirheiden vuoksi. Tulostettuja kuponkikoodeja tai viivakoodeja ei tarvitse jakaa kassoille. Sen sijaan kassat voivat valita **Käytä kuponkia** -painikkeen. Kuponki kohdistetaan automaattisesti tapahtumaan. Jos kuponkiotsikolle on olemassa useita kuponkeja, järjestelmä valitsee automaattisesti tapahtuman ensimmäisen aktiivisen kupongin.

**Kaikki alennukset** -sivulla myyjät voivat myös etsiä alennuksia avainsanojen perusteella. Avainsanahaku etsii kentät, joissa on alennuksen nimi ja alennuksen kuvaus. Myyjät voivat myös suodattaa alennuksia sen mukaan, vaatiiko alennus kuponkikoodin.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Ristiin- ja lisämyynti alennusten avulla

Monirivialennukset, kuten määräalennukset, yhdistelmäalennukset ja raja-arvoalennukset, ovat erinomainen tapa motivoida asiakkaita ostamaan enemmän tuotteita suurempien alennusten saamiseksi. Näin ne auttavat myös kasvattamaan asiakkaan ostoskoria ja vähittäismyyjän tuottoa. Näitä alennuksia voi julkaista sähköisen kaupankäynnin sivustoilla, yhteisöpalveluissa ja myymälän bannereissa.

Vaikka näitä kaikkia julkisuusmenetelmiä käytettäisiin, asiakkaat eivät välttämättä huomaa käyttää kampanjoita hyväkseen. Myyjät voivat helposti huomata, mitkä kampanjat ovat käytettävissä valitulla rivillä tai jopa koko ostoskorissa, jos vähittäismyyjät lisäävät Näytä kaikki alennukset -toiminnon painikkeen mihin tahansa painikeruudukkoon myyntipisteessä. Suosittelemme, että painike lisätään **Tapahtuma**-sivun painikeruudukkoon. Näin myyjät voivat valita tapahtumarivin ja valita sitten painikkeen, joka näyttää kaikki valitulla rivillä käytettävissä olevat alennukset. Myyjä voi myös valita toisen välilehden, jolla näytetään koko tapahtuman alennukset.

Aiemmin mainittu **Kaikki alennukset** -sivu näyttää vain alennukset, jotka eivät kilpaile minkään kohdistetun alennuksen kanssa. Näin varmistetaan, että jos myyjä kertoo asiakkaalle alennuksesta ja asiakas tekee vaaditun toiminnon (esimerkiksi ostaa yhden lisänimikkeen ja saa 10 prosenttia alennusta), alennus kohdistetaan tapahtumaan. Kuten aiemmin mainittiin, kuponkiin perustuvat alennukset näytetään vain, jos **Käytä ilman kuponkikoodia** -vaihtoehto on otettu käyttöön.

Yksinkertaisessa skenaariossa, jossa kaikilla alennuksilla on sama prioriteetti, alennuksen samanaikaisuustila on **Yhdistetty** ja alennuksen samanaikaisuuden ohjausobjektiksi on määritetty **Paras hinta ja yhdistelmä prioriteetin mukaan, ei koskaan yhdistelmää prioriteettien kesken**, **Kaikki alennukset** -sivulla näkyvät tuotteen käytettävissä olevat alennukset, koska kaikki alennukset ovat yhdistelmiä eivätkä kilpaile keskenään.

Seuraavissa kuvissa näkyy logiikka, joka määrittää, mitkä alennukset näytetään lisäskenaarioissa. Niitä ovat esimerkiksi skenaario, jossa alennuksen samanaikaisuustila on **Paras hinta** tai **Poissulkeva** ja käytetään kahta tai useampaa prioriteettia. Näissä skenaarioissa näytettäviä alennuksia muokataan lisää sen mukaan, onko alennuksen samanaikaisuuden ohjausobjektiksi määritetty **Paras hinta ja yhdistelmä prioriteetin mukaan, ei koskaan yhdistelmää prioriteettien kesken** vai **Vain paras hinta prioriteetissa, aina yhdistelmä prioriteettien kesken**.

Seuraavassa kuvassa on logiikka, jota käytetään alennuksen samanaikaisuuden ohjausobjektiksi on määritetty **Paras hinta ja yhdistelmä prioriteetin mukaan, ei koskaan yhdistelmää prioriteettien kesken**.

![Logiikka Paras hinta ja yhdistelmä prioriteetin mukaan, ei koskaan yhdistelmää prioriteettien kesken -kohdassa](./media/Model_1.png "Logiikka Paras hinta ja yhdistelmä prioriteetin mukaan, ei koskaan yhdistelmää prioriteettien kesken -kohdassa.").

Seuraavassa kuvassa on logiikka, jota käytetään alennuksen samanaikaisuuden ohjausobjektiksi on määritetty **Vain paras hinta prioriteetissa, aina yhdistelmä prioriteettien kesken**.

![Logiikka Vain paras hinta prioriteetissa, aina yhdistelmä prioriteettien kesken -kohdassa](./media/Model_2.png "Logiikka Vain paras hinta prioriteetissa, aina yhdistelmä prioriteettien kesken -kohdassa.").
