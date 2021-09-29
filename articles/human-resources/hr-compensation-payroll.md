---
title: Valmis maksettavaksi
description: Tässä ohjeaiheessa esitetään, miten työntekijä merkitään maksuvalmiiksi Dynamics 365 Human Resourcesissa.
author: marcelbf
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 80bba5446eb7a87d96a7da4ae856cb5ca114ce52
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2021
ms.locfileid: "7483779"
---
# <a name="ready-to-pay"></a>Valmis maksettavaksi

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

> [!NOTE]
> Jos haluat merkitä työntekijän maksuvalmiiksi, sinun on ensin otettava käyttöön **Palkanlaskennan integrointitoiminto (esiversio)** ominaisuuksien hallinnassa. Lisätietoja esiversiotoimintojen käyttöönotosta on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

Tämän ominaisuuden avulla henkilöstöhallinnon ammattilaiset voivat ymmärtää, mitkä työntekijät ovat valmiita palkanlaskennan käsittelyyn ja mitkä vaativat toimia ennen kuin kolmannen osapuolen palkanlaskentapalvelu kuluttaa ne.

## <a name="mark-employee-as-ready-to-pay"></a>Merkitse työntekijä maksuvalmiiksi

Työntekijätietojen kerääminen ja vahvistaminen voi olla aikaa vievää ja virheille altista. Tarjoamalla henkilöstöhallinnon ammattilaisille tavan tarkastella ja päivittää helposti työntekijöiden tietoja, Dynamics 365 Human Resources auttaa lyhentämään palkanlaskennan prosessiin valmistautumista.

Toimi näin, kun haluat merkitä työntekijän maksuvalmiiksi:

1. Avaa **Kompensaation hallinta**. Työtilassa on kaksi ruutua: 
    - **Työntekijät, jotka ovat valmiita maksamaan**
    - **Työntekijät eivät ole maksuvalmiita**
    ![Kompensaation hallinnan työtila.](./media/hr-ready-to-pay-1-workspace.png)

2. Valitse **Työntekijät eivät ole maksuvalmiita** -ruutu.

3. Valitse vahvistettavat työntekijät. Valitse **Palkanlaskenta**-välilehden **Maksuvalmis** -ryhmästä **Vahvista** .
    ![Työntekijöiden vahvistaminen.](./media/hr-ready-to-pay-2-validate.png)

4. Voit tarkastella tuloksia valitsemalla **Palkanlaskenta**-välilehden **Maksuvalmis** -ryhmästä **Tulokset** .

## <a name="validation"></a>Valintasäännöt

Ennen kuin työntekijä merkitään maksuvalmiiksi, järjestelmä tekee profiilin täydellisyyden tarkistuksen.

![Tulosten tarkistaminen.](./media/hr-ready-to-pay-3-results.png)

| Valintasäännöt | Lisätietoja |
| --- | --- |
| **Osoitteen tarkoituksen parametri** | Vahvistaa, onko parametri **Käytä palkanlaskentaosoitteiden tarkoitusta** valittuna. |
| **Palkanlaskennan osoite** | Vahvistaa, onko työntekijäprofiililla vähintään yksi osoite, jonka tarkoitus on **Palkanlaskennan sijainti** tai **Palkanlaskennan työsijainti**, ja tarkoitusta kohden on vain yksi osoite. |
| **Työsuhde** | Vahvistaa, onko työntekijällä vähintään yksi työsuhde (nykyinen, edellinen tai tuleva). |
| **Tunnusnumero** | Vahvistaa, onko **Käytä tunnustyyppejä palkanlaskennan käsittelyssä** -kentässä **Kyllä** **Henkilöstöhallintoparametrit**-sivulla, ja onko parametrissa ilmoitettu tunnustyyppi täytetty työntekijäprofiilissa. |
| **Etu- ja sukunimi** | Vahvistaa, että kentät **Nimi** ja **Sukunimi** ovat täytetyt.|
| **Lajittele** | Vahvistaa, että työntekijälle on määritetty tehtävä. |
| **Syntymäpäivämäärä** | Vahvistaa, että **Syntymäpäivä**-kenttä on täytetty. |
| **Kompensaatio** | Vahvistaa, että työntekijä on rekisteröity kiinteään kompensaatiosuunnitelmaan. |

Jos jokin näistä vahvistuksista epäonnistuu, et voi merkitä työntekijää maksuvalmiiksi.

Jos **Maksuvalmis** -kentän arvo on **Ei**, tämä on merkki siitä, että sinun on tehtävä toimenpide varmistaaksesi, että työntekijäprofiili on valmis. Tämä ei estä tietojen näkymistä missään tietoentiteetissä. 

## <a name="known-issues"></a>Tunnetut ongelmat

- **Virtaviivaistettu työntekijän syöttö** -ominaisuus on poistettava käytöstä ominaisuuksien hallinnassa. Kompensaation hallinnan työtilan ruudut eivät toimi oikein, jos käytät tätä ominaisuutta.
- **Työntekijä**-sivulla **Palkanlaskenta-välilehti**, **Maksuvalmis**-ryhmä on käytettävissä missä tahansa käyttäjäroolissa. 

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
