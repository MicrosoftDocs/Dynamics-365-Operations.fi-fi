---
title: Vapaatekstilasku-sivun laskujen TDS-laskenta
description: Tässä artikkelissa kerrotaan, miten laskujen Vero vähennettynä lähteissä (TDS) lasketaan vapaatekstilaskusivua käyttäen.
author: kailiang
ms.date: 02/12/2021
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
ms.openlocfilehash: b1cf0f5366315884e75a6fee25b88a3aac7d62de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856608"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>Vapaatekstilasku-sivun laskujen TDS-laskenta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten laskujen Vero vähennettynä lähteissä (TDS) lasketaan **Vapaatekstilasku**-sivua käyttäen.

1. Siirry kohtaan **Myyntireskontra \> Laskut \> Kaikki vapaatekstilaskut**.

    [![Vapaatekstilaskun sivu.](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Luo vapaatekstilasku valitsemalla **Uusi** ja kirjoita tarvittavat tiedot.
3. Valitse **Lasku**-välilehti. **Ennakonpidätysryhmä**-osiossa **Arvioitavan kohteen luonne** -kentässä näkyy asiakkaan arvioitavan kohteen luonteen luokka.
4. **TDS-ryhmä**-kentässä tarkastele tai muuta TDS-ryhmän oletusryhmää, joka on määritetty asiakkaalle.

    > [!NOTE]
    > Kun valitset arvon **TDS-ryhmä**-kentässä, **TCS-ryhmä**-kenttä ei ole enää käytettävissä. TDS lasketaan vain, jos **Laske ennakonpidätys** -vaihtoehdon asetuksena on **Kyllä** asiakkaalle **Kaikki asiakkaat** -sivulla.

5. Valitse **Verotiedot**-välilehden **Yritystiedot**-osan **Nimi**-kentästä yritykselle määritettävän vaihtoehtoisen osoitteen yrityksen nimi.

    **Ennakonpidätys**-osassa **Verotilin numero (TAN)** -kentässä näkyy valitun yrityksen verotilin numero (TAN).

6. Luo laskurivit **Laskurivit**-välilehdessä ja syötä tarvittavat tiedot.

    **Ennakonpidätysryhmä**-osiossa **Verotilin numero (TAN)** -kentässä näkyy TAN, ja **TDS-ryhmä**-kentässä näkyy TDS-ryhmä.

7. Valitse **Ennakonpidätys** avataksesi **Väliaikaiset ennakonpidätystapahtumat** -sivun. Sivun yläosassa on seuraavat kentät:

    - **Ennakonpidätyksen summa yhteensä** – TDS-kokonaissumma, joka on laskettu tapahtumalle TDS-ryhmälle.
    - **Arvo** – Tapahtuman TDS:n laskemiseen käytettävä kokonaisprosentti. Kokonaisprosentti perustuu kaavaan, joka on määritetty TDS-verokoodeille ja liitetty TDS-ryhmään.
    - **Oikaistu ennakonpidätyksen summa yhteensä** – Kaikkien TDS-ryhmän verokoodien oikaistu kokonaissumma.
    - **TDS** – Valittu valintaruutu ilmaisee, että tapahtumaan on liitetty TDS-ryhmä.

    **Yhteenveto**-, **Yleinen**- ja **Oikaisu**-välilehdissä näkyy laskettu TDS-summa ja oikaistun TDS-summan tiedot jokaiselle TDS-ryhmään liitetylle TDS-verokoodille.

8. Valitse **Raja** avataksesi **Raja**-sivun, jolla voit tarkistaa tiettyyn TDS-verokoodiin liitetylle TDS-verokomponentille määritetyn raja-arvon.
9. Valitse **Kaavan suunnittelutoiminto** avataksesi **Kaavan suunnittelutoiminto** -sivun, jossa voit tarkistaa tietylle TDS-verokoodille määritetyn kaavan.
10. Kirjaa vapaatekstilasku. Vapaatekstilaskulle laskettu TDS-summa kirjataan myyntireskontratilille, joka on määritetty kullekin TDS-verokoodille TDS-ryhmässä. TDS-verokoodien myyntireskontran tilit määritetään **Ennakonpidätyskoodit**-sivulla.
11. Valitse **Kirjattu ennakonpidätys** avataksesi **Ennakonpidätystapahtumat**-sivun. **Arvo**-kenttä näyttää tapahtuman TDS:n laskemiseen käytettävän kokonaisprosentin.

    **Yhteenveto**-, **Yleinen**- ja **Summa**-välilehtien kentissä on näkyvissä laskuriveille lasketut TDS-summat.

12. Tarkastele kunkin TDS-ryhmään liitetyn TDS-verokoodin TDS-laskentatietoja.
