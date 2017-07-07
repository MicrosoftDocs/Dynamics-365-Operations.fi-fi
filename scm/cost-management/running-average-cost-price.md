---
title: "Kustannushinnan käyttökeskiarvo"
description: "Varaston sulkemisprosessi selvittää varasto-ottotapahtumat vastaanottotapahtumiksi nimikkeen nimikemalliryhmässä valitun varastonarvostusmenetelmän perusteella. Ennen kuin varasto suljetaan, järjestelmä laskee kustannushinnan käyttökeskiarvon, jota käytetään yleensä varasto-ottotapahtumien kirjaamisessa."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a73ce12f1064c44b2af0fa4f33c63f1a6bddab89
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="running-average-cost-price"></a>Kustannushinnan käyttökeskiarvo

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Varaston sulkemisprosessi selvittää varasto-ottotapahtumat vastaanottotapahtumiksi nimikkeen nimikemalliryhmässä valitun varastonarvostusmenetelmän perusteella. Ennen kuin varasto suljetaan, järjestelmä laskee kustannushinnan käyttökeskiarvon, jota käytetään yleensä varasto-ottotapahtumien kirjaamisessa.

Järjestelmä arvioi nimikkeen juoksevan keskimääräisen kustannushinnan seuraavan kaavan avulla: 

Arvioitu hinta = (fyysinen summa + rahoituksellinen summa) / (fyysinen määrä + rahoituksellinen määrä)

## <a name="using-the-running-average-cost-price"></a>Kustannushinnan käyttökeskiarvon käyttäminen
Seuraava taulukko osoittaa, milloin järjestelmä kirjaa varastotapahtumia käyttämällä kustannushinnan käyttökeskiarvoa ja milloin käytetään kustannushintaa, joka on määritetty nimikkeen päätietueessa.

| Olosuhteet                                               | Järjestelmä käyttää arvioitua kustannushinnan käyttökeskiarvoa | Järjestelmä käyttää kustannushintaa, joka on määritetty nimikkeen päätietueessa |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Sekä osoittaja\* että nimittäjä\*\* ovat positiivisia.  | Kyllä                                                      | Nro                                                                |
| Osoittaja\* tai nimittäjä\*\* on negatiivinen tai molemmat ovat negatiivisia. | Nro                                                       | Kyllä                                                               |
| Nimittäjä\*\* on 0 (nolla).                        | Nro                                                       | Kyllä                                                               |

\*Osoittaja = (fyysinen summa + rahoituksellinen summa) \*\* nimittäjä = (fyysinen määrä + rahoituksellinen määrä) 

**Huomautus:** Jos nimikkeelle ei ole valittu **Sisällytä fyysinen arvo** -vaihtoehtoa, järjestelmä käyttää nollaa (0) sekä fyysiselle summalle että fyysiselle määrälle. Tietoja tästä vaihtoehdosta on ohjeaiheessa [Sisällytä fyysinen arvo](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Hinnoittelun paisumisen välttäminen
Harvoissa tapauksissa järjestelmä hinnoittelee useita varasto-ottoja, ennen kuin käytössä on tarpeeksi vastaanottoja, joihin hinnan voi perustaa. Tässä skenaariossa kustannushinnan käyttökeskiarvon arviot saattavat paisua liikaa. Seuraavalla tavalla voit kuitenkin välttää hintojen paisumisen tai pienentää sen vaikutuksia. **Skenaario** Seuraavat tapahtumat ilmenevät nimikkeelle, jolle olet valinnut **Sisällytä fyysinen arvo** -vaihtoehdon:

1.  Vastaanotat määrän 100 rahoituksellisesti hinnalla 100,00 dollaria
2.  Otat varastosta rahoituksellisesti määrän 200.
3.  Vastaanotat määrän 101 fyysisesti hinnalla 202,00 dollaria

Kun tutkit nimikkeen arvioitua kustannushinnan käyttökeskiarvoa, odotat kustannushinnan olevan 1,51 Yhdysvaltain dollaria. Seuraavan kaavan mukaan kustannushinnan käyttökeskiarvo onkin 102,00 Yhdysvaltain dollaria: arvioitu hinta = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 / 1 = 102 hinnoittelun vahvistus. Tämä johtuu siitä, että kun vaiheessa 2 varastosta otetaan rahoituksellisesti 200 nimikettä, järjestelmän on pakko hinnoitella 100 nimikettä, ennen kuin sen käytössä on yhtään vastaavia vastaanottoja. Tämä johtaa negatiiviseen varastoon. Järjestelmä arvioi yksikköhinnaksi 1,00 Yhdysvaltain dollari, kuten on odotettua, mutta kun vastaavat sata vastaanottoa saapuvat, niiden yksikköhinta onkin 2,00 Yhdysvaltain dollaria. 

**Huomautus:** Vaikka varasto-otot johtavat negatiiviseen varastoon, varasto on positiivinen, kun varasto-oton hinta lasketaan. Siksi käytetään kustannushinnan käyttökeskiarvoa nimikkeen päätietueen kustannushinnan sijaan. Tällöin järjestelmän varaston arvon vastakirjaus on 100,00 Yhdysvaltain dollaria. Vaikka vastakirjaus muodostuu yli sadasta kappaleesta ja kunkin yksikön vastakirjaus on 1,00 Yhdysvaltain dollari, varastossa on vain yksi kappale. Tästä syystä 100 Yhdysvaltain dollarin vastakirjaus kohdistetaan tähän yhteen kappaleeseen. Tämä taas johtaa arvioidun kustannushinnan liioiteltuun kasvuun. 

**Huomautus:** Huomaa, että jos skenaarion vaiheet 2 ja 3 tapahtuvat eri järjestyksessä, 200 nimikettä otetaan varastosta 1,51 Yhdysvaltain dollarin yksikköhintaan ja varastoon jää yksi kappale, jonka yksikköhinta on 1,51 Yhdysvaltain dollaria. Koska hinnoittelu voi paisua negatiivisen varaston yhteydessä, sitä on vaikea välttää seuraavissa tapauksissa:

-   Varasto-ottohinnat on arvioitava varaston arvon ja määrän perusteella.
-   Varaston arvoa ja määrää on muokattava varasto-ottojen ja vastaanottojen perusteella.
-   Liiketoimintamalli sallii lähettää tai hinnoitella enemmän kappaleita kuin varastossa on.
-   Jokainen lähetetty vastaanoton arvo ja määrä on hyväksyttävä.

Jos liiketoimintamalli sallii seuraavat käytännöt, voit niiden avulla välttää negatiivisia määriä, jotka mahdollistavat hinnoittelun paisumisen:

-   Jos valitset nimikkeelle **Sisällytä fyysinen arvo** -vaihtoehdon, poista **Fyysinen negatiivinen varasto** -valintaruudun valinta **Nimikemalliryhmät**-sivulla.
-   Jos *et* valitse nimikkeelle **Sisällytä fyysinen arvo** -vaihtoehtoa, poista **Rahoituksellinen negatiivinen varasto** -valintaruudun valinta **Nimikemalliryhmät**-sivulla.

Huomaa lisäksi, että fyysisten tapahtumien määrä sekä fyysisten ja rahoituksellisten hintojen välinen ero rajoittavat fyysisen varaston enimmäisvastakirjausta. Jos kaikki fyysiset tapahtumat päivitetään lopulta taloudellisesti, fyysinen arvo ei voi nousta liian suureksi. Huomaa, että paisumisilmiö pienenee huomattavasti, kun jaksotettu vastakirjaus jaetaan usean varastossa olevan kappaleen välille yhden kappaleen sijaan.




