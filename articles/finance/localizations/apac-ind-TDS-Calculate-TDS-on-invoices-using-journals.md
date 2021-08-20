---
title: Laskujen TDS:n laskeminen kirjauskansioiden avulla
description: Tässä aiheessa luetellaan kirjauskansioiden vaiheet Vero vähennettynä lähteissä (TDS) -arvon laskemiseksi.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: cfe473f39ee729957924fd7c161aed01138cd507eea56766af35177891676f65
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778890"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>Laskujen TDS:n laskeminen kirjauskansioiden avulla

[!include [banner](../includes/banner.md)]

Tässä aiheessa luetellaan kirjauskansioiden vaiheet Vero vähennettynä lähteissä (TDS) -arvon laskemiseksi.

Aloita avaamalla **Yleiset kirjauskansiot** -sivu (**Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot**).

[![Yleiset kirjauskansiot.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Luo kirjauskansiorivejä taulussa lueteltujen kirjauskansiolomakkeiden avulla. Valitse tilityyppi ja vastatilin tyyppi ja kirjoita tapahtuman summa. 

   > [!NOTE]
   > Valitse **Hyväksyttyjen laskujen kirjauskansio** -sivulla **Etsi tositteet** ja valitse, joissa TDS lasketaan. Tarkastele **Laskurekisteri**-sivulla tai **Etsi tositteet** -sivulla luotuja laskuja.  

2. **Yleiset**-välilehdessä **Kirjaustosite**-sivulla tarkastele tai muokkaa toimittajalle tai asiakkaalle määritettyä oletusarvoista TDS-ryhmää **TDS-ryhmä**-kentässä. Kirjauskansion riveille laskettu TDS-summa perustuu **TDS-ryhmä**-kentässä luetelluille TDS-verokoodeille määritettyyn kaavaan. 

   > [!NOTE]
   > **Ennakonpidätysryhmä**-kenttä ja **TCS-ryhmä**-kenttä eivät ole käytettävissä, kun valitset TDS-ryhmän **TDS-ryhmä**-kentästä. **Ennakonpidätysryhmä**-kenttä on käytettävissä vain **Kirjauskansio**-sivulla. TDS lasketaan vain, jos **Laske ennakonpidätys** -valintaruutu on valittuna toimittajalle tai asiakkaalle **Kaikki toimittajat**- tai **Kaikki asiakkaat** -sivuilla.   

3. Valitse **Verotiedot**-välilehti ja valitse yrityksen vaihtoehtoinen osoite, joka on määritetty tässä kentässä näkyvää yritystä varten, tarvittaessa. Yrityksen nimi näkyy **Nimi**-kentässä, joka on **Yritystiedot**-kenttäryhmän alla. 

4. Voit tarkastella toimittajan tai asiakkaan arvioitavan kohteen luonnetta **Arvioitavan kohteen luonne** -kentässä, joka kuuluu **Ennakonpidätys**-kenttäryhmään. **Verotilin numero** (**TAN**) -kentässä tarkastele valitun yrityksen näkyvissä olevaa TAN-numeroa.  

5. Valitse **Ennakonpidätys** **Ennakonpidätys**-valikossa avataksesi **Väliaikaiset ennakonpidätystapahtumat** -sivun. Seuraavat kentät tulevat näkyviin tilapäisten **Väliaikaiset ennakonpidätystapahtumat** -sivun yläosassa.

   - **Ennakonpidätyksen summa yhteensä** - TDS-kokonaissumma, joka on laskettu tapahtumalle TDS-ryhmälle.

   - **Arvo** - Tapahtuman TDS:n laskemiseen käytettävä kokonaisprosentti. Kokonaisprosentti perustuu kaavaan, joka on määritetty TDS-ryhmään liitetyille TDS-verokoodeille.

   - **Oikaistu ennakonpidätyksen summa yhteensä** - Kaikkien TDS-ryhmän verokoodien oikaistu kokonaissumma.

   - **TDS** - Jos tämä on valittuna, tapahtumaan liittyy TDS-ryhmä.

  **Yhteenveto**-, **Yleinen**- ja **Oikaisu**-välilehtien kentissä **Väliaikaiset ennakonpidätystapahtumat** -sivulla näkyy laskettu TDS-summa ja oikaistun TDS-summan tiedot jokaiselle TDS-ryhmään liitetylle TDS-verokoodille.

6. Valitse **Raja** avataksesi **Raja**-sivun. Näytä tiettyyn TDS-verokoodiin tällä sivulla liitetylle TDS-verokomponentille määritetty raja-arvo ja poikkeusraja.

   Avaa **Kaavojen suunnittelutoiminto** avataksesi **Kaavojen suunnittelutoiminto** -lomakkeen. Tarkastele kaavaa, joka on määritetty tietylle TDS-verokoodille tällä sivulla. Sulje **Kaavan suunnittelutoiminto**- ja **Väliaikaiset ennakonpidätystapahtumat** -sivu palataksesi **Kirjaustosite**-sivulle.

8. Lisää muut pakolliset tiedot. Vahvista ja kirjaa kirjauskansio. Ostolaskuissa laskettu TDS-summa kirjataan ostoreskontratilille. Myyntilaskuissa laskettu TDS-summa kirjataan myyntireskontratilille, joka on määritetty kullekin TDS-verokoodille TDS-ryhmässä. TDS-verokoodien ostoreskontran tai myyntireskontran tilit määritetään **Ennakonpidätyskoodit**-sivulla.

9. Valitse **Kirjattu** **ennakonpidätys** avataksesi **Ennakonpidätystapahtumat**-sivun. Tapahtuman TDS:n laskemiseen käytetty kokonaisprosentti on näkyvissä **Arvo**-kentässä.

   **Yhteenveto**-, **Yleinen**- ja **Summa**-välilehtien kentissä Ennakonpidätystapahtumat-sivulla näkyy laskettu TDS-summa ja oikaistun TDS-summan tiedot jokaiselle TDS-ryhmään liitetylle TDS-verokoodille.
