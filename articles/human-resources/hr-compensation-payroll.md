---
title: Valmis maksettavaksi
description: Tässä ohjeaiheessa esitetään, miten työntekijä merkitään maksuvalmiiksi Dynamics 365 Human Resourcesissa.
author: marcelbf
ms.date: 07/13/2020
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
ms.openlocfilehash: 70b3f31db459fe021caf08fe09b2e44a597294d1992ee16a69efd8745941a4bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732414"
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

1. Avaa **Kompensaation hallinta**. Työtilassa on kaksi ruutua 
    - **Työntekijät, jotka ovat valmiita maksamaan**
    - **Työntekijät eivät ole maksuvalmiita**
    ![Kompensaation hallinnan työtila.](./media/hr-ready-to-pay-1-workspace.png)

2. Valitse **Työntekijät eivät ole maksuvalmiita** -ruutu.

3. Valitse vahvistettavat työntekijät. Valitse **Palkanlaskenta**-välilehden **Maksuvalmis** -ryhmästä **Vahvista** .
    ![Työntekijöiden vahvistaminen.](./media/hr-ready-to-pay-2-validate.png)

4. Voit tarkastella tuloksia valitsemalla **Palkanlaskenta**-välilehden **Maksuvalmis** -ryhmästä **Tulokset** .

## <a name="validation"></a>Valintasäännöt

Ennen kuin työntekijä merkitään maksuvalmiiksi, järjestelmä tekee profiilin täydellisyyden perustarkistuksen.

![Tulosten tarkistaminen.](./media/hr-ready-to-pay-3-results.png)

Seuraavassa taulukossa on lisätietoja kustakin suoritettavasta tarkistuksesta. 

| Valintasäännöt | Lisätietoja |
| --- | --- |
| Osoitteen tarkoituksen parametri | Vahvistaa, onko parametri **Käytä palkanlaskentaosoitteiden tarkoitusta** käytössä. |
| Palkanlaskennan osoite | Vahvistaa, onko työntekijäprofiililla vähintään yksi osoite, jonka tarkoitus on "Palkanlaskennan sijainti" tai "Palkanlaskennan työsijainti", ja tarkoitusta kohden on vain yksi osoite. |
| Työsuhde | Tarkistaa, onko työntekijällä vähintään yksi työsuhde (nykyinen, edellinen tai tuleva). |
| Tunnusnumero | Tarkistaa, onko parametri "Käytä tunnustyyppejä palkanlaskennan käsittelyssä" kyllä ja jos on, onko parametrissa ilmoitettu tunnustyyppi on täytetty työntekijäprofiilissa. |
| Etu- ja sukunimi | Tarkistaa, onko työntekijäprofiili kelvollinen, ja tarkistaa, onko kentät **Nimi** ja **Sukunimi** täytetty.|
| Lajittele | Tarkistaa, onko työntekijälle määritetty tehtävä. |
| Syntymäpäivämäärä | Tarkistaa, onko työntekijäprofiili kelvollinen, ja tarkistaa, onko kenttä **Syntymäpäivä** täytetty. |
| Kompensaatio | Tarkistaa, onko työntekijä rekisteröity kiinteään kompensaatiosuunnitelmaan. |

Jos jokin näistä vahvistuksista epäonnistuu, et voi merkitä työntekijää maksuvalmiiksi.

Jos **Maksuvalmis** -kentän arvo on **Ei**, tämä on merkki siitä, että sinun on tehtävä toimenpide varmistaaksesi, että työntekijäprofiili on valmis. Tämä ei estä tietojen näkymistä missään tietoentiteetissä. 

## <a name="known-issues"></a>Tunnetut ongelmat

- **Virtaviivaistettu työntekijän syöttö** -ominaisuus on poistettava käytöstä ominaisuuksien hallinnassa. Kompensaation hallinnan työtilan ruudut eivät toimi oikein, jos käytät tätä ominaisuutta.
- Työntekijä-lomakkeen **Palkanlaskenta-välilehti**, **Maksuvalmis** -ryhmä on käytettävissä missä tahansa käyttäjäroolissa. 

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
