---
title: "Vähittäismyynnin kuponkien luonti"
description: "Tässä ohjeaiheessa on yleiskatsaus vähittäismyynnin kupongeista ja kerrotaan niiden määrittämisestä."
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e05361bf865e44ba6073198fba94d7102b1ed19
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="create-coupons-for-retail-sales"></a>Vähittäismyynnin kuponkien luonti

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a>Kuponkien yleiskatsaus

Kupongit ovat koodeja ja viivakoodeja, joilla vähittäismyynnin alennukset lisätään tapahtumiin. Kussakin kupongissa voi olla useita koodeja, ja kullakin koodilla voi olla oma voimassaolopäivämäärä. 

Kukin kuponki liittyy yhteen vähittäismyynnin alennukseen. Alennukseen liitetyt hintaryhmät määrittämät asiakkaat, jotka voivat käyttää kuponkia, tai kanavat, joissa kuponki on voimassa. 

Kupongit ovatkin siis eräänlainen ylimääräinen oikeellisuustarkistus muiden vähittäismyynnin alennusten lisäksi. Kuponki sisältää tarvittavat kuponkikoodit ja viivakoodit sekä kyseisteen koodien päivämääräalueet. Kupongissa voi olla myös valinnaisia käyttörajoituksia ja asiakkaalta edellytettäviä ominaisuuksia. Alennus ilmoittaa tuotejoukon, jota kuponki koskee. Alennusten hintaryhmät ilmoittavat asiakas-, kanava- tai luettelojoukon, jota kuponki koskee.

Alennus ja kuponki luodaan kuponkia varten erikseen. Ne linkitetään sitten valitsemalla alennus Microsoft Dynamics 365 for Retailin kuponkisivulla. 

> [!NOTE]
> Kun kuponki on linkitetty alennukseen, monet Microsoft Dynamics 365 for Retailin alennussivun kentät muuttuvat vain luku -muotoisiksi, sillä niitä hallitaan kupongin asetuksista. Niitä ovat esimerkiksi tilan ja vakiopäivämääräalueen kentät.

### <a name="limited-use-coupons"></a>Kupongit, joiden käyttö on rajoitettua

Kupongit voidaan määrittää siten, niiden käyttö on rajoitettua. Käyttöraja voidaan määrittä asiakas- tai kanavakohtaisesti tai yleisenä rajoituksena. Tätä rajoitusta noudatetaan, kun koodi tai viivakoodi annetaan tai skannataan myyntipisteessä tai myynnin tilaustenkäsittelyn aikana. Kuponki kirjataan käytetyksi, kun tilaus, johon kuponki on liitetty, on valmis.

Rajaa noudatetaan kupongin kuponkikoodikohtaisesti. Esimerkiksi kaksi kuponkikoodia sisältävää kertakäyttökuponkia voi käyttää kahdesta: kerran kummallakin koodilla. Jokainen kupongin koodi voidaan määrittää erikseen aktiiviseksi.

## <a name="managing-coupons"></a>Kuponkien hallinta

Alennus ja kuponki on luotava erikseen. Ne linkitetään sitten valitsemalla alennus kuponkisivulla. Kun kuponki on linkitetty alennukseen, monet alennuskentät muuttuvat vain luku -muotoisiksi, sillä niitä hallitaan kupongin asetuksista. Niitä ovat esimerkiksi tilan ja vakiopäivämääräalueen kentät.  

Kupongit ovatkin nyt eräänlainen ylimääräinen oikeellisuustarkistus muiden vähittäismyynnin alennusten lisäksi. Kuponki sisältää tarvittavat kuponkikoodit ja viivakoodit sekä kyseisteen koodien päivämääräalueet, käyttörajoitukset ja asiakkaalta edellytettävän ominaisuuden. Alennus ilmoittaa tuotejoukon, jota kuponki koskee. Alennusten hintaryhmät ilmoittavat asiakas-, kanava- tai luettelojoukon, jota kuponki koskee.

## <a name="system-setup-for-coupons"></a>Kupongeissa tarvittavat järjestelmäasetukset 

Ennen kuin kupongin määrittämistä on määritettävä kupongin viivakoodi ja kaksi kuponkinumerosarjaa. 

1.  Luo **Muotomerkit**-sivulla kuponkikoodin muotomerkit. Voit valita minkä tahansa käyttämättömän merkin.
2.  Luo **Viivakoodin muotoasetukset** -sivulla uusi viivakoodin muoto Valitse **Tyyppi**-kentässä **Kuponki**.
3.  Luo **Viivakoodiasetukset**-sivulla uusi juuri luomaasi viivakoodin muotoa käyttävä viivakoodi.
4.  Luo **Numerosarjat**-sivulla kaksi uutta numerosarjaa. Toinen numerosarja on tarkoitettu kuponkikooditunnukselle ja toinen kupongin numerolle. Kuponkikooditunnus on kunkin kupongin kuponkikoodin yksilöllinen tunnus. Kupongin numero on kupongin yksilöllinen tunnus. Kussakin kupongissa voi useita on kupongin käynnistäviä koodeja ja viivakoodeja.

    > [!NOTE]
    > Numerosarjaksi on **Alue**-kentässä valittava **Yritys**. Useimmissa tapauksissa kumpikin numerosarja pitäisi luoda automaattisesti.

5.  Valitse **Vähittäismyynnin yhteiset parametrit** -sivun **Viivakoodit**-välilehdessä aiemmin luomasi viivakoodi.
6.  Valitse **Vähittäismyynnin parametrit** -sivun **Numerosarjat**-välilehdessä kuponkinumerolle ja kuponkikooditunnukselle luomasi numerosarjat.
7.  Voit nyt avata **Kupongit**-sivun ja luoda uusia kuponkeja.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Osittaisten päivitysten vaikutus kuponkeihin

Kuponkitoiminto koostuu useista erillisistä Dynamics 365 for Retailin ominaisuuksista. Microsoft Dynamics 365 for Retail Headquarters (HQ) ja kanava voidaan päivittää osoittein kaikissa komponenteissa. Tämän vuoksi on tärkeää, että ymmärrät, miten osittaiset päivitykset vaikuttavat kuponkitoimintoon kokonaisuudessaan.

- **HQ päivitetään osittain, mutta Retail-palvelinta ja POS:stä ei päivitetä.** HQ-päivityksessä kuponki- ja alennussivut päivitetään samoin kuin vähittäismyynnin hinnoitteluohjelma. Jos vain toinen kahdesta komponentista päivitetään, osa Retailin sivuista ei vastaa hinnan laskentatietoja. Niinpä alennuksia laskettaessa voi esiintyä odottamattomia laskettuja alennuksia tai virheitä.
- **HQ päivitetään, mutta Retail-palvelinta ja POS:stä ei päivitetä (N-1).** Koska kaikkia vähittäismyymälöitä ei voi päivittää samalla kertaa, HQ kannattaa päivittää ennen myymälöiden päivitystä. N-1-skenaariossa kuponkeihin liittyvä uusi toiminto ei ole vielä päivittämättömien myymälöiden käytössä. Kuponkitoiminnossa otetaan esimerkiksi käyttöön poissulkemisrivit. Jos poissulkemisrivejä käytetään alennuksessa, aiempaa versiota käyttävät myymälät eivät voi käyttää niitä.
- **HQ:ta ei päivitetä, mutta Retail-palvelin ja POS päivitetään (N+1).** Koska Retail-palvelimen päivitetty hinnoitteluohjelma voi käsitellä vanhoja alennuskoodeja hinnan laskennan aikana, päivityksellä ei pitäisi olla toiminnallisia vaikutuksia tässä skenaariossa.

