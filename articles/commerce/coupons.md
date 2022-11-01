---
title: Kupongit
description: Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commercen kuponkeihin liittyvistä ominaisuuksista.
author: boycez
ms.date: 09/06/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2017-06-30
ms.openlocfilehash: 20427a04a552ddec013daa6576ec64ab7046e95f
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709756"
---
# <a name="coupons"></a>Kupongit

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan Microsoft Dynamics 365 Commercen kuponkeihin liittyvistä ominaisuuksista.

Kupongit ovat koodeja ja viivakoodeja, joilla alennukset lisätään tapahtumiin. Jälleenmyyjät jakavat kuponkeja mahdollisille ja olemassa oleville asiakkaille tehdäkseen tuotemerkin tunnetuksi, edistääkseen muuttumista, säilyttääkseen asiakaskannan, tehostaakseen myyntiä ja loppujen lopuksi parantaakseen tuottoa. Kupongeista on tullut eräs suosituimmista markkinointityökaluista. Ne muodostavat uuden toimintatavan sähköisen kaupankäynnin myynnissä.

Dynamics 365 Commercessa kupongit linkitetään alennuksiin. Niitä käytetään alennusten kanssa. Kukin kuponki liittyy yhteen alennukseen. Linkitetty alennus määrittää tuotejoukon, jossa kuponkia voidaan käyttää.

Alennukseen liittyvät hintaryhmät määrittävät ehdot, joissa kuponkia voidaan käyttää. Nämä ehdot sisältävät asiakasryhmät ja myyntikanavat. Kupongit määrittävät myös **Käyttöraja**- ja **Asiakas on pakollinen** -ominaisuudet, joita voidaan käyttää valinnaisten käyttöehtojen määrittämisessä.

Kussakin kupongissa voi olla useita kuponkikoodeja ja -viivakoodeja, ja kullakin koodilla voi olla oma voimassaolopäivämääräväli ja tila. Jos koodin tilaksi on määritetty **Ei käytössä**, koodia ei voi käyttää missään kanavassa.

## <a name="set-up-a-coupon"></a>Kupongin määrittäminen

Ennen kuin kupongin määrittämistä on määritettävä kupongin viivakoodi ja kaksi kuponkinumerosarjaa.

Voit määrittää kupongin Commerce headquartersissa alla olevien vaiheiden mukaisesti.

1. Siirry kohtaan **Retail ja Commerce \> Varastonhallinta \> Viivakoodit ja etiketit \> Muotomerkit**.
1. Valitse **Lisää**, jos haluat luoda **Kuponkikoodi**-tyyppisen muotomerkin. Voit valita **Merkki**-kentässä minkä tahansa käyttämättömän merkin.
1. Siirry kohtaan **Retail ja Commerce \> Varastonhallinta \> Viivakoodit ja etiketit \> Viivakoodimuodon määritys**.
1. Valitse **Uusi**, jos haluat **Kuponki**-tyyppisen viivakoodimuodon.
1. Siirry kohtaan **Retail ja Commerce \> Varastonhallinta \> Viivakoodit ja etiketit \> Viivakoodin määritys**.
1. Valitse **Uusi**, jos haluat luoda viivakoodin, joka käyttää luomaasi viivakoodimuotoa.
1. Siirry kohtaan **Organisaation hallinta \> Numerosarjat**.
1. Luo kaksi numerosarjaa seuraavasti:

    1. Yksi sarja **Kupongin numero** -viitteelle. Tämä sarja määrittää kupongin yksilöivä tunniste.
    1. Yksi sarja **Kuponkikoodin tunnus** -viitteelle. Tämä sarja määrittää kupongin kunkin kuponkikoodin yksilöivän tunnisteen.

    Numerosarjaksi on **Alue**-kentässä valittava **Yritys**. Useimmissa tapauksissa kumpikin numerosarja tulee luoda automaattisesti.

1. Siirry kohtaan **Commercen parametrit \> Hinnat ja alennukset \> Kupongit**.
1. Määritä **Kupongin viivakoodin muoto** -kenttä aiemmin luodussa viivakoodissa.
1. Siirry kohtaan **Commercen parametrit \> Numerosarjat**.
1. Valitse numerosarjat, jotka loit aiemmin **Kupongin numero**- ja **Kuponkikoodin tunnus** -viitteissä.

