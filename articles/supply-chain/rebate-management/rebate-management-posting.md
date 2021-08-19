---
title: Ostohyvitysten hallinnan kirjausasetukset
description: Tässä aiheessa käsitellään kirjausprofiilien määrittämistä. Kirjausprofiilien avulla määritetään ostohyvityksen hallinnan laskentarivien kirjausmerkinnät.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 4eb0c38baa0b46c535e9394673d5a046f761ac71a9633edcc6ee7f237ff7691d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725671"
---
# <a name="rebate-management-posting-setup"></a>Ostohyvitysten hallinnan kirjausasetukset

[!include [banner](../includes/banner.md)]

Ostohyvitysten hallinnan kirjausprofiilien avulla määritetään ostohyvityksen hallinnan laskentarivien kirjausmerkinnät. Kun sopimuksen otsikkoon on valittu kirjausprofiili, sitä sovelletaan kaikkiin sopimusriveihin.

Tämä toiminto toimii yritysten (oikeushenkilöiden) välillä. Voit määrittää yrityksen, johon varaukset jaksotetaan ja joka maksaa vaatimukset. Voit myös määrittää eri varausten debet-tilejä ja poiskirjauksen kredit-tilejä kirjauksen lähdeyritystä kohti.

Voit määrittää ostohyvitystenhallinnan kirjausprofiilit asiakkaille ja toimittajille kohdassa **Ostohyvitysten hallinta \> Ostohyvitysten hallinnan kirjausasetukset \> Ostohyvitysten hallinnan kirjausprofiilit**. **Ostohyvitysten hallinnan kirjausprofiilit** -sivulla on luetteloruutu, jossa näkyvät kaikki aiemmin luodut profiilit. Lisätä profiileja luetteloon tai poista niitä ruudukosta työkalurivin painikkeilla.

Tämän ohjeaiheen muut osat kuvaavat, kuinka käytettävissä olevia kenttiä käytetään profiilia luotaessa tai muokatessa.

## <a name="posting-profile-header"></a>Kirjausprofiilin otsikko

Seuraavassa taulukossa kuvataan asetukset, jotka ovat käytettävissä kunkin ostohyvityksen hallinnan kirjausprofiilin otsikko-osassa.

