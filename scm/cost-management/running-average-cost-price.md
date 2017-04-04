---
title: "Kustannushinnan käyttökeskiarvo"
description: "Varaston sulkemisprosessi selvittää varasto-ottotapahtumat vastaanottotapahtumia, joka valitaan nimikkeen malliryhmä varastonarvostusmenetelmän perusteella. Ennen kuin varaston sulkeminen on suoritettu, järjestelmä laskee juoksevan keskimääräisen kustannushinnan, jota käytetään yleensä silloin, kun kirjataan varasto-ottotapahtumat."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-04-07 15 - 11 - 47
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 685dfaa877699db3c36cc1ea77d956461f8e68ec
ms.lasthandoff: 03/29/2017


---

# <a name="running-average-cost-price"></a>Kustannushinnan käyttökeskiarvo

Varaston sulkemisprosessi selvittää varasto-ottotapahtumat vastaanottotapahtumia, joka valitaan nimikkeen malliryhmä varastonarvostusmenetelmän perusteella. Ennen kuin varaston sulkeminen on suoritettu, järjestelmä laskee juoksevan keskimääräisen kustannushinnan, jota käytetään yleensä silloin, kun kirjataan varasto-ottotapahtumat.

Järjestelmä arvioi tämä juoksevaa keskimääräistä kustannushintaa nimikkeen käyttämällä seuraavaa kaavaa: arvioitu hinta = (fyysinen summa + rahoitussumma) ÷ (fyysinen määrä + taloudellinen määrä)

## <a name="using-the-running-average-cost-price"></a>Kustannushinnan käyttökeskiarvon käyttäminen
Seuraavassa taulukossa näkyy, kun järjestelmä kirjaa varastotapahtumat käyttämällä juoksevan keskimääräisen kustannushinnan, ja kun se käyttää, joka määritetään sen sijaan nimikkeen päätietueen kustannushinnan.

| Olosuhteet                                               | Järjestelmä käyttää arvioitua kustannushintaa | Järjestelmä käyttää, joka on nimikkeen päätietueessa määritetty kustannushinta |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Sekä osoittaja\* ja nimittäjän\*\* ovat positiivisia.  | Kyllä                                                      | Nro                                                                |
| Osoittaja\*, nimittäjä\*\*, tai molemmat ovat negatiivisia. | Nro                                                       | Kyllä                                                               |
| Nimittäjä\*\* on 0 (nolla).                        | Nro                                                       | Kyllä                                                               |

\*Osoittaja = (fyysinen summa + summa) \*\*nimittäjä = (fyysinen määrä + taloudellinen määrä) **Huomautus:** Jos **fyysistä arvoa** kohteen vaihtoehto ei ole valittuna, järjestelmä käyttää sekä fyysisenä summana että fyysinen määrä on 0 (nolla). Tietoja tästä vaihtoehdosta on ohjeaiheessa [Sisällytä fyysinen arvo](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Hinnoittelun paisumisen välttäminen
Joissakin harvoissa tapauksissa järjestelmän hintoja useita ongelmia ennen kuin käytössä on tarpeeksi vastaanottoja hinnan pohjalta. Tässä skenaariossa kustannushinnan käyttökeskiarvon arviot saattavat paisua liikaa. Seuraavalla tavalla voit kuitenkin välttää hintojen paisumisen tai pienentää sen vaikutuksia. **Skenaario** Seuraavat tapahtumat ilmenevät nimikkeelle, jolle olet valinnut **Sisällytä fyysinen arvo** -vaihtoehdon:

1.  Vastaanotat määrän 100 rahoituksellisesti hinnalla 100,00 dollaria
2.  Otat varastosta rahoituksellisesti määrän 200.
3.  Vastaanotat määrän 101 fyysisesti hinnalla 202,00 dollaria

Kun tutkit nimikkeen arvioitua kustannushinnan käyttökeskiarvoa, odotat kustannushinnan olevan 1,51 Yhdysvaltain dollaria. Sen sijaan löydät arvioitu keskiarvo USD 102.00, joka perustuu seuraavan kaavan: arvioitu hinta = \[202 + (-100)\] / \[+ 101 (-100)\] = 102 / 1 = 102 hinnoittelun vahvistus Tämä johtuu, 200 nimikettä otetaan rahoituksellisesti vaiheessa 2, kun järjestelmä on hinta 100 kohdetta, ennen kuin käytössä on yhtään vastaavia vastaanottoja. Tämä johtaa negatiiviseen varastoon. Järjestelmä arvioi yksikköhinnan USD 1.00, sitten kun olemme luonnollisesti. mutta kun vastaavat sata vastaanottoa saapuvat, niiden yksikköhinta onkin 2,00 Yhdysvaltain dollaria. **Huomautus:** Vaikka varasto-otot johtavat negatiiviseen varastoon, varasto on positiivinen, kun varasto-oton hinta lasketaan. Siksi käytetään kustannushinnan käyttökeskiarvoa nimikkeen päätietueen kustannushinnan sijaan. Tässä vaiheessa järjestelmä on varaston arvo siirtymä on USD 100.00. Vaikka vastakirjaus muodostuu yli sadasta kappaleesta ja kunkin yksikön vastakirjaus on 1,00 Yhdysvaltain dollari, varastossa on vain yksi kappale. Tästä syystä 100 Yhdysvaltain dollarin vastakirjaus kohdistetaan tähän yhteen kappaleeseen. Tämä taas johtaa arvioidun kustannushinnan liioiteltuun kasvuun. **Huomautus:** Huomaa, että jos skenaarion vaiheet 2 ja 3 tapahtuvat eri järjestyksessä, 200 nimikettä otetaan varastosta 1,51 Yhdysvaltain dollarin yksikköhintaan ja varastoon jää yksi kappale, jonka yksikköhinta on 1,51 Yhdysvaltain dollaria. Koska hinnoittelu voi paisua negatiivisen varaston yhteydessä, sitä on vaikea välttää seuraavissa tapauksissa:

-   Varasto-ottohinnat on arvioitava varaston arvon ja määrän perusteella.
-   Varaston arvoa ja määrää on muokattava varasto-ottojen ja vastaanottojen perusteella.
-   Liiketoimintamalli sallii lähettää tai hinnoitella enemmän kappaleita kuin varastossa on.
-   Jokainen lähetetty vastaanoton arvo ja määrä on hyväksyttävä.

Jos liiketoimintamalli sallii seuraavat käytännöt, voit niiden avulla välttää negatiivisia määriä, jotka mahdollistavat hinnoittelun paisumisen:

-   Jos valitset nimikkeelle **Sisällytä fyysinen arvo** -vaihtoehdon, poista **Fyysinen negatiivinen varasto** -valintaruudun valinta **Nimikemalliryhmät**-sivulla.
-   Jos *et* valitse nimikkeelle **Sisällytä fyysinen arvo** -vaihtoehtoa, poista **Rahoituksellinen negatiivinen varasto** -valintaruudun valinta **Nimikemalliryhmät**-sivulla.

Huomaa lisäksi, että fyysisten tapahtumien määrä sekä fyysisten ja rahoituksellisten hintojen välinen ero rajoittavat fyysisen varaston enimmäisvastakirjausta. Jos kaikki fyysiset tapahtumat päivitetään lopulta taloudellisesti, fyysinen arvo ei voi nousta liian suureksi. Huomaa, että paisumisilmiö pienenee huomattavasti, kun jaksotettu vastakirjaus jaetaan usean varastossa olevan kappaleen välille yhden kappaleen sijaan.


