---
title: Vakiokustannusten varianssin kirjaus
description: Tässä artikkelissa on tietoja kirjausprofiilien ja vakiokustannusten määrittämisestä.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: e7b2d04f32b75dbd1354b3ef74a41ea1b6469c8a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894874"
---
# <a name="standard-cost-variance-posting"></a>Vakiokustannusten varianssin kirjaus

Kun käytät standardikustannuslaskentaa yhdelle tai usealle tuotteelle organisaatiossasi, sinun on määritettävä [standardikustannuslaskennan edellytykset](/supply-chain/cost-management/prerequisites-standard-costs.md). Tässä artikkelissa kuvataan kirjaustilit, joita tarvitaan seuraavien edellytysten vaiheessa 3: "Määritä standardikustannusvariansseihin liittyvät tilit varastokirjauksiin".

Ostoissa ja tuotantotilauksissa voi esiintyä erilaisia variansseja. Esimerkkejä tuotantovariansseista: [Tuotannon varianssien yhteiset lähteet](/supply-chain/cost-management/common-sources-of-production-variances.md). Ostotilauksen hinnan varianssit tapahtuvat, kun käytetään ostetun nimikkeen standardikustannusta, ja tuotteen standardikustannuksen ja ostotilauksen laskutetun määrän välillä on ero.

## <a name="sample-posting-profile-configuration"></a>Malli kirjausprofiilin konfiguraatiosta

Seuraavassa taulukossa on esimerkkejä oletuskirjaustyypeistä. Se sisältää päätilien otantatiedot ja kuvaukset.

- Veloitus/hyvitys? -sarake ilmaisee, kirjaako tapahtuma tavallisesti veloituksen vai hyvityksen. Joissakin tapauksissa tapahtuma voi kirjata joko veloituksen tai hyvityksen.
- Selvitystili-sarake ilmaisee, että kirjaustyyppi on selvitystili. Tämä tarkoittaa, että tälle tilille kirjattu summa palautetaan automaattisesti, kun myöhempi tapahtuma kirjataan.
- P/F-sarakkeessa näkyy kirjaustyyppi. "P" tarkoittaa fyysistä kirjausta ja "F" kirjanpitokirjauksia.
- "Seuraa"-sarakkeessa näkyy, onko kirjaustyypin päätili tavallisesti sama kuin toisen kirjaustyypin päätili. Se ilmaisee erityisesti kirjaustyypin, jota käytetään yleensä.

> [!NOTE]
> Päätilit ja päätilien nimet taulukossa ovat vain ehdotuksia. Suosittelemme, että määrität yrityksesi tarpeille parhaan konfiguraation yhdessä kirjanpitäjän kanssa.

| Kirjaustyyppi | Päätiliesimerkki. | Päätilin nimen esimerkki | Tilityyppi | Veloitus/hyvitys? | Selvitystili | P/F | Seuraa | Kuvaus |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Ostohintavarianssi | 510310 | Ostohintavarianssi | Kulut | Joko | En | F | Ei käytettävissä | Tätä tiliä käytetään, kun ostotilauksen ostohinnan ja standardikustannuksen välillä on varianssi. |
| Varastokustannuksen uudelleenarvostus | 510330 | Varastokustannuksen uudelleenarvostus | Kulut | Joko | En | F | Ei käytettävissä | Tätä tiliä käytetään, kun uusi kustannuslaskentaversio aktivoidaan standardikustannusnimikkeelle käytettävissä olevan varaston uudelleenarvostamiseksi. |
| Kustannuksen muutoksen varianssi | 510320 | Kustannuksen muutoksen varianssi | Kulut | Joko | En | F | Ei käytettävissä | Tätä tiliä käytetään, kun standardikustannuksissa on eroja eri toimipaikkojen välillä tai kun nimike palautetaan ja tuotteen alkuperäisen standardikustannuksen ja nykyisen standardikustannuksen välillä on muutos. |
| Tuotannon eräkokovarianssi | 510370 | Tuotannon eräkokovarianssi | Kulut | Joko | En | F | Ei käytettävissä | Tätä tiliä käytetään, kun tuoterakenteen laskentaperusteen ja tuotantotilauksen kustannuslaskennan todellisen määrän välillä on eroja. |
| Tuotantohintavarianssi | 510340 | Tuotantohintavarianssi | Kulut | Joko | En | F | Ei käytettävissä | Tätä tiliä käytetään, kun tuotantotilauksen arvioitujen kustannusten ja toteutuneiden kustannusten välillä on hintaeroja. |
| Tuotannon määrävarianssi | 510350 | Tuotannon määrävarianssi | Kulut | Joko | En | F | Ei käytettävissä | Tätä tiliä käytetään, kun tuotantotilauksen arvioitujen kustannusten ja toteutuneiden kustannusten välillä on määräeroja. |
| Tuotannon korvausvarianssi | 510360 | Tuotannon korvausvarianssi | Kulut | Joko | En | F | Ei käytettävissä | Tätä tiliä käytetään, kun tuotantotilauksessa on odottamatonta kulutusta. |
| Pyöristysvarianssi | 618160 | Pyöristysero | Kulut | Joko | En | F | Ei käytettävissä | Tätä tiliä käytetään, kun syntyy pyöristysero laskettaessa tuotantokustannuksia standardikustannuksista. |
