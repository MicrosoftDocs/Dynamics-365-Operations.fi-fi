---
title: Liitä TDS-verokoodit TDS-veroryhmiin ja määritä TDS:n laskentakaava
description: Tässä ohjeaiheessa on tietoja siitä, miten määritetään Vero vähennettynä lähteissä (TDS) -veroryhmät ja liitetään TDS-verokoodeja TDS-veroryhmiin. TDS-veroryhmän TDS:n laskemiseksi on määritettävä kaava siihen liitetyille TDS-verokoodeille.
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
ms.openlocfilehash: 81aac53cca91a75cde811c314bd6f7039852d32505fe6540921e17f3d1bbc7ad
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739307"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>Liitä TDS-verokoodit TDS-veroryhmiin ja määritä TDS:n laskentakaava

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja siitä, miten määritetään Vero vähennettynä lähteissä (TDS) -veroryhmät ja liitetään TDS-verokoodeja TDS-veroryhmiin. TDS-veroryhmän TDS:n laskemiseksi on määritettävä kaava siihen liitetyille TDS-verokoodeille.

Seuraavia ohjeita noudattamalla voit määrittää TDS-veroryhmän, liittää siihen TDS-verokoodit ja määrittää TDS:n laskentakaavan.

1. Siirry kohtaan **Vero \> Välilliset verot \> Ennakonpidätys \> Ennakonpidätysryhmät**.

    [![Ennakonpidätysryhmät-sivu.](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. Valitse toimintoruudusta **Uusi**, jos haluat luoda TDS:lle ennakonpidätysryhmän, ja syötä tarvittavat tiedot.
3. Valitse **Verotyyppi**-kentästä **TDS**.
4. Luo rivi valitsemalla **Asetukset**-pikavälilehdellä **Lisää**.
5. Valitse **Ennakonpidätyskoodi**-kentässä TDS-verokoodi TDS-veroryhmälle. **Ennakonpidätyksen nimi** -kentässä näkyy TDS-verokoodin nimi, ja **Arvo**-kenttä näyttää arvon.
6. Jos haluat ohittaa TDS-tapahtumissa TDS-verokoodiin liitetylle TDS-verokomponentille määritetyn raja- ja poikkeusrajan, valitse **Ohita raja** -valintaruutu.
7. Valitse **Veroton**-valintaruutu, jos haluat estää veroryhmän laskemisen tapahtumissa.
8. Avaa kaavan suunnittelutoiminto valitsemalla toimintoruudusta **Suunnittelutoiminto**, jotta voit määrittää kaavan TDS:n laskemiseksi TDS-veroryhmälle. **Suunnittelutoiminto**-sivulla **Verot**-välilehdessä näkyvät TDS-verokoodit, jotka on valittu TDS-veroryhmälle.

    [![Suunnittelutoiminto-sivu.](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. Luo rivi valitsemalla **Laskelma**-välilehdessä **Alt+N**. **Tunnus**-kentässä näkyy automaattisesti luotu TDS-laskennan prioriteettitunnus.
10. Valitse **Verokoodi**-kentässä TDS-verokoodi, jolle kaava määritetään. Kaikki TDS-verokoodit, jotka on valittu TDS-veroryhmälle, ovat valittavissa tässä kentässä.
11. Valitse **Veron peruste** -kentässä TDS-laskennan peruste:

    - **Bruttosumma** – Laske TDS-arvo tapahtuman bruttosumman perusteella (laskun summa) verokoodille määritetyn laskentalausekkeen avulla.
    - **Ilman bruttosummaa** – Laske TDS verokoodille määritetyn laskentalausekkeen perusteella.

    > [!NOTE]
    > **Veron peruste** -kentän arvoksi ei voi määrittää **Ilman bruttosummaa** TDS-verokoodille, jonka prioriteettitunnus on **1**.

12. TDS-laskenta perustuu kaavaan, joka on määritetty **Laskelmalauseke**-kentässä jokaiselle TDS-veroryhmään liitetylle verokoodille. Valitse plusmerkki- (**+**), miinusmerkki- (**-**), kertomerkki- (**\**_) tai jakomerkki (_*/**) -painike syöttääksesi laskemalausekkeen valitulle TDS-verokoodille **Laskelmalauseke**-kentässä.

    > [!NOTE]
    > TDS-verokoodille, jonka prioriteettitunnus on **1**, ei voida määrittää laskelmalauseketta.

13. Voit määrittää TDS-verokoodin laskelmalausekkeen **Laskelmalauseke**-kentässä lisäämällä **Verot**-välilehdessä käytettävissä olevat TDS-verokoodit. Voit lisätä TDS-verokoodeja **Laskelmalauseke**-kentässä seuraavilla tavoilla:

    - Vedä tarvittava verokoodi **Verot**-välilehdestä **Laskelmalauseke**-kenttään.
    - Kaksoisnapauta (tai kaksoisnapsauta) vaadittua verokoodia **Verot**-välilehdessä.
    - Valitse ja pidä valittuna tarvittavaa verokoodia (tai paina hiiren kakkospainikkeella) **Verot**-välilehdessä ja valitse sitten **Lisää verokoodi**.

    > [!NOTE]
    > Lisää laskelmalauseke ennen jokaista TDS-verokoodia. Laskentakaavaan lisätyt TDS-verokoodit näkyvät hakasulkeissa (\[...\]).

14. Voit poistaa verokoodille **Laskentalauseke**-kentässä määritetyn laskentalausekkeen valitsemalla **C**-painikkeen.
15. Jos haluat poistaa tietueen **Laskelma**-välilehdessä, valitse **Poista**.
16. Sulje sivu.
