---
title: TDS-maksujen tilitys TDS-viranomaistoimittajille ja TDS:n challan-tietojen luominen
description: Tässä aiheessa kerrotaan, miten TDS-maksut tilitetään TDS-viranomaistoimittajille.
author: kailiang
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: e9dcf2e9d5fc1a1f9eae9d93050b0831bd42f78c
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725536"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>TDS-maksujen tilitys TDS-viranomaistoimittajille ja TDS:n challan-tietojen luominen

[!include [banner](../includes/banner.md)]

Tässä aiheessa kerrotaan, miten TDS-maksut tilitetään TDS-viranomaistoimittajille.

1. Valitse **Ostoreskontra \> Maksut \> Toimittajan maksukirjauskansio**.

    [![Toimittajan maksukirjauskansio -sivu.](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. Valitse **Toimittajan maksukirjauskansio** -sivulla **Uusi** luodaksesi kirjauskansion rivin.
3. Valitse **Tili**-kentässä TDS-viranomaistoimittaja, jolle tilitetään TDS-maksut.
4. Valitse **Tilitystapahtumat** avataksesi **Tilitystapahtumat**-sivun, jolla voit tarkastella TDS-viranomaistoimittajan tilitettyjä TDS-tapahtumia.

    Tilityskauden tilitetyt TDS-tapahtumat näytetään seuraavasti:

    - TDS-tapahtumat, joissa arvioinnin kohteen luokka on **Yritys**, näkyy yhtenä tapahtumarivinä.
    - TDS-tapahtumat, joiden arvioitavan kohteen luonne on **HUF**, **Firma**, **Yksittäinen**, **AOP**, **BOI**, **Paikallinen viranomainen** tai **Muut**, näkyvät yhtenä tapahtumarivinä.
    - **Summa**-kentässä näkyy TDS-kokonaissumma, joka on maksettava TDS-viranomaistoimittajalle.

5. Valitsemalla **Ennakonpidätystapahtumat** voit tarkastella eri TDS-tapahtumia, jotka sisältyvät tilitystietueeseen. Voit tarkastella kunkin TDS-tapahtuman jakoa, joka on sisällytetty tilityskauden tilitysprosessiin tällä sivulla.
6. Valitse **Yhteenveto**-välilehdestä **Merkitse**-valintaruutu TDS-tapahtumille, jotka tilitetään TDS-viranomaistoimittajalle.

    **Yhteenveto**-sivulla näkyvät seuraavat tiedot kutakin avointa TDS-tapahtumaa varten:

    - **Päivämäärä** – TDS-tapahtumapäivä.
    - **Tosite** – Tositteen numero.
    - **Lähde** – Moduuli, josse TDS-tapahtuma kirjataan.
    - **Toimittaja/asiakas** – Toimittajan tai asiakkaan tilinumero, josta TDS vähennetään.
    - **Vähennyksen saajan/osapuolen nimi** – Toimittajan tai asiakkaan nimi, joilta TDS vähennetään.
    - **Arvioitavan kohteen luonne** – Sen arvioitavan kohteen luokan luonne, johon vähennyksen saaja kuuluu.
    - **Summa** – Laskun summa, jonka perusteella TDS laskettiin.
    - **Veron summa** – Tapahtumalle laskettu TDS-summa.

    > [!NOTE]
    > Poista niiden TDS-tapahtumien **Merkitse**-valintaruudun valinta, joita ei pitäisi selvittää TDS-viranomaistoimittajalle.

    **Yleinen**-välilehden **PAN**-kentässä näkyy vähennyksen saajan pysyvä tilinumero (PAN). **Päivämäärä**-kentässä näkyy TDS-laskelman päivämäärä, ja **Arvo**-kentässä näkyy TDS-laskennassa käytetty kokonaisprosentti.

7. Valitsemalla **Tosite** voit tarkastella TDS-tapahtuman tositemerkintöjä.
8. Sulje sivu.
10. Avaa **Ennakonpidätyksen komponentit** -sivu valitsemalla **Ennakonpidätyksen komponentit**. Sivulla voit tarkastella TDS-verokomponenttia kohti laskettua TDS:ää tietylle TDS-verokoodille.

    **Yhteenveto**-välilehden **Verokomponentti**-kentässä näkyy tapahtumassa käytetty TDS-verokomponentti. **Summa**-kentässä näkyy TDS-summa, joka on laskettu TDS-verokomponentille perusvaluuttana. **Kertynyt summa** -kentässä näkyy TDS-kokonaissumma, joka on laskettu kaikkien tilitettyjen tapahtumien TDS-komponentille.

    **Summa**-välilehden **Oletusvaluutta**-osassa näkyy TDS-verokomponentille laskettu TDS-veron summa oletusvaluuttana. **Toissijainen valuutta** -osassa summa esitetään toissijaisena valuuttana.

11. Sulje **Ennakonpidätyksen komponentit** -sivu.
12. Huomaa **Avoimen tapahtuman muokkaus** -sivulla **Summa**-kentäss, että TDS-viranomaistoimittajalle tilitettävä kokonaissumma tilityskaudelta päivitetään.
13. Jos haluat selvittää eri TDS-tilityskausien TDS-tapahtumat TDS-viranomaistoimittajalle, valitse tapahtumien **Merkitse**-valintaruutu.
14. Sulje **Avoimen tapahtuman muokkaus** -sivu.

    > [!NOTE]
    > Jos **Ennakonpidätystapahtumat**-sivulla on valittu tilitystä varten vain muutamia tapahtumia, valittujen tapahtumien TDS-kokonaissumma päivitetään **Korjaus**-kentässä **Avoimen tapahtuman muokkaus** -sivulla. Korjaussumma päivitetään **Kirjaustosite**-sivun kirjauskansion rivillä, ja **Avoimen tapahtuman muokkaus** -sivu suljetaan.

    **Kirjaustosite**-sivulla **Veloitus**-kentässä näkyy kokonaissumma, joka maksetaan TDS-viranomaiselle.

15. Kirjoita vastatilin tiedot.

    > [!NOTE]
    > Jos TDS-tapahtumilla on eri TAN-numerot, **Kirjaustosite**-sivulle luodaan kirjauskansion rivit TAN-numeroa kohden.

16. Valitse **Toimitusmaksu**-välilehden **Maksutunnus**-kentästä maksun tunnus, jonka maksutyyppi on **Korko** tai **Muut**, jos haluat veloittaa toimitusmaksun TDS-viranomaistoimittajalle suoritetuista viivästyneistä maksuista.

    **Verotiedot**-välilehden **Yritystiedot**-osassa **Nimi**-kentässä näkyy yrityksen nimi. **Ennakonpidätys**-osassa **Verotilin numero (TAN)** -kentässä näkyy tapahtumariviin liittyvä TAN.

17. Vahvista ja kirjaa kirjauskansio.
18. Valitse **Ennakonpidätys \> Challan-tiedot** syöttääksesi tapahtuman challan-tiedot.

    **Tosite**-kentässä näkyy tapahtuman tositenumero.
    
19. Valitse **Kirjamerkinnän avulla talletettu TDS** -valintaruutu, jos TDS-summa talletetaan kirjamerkinnän avulla.
20. Kirjoita **Challan-numero**-kenttään challan-numero, jota käytetään maksun suorittamiseen TDS-viranomaistoimittajalle.
21. Syötä **Päivämäärä**-kenttään challan-päivämäärä.
22. Valitse **Pankin nimi** -kentässä sen pankin nimi, jonne TDS-viranomaistoimittajalle maksettava TDS-summa talletetaan. Tässä kentässä luetellaan kaikki pankkitilit, jotka on määritetty TDS-viranomaistoimittajalle kohdassa **Ostoreskontra \> Kaikki toimittajat \> Asetukset \> Pankkitilit**.
23. Syötä **BSR-koodi**-kenttään pankin Basic Statistical Return (BSR) -koodi.
24. Sulje sivu.

### <a name="example"></a>Esimerkki

Kausi 1.4.2009 selvitetään **Vuokra**-TDS-komponenttiryhmälle käyttämällä kausittaista TDS-selvitysprosessia. TDS-kokonaissumma 141 625,00 kirjataan TDS-toimittajaviranomaisen tilille TDS-tilityskaudelta. Voit tarkastella tätä summaa TDS-viranomaistoimittajan **Avoimen tapahtuman muokkaus** -sivun **Summa**-kentässä.

Jos valitset **Ennakonpidätystapahtumat** tarkastellaksesi kauden tilitettyjä TDS-tapahtumia, seuraavat tiedot ovat näkyvissä.

| TDS-summa |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

Tietyn TDS-summan kohdalla voit valita **Ennakonpidätyksen komponentit** tarkastellaksesi TDS-verokomponenttia kohti laskettua TDS:ää tietylle TDS-verokoodille. Tässä esimerkissä valitaan **Ennakonpidätyksen komponentit** TDS-summalle 16 995,00. Tapahtumalle komponenttikohtaisesti laskettu veron summa näytetään.

| Verokomponentti | Määrä    | Kumulatiivinen summa |
|---------------|-----------|--------------------|
| TDS           | 1,5000.00 | 125,000.00         |
| Lisämaksu     | 1,500.00  | 12,500.00          |
| PE-Cess       | 330.00    | 2,750.00           |
| SHE Cess      | 165.00    | 1,375.00           |

Jos valitse vain TDS-summat 16 995,00, 22 660,00 ja 2 8325,00 tilitykselle **Ennakonpidätystapahtumat**-sivulla, tilityksen kokonaissumma näkyy muodossa **67 980,00** **Korjaus**-kentässä **Avoimen tapahtuman muokkaus** -sivulla. Jos tämä tapahtuma on merkitty tilitystä varten ja **Avoimen tapahtuman muokkaus** -sivu on suljettu, summa **67 980,00** näkyy **Veloitus**-kentässä **Kirjaustosite**-sivulla.

Voit nyt kirjata kirjauskansion ja luoda TDS-challan-numeron.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>TDS-viranomaistoimittajille tehtyjen ennakkomaksujen oikaisu

Voit oikaista TDS-viranomaistoimittajalle maksetun ennakkomaksun todelliseksi maksuksi valitsemalla **Ostoreskontra \> Toimittajat \> Kaikki toimittajat \> Tapahtumien muokkaus**. Jos todellinen tehty maksu ylittää ennakkomaksun, tapahtumalle luodaan kaksi challan-numeroa. TDS-kyselyssä näkyy kuitenkin vain ensimmäinen challan-numero.
