---
title: Vähittäismyynnin kuponkien määrittäminen
description: Tässä ohjeaiheessa on yleiskatsaus kupongeista ja niiden määrittämisestä.
author: scott-tucker
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: bc79970528e23397b756fa15a715fba834edcc06e4522c6c35b64aede4976300
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745305"
---
# <a name="set-up-coupons-for-retail-sales"></a>Vähittäismyynnin kuponkien määrittäminen

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Kuponkien yleiskatsaus

Kupongit ovat koodeja ja viivakoodeja, joilla alennukset lisätään tapahtumiin. Kussakin kupongissa voi olla useita koodeja, ja kullakin koodilla voi olla oma voimassaolopäivämäärä.

Kukin kuponki liittyy yhteen alennukseen. Alennukseen liitetyt hintaryhmät määrittämät asiakkaat, jotka voivat käyttää kuponkia, tai kanavat, joissa kuponki on voimassa.

Kupongit ovatkin siis eräänlainen ylimääräinen oikeellisuustarkistus muiden alennusten lisäksi. Kuponki sisältää tarvittavat kuponkikoodit ja viivakoodit sekä kyseisteen koodien päivämääräalueet. Kupongissa voi olla myös valinnaisia käyttörajoituksia ja asiakkaalta edellytettäviä ominaisuuksia. Alennus ilmoittaa tuotejoukon, jota kuponki koskee. Alennusten hintaryhmät ilmoittavat asiakas-, kanava- tai luettelojoukon, jota kuponki koskee.

Alennus ja kuponki luodaan kuponkia varten erikseen. Sitten linkität ne valitsemalla alennuksen kuponkisivulta Commercessa.

> [!NOTE]
> Kun kuponki on linkitetty alennukseen, monet Commercen alennussivun kentät muuttuvat Vain luku -muotoisiksi, sillä niitä hallitaan kupongin asetuksista. Niitä ovat esimerkiksi tilan ja vakiopäivämääräalueen kentät.
> 
> Kun käytät kuponkeja puhelinkeskuskanavassa, sinun on valittava **Laske uudelleen** -painike **(Myy-välilehti > Laske > Uudelleenlaskenta)**, jotta kupongin alennus voidaan ottaa käyttöön. Tämä lisävaihe poistetaan tulevassa versiossa.

### <a name="limited-use-coupons"></a>Kupongit, joiden käyttö on rajoitettua

Kupongit voidaan määrittää siten, niiden käyttö on rajoitettua. Käyttöraja voidaan määrittä asiakas- tai kanavakohtaisesti tai yleisenä rajoituksena. Tätä rajoitusta noudatetaan, kun koodi tai viivakoodi annetaan tai skannataan myyntipisteessä tai myynnin tilaustenkäsittelyn aikana.

Rajaa noudatetaan kupongin kuponkikoodikohtaisesti. Esimerkiksi kaksi kuponkikoodia sisältävää kertakäyttökuponkia voi käyttää kahdesta: kerran kummallakin koodilla. Jokainen kupongin koodi voidaan määrittää erikseen aktiiviseksi.

Kuponkeja voidaan käyttää minkä tahansa myyntikanavan Call Center -tilauksiin, kuponkien rajoitettua käyttöä voidaan käyttää vain niihin Call Center -tilauksiin, joissa **Tilauksen valmistumisasetus** on käytössä. Jos tämä ei ole käytössä, Call centerin tilauksissa voi käyttää vain ei-rajoitettuja käyttötyyppikuponkeja.

> [!NOTE]
> Kuponkikoodin käyttörajan saavutuksen jälkeen järjestelmä *ei* vaihda kuponkikoodin tilaksi automaattisesti Käytetty. Kuitenkin se kuponkikoodi on saavuttanut käyttörajan, eikä sitä voi käyttää. Jos kuponkikoodin tilaksi on manuaalisesti määritetty jokin muu kuin **Aktiivinen**, kyseistä kuponkikoodia ei voi käyttää missään kanavassa.  

## <a name="managing-coupons"></a>Kuponkien hallinta

Alennus ja kuponki on luotava erikseen. Ne linkitetään sitten valitsemalla alennus kuponkisivulla. Kun kuponki on linkitetty alennukseen, monet alennuskentät muuttuvat vain luku -muotoisiksi, sillä niitä hallitaan kupongin asetuksista. Niitä ovat esimerkiksi tilan ja vakiopäivämääräalueen kentät.

