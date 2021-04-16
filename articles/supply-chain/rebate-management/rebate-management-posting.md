---
title: Ostohyvitysten hallinnan kirjausasetukset
description: Tässä aiheessa käsitellään kirjausprofiilien määrittämistä. Kirjausprofiilien avulla määritetään ostohyvityksen hallinnan laskentarivien kirjausmerkinnät.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: e79feb567a48d08a9063bf20cface3c5c7fe8ecc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831743"
---
# <a name="rebate-management-posting-setup"></a>Ostohyvitysten hallinnan kirjausasetukset

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

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
| Moduuli | Valitse profiiliin liitettyjen ostohyvitysten ja rojaltien tyyppi (*Asiakas* tai *Toimittaja*). |
| Laji | Valitse profiilityyppi (*Ostohyvitys* tai *Rojalti*). |
| Maksutyyppi | <p>Tämä kenttä määrittää kirjatun ostohyvityksen tuotoksen muodon.<p><p>Kun **Tyyppi**-kentän arvoksi on määritetty *Ostohyvitys*, seuraavat arvot ovat käytettävissä:</p><ul><li>*Ei mitään* – Oletuskirjaustyyppiä ei ole. Siksi tyyppi on määritettävä käsittelyn aikana.</li><li>*Maksa ostoreskontran avulla* – Ostohyvityksen kirjaaminen luo ostohyvityksen asiakkaassa määritetyn maksusuoritustoimittajan toimittajalaskun.</li><li>*Asiakkaan vähennykset* – Kun ostohyvitys kirjataan, ostohyvityksen asiakkaalle luodaan asiakkaan vähennyskirjauskansio.</li><li>*Veroalskun asiakkaan vähennykset* – Kun ostohyvitys kirjataan, ostohyvityksen asiakkaalle luodaan vapaatekstilasku.</li><li>*Kaupankäynnin kulut* – Kun ostohyvitys kirjataan, ostohyvityksen asiakkaalle luodaan asiakkaan vähennyskirjauskansio.</li><li>*Raportointi* – Kun ostohyvitys kirjataan, ostohyvityksen asiakkaalle luodaan asiakkaan vähennyskirjauskansio.</li></ul><p>Kun **Tyyppi**-kentän arvoksi on määritetty *Rojalti*, seuraavat arvot ovat käytettävissä:</p><ul><li>*Ei mitään* – Oletuskirjaustyyppiä ei ole. Siksi tyyppi on määritettävä käsittelyn aikana.</li><li>*Maksa ostoreskontran avulla* – Ostohyvityksen kirjaaminen luo ostohyvityksen toimittajatilille toimittajalaskun.</li><li>*Raportointi* – Ostohyvityksen kirjaaminen luo ostohyvityksen toimittajatilille toimittajalaskun.</li></ul><p>Lisätietoja on myöhemmässä [Maksutyypit](#payment-types)-osassa. |
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
> - Sopimuksille, joiden **Täsmäytä mennessä** -kentän arvona on *Rivi*, voit käyttää kirjausprofiilia, joka vastakirjaa sopimusrivin dynaamisen sopimustiliin, koska asiakas määritetään sopimusriviä kohti.

## <a name="posting-fasttab"></a>Kirjauksen pikavälilehti

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kunkin ostohyvityksen hallinnan kirjausprofiilin **Kirjaus**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Luottotyyppi | Valitse, hyvitetäänkö kirjanpitotiliä vai asiakasta tai toimittajaa. |
| Kredit-tili | Tili, jolle hyvityssummat kirjataan ostohyvitysten yhteydessä. Tätä tiliä käytetään myös veloitustilinä, kun ostohyvitys kirjataan asiakkaalle hyvityksenä. |
| Kirjauskansion nimi<br>(**Varaus**-osassa) | Valitse kirjatun varauksen kirjaamisen kirjauskansion nimi. |
| Laji | Valitse, kirjataanko ostohyvitys kirjanpitotilille vai asiakkaalle tai toimittajalle. Jos otsikon **Maksutyyppi**-kentän arvoksi on määritetty *Verota laskujen asiakasvähennyksiä*, tämän kentän arvoksi tulee *Asiakas/Toimittaja*. |
| Käytä tilin lähdettä | <p>Valitse jokin seuraavista:</p><ul><li>*Ei mitään* – Jos valitset tämän arvon, **Ostohyvitystili**-kentässä on määritettävä tili.</li><li>*Sopimustili* – Käytä ostohyvitysrivillä määritettyä asiakas- tai toimittajatiliä. Voit valita tämän arvon vain sopimuksille, joissa **Täsmäytä mennessä** -kentän arvoksi on määritetty *Rivi* ja sopimusriveille, joissa **Tilikoodi**-kentän arvo on *Taulu*. Se ei koske asiakkaan rojaltien kirjausprofiileja.</li></ul> |
| Ostohyvitystili | Tili, jolle todellinen ostohyvityskulu kirjataan. |
| Kirjauskansion nimi<br>(**Ostohyvitysten hallinta** -osassa) | Valitse sen kirjauskansion nimi, johon kirjataan asiakkaalle ostohyvityssumman hyvityslasku. Tämä kenttä ei ole käytettävissä, kun otsikon **Maksutyyppi**-kentän arvoksi on määritetty *Verota laskujen asiakasvähennyksiä*. |
| Nimikkeen arvonlisäveroryhmä | Määritä, onko ostohyvitys verotettava. |
| Kirjauskansion nimi<br>(**Kirjaa pois** -osassa) | Jos kirjattu ostohyvitys ei ole sama kuin varaus, erotus voidaan kirjata pois. Valitse kirjatun poiskirjauksen kirjaamisen kirjauskansion nimi. |

## <a name="posting-by-company-fasttab"></a>Kirjaus yrityksen mukaan -pikavälilehti

Kunkin ostohyvityksenhallinnan kirjausprofiilin **Kirjaus yrityksen mukaan** -pikavälilehdessä voit määrittää kirjaustilin, jota kukin yritys (oikeushenkilö) käyttää ruudukossa.

Voit lisätä ruudukkoon yrityksiä tai poistaa niitä työkalurivin painikkeiden avulla. Aina kun lisäät rivin ruudukkoon, määritä riville oikeushenkilö määrittämällä **Yritys**-kenttä. **Nimi**-kenttä määritetään tällöin automaattisesti.

Valitse kunkin yrityksen rivi ja syötä sitten seuraavat tiedot ruudukon alla olevia kenttiä käyttäen:

- **Veloitustyyppi** – Valitse, veloitetaanko kirjanpitotiliä vai asiakasta tai toimittajaa.
- **Debet-tili** – Määritä tili, jolle veloitussumma kirjataan, kun ostohyvityksen varauksia tehdään.
- **Päätili** – Valitse poiskirjausten päätili.
