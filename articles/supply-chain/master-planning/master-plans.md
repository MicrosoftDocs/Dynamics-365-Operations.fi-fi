---
title: Pääsuunnitelmat – yleiskatsaus
description: Voit käyttää useita pääsuunnitelmia. Pääsuunnitelmilla voidaan tukea yrityksen päivittäistä toimintaa, simuloida eri suunnittelustrategioita, joita halutaan seurata, sekä ottaa käyttöön esimerkiksi yrityksen sisäistä suorituskykyä tai asiakastyytyväisyyttä koskevia käytäntöjä.
author: ChristianRytt
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "7911"
- intro-internal
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75f18d708bf71a7bec1d8a5bd95008aaa2ec4d90
ms.sourcegitcommit: 2084fc166d027f8192a08cd5c00169c448869ac8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2021
ms.locfileid: "7582537"
---
# <a name="master-plans-overview"></a>Pääsuunnitelmat – yleiskatsaus

[!include [banner](../includes/banner.md)]

Voit käyttää useita pääsuunnitelmia. Pääsuunnitelmilla voidaan tukea yrityksen päivittäistä toimintaa, simuloida eri suunnittelustrategioita, joita halutaan seurata, sekä ottaa käyttöön esimerkiksi yrityksen sisäistä suorituskykyä tai asiakastyytyväisyyttä koskevia käytäntöjä.

Voit määrittää pääsuunnitelmia **Pääsuunnitelmat**-sivulla.

Suunnitelmia on kahdentyyppisiä:

- **Staattinen suunnitelma** - Pääsuunnittelua laskettaessa luodaan nettotarvesuunnitelma käyttämällä tämänhetkisiä tietoja. Tämä suunnitelma ei muutu, ennen kuin pääsuunnittelu suoritetaan seuraavan kerran tai muutat suunnitelmaa manuaalisesti. Tämä on toimintasuunnitelma, jota yrityksen henkilöstö, kuten ostojen ja tuotannon suunnittelija, voi käyttää päätöstensä pohjana ja päivittäisten tehtäviensä tukena.
- **Dynaaminen suunnitelma** – Tämä suunnitelma lähtee samasta nettotarvesuunnitelmasta, joka luotiin pääsuunnittelussa. Voit kuitenkin päivittää dynaamisen suunnitelman aina, kun perustiedot muuttuvat. Voit tehdä päivityksen esimerkiksi luodessasi uutta myyntitilausta. Näin voit seurata muuttuvaa tilauksen verkostoa ja nimikkeiden saatavuutta sen vaikuttamatta staattiseen suunnitelmaan, jota muut käyttävät työprosesseissaan.

Yritys voi halutessaan käyttää pelkkää dynaamista suunnitelmaa tai sekä staattisia että dynaamisia suunnitelmia. Lisäksi mikä tahansa pääsuunnitelma voidaan konfiguroida heijastamaan tiettyä strategiaa tai ongelmakohtaa. Esimerkkejä ovat seuraavat:

- Varastotasot asetetaan suuremmiksi varaston loppumisen välttämiseksi.
- Varmuusmarginaalit asetetaan pidemmiksi epäluotettavien toimittajien varalta.

Alkuperäinen dynaaminen suunnitelma voidaan myös asettaa päivittymään uuden tarvesuunnitelman mukaisesti aina, kun pääsuunnittelu suoritetaan. Voit määrittää asetukset **Pääsuunnittelun parametrit** -sivulla.

## <a name="additional-resources"></a>Lisäresurssit

- [Kattavuusasetukset](coverage-settings.md)
- [Pääajoituksen taktisen ja operatiivisen suunnittelun erottaminen](https://community.dynamics.com/ax/b/dynamicsaxmanufacturingrdteamblog/posts/separating-tactical-and-operative-planning-for-master-scheduling)
- [Pääsuunnittelu: käytetäänkö staattista ja dynaamista pääsuunnittelua vai yhtä suunnitelmaa?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