Kupongit ovatkin nyt eräänlainen ylimääräinen oikeellisuustarkistus muiden alennusten lisäksi. Kuponki sisältää tarvittavat kuponkikoodit ja viivakoodit sekä kyseisteen koodien päivämääräalueet, käyttörajoitukset ja asiakkaalta edellytettävän ominaisuuden. Alennus ilmoittaa tuotejoukon, jota kuponki koskee. Alennusten hintaryhmät ilmoittavat asiakas-, kanava- tai luettelojoukon, jota kuponki koskee.

## <a name="system-setup-for-coupons"></a>Kupongeissa tarvittavat järjestelmäasetukset

Ennen kuin kupongin määrittämistä on määritettävä kupongin viivakoodi ja kaksi kuponkinumerosarjaa.

1. Luo **Muotomerkit**-sivulla kuponkikoodin muotomerkit. Voit valita minkä tahansa käyttämättömän merkin.
2. Luo **Viivakoodin muotoasetukset** -sivulla uusi viivakoodin muoto Valitse **Tyyppi**-kentässä **Kuponki**.
3. Luo **Viivakoodiasetukset**-sivulla uusi juuri luomaasi viivakoodin muotoa käyttävä viivakoodi.
4. Luo **Numerosarjat**-sivulla kaksi uutta numerosarjaa. Toinen numerosarja on tarkoitettu kuponkikooditunnukselle ja toinen kupongin numerolle. Kuponkikooditunnus on kunkin kupongin kuponkikoodin yksilöllinen tunnus. Kupongin numero on kupongin yksilöllinen tunnus. Kussakin kupongissa voi useita on kupongin käynnistäviä koodeja ja viivakoodeja.

    > [!NOTE]
    > Numerosarjaksi on **Alue**-kentässä valittava **Yritys**. Useimmissa tapauksissa kumpikin numerosarja pitäisi luoda automaattisesti.

5. Valitse **Commercen parametrit** -sivun **Viivakoodit**-välilehdessä aiemmin luomasi viivakoodi.
6. Valitse **Commercen jaetut parametrit** -sivun **Numerosarjat**-välilehdessä kuponkinumerolle ja kuponkikooditunnukselle luomasi numerosarjat.
7. Voit nyt avata **Kupongit**-sivun ja luoda uusia kuponkeja.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Osittaisten päivitysten vaikutus kuponkeihin

Kuponkitoiminto koostuu useista erillisistä ominaisuuksista. Commerce Headquarters (HQ) ja kanava voidaan päivittää osoittein kaikissa komponenteissa. Tämän vuoksi on tärkeää, että ymmärrät, miten osittaiset päivitykset vaikuttavat kuponkitoimintoon kokonaisuudessaan.

- **HQ päivitetään osittain, mutta Commerce Scale Unitia ja POS:stä ei päivitetä.** HQ-päivityksessä kuponki- ja alennussivut päivitetään samoin kuin kaupan hinnoitteluohjelma. Jos vain toinen kahdesta komponentista päivitetään, osa Commercen sivuista ei vastaa hinnan laskentatietoja. Niinpä alennuksia laskettaessa voi esiintyä odottamattomia laskettuja alennuksia tai virheitä.
- **HQ päivitetään, mutta Commerce Scale Unitia ja POS:stä ei päivitetä (N-1).** Koska kaikkia myymälöitä ei voi päivittää samalla kertaa, HQ kannattaa päivittää ennen myymälöiden päivitystä. N-1-skenaariossa kuponkeihin liittyvä uusi toiminto ei ole vielä päivittämättömien myymälöiden käytössä. Kuponkitoiminnossa otetaan esimerkiksi käyttöön poissulkemisrivit. Jos poissulkemisrivejä käytetään alennuksessa, aiempaa versiota käyttävät myymälät eivät voi käyttää niitä.
- **HQ:ta ei päivitetä, mutta Commerce Scale Unit ja POS päivitetään (N-1).** Koska Commerce Scale Unitin päivitetty hinnoitteluohjelma voi käsitellä vanhoja alennuskoodeja hinnan laskennan aikana, päivityksellä ei pitäisi olla toiminnallisia vaikutuksia tässä skenaariossa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
