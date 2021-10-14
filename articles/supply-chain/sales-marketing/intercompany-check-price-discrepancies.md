---
title: Tarkista konsernin sisäiset tilaushintojen erot
description: Tässä ohjeaiheessa käsitellään konsernin sisäisten tilaushintojen erojen tarkistamista
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: f9a0ba4980f8acf56d84dc865094b405b7402ad5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548231"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Tarkista konsernin sisäiset tilaushintojen erot

[!include [banner](../../includes/banner.md)]

Tämän menettelyn avulla voit tarkistaa konsernin sisäisten tilausten hintojen ristiriidat.

1. Valitse **Hankinta \> Kausittainen \> Tyhjennä \> Tarkista konsernin sisäiset tilaushintojen erot**.
1. Määritä tarvittaessa erätyö ja valitse sitten **OK**, jotta voit tarkistaa konsernin sisäisten myyntitilausten ja ostotilausten hinnat ja alennukset. Muussa tapauksessa sulje sivu tarkistusta suorittamatta valitsemalla **Peruuta**.

    > [!TIP]
    > Jos synkronointi- tai hintaongelmia, ne ilmoitetaan avautuvassa tietosanomassa. Tietosanoma voi tulostaa viitteeksi.

1. Avaa tilaus nykyisessä yrityksessä valitsemalla kyseinen rivi tietosanomassa. Avaa tilaus liittyvässä yrityksessä valitsemalla ensin **Konsernin sisäinen** ja sitten **Konsernin sisäinen ostotilaus** tai **Konsernin sisäinen myyntitilaus**.

    > [!NOTE]
    > Konsernin sisäisen tilauksen päivityksen salliminen:
    >
    > 1. Siirry kohtaan **Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**.
    > 1. Valitse toimintoruudussa **Yleiset**-välilehti ja valitse sitten **Konsernin sisäinen**.
    > 1. Valitse **Konsernin sisäinen** -sivulla **Ostotilauskäytännöt** tai **Myyntitilauskäytännöt**.
    > 1. Valitse kummallakin alueella **Salli hinnan muokkaus** ja **Salli alennuksen muokkaus**.

1. Avaa sellainen konsernin sisäinen tilaus, jossa hinta halutaan säilyttää.
1. Vaihda kunkin tilausrivin **Yksikköhinta**-kentän arvo ja palauta se sitten alkuperäiseksi. Vaihda rivin **Alennus**-kentän arvo edestakaisin ja vaihda soveltuvien **Ostojen kulut**- tai **Myynnin kulut**-kenttien arvot edestakaisin. Arvojen muuttaminen edestakaisin käynnistää hintojen, alennusten ja muiden kulujen synkronoinnin tältä konsernin sisäisen tilauksen riviltä viitatulle konsernin sisäisen tilauksen riville, jolloin arvot kohdistetaan automaattisesti.

    > [!NOTE]
    > Synkronointi on voimassa vain, jos konsernin sisäistä myyntitilausta ei ole laskutettu. Jos konsernin sisäinen myyntitilaus on lasku-kirjattu ja myyntilaskun kirjauskansio on luotu, muutokset on tehtävä suoraan konsernin sisäisen ostotilauksen riveille määrittämällä konsernin sisäisen myyntilaskun kirjauskansiota vastaavat hinnat, alennukset ja kulut. Jos tätä toimenpidettä ei suoriteta, tilausten kokonaissummat eivät vastaa toisiaan eikä konsernin sisäistä ostotilausta voida laskukirjata.

1. Toista menettelyä, kunnes kaikki konsernin sisäiset osto- ja myyntitilaukset on synkronoitu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
