---
title: Suunnittelun muutosten hallinnan usein kysytyt kysymykset
description: Tässä artikkelissa on vastauksia suunnittelun muutosten hallinnan usein kysyttyihin kysymyksiin.
author: t-benebo
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-25
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 16d29fa6485bae866a5209a855dfb928e8bc4783
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870779"
---
# <a name="engineering-change-management-faq"></a>Suunnittelun muutosten hallinnan usein kysytyt kysymykset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on vastauksia suunnittelun muutosten hallinnan usein kysyttyihin kysymyksiin.

## <a name="should-i-track-the-version-in-transactions"></a>Pitäisikö seurata tapahtumien versiota?

Kun luot suunnittelumuutosluokan, **Suunnittelun muutoksen luokan tiedot** -sivulla on vaihtoehto, jonka nimi on **Version seuranta tapahtumissa**. Mikä tämä asetus on ja mitä se tekee?

- Jos määrität **Version seuranta tapahtumissa** arvoksi *Kyllä*, **Dimensioryhmä**-kenttä suodatetaan siten, että siinä näkyvät vain dimensioryhmät, joissa versio on aktiivinen dimensio.
- Jos määrität **Version seuranta tapahtumissa** arvoksi *Ei*, **Dimensioryhmä**-kenttä suodatetaan siten, että siinä näkyvät vain dimensioryhmät, joissa versiodimentio **ei** ole aktiivinen dimensio.

### <a name="if-you-track-the-version-in-transactions"></a>Jos seuraat tapahtumien versiota

Jos olet valinnut suunnitteluluokissa dimensioryhmän, jossa versio on aktiivinen dimensio, voit seurata tämän luokan tuotteiden tapahtumien versioita. Tässä tapauksessa suunnittelutuote on päätuote ja tuotteen kukin versio on tuotevariantti, joka käyttää version dimensiota. Muita dimensioita voidaan käyttää yhdessä versiodimension kanssa.

Tässä tapauksessa kutakin suunnitteluversiota käsitellään muuttujana kaikissa prosesseissa. Jos tapahtumassa on tietty muuttuja (jotta voit määrittää, mikä muuttuja on myyty tai ostettu), sinun on hallittava kunkin version varastoa, pääsuunnittelu suunnittelee toimituksen kullekin versiolle ja niin edelleen. Jos poistat version käytöstä markkinoilta, voimassaolon alkamis- ja päättymispäivämäärät on oikaistava manuaalisesti siten, että ne vastaavat muutosta. Varastoa on myös hallittava sen varmistamiseksi,että varastoissa ei ole nimikkeiden käyttämättömiä versioita.

Vaikka tämä vaihtoehto vaatiikin enemmän hallintotyötä, se on suositeltava, jos tarvitset erinomaista jäljitettävyyttä kussakin tapahtumassa käytetyistä versioista.

### <a name="if-you-dont-track-the-version-in-transactions"></a>Jos et seuraa tapahtumien versiota

Jos olet valinnut suunnitteluluokissa dimensioryhmän, jossa versio **ei** ole aktiivinen dimensio, **et** voi seurata tämän luokan tuotteiden tapahtumien versioita. Täss tapauksessa jos et käytä muuta dimensiota, suunnittelutuote on erillinen tuote. Tuote on silti versioitu, ja voit hallita tiettyjen versioiden (esimerkiksi tuoterakenteen \[BOM] ja reitityksen) tietoja, mutta et voi jäljittää kussakin tapahtumassa käytettyä tiettyä versiota. Voimassaolon alkamis- ja päättymispäivät ilmaisevat kunkin version voimassaolon.

Tätä vaihtoehtoa on paljon helpompi hallita, sillä jos haluat vaihtaa versiosta toiseen, sinun on tehtävä tarvittavat muutokset muutostilaukseen ja päivitettävä sitten suunnitteluversion voimassaolon alkamis- ja päättymispäivämäärät. Tuotantoprosessi poimii sitten tuotteen (ja sen tietyn version) vaadittavan tuoterakenteen ja reitityksen.

Useimmat organisaatiot valitsevat tämän vaihtoehdon, koska siinä on käytössä versio- ja muutostenhallinta, mutta ei lisää kunkin tapahtuman, varaston ja pääsuunnittelun aikana käytettävissä olevan version lisäkustannusta.

## <a name="which-fields-are-copied-from-the-released-item-template"></a>Mitkä kentät kopioidaan vapautetusta nimikemallista?

Kun suunnitteluyritys luo suunnittelutuotteen, tuote luodaan suunnitteluyrityksen vapautettuna tuotteena. Luotu vapautettu tuote perustuu valittuun *vapautettuun nimikemalliin*. (Vapautettu nimikemalli on itsekin olemassa oleva vapautettu tuote.) Vapautettua nimikemallia käytetään myös, kun tuote vapautetaan toimivaan yritykseen. Vapautetun nimikkeen malli määrittää joka tapauksessa suurimman osan vapautetun tuotteen kenttäarvoista, ja arvot tulevat liitetyltä **Vapautetun tuotteen tiedot** -sivulta.

Seuraavissa taulukoissa näkyvät kentät, jotka kopioidaan näiden prosessien aikana.

