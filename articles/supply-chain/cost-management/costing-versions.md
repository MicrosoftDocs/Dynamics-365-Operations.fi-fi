---
title: Kustannuslaskelmaversiot – yleiskatsaus
description: Tässä artikkelissa on tietoja kustannuslaskennan versioista, niiden ylläpitämisestä ja niihin sisällytettävien tietojen tyypeistä. Kustannuslaskelmaversion on ensisijaisesti tarkoitus sisältää nimikkeitä, kustannusluokkia ja välillisten kustannusten laskentakaavoja koskevia kustannustietueita.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 54532
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16af19fb7f4f18c417522175643649681e5912da
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201844"
---
# <a name="costing-versions-overview"></a>Kustannuslaskelmaversiot – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja kustannuslaskennan versioista, niiden ylläpitämisestä ja niihin sisällytettävien tietojen tyypeistä. Kustannuslaskelmaversion on ensisijaisesti tarkoitus sisältää nimikkeitä, kustannusluokkia ja välillisten kustannusten laskentakaavoja koskevia kustannustietueita.

Kustannuslaskelmaversiolla voi olla useampia kuin yksi käyttötarkoituksia sen mukaan, mitä tietoja kustannuslaskelmaversio sisältää. Kustannuslaskelmaversion on ensisijaisesti tarkoitus sisältää nimikkeitä, kustannusluokkia ja välillisten kustannusten laskentakaavoja koskevia kustannustietueita. Kustannuslaskelmaversiossa voi olla standardikustannustietueiden joukko tai suunniteltujen kustannustietueiden joukko, joka perustuu kustannuslaskelmaversioon määritettyyn kustannuslaskelmatyyppiin.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Standardikustannusten tai suunniteltujen kustannusten kustannuslaskentaversiot
### <a name="standard-costs"></a>Standardikustannukset

Kustannuslaskentaversio voi tukea nimikkeiden standardikustannusvarastomallia, kun kustannuslaskentaversio sisältää nimikkeitä ja valmistusprosesseja koskevan standardikustannustietueiden joukon. Valmistusprosesseja koskevat kustannustiedot esitetään reitityksen työvaiheiden kustannusluokkina ja valmistuksen yleiskustannusten laskentakaavoina.

### <a name="planned-costs"></a>Suunnitellut kustannukset

Kustannuslaskentaversio voi sisältää joukon nimikkeitä ja valmistusprosesseja koskevia suunniteltuja kustannustietueita. Suunniteltuja kustannuksia sisältävää kustannuslaskentaversiota käytetään usein kustannuslaskennan simulointien tukemiseen; esimerkiksi ostetun materiaalin tai valmistusprosessien kustannuksissa tapahtuvien muutosten vaikutus valmistettujen nimikkeiden laskettuihin kustannuksiin voidaan simuloida. Suunniteltujen kustannusten nimikkeen kustannustietueet voivat tukea myös todellisen kustannusvarastomallin käyttämistä, koska nimikkeen kustannustietueista saadaan nimikekustannusten alkuarvot. Tällaisia arvoja ovat esimerkiksi valmistettujen nimikkeiden suunniteltujen kustannusten laskeminen.

## <a name="entering-costs"></a>Kustannusten lisääminen
Kustannuslaskelmaversion kustannustietueiden tietojen ylläpitoon kuuluu kustannusten lisääminen ostetuille nimikkeille sekä nimikkeille, jotka on siirretty toimipaikasta toiseen. Muita valmistajille kuuluvia tietojen ylläpitotoimia ovat reitityksen työvaiheisiin liittyvien kustannusluokkien kustannusten lisääminen, valmistuksen yleiskustannuksia kuvaavien välillisten kustannusten laskentakaavojen lisääminen sekä valmistettujen nimikkeiden kustannusten laskeminen. 

