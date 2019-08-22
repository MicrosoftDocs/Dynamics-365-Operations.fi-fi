---
title: Kuluraporttien uusi toteutus
description: Tässä ohjeaiheessa on tietoja uudelleensuunnitellusta ja uudistetuista kuluraporttikirjauksen kokemuksista Microsoft Dynamics 365 for Finance and Operations. Uusi kokemus yksinkertaistaa kuluraporttien täyttämistä ja lyhentää tarvittavaa aikaa.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 320984fc6be231c941df17abb7246e92f6aa4b9a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841054"
---
# <a name="expense-reports-reimagined"></a>Kuluraporttien uusi toteutus

[!include[banner](../includes/banner.md)]

Kuluraporttimerkintää on uudistettu siten, että se yksinkertaistaa täyttämisprosessia ja lyhentää tarvittavaa aikaa. Tässä ovat uuden kulukokemuksen tärkeimmät osat:

- Uusi kulujenhallintatyötila, jonka avulla voit käyttää edustajan kuluja.
- Uusi kuittien vastaavuuskokemus, joka näyttää paremmin otsikkotason vastaanotot ja helpottaa vastaanottojen liittämistä kuluriveihin.
- Uusi vain luku -muotoinen ruudukko, jonka avulla voit tarkastella useita muita kulurivejä ja muita tietosarakkeita. Voit nyt tarkastella kaikkia eriteltyjä ja jaettuja rivejä sekä niiden pääkuluja.
- Yksinkertaistettu ruutu kulujen muokkaamista varten.
- Uusitut virhe-, varoitus- ja käytäntösanomat auttavat takaamaan, että sinulla on oikea konteksti, jotta ymmärrät, mikä ongelma on ja miten se ratkaistaan. Microsoft on poistanut useita sanomia, jotka tulivat näkyviin, ennen kuin käyttäjillä oli mahdollisuus suorittaa tehtävänsä ja käsitellä ongelmia, kuten epätäydellinen erittelysanoma.
- Uusi sivu, jonka avulla voit määrittää, mitkä kentät ovat pakollisia organisaatiossa, mitkä kentät ovat valinnaisia ja mitä kenttiä ei saa siepata. Tämän sivun avulla voit pienentää käyttäjien määrittämien kenttien määrää.
- Kuluraporttien uusi ulkoasu ja tuntuma, jolloin raportit eivät enää vaikuta siltä kuin ne olisi suunniteltu kirjanpitoihmisille.

Voit ottaa uuden käyttökokemuksen käyttöön käyttämällä **Ominaisuuksien hallinta** -työtilaa, kun haluat ottaa **Kuluraporttien uusi toteutus** -ominaisuuden käyttöön. Kun otat tämän toiminnon käyttöön, seuraavat toiminnot toteutuvat:

- Aiemmin luotu kulujen työtila korvataan uudella työtilalla.
- Uusi kulukentän näkyvyyden valikkovaihtoehto lisätään.
- Kuluraporttien (aiemmin luodun sivun) tai kuluraportin kenttien aiemmin luotuja valikkokohteita ei poisteta.
- Työn kulut ja hyväksynnät ovat edelleen olemassa kuluraportit-sivulla.

## <a name="getting-started-video-for-new-users"></a>Aloitusvideo uusille käyttäjille

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

[Kulukokemus Dynamics 365 for Finance and Operationsissa](https://youtu.be/Ocy-MsTvEE0) -video (näkyy ylempänä) sisältyy [Finance and Operations -soittolistaan](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), joka on saatavilla YouTubessa.

## <a name="new-features"></a>Uudet ominaisuudet

| Uusi ominaisuus | Kuvaus |
|---|----|
| Kulukentän näkyvyys | Uuden asetussivun avulla voit määrittää, mitkä kentät poistetaan käytöstä organisaatiossa, mitä kenttiä tarvitaan ja mitkä kentät ovat suositeltavia. |
| Pakolliset kentät | Uuden yksinkertaisen konfiguraation avulla voit tehdä joitakin tarvittavia kenttiä tarvitsematta käyttää käytäntökehystä. |
| Valinnaiset kentät | Valinnaisten kenttien toinen sivu lisätään. Näin työntekijät eivät tunne, että heidän on asetettava kentät, mutta kentät ovat edelleen helposti saatavilla. |
| Lisää vastaanotot, joita ei ole liitetty | Mahdollisuus lisätä ei-liitettyjä vastaanottoja kuluraporttiin näkyy enemmän työtilassa ja kuluraportissa. |
| Parannettu sanoman välitys | Parempi näkyvyys kuluriveille, joilla on varoituksia tai virheitä. |
| Sanomapalkin sanomien vähentäminen| Infolokin sanomien määrä väheni ja useissa tapauksissa yritettiin estää kaksoisarvoja sisältävien sanomien näkyminen. |
| Yhteen ryhmiteltyinä yhteiset toimenpiteet | Käyttöliittymä siivottiin lisäämällä uusia toimintoja -painike useimmille yleisille rivitason toiminnoille ja lisäämällä kolme pistettä (...) otsikolle ja muille harvemmin käytetyille toiminnoille. |
| Uusi työtila näkyvyyden lisäämiseksi | Uusi työtila yhdistää ominaisuudet ja linkit, joiden avulla käyttäjät voivat siirtyä eri alueille. |
| Aiemmin luotujen kulujen ja vastaanottojen lisääminen kulujen luonnin yhteydessä | Kun luot kuluraportteja, voit lisätä kaikki tai valitut kulut ja vastaanotot. |
| Vaihtokurssin laskin | Järjestelmä lisää vaihtokurssin laskimen, jonka avulla voit laskea käteistapahtumien vaihtokurssin. |
| Tallenna ja lisää uusia kulurivejä | **Tallenna**- ja **Uusi**-painikkeet ovat käytettävissä, kun uusia kuluja syötetään, jotta kulurivit voidaan syöttää nopeasti. |
| Parempi näkyvyys jaetuille ja eritellyille riveille | Eritellyt ja jaetut rivit lisätään suoraan kulujen luetteloon, mikä parantaa näkyvyyttä ja auttaa selvittämään, onko käytössä käytäntövirheitä tai muita virheitä. |
| Näytä kuitit erittelyissä | Kuitit voidaan näyttää erittelyn aikana. |

Ensimmäinen julkaisu keskittyy kulukirjaus skenaarioon. Kuluraporttien tarkistus tai hyväksymisskenaario käyttää edelleen aiemmin luotua kulukirjaussivua.

Aiemmin luodussa sivussa on seuraavat ominaisuudet, mutta ne eivät ole vielä näkyvissä uudella sivulla. Nämä ominaisuudet otetaan uudelleen käyttöön seuraavien useiden julkaisujen aikana:

- Hyväksynnät
- Ostoreskontran hyväksynnät ja kirjanpidon muokkausmahdollisuus
- Useita aloituskohtia
- Matkustusehdotuksen integrointi
- Kulukentän näkyvyyden tietoyksikkö
- Päivärahakulujen kirjaus
- Rivitason työnkulku
- Väliaikaisen hyväksyjän tuki
- Lisäerittely