| Kenttä | kuvaus |
|---|---|
| Kirjausprofiili | Anna profiilille yksilöivä nimi. |
| kuvaus | Määritä profiilin kuvaus. |
| Moduuli | Valitse profiiliin liitettyjen ostohyvitysten ja rojaltien moduuli (*Asiakas* tai *Toimittaja*). |
| Laji | Valitse profiilityyppi (*Ostohyvitys* tai *Rojalti*). |
| Maksutyyppi | <p>Tämä kenttä määrittää kirjatun ostohyvityksen tuotoksen muodon.<p><p>Kun **Tyyppi**-kentän arvoksi on määritetty *Ostohyvitys*, seuraavat arvot ovat käytettävissä:</p><ul><li>*Maksa ostoreskontran avulla* – Asiakkaan ostohyvityksen kirjaaminen luo ostohyvityksen asiakkaassa määritetyn maksusuoritustoimittajan toimittajalaskun. Toimittajan ostohyvityksen kirjaaminen luo ostohyvityksen toimittajatilille toimittajalaskun.</li><li>*Asiakkaan vähennykset* – Kun ostohyvitys kirjataan, ostohyvityksen asiakkaalle luodaan asiakkaan vähennyskirjauskansio.</li><li>*Veroalskun asiakkaan vähennykset* – Kun ostohyvitys kirjataan, ostohyvityksen asiakkaalle luodaan vapaatekstilasku.</li><li>*Kaupankäynnin kulut* – Kun ostohyvitys kirjataan, ostohyvityksen asiakkaalle luodaan asiakkaan vähennyskirjauskansio.</li><li>*Raportointi* – Kun ostohyvitys kirjataan, ostohyvityksen asiakkaalle luodaan asiakkaan vähennyskirjauskansio.</li></ul><p>Kun **Tyyppi**-kentän arvoksi on määritetty *Rojalti*, seuraavat arvot ovat käytettävissä:</p><ul><li>*Maksa ostoreskontran avulla* – Ostohyvityksen kirjaaminen luo ostohyvityksen toimittajatilille toimittajalaskun.</li><li>*Raportointi* – Ostohyvityksen kirjaaminen luo ostohyvityksen toimittajatilille toimittajalaskun.</li></ul><p>Lisätietoja on myöhemmässä [Maksutyypit](#payment-types)-osassa. |
| Yhtiö | Valitse yritys (oikeushenkilö), johon varaukset jaksotetaan ja joka maksaa vaatimukset. |

### <a name="payment-types"></a>Maksutyypit

Seuraavassa taulukossa on yhteenveto siitä, miten **Maksutyyppi**-kentän eri asetukset vaikuttavat siihen, mihin maksut kirjataan. Maksut voidaan kirjata asiakastilille, toimittajatilille tai maksusuoritustilille kohdetapahtuman ja ostohyvitystyypin mukaan.

| Maksutyyppi | Kohdetapahtumatyyppi | Ostohyvityksen tyyppi | Maksu koteeseen (laskutustili) |
|---|---|---|---|
| Käytä maksamiseen ostoreskontraa | Toimittajan laskun kirjauskansio | Asiakkaan ostohyvitys | Asiakkaan maksusuorituksen toimittajatili |
| Käytä maksamiseen ostoreskontraa | Toimittajan laskun kirjauskansio | Asiakkaan rojalti | Toimittajanro |
| Käytä maksamiseen ostoreskontraa | Toimittajan laskun kirjauskansio | Toimittajan ostohyvitys | Toimittajanro |
| Asiakkaan vähennykset | Kirjauskansio | Asiakkaan ostohyvitys | Asiakastili |
| Verota laskujen asiakasvähennyksiä | Vapaatekstilasku | Asiakkaan ostohyvitys | Asiakastili |
| Kaupankäynnin kulut | Kirjauskansio | Asiakkaan ostohyvitys | Asiakastili |
| Raportointi | Kirjauskansio | Asiakkaan ostohyvitys | Asiakastili |
| Raportointi | Toimittajan laskun kirjauskansio | Asiakkaan rojalti | Toimittajanro |
| Raportointi | Toimittajan laskun kirjauskansio | Toimittajan ostohyvitys | Toimittajanro |

> [!NOTE]
> Ota huomioon seuraavat seikat, kun määrität [ostohyvitysten hallinnan sopimuksia](rebate-management-deals.md):
>
> - Sopimuksille, joiden **Täsmäytä mennessä** -kentän arvona *Sopimus*, et voi käyttää dynaamista sopimustiliä kirjaamisen aikana. On käytettävä määritettyä asiakas- tai toimittajatiliä.
> - Sopimuksille, joiden **Täsmäytä mennessä** -kentän arvona on *Rivi*, voit käyttää kirjausprofiilia, joka vastakirjaa sopimusrivin dynaamisen sopimustiliin, koska asiakas tai toimittaja määritetään sopimusriviä kohti.

## <a name="posting-fasttab"></a>Kirjauksen pikavälilehti

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kunkin ostohyvityksen hallinnan kirjausprofiilin **Kirjaus**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Luottotyyppi | Valitse, hyvitetäänkö kirjanpitotiliä vai asiakasta. Jos otsikon **Maksutyyppi**-kentän arvoksi on määritetty *Verota laskujen asiakasvähennyksiä*, tämän kentän arvoksi tulee *Kirjanpitotili*. Toimittajan ostohyvitysten osalta tämän kentän arvona on *Kirjanpitotili*. |
| Kredit-tili | Valitse tili, jolle hyvityssummat kirjataan ostohyvitysten yhteydessä. Tätä tiliä käytetään myös vastatilinä, kun ostohyvitys kirjataan asiakkaalle hyvityksenä tai kuluna toimittajalle. |
| Kirjauskansion nimi<br>(**Varaus**-osassa) | Valitse kirjatun varauksen kirjaamisen kirjauskansion nimi. |
| Laji | Valitse, kirjataanko ostohyvitys kirjanpitotilille vai asiakkaalle tai toimittajalle. Jos otsikon **Maksutyyppi**-kentän arvoksi on määritetty *Verota laskujen asiakasvähennyksiä*, tämän kentän arvoksi tulee *Asiakas/Toimittaja*. |
| Käytä tilin lähdettä | <p>Valitse jokin seuraavista:</p><ul><li>*Korjattu tili* – Jos valitset tämän arvon, **Ostohyvitystili**-kentässä on määritettävä tili.</li><li>*Sopimusrivitili* – Käytä ostohyvitysrivillä määritettyä asiakas- tai toimittajatiliä. Voit valita tämän arvon vain sopimuksille, joissa **Täsmäytä mennessä** -kentän arvoksi on määritetty *Rivi* ja sopimusriveille, joissa **Tilikoodi**-kentän arvo on *Taulu*. Se ei koske myyntitilauksiin perustuvia asiakkaan maksuprofiileja tai toimittajan ostohyvitystä.</li></ul> |
| Ostohyvitystili | Tili, jolle todellinen ostohyvityskulu kirjataan. |
| Kirjauskansion nimi<br>(**Ostohyvityksen hallinta** -kenttäryhmässä) | Valitse sen kirjauskansion nimi, johon kirjataan asiakkaalle tai toimittajalle ostohyvityssumman hyvityslasku. Tämä kenttä ei ole käytettävissä, kun otsikon **Maksutyyppi**-kentän arvoksi on määritetty *Verota laskujen asiakasvähennyksiä*. Asiakkaan ostohyvitysten *Päivittäisten* kirjaustyyppien kirjauskansioiden nimet ovat käytettävissä. Asiakkaan rojaltit ja toimittajan ostohyvitykset ovat käytettävissä *Toimittajalaskun kirjauksia* -kirjauskansiotyypin kirjauskansion nimiä. |
| Nimikkeen arvonlisäveroryhmä | Määritä, onko ostohyvitys verotettava. |
| Kirjauskansion nimi<br>(Kohteessa **Poiskirjaus**-kenttäryhmä) | Jos kirjattu ostohyvitys ei ole sama kuin varaus, erotus voidaan kirjata pois. Valitse kirjatun poiskirjauksen kirjaamisen kirjauskansion nimi. |

## <a name="posting-by-company-fasttab"></a>Kirjaus yrityksen mukaan -pikavälilehti

Kunkin ostohyvityksenhallinnan kirjausprofiilin **Kirjaus yrityksen mukaan** -pikavälilehdessä voit määrittää kirjaustilin, jota kukin yritys (oikeushenkilö) käyttää ruudukossa.

Voit lisätä ruudukkoon yrityksiä tai poistaa niitä työkalurivin painikkeiden avulla. Aina kun lisäät rivin ruudukkoon, määritä riville oikeushenkilö määrittämällä **Yritys**-kenttä. **Nimi**-kenttä määritetään tällöin automaattisesti.

Valitse kunkin yrityksen rivi ja syötä sitten seuraavat tiedot ruudukon alla olevia kenttiä käyttäen:

- **Veloitustyyppi** – Valitse, veloitetaanko kirjanpitotiliä vai toimittajaa. Asiakkaan ostohyvitysten ja provisioiden osalta tämän kentän arvona on *Kirjanpitotili*.
- **Debet-tili** – Määritä tili, jolle veloitussumma kirjataan, kun ostohyvityksen varauksia tehdään.
- **Päätili** – Valitse poiskirjausten päätili.
