---
title: Verokomponenttien määrittäminen TDS-verotyypille
description: Tässä aiheessa kuvataan, miten ennakonpidätyksen komponentit määritetään Vero vähennettynä lähteissä (TDS) -verotyypille. Se myös kertoo, miten määritetään kunkin TDS-komponentin TDS:n laskemiseen käytettävä raja.
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
ms.openlocfilehash: 9c86341f7528e2c85b813e4f825ae34f10680a9b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727114"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Verokomponenttien määrittäminen TDS-verotyypille

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan, miten ennakonpidätyksen komponentit määritetään Vero vähennettynä lähteissä (TDS) -verotyypille. TDS-komponentit ovat TDS, lisämaksu, PE-Cess ja SHE Cess. Aiheessa kerrotaan myös, miten määritetään kunkin TDS-komponentin TDS:n laskemiseen käytettävä raja. Voit myös määrittää poikkeusraja-arvon, jota käytetään kunkin TDS-komponentin TDS-laskennassa.

Määritä TDS-komponentit seuraavasti.

1. Siirry kohtaan **Vero \> Asetukset \> Ennakonpidätys \> Ennakonpidätyksen komponentit**.

    [![Ennakonpidätyksen komponentit -sivu.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. Valitse **Verotyyppi**-kentässä **TDS**, haluat määrittää ennakonpidätyksen komponentit TDS-verotyypille.
3. Valitse toimintoruudussa **Uusi** ja luo rivi.
4. Kirjoita **Ennakonpidätyksen komponentti** -kenttään TDS-komponentin nimi.
5. Valitse **Ennakonpidätyksen komponenttiryhmä** -kentässä TDS-ennakonpidätyksen komponenttiryhmä, jonne TDS-komponentti liitetään.
6. Kirjoita **Yleiset**-pikavälilehden **Kuvaus**-kenttään TDS-komponentin kuvaus.
7. Valitse toimintoruudusta **Raja** avataksesi **Raja**-sivun, jotta voit määrittää raja-arvon, jota käytetään TDS-komponentin TDS:n laskemiseen.
8. Määritä **Päivämäärästä**- ja **Päivämäärään**-kenttien avulla kausi, jota raja koskee.
9. Määritä **Yleinen**-pikavälilehden **Raja**-kenttään rajasumma, jota käytetään TDS-komponentin TDS:n laskemiseen. Vero vähennetään lähteestä vain, kun kumulatiivinen laskun summa ylittää rajan.

    Jos rajasumma on esimerkiksi 10 000, TDS lasketaan kun kumulatiivinen laskun summa ylittää 10 000 (eli kun se on 10 001 tai suurempi).

10. Määritä **Poikkeusraja-arvo**-kenttään poikkeusraja-arvon summa, jota käytetään TDS-komponentin TDS:n laskemiseen. Laskurivillä oleva vero vähennetään lähteestä vain, kun summa ylittää poikkeusraja-arvon.

    Jos poikkeusrajan summa on esimerkiksi 5 000, TDS lasketaan tietylle laskuriville, jos laskurivin summa ylittää 5 000 (toisin sanoen on 5 001 tai suurempi).

    [![Raja-arvo-sivu.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Poikkeusraja-arvon summan on oltava pienempi tai yhtä suuri kuin raja-arvon summa.
    >
    > Tapahtumalle vähennetään vero, jos tapahtuman summa ylittää poikkeusraja-arvon, vaikka kumulatiivinen laskun summa ei ylittää **Raja**-kentässä määritettyä rajaa.

11. Sulje **Raja**-sivu palataksesi **Ennakonpidätyksen komponentit** -sivulle.
12. Valitse toimintoruudussa **Kopioi** avataksesi **Kopioi ennakonpidätyksen komponentit** -valintaikkunan, jotta voit kopioida TDS-komponentit, jotka on määritetty yhdelle TDS-komponenttiryhmälle, toiseen TDS-komponenttiryhmään.
13. Valitse **Alkaen**-kentästä TDS-komponenttiryhmä, josta TDS-komponentit kopioidaan. Valitse **Asti**-kentässä ennakonpidätyksen komponenttiryhmä, jonne TDS-komponentit kopioidaan.

    > [!NOTE]
    > Yleisiä TDS-komponentteja, jotka on liitetty molempiin TDS-komponenttiryhmiin, ei kopioida.

14. Valitse **OK**, kun haluat kopioida ja luoda TDS-komponentit toiselle TDS-komponenttiryhmälle **Ennakonpidätyksen komponentit** -sivulla.

    [![Ennakonpidätyksen komponenttien kopioiminen -valintaikkuna.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Sulje sivu.
