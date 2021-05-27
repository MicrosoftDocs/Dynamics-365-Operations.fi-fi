---
title: TDS-laskujen laskeminen ostotilauslomakkeen ja myyntitilauslomakkeen avulla
description: Tässä aiheessa luetellaan erityyppisten laskujen vaiheet Vero vähennettynä lähteissä (TDS) -arvon laskemiseksi.
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
ms.openlocfilehash: e7925206f3c060c6332de9d4972c8a7fb0066be2
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023198"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>TDS-laskujen laskeminen ostotilauslomakkeen ja myyntitilauslomakkeen avulla

[!include [banner](../includes/banner.md)]

Tässä aiheessa luetellaan vaiheet, joilla lasketaan Vero vähennettynä lähteissä (TDS) erilaisissa laskuissa **Ostotilaus**-, **Ostokirjauskansio**-, **Yleistilaus**- ja **Myyntitilaus**-sivuilla.

1. Luo ostotilaus, ostokirjauskansio, oston yleistilaus tai myyntitilaus käyttämällä luettelosivua. Kirjoita tarvittavat tiedot.

2. Valitse **Asetukset**-välilehti, jos haluat tarkastella toimittajan tai asiakkaan arvioitavan kohteen luonnetta. Nämä tiedot on lueteltu **Arvioitavan kohteen luonne** -kentässä **Ennakonpidätysryhmä**-kenttäryhmässä.

3. **TDS-ryhmä**-kentässä tarkastele tai muokkaa TDS-ryhmän oletusryhmää, joka on määritetty toimittajalle tai asiakkaalle.

   > [!NOTE]
   > **TCS-ryhmä**-kenttä ei ole käytettävissä, kun valitset TDS-ryhmän **TDS-ryhmä**-kentässä. TDS lasketaan vain, jos **Laske ennakonpidätys** -valintaruutu on valittuna toimittajalle tai asiakkaalle **Kaikki toimittajat**- tai **Kaikki asiakkaat** -sivulla.  

4. Luo nimikerivit **Rivit**-välilehdessä ja syötä tarvittavat tiedot.

5. Valitse **Asetukset**-välilehti (rivitaso), jos haluat tarkastella tai muuttaa otsikon tasolla määritettyä TDS-ryhmää. TDS-ryhmä näkyy **TDS-ryhmä**-kentässä, joka on **Ennakonpidätysryhmä**-kenttäryhmässä.

6. Valitse **Verotiedot**-välilehti ja valitse vaihtoehtoiset osoitteet, jotka on määritetty tässä kentässä näkyvää yrityksen nimeä varten. Yrityksen nimi näkyy **Nimi**-kentässä, joka on **Yritystiedot**-kenttäryhmän alla. 

   Valitun yrityksen verotilin numero (TAN) näkyy **Verotilin numero** (**TAN**) -kentässä **Ennakonpidätys**-kenttäryhmässä. 

7. Valitse **Ennakonpidätys** avataksesi **Väliaikaiset ennakonpidätystapahtumat** -sivun. Tarkastele seuraavia kenttiä tilapäisten **Väliaikaiset ennakonpidätystapahtumat** -sivun yläosassa.

   - **Ennakonpidätyksen** **summa** **yhteensä** - TDS-kokonaissumma, joka on laskettu tapahtumalle TDS-ryhmälle.

   - **Arvo** - Tapahtuman TDS:n laskemiseen käytettävä kokonaisprosentti. Kokonaisprosentti perustuu kaavaan, joka on määritetty TDS-ryhmään liitetyille TDS-verokoodeille.

   - **Oikaistu ennakonpidätyksen summa yhteensä** - Kaikkien TDS-ryhmän verokoodien oikaistu kokonaissumma.

   - **TDS** - Jos tämä on valittuna, tapahtumaan liittyy TDS-ryhmä.

**Yhteenveto**-, **Yleinen**- ja **Oikaisu**-välilehtien kentissä **Väliaikaiset ennakonpidätystapahtumat** -sivulla näkyy laskettu TDS-summa ja oikaistun TDS-summan tiedot jokaiselle TDS-ryhmään liitetylle TDS-verokoodille.

8. Valitse **Raja** avataksesi **Raja**-sivun. Näytä tiettyyn TDS-verokoodiin tällä sivulla liitetylle TDS-verokomponentille määritetty raja-arvo.

9. Avaa **Kaavojen suunnittelutoiminto** avataksesi **Kaavojen suunnittelutoiminto** -sivun. Tarkastele kaavaa, joka on määritetty tietylle TDS-verokoodille tällä sivulla. 

10. Kirjaa lasku. Ostolaskuissa laskettu TDS- summa kirjataan ostoreskontratilille ja myyntilaskuissa laskettu TDS-summa kirjataan myyntireskontratilille, joka on määritetty kullekin TDS-ryhmän TDS-verokoodille. TDS-verokoodien ostoreskontran tai myyntireskontran tilit määritetään **Ennakonpidätyskoodit**-sivulla.

11. Valitse **Kysely**-painike **> Lasku > Kirjattu ennakonpidätys** -painike avataksesi **Ennakonpidätystapahtumat**-sivun. Voit tarkastella tapahtuman TDS:n laskemiseen käytettyä kokonaisprosenttia **Arvo**-kentässä.

**Yhteenveto**-, **Yleinen**- ja **Summa**-välilehtien kentissä **Ennakonpidätystapahtumat**-sivulla näkyvät tapahtumalle lasketun TDS:n tiedot. Näytä kunkin TDS-ryhmään liitetyn TDS-verokoodin TDS-laskentatiedot.
