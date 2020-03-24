---
title: Luotonvalvonnan yleiskatsaus
description: Tässä ohjeaiheessa on luotonvalvonnan toimintojen yleiskatsaus.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a822e5f5a6cb71a0234b1776211788578470b0bb
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124297"
---
# <a name="credit-and-collections-overview"></a>Luotonvalvonnan yleiskatsaus

[!include [banner](../includes/banner.md)]

Voit hallita asiakkaiden luottorajoja ja suorittaa tarvittaessa perintätehtäviä.

## <a name="credit-management"></a>Luotonhallinta

Asiakkaan luotonhallinnan avulla voit hallita luottorajoja ja hallita myyntitilausten siirtymistä kirjausprosessissa luotujen luottosääntöjen perusteella.

Luotonhallintaprosessi voi sisältää seuraavia vaiheita:

- Lisätietoja asiakkaan luottokelpoisuudesta antavien luottomääritteiden päivittäminen.
- Luottorajojen luonti asiakkaille käyttämällä luottorajan oikaisuja.
- Väliaikaisten luottorajojen luonti asiakkaille käyttämällä luottorajan oikaisuja. Tällä tavoin luottorajaa voidaan nostaa tai laskea väliaikaisesti liiketoimintatarpeiden perusteella.
- Luottorajaan mahdollisesti vaikuttavien tietojen, kuten vakuus- tai takaustietojen, lisääminen.
- Asiakkaat yhteen liittävien asiakkaan luottoryhmien luominen siten, että ne voivat jakaa yhden luottorajan.
- Riskipisteiden määrittäminen asiakkaille ja näiden pistemäärien käyttäminen luomaan luottorajoja kyseisille asiakkaille automaattisesti luottorajan oikaisujen avulla.
- Estosääntöjen luominen asettamaan tilaus pitoon jonkin kirjausprosessin aikana esimerkiksi seuraavien seikkojen perusteella: riski, maksuehdot, luottorajat, erääntyneet summat ja käytetyn luottorajan prosenttiosuus.
- Pidossa olevien myyntitilausluettelon hallinta, pitosyiden tarkastelu ja ongelmien ratkaiseminen.
- Myyntitilausten vapauttaminen ja niiden jatkaminen kirjausprosessin läpi.
- Työnkulun määrittäminen hallitsemaan luottorajan muutosten ja myyntitilausten vapauttamisen hyväksymistä.

## <a name="collections-management"></a>Perinnän hallinta

**Perintä**-sivu on keskitetty näkymä myyntireskontran perimistietojen hallitaan. Perintäjohtajat voivat hallita perintää tästä keskitetystä näkymästä. Perimisasiamiehet voivat aloittaa perintäprosessin joko ennalta määritettyjen ehtojen mukaan muodostettavasta asiakasluettelosta tai **Asiakkaat**-sivulta.

Ennen kuin aloitat perinnän määrittämisen tai perinnän käyttämisen, on hyvä ymmärtää seuraavat käsitteet:

- Asiakkaan erääntymistilannevedokset sisältävät erääntyneet saldotiedot tietyltä aikajaksolta.
- Perinnän asiakaspoolit helpottavat työn organisointia.
- Perimisasiamiehet voivat ylläpitää omia asiakaspoolejaan.
- Luettelosivuilla voi järjestää perinnän asiakkaita, tehtäviä ja tapauksia.
- Kaikki asiakkaan perintätiedot yhdellä sivulla, jolta voit ryhtyä toimenpiteisiin.
- Korkojen ja maksujen peruuttaminen, palauttaminen tai kääntäminen yhdellä toiminnolla.
- Poistotapahtumia voidaan luoda yhdessä vaiheessa.
- Ei katetta (NSF) -maksut voidaan käsitellä yhdessä vaiheessa.

Näiden käsitteiden kuvaukset ovat kohdassa [Perinnän hallinnan keskeiset käsitteet](./cm-collections-concepts.md).

## <a name="additional-resources"></a>Lisäresurssit

[Asiakkaan luotonhallinnan parametrien määrittäminen](./cm-credit-mgmt-setup.md)

[Asiakkaan luotonhallinnan määritystiedot](./cm-setup-information.md)

[Asiakkaan luotonhallintatietojen lisääminen](./cm-add-credit-mgmt-information-customer.md)

[Asiakasluottoryhmät](./cm-customer-credit-groups.md)

[Asiakkaan luottorajan oikaisut](./cm-credit-limit-adjustments.md)

[Myyntitilausten luottorajapidot](./cm-sales-order-credit-holds.md)

[Asiakkaan luotonhallinnan kausittaiset tehtävät](./cm-periodic-tasks.md)
