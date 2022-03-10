---
title: Maksujen ja velkakirjojen TDS-laskenta
description: Tässä ohjeaiheessa on viitetietoja erilaisista maksutapahtumista, joiden perusteella Vero vähennettynä lähteissä (TDS) lasketaan.
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
ms.openlocfilehash: 28afd04b1c341985f7ac15e05aba7a9039a59d869dd5bc60b4163d2ba1ae4ec0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750337"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>Maksujen ja velkakirjojen TDS-laskenta

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on viitetietoja erilaisista maksutapahtumista, joiden perusteella Vero vähennettynä lähteissä (TDS) lasketaan.

| Sarjanumero | Tapahtumatyyppi | Tapahtuman summa | Sivun nimi ja polku | Tilin tyyppi ja vastatilin tyyppi |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Ennakkomaksu / Maksu laskua vastaan (TDS-ostoreskontra) | Debet tai Kredit | <ul><li>Yleinen kirjauskansio (**Kirjanpito \> Kirjauskansioviennit \> Yleiset kirjauskansiot**)</li><li>Laskun kirjauskansio (**Ostoreskontra \> Laskut \> Laskun kirjauskansio**)</li><li>Maksukirjauskansio (**Ostoreskontra \> Maksut \> Toimittajan maksukirjauskansio**)</li></ul> | Toimittaja (Dr.), Pankki (Cr.) |
| 2             | Ennakkomaksu / Maksu laskua vastaan (Asiakkaalta tehdyt ostot – TDS-ostoreskontra) | Debet tai Kredit | <ul><li>Yleinen kirjauskansio (**Kirjanpito \> Kirjauskansioviennit \> Yleiset kirjauskansiot**)</li><li>Laskun kirjauskansio (**Ostoreskontra \> Laskut \> Laskun kirjauskansio**)</li><li>Maksukirjauskansio (**Ostoreskontra \> Maksut \> Toimittajan maksukirjauskansio**)</li></ul> | Asiakas (Dr.), Pankki (Cr.) |
| 3             | Velkakirjat | Veloitus | Aseta velkakirjakirjauskansio (**Ostoreskontra \> Maksut \> Velkakirjat \> Aseta velkakirjakirjauskansio**) | Toimittaja (Dr.), Kirjanpito (Cr.) |
| 4             | Muut tulot (TDS-myyntireskontra) | Debet tai Kredit | Yleinen kirjauskansio (**Kirjanpito \> Kirjauskansioviennit \> Yleiset kirjauskansiot**) | Pankki (Dr.), Kirjanpito (Cr.) |
| 5             | Muut kulut (TDS-ostoreskontra) | Debet tai Kredit | Yleinen kirjauskansio (**Kirjanpito \> Kirjauskansioviennit \> Yleiset kirjauskansiot**) | Pankki (Dr.), Kirjanpito (Cr.) |

Noudattamalla näitä ohjeita voit laskea maksujen ja velkakirjojen TDS:n.

1. Luo kirjauskansion rivit kirjauskansiosivuille. Valitse tilin tyyppi ja vastatilin tyyppi.
2. Valitse **Toiminnot \> Tilitys** avataksesi **Avoimen tapahtuman muokkaus** -sivun. Valitse sitten tietty tilitettävä lasku. Jos laskutuksen tasolla on jo laskettu TDS, **Summan alkuperä** -kentässä näkyy perussumma, jolle TDS laskettiin. **TDS-summa** -kentässä näkyy tapahtumalle laskettu TDS-summa. **Summa**-kentässä näkyy nettomaksusumma (maksun summa sen jälkeen, kun TDS on vähennetty).

    > [!NOTE]
    > Laskua vastaan tehtyä maksua koskevat seuraavat ehdot:
    >
    > - Jos maksun summa ja laskun summa ovat samat, TDS:ää ei lasketa, jos se on jo laskettu laskun tasolla.
    > - Jos laskun summa TDS-summan vähennyksen jälkeen on enemmän kuin maksun summa, TDS:ää ei lasketa.
    > - Jos laskun summa TDS-summan vähennyksen jälkeen on pienempi kuin maksun summa, TDS lasketaan laskun summan ylittävälle summalle.

