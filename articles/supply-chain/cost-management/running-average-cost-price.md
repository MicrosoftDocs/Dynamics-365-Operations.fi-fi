---
title: Kustannushinnan käyttökeskiarvo
description: Varaston sulkemisprosessi selvittää varasto-ottotapahtumat vastaanottotapahtumiksi nimikkeen nimikemalliryhmässä valitun varastonarvostusmenetelmän perusteella. Ennen kuin varasto suljetaan, järjestelmä laskee kustannushinnan käyttökeskiarvon, jota käytetään yleensä varasto-ottotapahtumien kirjaamisessa.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d324324312ce9e47b07de8e3de952b8d7c53647
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672175"
---
# <a name="running-average-cost-price"></a>Kustannushinnan käyttökeskiarvo

[!include [banner](../includes/banner.md)]

Varaston sulkemisprosessi selvittää varasto-ottotapahtumat vastaanottotapahtumiksi nimikkeen nimikemalliryhmässä valitun varastonarvostusmenetelmän perusteella. Ennen kuin varasto suljetaan, järjestelmä laskee kustannushinnan käyttökeskiarvon, jota käytetään yleensä varasto-ottotapahtumien kirjaamisessa.

Järjestelmä arvioi nimikkeen juoksevan keskimääräisen kustannushinnan seuraavan kaavan avulla:

Arvioitu hinta = (fyysinen summa + rahoituksellinen summa) / (fyysinen määrä + rahoituksellinen määrä)

## <a name="default-item-cost"></a>Nimikkeen oletuskustannus

Vapautetun tuotteen oletuskustannus voidaan konfiguroida **vapautetun tuotteen tietosivulla** kahdella tavalla:

- Luo vakiokustannus valitsemalla **Nimikkeen hinta** **Määritys**-ryhmässä toimintoruudun **Kustannusten hallinta** -välilehdessä. Jos käytät tätä menetelmää, sinun on käytettävä standardikustannusten kustannuslaskelmaversiota ja kustannus on aktivoitava.
- Määritä vapautetun tuotteen nimikkeen oletuskustannushinta syöttämällä arvo **Kustannustenhallinta**-pikavälilehden **Hinta**-kenttään.

Hinnan kirjoittamisen tai luomisen lisäksi voit valita **Vapautetun tuotteen tiedot** -sivun **Kustannustenhallinta**-pikavälilehden **Käytä viimeisintä kustannushintaa** -valintaruudun. Tällöin järjestelmä päivittää **Hinta**-kentän automaattisesti , kun kirjaat taloudellisen päivityksen. Jos esimerkiksi kirjaat ostotilauslaskun, kenttään määritetään laskun ostohinta.

Jos kustannushinta on käytössä aktiivisessa kustannuslaskelmaversiossa ja määrität hinnan **Kustannusten hallinta** -pikavälilehdessä, järjestelmä käyttää aktiivisen kustannuslaskelmaversion hintaa ennen **Kustannusten hallinta** -pikavälilehdissä määritettyä hintaa.

## <a name="using-the-running-average-cost-price"></a>Kustannushinnan käyttökeskiarvon käyttäminen

Seuraava taulukko osoittaa, milloin järjestelmä kirjaa varastotapahtumia käyttämällä kustannushinnan käyttökeskiarvoa ja milloin käytetään kustannushintaa, joka on määritetty nimikkeen päätietueessa.

| Olosuhteet | Järjestelmä käyttää arvioitua kustannushinnan käyttökeskiarvoa | Järjestelmä käyttää nimikkeen oletuskustannushintaa |
| --- | --- | --- |
| Sekä osoittaja\* että nimittäjä\*\* ovat positiivisia. | Kyllä | Ei |
| Osoittaja\* tai nimittäjä\*\* on negatiivinen tai molemmat ovat negatiivisia. | Ei | Kyllä |
| Nimittäjä\*\* on 0 (nolla). | Ei | Kyllä |

\* Osoittaja = (fyysinen summa + rahoitussumma)  
\*\* Nimittäjä = (fyysinen määrä + rahoitusmäärä)

