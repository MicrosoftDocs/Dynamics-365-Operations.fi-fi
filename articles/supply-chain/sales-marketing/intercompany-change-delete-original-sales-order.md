---
title: Alkuperäisen konsernin sisäisen myyntitilauksen muuttaminen tai poistaminen
description: Tässä aiheessa käsitellään alkuperäisen myyntitilauksen muuttamis- ja poistamistoimintoja
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7bd6bdbf65499e9f18bf6bb5e160a5634bc37fba
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548237"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Alkuperäisen konsernin sisäisen myyntitilauksen muuttaminen tai poistaminen

[!include [banner](../../includes/banner.md)]

Kun myyntitilausta muutetaan, muutokset synkronoituvat automaattisesti sekä soveltuvaan konsernin sisäiseen osto- että myyntitilaukseen.

> [!NOTE]
> Tekemäsi muutokset eivät vaikuta ulkopuolisten toimittajien ostotilauksiin eivätkä ulkopuolisten toimittajien ostotilausriveihin yhteydessä oleviin alkuperäisiin myyntiriveihin.

Seuraavassa taulukossa on yhteenveto mahdollisista muutoksista ja odotettavissa olevista tuloksista.

| Toiminto | Tulos |
|---|---|
| Alkuperäisen myyntitilauksen poistaminen | Myös liittyvä konsernin sisäinen ostotilaus ja -myyntitilaus poistetaan. Jos tilauksen tila on **Keräysluettelo** tai sitä myöhempi käsittelyvaihe, myyntitilausta ei voi poistaa. |
| Alkuperäisen myyntitilausrivin poistaminen | Myös liittyvä konsernin sisäisen ostotilauksen ja myyntitilauksen rivi poistetaan. Jos tilauksen tila on **Keräysluettelo** tai sitä myöhempi käsittelyvaihe, myyntitilausriviä ei voi poistaa. |
| Uuden myyntirivin lisääminen alkuperäiseen myyntitilaukseen | Uusi myyntitilaus rivi luodaan sekä konsernin sisäiseen ostotilaukseen että myyntitilauksen. |
| Alkuperäisen myyntitilausrivin määrän muuttaminen | Määrä synkronoidaan sekä konsernin sisäisen ostotilauksen että myyntitilauksen rivillä. Nettomäärä lasketaan uudelleen kaikissa tilauksissa. |
| Suoratoimituksen poistaminen käytöstä alkuperäisessä myyntitilauksessa | Alkuperäisen myyntitilauksen **Suoratoimitus**-kenttää ei voi muuttaa, jos yrityksen sisäisen myyntitilauksen rivin tila on vähintään **Keräysluettelo**, **Toimitustilaus** tai **Keräysluettelon kirjauskansio**. Konsernin sisäisen ostotilauksen toimitusosoite muuttuu vakiotoimitusosoitteeksi (ostotilauksen vakiotoimitusosoitteeksi). Myös konsernin sisäiset ostotilausrivit muutetaan rivien vakiotoimitusosoitteeksi. Molemmat synkronoidaan konsernin sisäisten myyntitilauksen ja sen rivien kanssa. Alkuperäisen myyntitilauksen kaikkien rivien toimitustyypiksi muuttuu **Ei mitään**, ja kenttä synkronoituu konsernin sisäisten ostotilausrivien kanssa. Toiminto ei vaikuta ulkopuolisten toimittajien ostotilauksiin eikä ulkopuolisten toimittajien ostotilausriveihin yhteydessä oleviin alkuperäisiin myyntiriveihin. Konsernin sisäisen ostotilauksen ja sen rivien toimituspäivä sekä niissä pyydetty vastaanotto- ja lähetyspäivä päivitetään. |
| Suoratoimituksen käyttöönotto alkuperäisessä myyntitilauksessa | Jos yrityksen sisäisen myyntitilauksen rivin tila on vähintään **Keräysluettelo**, **Toimitustilaus** tai **Keräysluettelon kirjauskansio**, alkuperäisen myyntitilauksen **Suoratoimitus**-kenttää ei voi muuttaa. Konsernin sisäisen ostotilauksen toimitusosoite muutetaan alkuperäisen myyntitilauksen toimitusosoitteeksi ja synkronoidaan konsernin sisäisen myyntitilauksen kanssa. Alkuperäisen myyntitilauksen kaikkien rivien toimitustyypiksi muuttuu **Suoratoimitus**, ja kenttä synkronoituu konsernin sisäisten ostotilausrivien kanssa. Kunkin alkuperäisen myyntitilausrivin toimitusosoite synkronoituu sekä konsernin sisäisten ostotilausrivien että myyntitilausrivien kanssa. Konsernin sisäisen ostotilauksen ja sen rivien toimituspäivä sekä niissä pyydetty vastaanotto- ja lähetyspäivä päivitetään. |
| Huomautuksen lisääminen alkuperäisen myyntitilauksen otsikkoon ja sen riveille | Huomautus kopioidaan konsernin sisäiseen ostotilaukseen ja myyntitilaukseen. |
| Huomautuksen muokkaaminen tai poistaminen | Jos huomautusta muokataan tai se poistetaan, myös konsernin sisäisen ostotilauksen ja myyntitilauksen huomautuksia muokataan tai ne poistetaan vastaavasti. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