3. **Kirjaustosite**-sivulla **Yhteenveto**-välilehdessä **TDS-ryhmät**-kentässä tarkastele tai muuta toimittajalle tai asiakkaalle määritettyä oletusarvoista TDS-ryhmää. Kirjauskansion riveille laskettu TDS perustuu TDS-ryhmässä TDS-verokoodeille määritettyyn kaavaan.

    > [!NOTE]
    > TDS lasketaan vain, jos **Laske ennakonpidätys** -vaihtoehdon asetuksena on **Kyllä** toimittajalle **Toimittajat**-sivulla.

4. Valitse **Verotiedot**-välilehden **Yritystiedot**-osan **Nimi**-kentästä yritykselle määritettävien vaihtoehtoisten osoitteiden yrityksen nimi.

    Voit tarkastella toimittajan tai asiakkaan arvioitavan kohteen luonnetta **Ennakonpidätysryhmä**-osiossa **Arvioitavan kohteen luonne** -kentässä. **Verotilin numero (TAN)** -kentässä näkyy valitun yrityksen verotilin numero (TAN).

5. Valitse **Ennakonpidätys-painike \> ennakonpidätys** avataksesi **Väliaikaiset ennakonpidätystapahtumat** -sivun. Sivun yläosassa on seuraavat kentät:

    - **Ennakonpidätyksen summa yhteensä** – TDS-kokonaissumma, joka on laskettu tapahtumalle TDS-ryhmälle.
    - **Arvo** – Tapahtuman TDS:n laskemiseen käytettävä kokonaisprosentti. Kokonaisprosentti perustuu kaavaan, joka on määritetty TDS-verokoodeille ja liitetty TDS-ryhmään.
    - **Oikaistu ennakonpidätyksen summa yhteensä** – Kaikkien TDS-ryhmän verokoodien oikaistu kokonaissumma.
    - **TDS** – Valittu valintaruutu ilmaisee, että tapahtumaan on liitetty TDS-ryhmä.

    **Yhteenveto**-, **Yleinen**- ja **Oikaisu**-välilehdissä näkyy laskettu TDS-summa ja oikaistun TDS-summan tiedot jokaiselle TDS-ryhmään liitetylle TDS-verokoodille.

6. Valitse **Raja** avataksesi **Raja**-sivun, jolla voit tarkistaa tiettyyn TDS-verokoodiin liitetylle TDS-verokomponentille määritetyn raja-arvon.
7. Valitse **Kaavan suunnittelutoiminto** avataksesi **Kaavan suunnittelutoiminto** -sivun, jossa voit tarkistaa tietylle TDS-verokoodille määritetyn kaavan.
8. Sulje **Kaavan suunnittelutoiminto**- ja **Väliaikaiset ennakonpidätystapahtumat** -sivu palataksesi **Kirjaustosite**-sivulle.
9. Vahvista ja kirjaa kirjauskansio. Laskettu TDS-summa kirjataan ostoreskontratilille, joka on määritetty kullekin TDS-verokoodille TDS-ryhmässä. TDS-verokoodien myyntireskontran tilit määritetään **Ennakonpidätyskoodit**-sivulla.
10. Valitse **Kirjattu ennakonpidätys** avataksesi **Ennakonpidätystapahtumat**-sivun. **Arvo**-kenttä näyttää tapahtuman TDS:n laskemiseen käytettävän kokonaisprosentin.

    **Yhteenveto**-, **Yleinen**- ja **Summa**-välilehtien kentissä näkyvät tapahtumaan liitetylle TDS-ryhmälle lasketut TDS-summat.

11. Tarkastele kunkin TDS-ryhmään liitetyn TDS-verokoodin TDS-laskentatietoja.

## <a name="generate-payments"></a>Muodosta maksut

Luo maksuja noudattamalla seuraavia ohjeita.

1. Noudata seuraavia ohjeita:

    - Valitse **Ostoreskontra \> Maksut \> Toimittajan maksukirjauskansio**.
    - Valitse **Myyntireskontra \> Maksut \> Asiakkaan maksukirjauskansio**.
    - Valitse **Ostoreskontra \> Maksut \> Velkakirjat \> Aseta velkakirjakirjauskansio**.
    - Valitse **Myyntireskontra \> Maksut \> Vekseli \> Aseta vekselikirjauskansio**.
    - Valitse **Myyntireskontra \> Maksut \> Vekseli \> Tarkista vekselikirjauskansio**.

2. Valitse **Rivit**.
3. Valitse **Toiminnot \> Muodosta maksut**.