> [!NOTE]
> Jos nimikkeelle ei ole valittu **Sisällytä fyysinen arvo** -vaihtoehtoa, järjestelmä käyttää nollaa (0) sekä fyysiselle summalle että fyysiselle määrälle. Tietoja tästä vaihtoehdosta on ohjeaiheessa [Sisällytä fyysinen arvo](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Hinnoittelun paisumisen välttäminen

Harvoissa tapauksissa järjestelmä hinnoittelee useita varasto-ottoja, ennen kuin käytössä on tarpeeksi vastaanottoja, joihin hinnan voi perustaa. Tässä skenaariossa kustannushinnan käyttökeskiarvon arviot saattavat paisua liikaa. Seuraavalla tavalla voit kuitenkin välttää hintojen paisumisen tai pienentää sen vaikutuksia.

**Skenaario:** Seuraavat tapahtumat ilmenevät nimikkeelle, jolle olet valinnut **Sisällytä fyysinen arvo** -vaihtoehdon:

1. Vastaanotat määrän 100 rahoituksellisesti hinnalla 100,00 dollaria
2. Otat varastosta rahoituksellisesti määrän 200.
3. Vastaanotat määrän 101 fyysisesti hinnalla 202,00 dollaria

Kun tutkit nimikkeen arvioitua kustannushinnan käyttökeskiarvoa, odotat kustannushinnan olevan 1,51 Yhdysvaltain dollaria. Sen sijaan käytössäsi on arvioitu käyttökeskiarvo 102,00 USD, joka perustuu seuraavaan kaavaan:

Arvioitu hinta = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

Hinnoittelu voimistuu, koska kun vaiheessa 2 varastosta otettavaa nimikettä on 200, järjestelmän on hinnoiteltava 100 nimikettä, ennen kuin sillä on vastaavia vastaanottoja. Tämä johtaa negatiiviseen varastoon. Järjestelmä arvioi yksikköhinnaksi 1,00 Yhdysvaltain dollaria, kuten on odotettua. mutta kun vastaavat sata vastaanottoa saapuvat, niiden yksikköhinta onkin 2,00 Yhdysvaltain dollaria.

> [!NOTE]
> Vaikka varasto-otot johtavat negatiiviseen varastoon, varasto on positiivinen, kun varasto-oton hinta lasketaan. Siksi käytetään kustannushinnan käyttökeskiarvoa nimikkeen päätietueen kustannushinnan sijaan. Tällöin järjestelmän varaston arvon vastakirjaus on 100,00 Yhdysvaltain dollaria. Vaikka vastakirjaus muodostuu yli sadasta kappaleesta ja kunkin yksikön vastakirjaus on 1,00 Yhdysvaltain dollari, varastossa on vain yksi kappale. Tästä syystä 100 Yhdysvaltain dollarin vastakirjaus kohdistetaan tähän yhteen kappaleeseen. Tämä taas johtaa arvioidun kustannushinnan liioiteltuun kasvuun.
>
> Huomaa, että jos skenaarion vaiheet 2 ja 3 tapahtuvat eri järjestyksessä, 200 nimikettä otetaan varastosta 1,51 Yhdysvaltain dollarin yksikköhintaan ja varastoon jää yksi kappale, jonka yksikköhinta on 1,51 Yhdysvaltain dollaria. Koska hinnoittelu voi paisua negatiivisen varaston yhteydessä, sitä on vaikea välttää seuraavissa tapauksissa:
>
> - Varasto-ottohinnat on arvioitava varaston arvon ja määrän perusteella.
> - Varaston arvoa ja määrää on muokattava varasto-ottojen ja vastaanottojen perusteella.
> - Liiketoimintamalli sallii lähettää tai hinnoitella enemmän kappaleita kuin varastossa on.
> - Jokainen lähetetty vastaanoton arvo ja määrä on hyväksyttävä.

Jos liiketoimintamalli sallii seuraavat käytännöt, voit niiden avulla välttää negatiivisia määriä, jotka mahdollistavat hinnoittelun paisumisen:

- Jos valitset nimikkeelle **Sisällytä fyysinen arvo** -vaihtoehdon, poista **Fyysinen negatiivinen varasto** -valintaruudun valinta **Nimikemalliryhmät**-sivulla.
- Jos **et** valitse nimikkeelle **Sisällytä fyysinen arvo** -vaihtoehtoa, poista **Rahoituksellinen negatiivinen varasto** -valintaruudun valinta **Nimikemalliryhmät**-sivulla.

Huomaa lisäksi, että fyysisten tapahtumien määrä sekä fyysisten ja rahoituksellisten hintojen välinen ero rajoittavat fyysisen varaston enimmäisvastakirjausta. Jos kaikki fyysiset tapahtumat päivitetään lopulta taloudellisesti, fyysinen arvo ei voi nousta liian suureksi. Huomaa, että paisumisilmiö pienenee huomattavasti, kun jaksotettu vastakirjaus jaetaan usean varastossa olevan kappaleen välille yhden kappaleen sijaan.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Nollakustannushinnan välttäminen otoissa

Kun **Sisällytä fyysinen arvo** -asetusta ei ole valittu **Nimikemalliryhmä**-sivulla, varasto-oton kustannushinta voi olla nolla, jos varastossa ei ole taloudellisesti päivitettyjä vastaanottoja. Vältä tämä skenaario harkitsemalla seuraavia vaihtoehtoja:

- Valitse **Sisällytä fyysinen arvo** -asetus **Nimikemalliryhmä**-sivulla. Tämä vaihtoehto estää varasto-oton nollakustannushinnan, jos vastaanotto päivitetään fyysisesti. Jos negatiivista fyysistä varastoa ei sallita, varasto-otot laskevat juoksevan keskiarvon fyysisesti päivitettyjen tapahtumien mukaan.
- Luo nimikkeen oletuskustannushinta aktivoimalla kustannuslaskelmaversio, jolla on standardikustannus, tai lisää hinta **Vapautetun tuotteen tiedot** -sivun **Kustannustenhallinta**-pikavälilehteen. Tämä vaihtoehto on paras, kun **Sisällytä fyysinen arvo** -valintaa ei ole valittu **Nimikemalliryhmä**-sivulla, koska järjestelmän käytössä on aina varahinta.
- Valitse **Käytä viimeisintä kustannushintaa** - vaihtoehto **Vapautetun tuotteen tiedot** -sivun **Kustannustenhallinta**-pikavälilehdessä. Tämä vaihtoehto pitää **Hinta**-kentän ajan tasalla aina, kun vastaanotto päivitetään taloudellisesti. Jos valitset tämän vaihtoehdon, mutta et määritä oletushintaa tai aktivoi kustannusta vakiokustannuslaskelmaversiossa, varasto-otossa voi edelleen olla nollakustannus.

Jos varasto-ottotapahtumien kustannukset ovat nolla, *varaston sulkemis- ja oikaisuprosessi* korjaa kustannushinnan luomalla oikaisun, kun vastaanotot on päivitetty kirjanpitoon. Muista, että tilikausi, jolloin päivitys tapahtuu, saattaa olla eri kuin tilikausi, jolloin nimikkeet on vastaanotettu tai lähetetty fyysisesti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
