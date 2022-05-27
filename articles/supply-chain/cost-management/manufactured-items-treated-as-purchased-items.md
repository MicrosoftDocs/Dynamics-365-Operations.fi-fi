---
title: Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen
description: 'Tuotteita voi hankkia eri tavoin: ne voivat olla tuotettuja ja hankittuja (ostettuja). Tässä artikkelissa kuvataan joitakin seikkoja, jotka on otettava huomioon määritettäessä tuotteita monitasoista hankintaa varten.'
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4910faa2e66cb61f6064e686c49369d14526cc1f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674502"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a>Tuotettavissa tai hankittavissa olevien tuotteiden määrittäminen

[!include [banner](../includes/banner.md)]

Tuotteita voi hankkia eri tavoin: ne voivat olla tuotettuja ja hankittuja (ostettuja). Tässä artikkelissa kuvataan joitakin seikkoja, jotka on otettava huomioon määritettäessä tuotteita monitasoista hankintaa varten. 

Monitasoista hankintaa käytetään yleensä ostettuun nimikkeeseen, jota valmistetaan satunnaisesti tai kun nimike, joka oli ensisijaisesti valmistettu nimike, muuttuu siten, että se on nyt ensisijaisesti ostettu nimike. Nimike määritetään ensin valmistetuksi nimikkeeksi, jotta tuoterakenne- ja reititystiedot voidaan määrittää, sekä nimikkeen tuotantotilauksien tueksi. Tuotantotyypiksi on määritettävä **Tuoterakenne** (tai prosessivalmistuksessa **Resepti** tai **Oheistuote**).

Standardikustannuksia käytettäessä nimikkeen kustannustietueen voi laskea valmistetulle nimikkeelle. Nimikkeen kustannustietue ei kuitenkaan välttämättä vastaa hankintatarkoituksissa tarvittavaa vakiokustannusta. Tällöin vakiokustannus on kirjoitettava manuaalisesti ja aktivoitava nimikkeen kustannustietuetta varten. Kustannusten laskennassa kannattaa valita erityinen tuoterakenne ja reititys, joka vastaa tuotteen toimitusmiksiä tilikaudella. Näin varianssit voidaan minimoida. Lisäksi yhdessä toimipaikassa valmistettu nimike voidaan siirtää toiseen toimipaikkaan. Siksi nimikkeen kustannus on syötettävä manuaalisesti ja aktivoitava toimipaikalle, johon nimike siirretään. Kun valmistettua nimikettä käytetään komponenttina korkeamman tason tuotteissa, komponentin kustannuksia tulee käsitellä ostettuna nimikkeenä. Tämän ohje pätee riippumatta siitä, onko komponentin kustannukset laskettu vai syötetty manuaalisesti. Toisin sanoen tuoterakennelaskennassa nimikkeen kustannuksia on käsiteltävä ostettuna komponenttina sen sijaan, että kustannukset laskettaisiin käyttämällä nimikkeen tuoterakennetta ja reititystietoja. 

Voit estää laskennan valitsemalla **Lopeta hajotus** -merkin, joka on sisällytetty nimikkeelle määritettyyn tuoterakenteen laskentaryhmään. Voit estää pääajoituksen laskentaa hajottamasta tarpeita nimikkeen kautta asettamalla hajotuksen lopetusrajaksi 0 (nolla) päivää nimikkeen kattavuudessa tai kattavuusryhmässä. Pääajoituksen laskenta käsittelee tämän jälkeen nimikkeen ostettuna nimikkeenä eikä suorita lisää laskutoimituksia nimikkeen tuoterakenne- ja reititystiedoille.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]