| Pikavälilehti | Kentät, jotka kopioidaan suunnitteluyrityksen tuoteluonnissa | Kentät, jotka kopioidaan vapautuksessa operatiiviselle yritykselle |
|---|---|---|
| **Yleistä** | Kaikki **Hallinta**-osan kentät | Samat kentät, jotka kopioidaan suunnitteluyritykselle |
| **Osto** | Kaikki kentät | Kaikki kentät paitsi **Yksikkö** |
| **Myynti** | Kaikki seuraavien osien kentät: **Myyntitilaus**, **Hallinta**, **Verotus**, **Hinnanpäivitys**, **Perusmyyntihinta**, **Kulut**, **Alennukset** ja **Vaihtoehtoinen tuote** | Kaikki samat kentät, jotka kopioidaan suunnitteluyritykselle, paitsi **Yksikkö** |
| **Ulkomaankauppa** | Kaikki kentät | Kaikki kentät |
| **Varastonhallinta** | Kaikki kentät ja osat *paitsi* **Fyysiset mitat** ja **Todellinen paino** | Kaikki samat kentät, jotka kopioidaan suunnitteluyritykselle, paitsi **Yksikkö** |
| **Kehittäjä**, **Suunnitelma**, **Kustannusten hallinta**, **Projektien hallinta**, **Taloushallinnon dimensio** ja **Varasto** | Kaikki kentät | Kaikki kentät paitsi **Tuoterakenneyksikkö** |
| **Tuotevariantit** | Kaikki **Oletustuotevariantt**-osan kentät | Samat kentät, jotka kopioidaan suunnitteluyritykselle |

Edellisessä taulukossa näkyvien kenttien lisäksi kaikki oletustilausasetukset kopioidaan vapautetusta nimikemallista silloin, kun tuote luodaan suunnitteluyhtiössä sekä kun se vapautetaan operatiiviseen yritykseen. (Voit tarkastella vapautetun nimikemallin oletustilausasetuksia avaamalla asianmukaisen **Vapautetun tuotteen tiedot** -sivun ja valitsemalla sitten toimintoruudun **Varastonhallinta**-välilehdessä **Oletustilausasetukset**.)

> [!NOTE]
>
> - Yksikön oletusarvo tulee mallista.
> - Kun vähittäismyyjät käyttävät Dynamics 365 Commerce -toimintoja, kun määrität tuotteeseen vähittäismyyntiluokan, vähittäismyyntiluokka määrittää oletusarvoja moniin vapautetun tuotteen tason kenttiin. Nämä oletusarvot korvaavat oletusarvot, jotka malli on jo määrittänyt tai jotka on kopioitu suunnittelusta.

## <a name="should-i-create-a-separate-legal-entity-for-engineering-products-or-use-an-existing-legal-entity"></a>Pitäisikö luoda erillinen yritys tuotteiden suunnittelua varten vai käyttää olemassa olevaa yritystä?

Liiketoimintavaatimukset määrittävät, luodaanko uusi yritys tuotteiden suunnittelua varten.

Luomalla erillisen suunnitteluyrityksen voit pitää suunnittelutiedot erillään toisistaan ja lisätä sitten muutoksia tarpeen mukaan paikallisissa operatiivisissa yrityksissä. Näin voit saavuttaa seuraavat tavoitteet:

- Säilytä erillinen yritys, jossa suunnittelutuotteet luodaan ja niitä hallitaan.
- Estä suunnittelutuotteita näkymästä yhdessä muiden vapautettujen tuotteiden kanssa, kunnes ne ovat valmiita ja vapautettuja.
- Erota selkeästi tiedot, jotka ovat riippuvaisia suunnittelusta ja paikallisista tiedoista.

Aiemmin luotua yritystä kannattaa kuitenkin käyttää suunnitteluyrityksenä, jos seuraavat kohdat koskevat sinua:

- Järjestelmässäsi on vain yksi yritys ja/tai suunnittelussa olevien tuotteiden selkeä erottelu ei ole tarpeen.
- Et halua kopioida joitakin tietoja, kuten resurssiryhmiä, resursseja, toimintoja ja (mahdollisesti) sivustoja.

## <a name="what-is-the-nomenclature-for-engineering-versions-and-variants"></a>Mikä on suunnitteluversioiden ja -muuttujien nimikkeistö?

Suunnittelutuotteiden ja tuotemuuttujien nimikkeistö toimii seuraavasti:

- Suunnittelutuotteessa (eli erillisessä tuotteessa, jos dimensioita ei käytetä tai päätuotteessa, jos käytössä on dimensio), numerosäännön nimikkeistö määritetään suunnittelutuotteen luokassa. Siellä käytettävissä on myös numerosarja, tekstivakiot sekä määritteiden nimet ja arvot.
- Jokaisen suunnittelutuotteen muuttujan osalta (jos suunnittelutuote on päätuote, muuttujat määritetään suunnittelutuoteluokassa, jossa määrität dimensioryhmän), kunkin muuttujan numerosäännön nimikkeistö määritetään dimensioryhmässä. Tässä tapauksessa voit käyttää päätuotetunnusta sekä dimensioarvoja ja nimiä.