Kustannuslaskentaversion nimikkeen kustannustiedot koostuvat kunkin nimikkeen vähintään yhdestä kustannustietueesta. Kun nimikkeen kustannustietue lisätään ensimmäisen kerran, sen tila on **Odottaa** ja siinä on voimaantulopäivämäärä. Kun aktivoit nimikkeen kustannustietueen, tilaksi päivitetään **Aktiivinen** ja voimaantulopäivä päivitetään aktivointipäiväksi. Nimikkeen eri kustannustietueet voivat vastata eri toimipaikkoja, voimaantulopäiviä tai tiloja. Kun tulevan päivämäärän valmistettujen nimikkeiden kustannuksia lasketaan, asiaankuuluvan voimaantulopäivän mukaisia kustannustietueita käytetään tuoterakennelaskelmassa huolimatta siitä, onko tila **Odottaa** tai **Aktiivinen**. Nimikkeen nykyistä aktiivista kustannustietuetta käytetään tuotantotilauksen kustannusten arviointiin sekä varastotapahtumien arviointiin standardikustannusvarastomallia käytettäessä. Kustannusluokkien kustannustietueiden ja välillisten kustannusten laskentakaavojen ylläpitotoimet ovat samankaltaisia kuin nimikkeen kustannustietueiden ylläpitotoimet. 

Kaksi kustannuslaskelmaversion estomenettelyä määrittää, voidaanko odottavat kustannukset säilyttää ja voidaanko odottavat kustannukset aktivoida. Estomenettelyiden avulla voit ensin sallia tietojen ylläpitämisen ja estää sitten niiden avulla kustannuslaskentaversion kustannustietueiden ylläpitämisen. 

Kustannuslaskelmaversiossa voi olla myös tietoja nimikkeen myynti- tai ostohinnoista. Niitä käytetään tuoterakennelaskelmissa.

## <a name="item-sales-prices-for-bom-calculations"></a>Tuoterakennelaskelmien nimikkeen myyntihinnat
Tärkein syy myyntihintatietojen sisällyttämiseen on valmistetun nimikkeen lasketun myyntihinnan säilyttäminen. Laskettu myyntihinta voidaan sitten analysoida ja määrittää sen perusteella, miten komponentit, reititystoiminnot ja yleiskustannukset vaikuttavat kuluihin ja myyntihintoihin. 

Myyntihintatietojen sisällyttämisen toissijainen syy on komponenttinimikkeiden myyntihintatietueiden määrittäminen. Näillä tietueilla voidaan sitten laskea valmistettujen nimikkeiden myyntihinta. Määrität ensin tuoterakenteen laskentaryhmään upotettavan myyntihintaryhmän ja määritä tuoterakenteen laskentaryhmän ostettuihin nimikkeisiin. Kun sitten suoritat suunniteltuja kustannuksia käyttäviä tuoterakennelaskelmia, valitset tuoterakenteen laskentaryhmän kustannushintamallin. 

Muussa tapauksessa nimikkeiden myyntihintatietueita käytetään vain viitetietoina riippumatta siitä, määritetäänkö ne manuaalisesti vai lasketaanko ne. Nimikkeen myyntihintatietueen aktivoinnin ansiosta voit päivittää nimikkeen perusmyyntihinnan. Perusmyyntihinta ei ole kuitenkaan ole toimipaikkakohtainen ja se voidaan ohittaa manuaalisesti. Nimikkeen perusmyyntihintaa käytetään myyntitilauksien ja -tarjousten oletusmyyntihintana.

## <a name="item-purchase-prices-for-bom-calculations"></a>Tuoterakennelaskelmien nimikkeen ostohinnat
Tärkein syy ostohintatietojen käyttöönotolle on komponenttinimikkeiden ostohintatietueiden määrittäminen, jotta tietueilla voidaan laskea valmistettujen nimikkeiden kustannukset. Nimikkeen ostohintatietueet täytyy lisätä manuaalisesti. 

Ostohintasisältö otetaan käyttöön määrittämällä ensin nimikkeen ostohinnan kustannushintamallin sisältävä tuoterakenteen laskentaryhmä ja määrittämällä sitten tämä laskentaryhmä ostettuihin nimikkeisiin. Voit sitten käyttää tuoterakenteen laskentaryhmän kustannushintaryhmää, kun suoritat tuoterakennelaskelmia, joissa lasketaan suunniteltujen kustannusten avulla valmistettujen nimikkeiden myyntihinta. 

Nimikkeiden ostohintatietueiden käytetään myös viitetietoina. Kun nimikkeen ostohintatietueen tila vaihdetaan tilasta **Odottaa** tilaan **Aktiivinen**, voit päivittää nimikkeen perusostohinnan. Perusostohinta ei ole kuitenkaan ole toimipaikkakohtainen, ja se voidaan ohittaa manuaalisesti. Nimikkeen perusostohintaa käytetään ostotilausten oletusostohintana.



