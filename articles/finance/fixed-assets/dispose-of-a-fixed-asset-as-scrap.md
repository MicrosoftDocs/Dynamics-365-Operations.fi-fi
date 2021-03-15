---
title: Hävikiksi merkityn käyttöomaisuuden poistaminen
description: Tässä ohjeaiheessa käsitellään hävikkinä poistetun käyttöomaisuuden tapahtumien eliminointiprosessia.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4dee4468079a9ad500f513900cec090acf6026ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969125"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Hävikiksi merkityn käyttöomaisuuden poistaminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään hävikkinä poistetun käyttöomaisuuden tapahtumien eliminointiprosessia. Eliminoitavia tapahtumatyyppejä ovat esimerkiksi käyttöomaisuuden hankinta sekä kumuloituneet poistotapahtumat ja muut käyttöomaisuustapahtumat. Näiden tapahtumien eliminointi vaikuttaa tasetileihin, kuten hankintaoikaisu-, poisto-oikaisu-, uudelleenarvostus-, kirjanpitoarvon korotus- ja kirjanpitoarvon alentamistilit.

| Tapahtuma                                         | Debet (Dr.) | Kredit (Cr.) |
|-----------------------------------------------------|-------------|--------------|
| Dr. kertynyt poisto                        | X           |              |
| Cr. käyttöomaisuuden voitto/tappio                          |             | X            |
| Dr. käyttöomaisuuden voitto/tappio                          | X           |              |
| Cr. käyttöomaisuuserän hankintatili                 |             | X            |
| Dr. käyttöomaisuuden voitto/tappio (nettokirjanpitoarvo \[NKPA\]) | X           |              |
| Cr. käyttöomaisuuden voitto/tappio (NKPA)                    |             | X            |

> [!NOTE]
> Yrityksen talousjohtajan tai controllerin kannattaa tehdä tiivistä yhteistyötä, jotta kullekin tapahtumatyypille tunnistetaan oikeat käytettävät tilit ja jotta voidaan varmistaa, että poistoprosessi ja sen luomat tapahtumat päivittävät kyseiset tilit oikein.

Ennen kuin käyttöomaisuus voidaan poistaa hävikkinä, on luotava kirjanpitotilit, jotka on liitetty käyttöoikeuden hankinta-arvoon, kuluvan vuoden poistoon, edellisten vuosien poistoon ja käyttöomaisuuden NKPA:han. Käyttöomaisuuden tapahtumatyyppien luettelo on **Käyttöomaisuuden kirjausprofiilit** -sivulla. Valitse ensin **Käyttöomaisuuserät \> Asetukset \> Käyttöomaisuuserän kirjausprofiili** ja valitse sitten **Luovutus**-pikavälilehdessä **Hävikki** ruudulla yläpuolella olevassa kentässä. Seuraavassa kuvassa on luettelo **Käyttöomaisuuserän kirjausprofiili** -sivulla.


[![Käyttöomaisuuden poistaminen hävikkinä, kuva 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

Seuraavassa esimerkissä käyttöomaisuus hankittiin 1.1.2018 ja se hävitetään 31.3.2019.

- **Hankintahinta:** 24 000,00 Yhdysvaltain dollaria (USD)
- **Käyttöikä:** kaksi vuotta
- **Poistomenetelmä:** Tasapoisto - käyttöaika
- **Poistosumma:** 1 000,00 USD kuukaudessa

Käyttöomaisuuden NKPA lasketaan seuraavan kaavan avulla:

Nettokirjanpitoarvo = hankintahinta – poisto

Tässä esimerkissä käyttöomaisuus hankittiin ja siinä tehtiin poistoja 15 kuukautta tammikuusta 2018 maaliskuuhun 2019. Tämän vuoksi käyttöomaisuuserän NKPA on 9 000,00 USD (24 000,00 USD – 15 000,00 USD).

[![Käyttöomaisuuden poistoesimerkki](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Luo poistokirjanpito valitsemalla ensin **Käyttöomaisuuserät \> Kirjauskansioviennit \> Käyttöomaisuuden kirjauskansio** ja valitse sitten toimintoruudussa **Rivit**. Valitse ensin **Poistohävikki** ja valitse sitten käyttöomaisuuserän tunnus. Jotta käyttöomaisuus voitaisiin poistaa kokonaan, älä anna arvoa **Debet**- eikä **Kredit**-kenttään.

[![Käyttöomaisuuden kirjauskansio](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Käyttöomaisuuden poistohävikkitapahtuma muuttaa käyttöomaisuuskirjan kentän arvoja seuraavin tavoin:

- **Saldo**-osan **Tila**-kenttään on päivitetty **Romutettu**.
- **Otto**-osan **Myyntipäivä**-kentän arvoksi määritetään päivämäärä, jolloin käyttöomaisuus hävitettiin.

[![Käyttöomaisuuden kirjauskansion tiedot](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

Seuraavassa kuvassa on käyttöomaisuussaldo.

[![Käyttöomaisuussaldo](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

Seuraavassa kuvassa on kirjattu tosite.

[![Nettokirjanpitoarvo](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]