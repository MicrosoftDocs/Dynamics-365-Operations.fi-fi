---
title: Konsernin sisäisten tilausten muuttaminen
description: Tässä artikkelissa käsitellään konsernin sisäisten tilausten muuttamistoimintoa
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f139678fbb59b9132ece1ab758e141ec7cdb7a19
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852183"
---
# <a name="change-intercompany-orders"></a>Konsernin sisäisten tilausten muuttaminen

[!include [banner](../../includes/banner.md)]

Jos muutat konsernin sisäistä myynti- tai ostotilausta, muutos vaikuttaa myös vastaavan yrityksen vastaavaan myynti- tai ostotilaukseen.

## <a name="adding-new-lines"></a>Uusien rivien lisääminen

Konsernin sisäiseen myynti- tai ostotilaukseen voi lisätä uusia rivejä, jos alkuperäinen myyntitilaus on osa konsernin sisäistä tilausketjua. Uusia rivejä voi lisätä myös, jos alkuperäinen myyntitilaus ei ole suoratoimitus. Jos alkuperäinen myyntitilaus on suoratoimitus, uusia tilausrivejä voi lisätä konsernin sisäiseen myynti- ja ostotilaukseen vain, jos **Salli epäsuora luonti** -kenttä on valittu alkuperäisen myyntitilauksen **Konsernin sisäiset asetukset** -pikavälilehdessä.

## <a name="changing-prices-and-discounts"></a>Hintojen ja alennusten muuttaminen

Hintoja ja alennuksia voi muuttaa, jos **Salli hinnan muokkaus**- ja **Salli alennuksen muokkaus** -valintaruudut on valittu **Konsernin sisäinen** -sivulla.

Jos muutat konsernin sisäisen myyntitilausrivin jonkin aiemmin luodun rivin yksikköhintaa, myös konsernin sisäisen ostotilauksen yksikköhinta muuttuu.

Jos muutat konsernin sisäisen myyntitilausrivin jotakin alennuskenttää, vastaavat kentät päivitetään konsernin sisäisessä ostotilauksessa.

## <a name="changing-and-adding-new-charges"></a>Uusien kulujen muuttaminen ja lisääminen

Kuluja voi muuttaa, jos **Salli hinnan muokkaus**- ja **Salli alennuksen muokkaus** -valintaruudut on valittu **Konsernin sisäinen** -sivulla.

Jos uusi kulu lisätään konsernin sisäisen myyntitilauksen otsikkoon ja konsernin sisäiselle myyntiriville, kumpikin kulu kopioidaan konsernin sisäiseen ostotilaukseen. Tämän vuoksi konsernin sisäisessä myyntitilauksessa ja konsernin sisäinen ostotilauksessa on sama kokonaissumma. Kuluja ei koskaan kopioida alkuperäiseen myyntitilaukseen.

## <a name="copying-a-fee"></a>Maksun kopioiminen

Maksu voidaan kopioida alkuperäiseen myyntitilaukseen luomalla se uutena myyntirivinä, jonka nimiketyyppi on **Palvelu**.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Määrien muuttaminen sekä konsernin sisäisten osto- ja myyntitilausrivien poistaminen

Voit muuttaa konsernin sisäisen osto- tai myyntitilausrivin määrää tai poistaa sen vain, jos rivi on luotu suoraan **Myyntitilaus**- tai **Ostotilaus**-lomakkeessa. Tämä muutoksen myötä konsernin sisäisestä osto- tai myyntitilauksesta tai myyntitilausriveistä tulee lähde.

## <a name="origins-of-orders-and-order-lines"></a>Tilausten ja tilausrivien alkuperät

Konsernin sisäisillä tilauksilla ja tilausriveillä on kaksi alkuperävaihtoehtoa:

- **Johdettu** – tilaus on luotu automaattisesti konsernin sisäisestä tilausketjusta.
- **Lähde** – käyttäjä on luonut tilauksen manuaalisesti.

Alkuperä ilmaistaan konsernin sisäisten osto- ja myyntitilausten otsikon **Alkuperä**-kentässä. Tämä kenttä sijaitsee myyntitilauksen **Konsernin sisäiset asetukset** -pikavälilehdessä ja ostotilaukset **Asetukset**-välilehdessä.

**Johdettu**- ja **Lähde**-alkuperä koskevat vain konsernin sisäisiä tilauksia. Kaikkien muiden myyntitilausten, ostotilausten ja myyntirivien **Alkuperä**-kenttä on tyhjä. Tämä kenttä on tyhjä myös alkuperäisessä myyntitilauksessa.

## <a name="example-derived-origin"></a>Esimerkki: Johdettu-alkuperä

Alkuperäinen myyntitilaus luodaan ulkoiselle asiakkaalle. Tässä myyntitilauksessa on yksi tilausrivi. Tämä alkuperäinen myyntitilaus luo konsernin sisäisen ostotilauksen, jossa on yksi tilausrivi, joka puolestaan luo yhden tilausrivin sisältävän konsernin sisäisen myyntitilauksen. Konsernin sisäisen ostotilauksen otsikko ja tilausrivi luodaan automaattisesti alkuperäisestä myyntitilauksesta.

**Alkuperä**-kentän arvo konsernin sisäisen ostotilauksen **Asetukset**-pikavälilehdessä ja konsernin sisäisen myyntitilauksen otsikoiden **Konsernin sisäiset asetukset** -pikavälilehdessä on **Johdettu**. Myös osto- ja myyntitilausrivien **Rivin tiedot** -välilehden **Alkuperä**-kentän arvo on **Johdettu**.

Jos tilausrivin alkuperä on **Johdettu**, tilausriviä ei voi poistaa suoraan. Tilausrivi voidaan poistaa vain tilausrivin luoneesta lähteestä. Myös tilattua määrää voidaan muuttaa vain tilausrivin luoneessa lähteessä.

Jos alkuperäinen myyntitilaus ja alkuperäinen myyntitilausrivi ovat osa konsernin sisäistä tilausketjua, voit muuttaa tilattuja määriä alkuperäisessä myyntitilauksessa. Voit myös poistaa tilausrivejä alkuperäisessä myyntitilauksessa.

## <a name="example-source-origin"></a>Esimerkki: Lähde-alkuperä

Konsernin sisäiselle toimittajalle luodaan ostotilaus. Sekä konsernin sisäisen ostotilauksen että ostotilausrivin alkuperä on **Lähde**. Niinpä konsernin sisäinen ostotilaus ohjain ja toimittajan yrityksessä automaattisesti luodun konsernin sisäisen myyntitilauksen alkuperänä on **Johdettu**.

Myöskään konsernin sisäisessä ostotilauksessa luodun tilausrivien tilattuja määriä ei voi muuttaa konsernin sisäisessä myyntitilauksessa. Tilausrivi voidaan poistaa vain konsernin sisäisessä ostotilauksessa. Jos konsernin sisäiseen myyntitilaukseen lisätään uusi rivi, konsernin sisäisen myyntitilausrivin alkuperä on sitten **Lähde**.

Kun alkuperäinen myyntitilaus on osa konsernin sisäistä tilausketjua, konsernin sisäisiä tilauksia ja tilausrivejä voi aina hallita alkuperäisen myyntitilauksen avulla.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