Jos haluat määrittää kupongin, luo ensin alennus ja kuponki erikseen ja linkitä ne valitsemalla alennus kupongin määrityksen **Alennus**-kentässä. Kun kuponki on linkitetty alennukseen, linkitetyn alennuksen **Tila**-, **Voimaantulopäivä**- ja **Vanhentumispäivä**-kentät muuttuvat vain luku -kentiksi, koska arvot määritetään kupongin tilan ja voimassaolokauden mukaan. Kun kupongin tilaksi on määritetty **Aktiivinen**, linkitetyn alennuksen tilaksi päivitetään automaattisesti **Käytössä**. Samoin kun kupongin tilaksi on määritetty **Passiivinen**, linkitetyn alennuksen tilaksi päivitetään automaattisesti **Ei käytöstä**.

## <a name="use-a-coupon"></a>Kupongin käyttäminen

Jos haluat lisätä kupongin myyntitapahtumaan Commercen myyntipisteessä, voit käyttää kuponkikoodia tai kupongin viivakoodia. Jos haluat käyttää kuponkikoodi, valitse **Lisää kuponkikoodi** -toiminto ja syötä koodi. Jos haluat käyttää kupongin viivakoodia, voit joko skannata viivakoodin skannerilla tai syöttää sen käyttämällä numeronäppäimistöä **Tapahtuma**-näytössä.

Jälleenmyyjät haluavat joskus kassojen antavan kiinteitä alennuksia asiakkaille lepyttelytarkoituksissa tai tuotevikojen vuoksi, mutta he eivät halua tulostaa kuponkikoodeja ja jakaa niitä kassoille. Tässä tapauksessa voit määrittää kupongin **Käytä ilman kuponkikoodia** -vaihtoehdon arvoksi **Kyllä**. Myyntipisteen kassat voivat tämän jälkeen käyttää **Käytä kuponkia** -toimintoa **Näytä käytettävissä olevat alennukset** -toiminnossa, jos haluat lisätä kupongin tapahtumaan ilman koodin manuaalista syöttämistä. Jos kupongilla on useita kuponkikoodeja, järjestelmä valitsee automaattisesti ensimmäisen aktiivisen kupongin ja käyttää sitä tapahtumassa.

Jos haluat lisätä kupongin puhelinkeskuksen myyntitilaukseen, puhelinkeskuksen käyttäjän on valittava **Kupongit**-kohta myyntitilaussivun **Hallitse**-välilehdessä.

Ostaja voi lisätä kupongin sähköisen kaupankäynnin tilaukseen syöttämällä kuponkikoodin **kampanjakoodin** kenttään ostoskorissa.

Kun kuponki on lisätty myyntitilaukseen, hinnoittelumoduuli käynnistää välittömästi uudelleenlaskennan koko tilauksessa siitä huolimatta, onko viivytetty laskenta otettu käyttöön vai ei.

> [!NOTE]
> Commercen versiossa 10.0.30 ja uudemmissa versioissa puhelinkeskuksen käyttäjien on valittava **Laske uudelleen** -kohta **Laskenta**-ryhmässä toimintaruudun **Myynti**-välilehdessä, kun he ovat lisänneet kupongin puhelinkeskuksen myyntitilaukseen. Näin otetaan käyttöön kuponkiin liitetty alennus.

## <a name="coupon-usage-limit"></a>Kupongin käyttöraja

Kupongit voidaan määrittää siten, niiden käyttö on rajoitettua. Käyttöraja voidaan määrittä asiakas- tai kanavakohtaisesti tai yleisenä rajoituksena. Käyttörajaa noudatetaan kupongin kuponkikoodikohtaisesti. Esimerkiksi kaksi kuponkikoodia sisältävää kertakäyttökuponkia voi käyttää kummassakin kuponkikoodissa kerran, eli yhteensä kaksi kertaa.

Kuponkeja voidaan käyttää eri myyntikanavissa. Puhelinkeskuksessa rajoitetun käytön kuponkeja voidaan käyttää kuitenkin vain, kun puhelinkeskuksen **Ota käyttöön tilausten viimeistely** -asetus on otettu käyttöön. Jos **Ota käyttöön tilausten viimeistely** -asetus on poistettu käytöstä, voidaan käyttää vain muita kuin rajoitetun käytön kuponkeja.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
