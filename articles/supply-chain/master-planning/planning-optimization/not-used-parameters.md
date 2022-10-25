---
title: Parametrit, joita suunnittelun optimointi ei käytä
description: Tässä artikkelissa on luettelo parametreistä, joita suunnittelun optimointi ei ota huomioon sen toiminnan aikana.
author: t-benebo
ms.date: 09/02/2021
ms.topic: article
ms.search.form: ReqParameters, ReqGroup, ReqItemTable, ReqPlanSched, EcoResProductDetailsExtended, InventItemOrderSetup, WorkCalendarTable, PdsDispositionMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-29
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: db8a8e929bf75c4d1dac0c1b0a7cbc848ff291a9
ms.sourcegitcommit: b3579ac62e1ea15664a114abcc2409cad76d4f19
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/14/2022
ms.locfileid: "9682665"
---
# <a name="parameters-not-used-by-planning-optimization"></a>Parametrit, joita suunnittelun optimointi ei käytä

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa on luettelo parametreistä, joita suunnittelun optimointi ei ota huomioon sen toiminnan aikana. Suunnittelupalvelu saattaa ohittaa parametrin, jos esimerkiksi siihen liittyviä toimintoja ei vielä tueta. Parametri saattaa myös olla vanhentunut toiminnallisten muutosten vuoksi.

Seuraavissa osiossa on luettelo parametreista, joita suunnittelun optimointi ei käytä tietyillä sivuilla. Ne selittävät myös, miksi kutakin parametria ei käytetä.

## <a name="master-planning-parameters-page"></a>Pääsuunnittelun parametrit -sivu

Suunnittelun optimointi ei käytä seuraavia parametreja tai asetuksia **Pääsuunnittelun parametrit** -sivulla:

- **Yleinen**-välilehti:

  - **Nykyinen ennustesuunnitelma** – Odottaa *ennusteiden* tukea.
  - **Nykyinen staattinen pääsuunnitelma** – Odottaa *Kopioi staattinen dynaamiseen suunnitelmaan* -asetuksen tukea.
  - **Nykyinen dynaaminen pääsuunnitelma** – Odottaa *Kopioi staattinen dynaamiseen suunnitelmaan* -asetuksen tukea.
  - **Kopioi valmis ja päivitetty staattinen pääsuunnitelma dynaamiseen pääsuunnitelmaan** – Odottaa *Kopioi staattinen dynaamiseen suunnitelmaan* -asetuksen tukea.
  - **Laskettujen viiveiden alkamisaika** – Odottaa *Lasketut viiveet* -asetuksen tukea.
  - **Käytä dynaamisia negatiivisia päiviä** – Suunnittelun optimointi käyttää aina *Dynaamiset negatiiviset päivät* -menetelmää.
  - **Tämän päivän päivämäärä** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Välimuistin käyttö** – Microsoft Azure -tilauksen kokoonpano käsittelee suorituskykypisteet.
  - **Lisätyöaseman tehtävänipun tehtävien määrä** – Azure-tilauskokoonpano käsittelee suorituskykypisteet.
  - **Esikäsittely: Suodata automaattisesti kohteilla, joilla on suora kysyntä** – Azure-tilauskokoonpano käsittelee suorituskykypisteet.
  - **Jälkikäsittely: Suodata automaattisesti kohteilla, joilla on suora kysyntä** – Azure-tilauskokoonpano käsittelee suorituskykypisteet.
  - **Vahvistusmyyntirakenteen tilausten määrä** – Azure-tilauskokoonpano käsittelee suorituskykypisteet.
  - **Säikeiden määrä** – Azure-tilauskokoonpano käsittelee suorituskykypisteet.
  - **Suunnitteluprosessin aikakatkaisu minuuteissa** – Azure-tilauskokoonpano käsittelee suorituskykypisteet.
  - **Ajoituksen alkamisaika** – Odottaa *Ajoitus*-toiminnon tukea.

- **Suunnitellut tilaukset** -välilehti:

  - **Vastaanottoaika** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Tuotanto** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Projekti**-osion kentät – Odottaa *Ajoitus*-toiminnon tukea.

## <a name="coverage-groups-page"></a>Kattavuusryhmät -sivu

Suunnittelun optimointi ei käytä seuraavia parametreja tai asetuksia **Kattavuusryhmät**-sivulla:

- **Yleinen**-pikavälilehti:

  - **Positiiviset päivät** – *Positiiviset päivät* -arvoa ei käytetä. Suunnittelun optimoinnissa positiivisten päivien arvo katsotaan rajattomaksi.
  - **Kuluta käytettävissä olevaa varastoa** – Odottaa *Käytettävissä olevan varaston kulutus* -asetuksen tukea.
  - **Käytä määritettyä tuoterakennetta tai kaavaversiota** – Odottaa *Kaavan versiot, joissa on oheis-/sivutuotteita* -asetuksen tukea.
  - **Käytä määritettyä reittiversiota** – Odottaa *Kysyntä tietyillä määritetyillä tuoterakenne- tai reititysvaatimuksilla* -asetuksen tukea.


- **Muu**-pikavälilehti:

  - **Lukitusaikaraja (päivää)** – *Lukitusaikaraja*-asetusta ei aiota tukea suunnittelun optimoinnissa.
  - **Tuoterakenteen hajotuksen aikaraja (päivää)** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Kapasiteetin aikataulutuksen aikaraja (päivää)** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Hyväksyttyjen ehdotusten aikaraja (päivää)** – Odottaa *Ehdotus*-asetuksen tukea.
  - **Ennustesuunnitelma aikaraja** – Odottaa *Ennuste*-toiminnon tukea.

- **Viiveet**-pikavälilehti:

  - **Lasketut viiveet** – Odottaa *Lasketut viiveet* -asetuksen tukea.
  - **Laskettujen viiveiden aikaraja (päivää)** – Odottaa *Lasketut viiveet* -asetuksen tukea.

## <a name="item-coverage-page"></a>Nimikkeen kattavuus -sivu

Suunnittelun optimointi ei käytä seuraavia parametreja tai asetuksia **Nimikkeen kattavuus** -sivulla:

- **Yleinen**-välilehti:

  - **Suunniteltu tilaustyyppi** – Suunnittelun optimointi ei tue *Kanban*-vaihtoehtoa, joka odottaa *Kanban*-asetuksen tukea.
  - **Lukitusaikaraja (päivää)** – *Lukitusaikaraja*-asetusta ei aiota tukea suunnittelun optimoinnissa.
  - **Tuoterakenteen hajotuksen aikaraja (päivää)** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Kapasiteetin aikataulutuksen aikaraja (päivää)** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Hyväksyttyjen ehdotusten aikaraja (päivää)** – Odottaa *Ehdotus*-asetuksen tukea.
  - **Täytä vähimmäisarvo** – Suunnittelun optimointi ei tue *Tämän päivän päivämäärä*-, *Ensimmäinen varasto-otto*- tai *Kattavuuden aikaraja* -vaihtoehtoa. Se käyttää aina *Tämän päivän päivämäärä + hankinta-aika* -vaihtoehtoa.
  - **Minimikaudet** – Odottaa *Vähimmäisvarastotaso*-asetuksen tukea.
  - **Suunnittelukaava** – Odottaa *Kaavan versiot, joissa on oheis-/sivutuotteita* -asetuksen tukea.
  - **Oletusprioriteetti** – Odottaa *Kaavan versiot, joissa on oheis-/sivutuotteita* -asetuksen tukea.
  - **Nykyinen prioriteetti** – Odottaa *Kaavan versiot, joissa on oheis-/sivutuotteita* -asetuksen tukea.
  - **Muutospäivämäärä** – Odottaa *Kaavan versiot, joissa on oheis-/sivutuotteita* -asetuksen tukea.
  - **Kuluta käytettävissä olevaa varastoa** – Odottaa *Käytettävissä olevan varaston kulutus* -asetuksen tukea.

- **Läpimenoaika**-välilehti:

  - **Ostoaika** – Suunnittelun optimointipalvelun 6.8.2021 julkaisua aiemmissa versioissa suunnittelun optimointi käyttää tätä parametria oikeiden tilaus- ja toimituspäivämäärien laskemiseen, mutta se ei tallenna itse laskettua läpimenoaikaa suunniteltuun tilaukseen. Myöhemmissä versioissa palvelu käyttää myös laskettua läpimenoaikaa **Läpimenoaika**-kentän ja **Työpäivät**-asetuksen määrittämiseen kulloisenkin suunnitellun tilauksen edellyttämällä tavalla.
  - **Tuotantoaika** – Suunnittelun optimointipalvelun 6.8.2021 julkaisua aiemmissa versioissa suunnittelun optimointi käyttää tätä parametria oikeiden tilaus- ja toimituspäivämäärien laskemiseen, mutta se ei tallenna itse laskettua läpimenoaikaa suunniteltuun tilaukseen. Myöhemmissä versioissa palvelu käyttää myös laskettua läpimenoaikaa **Läpimenoaika**-kentän ja **Työpäivät**-asetuksen määrittämiseen kulloisenkin suunnitellun tilauksen edellyttämällä tavalla.
  - **Siirtoaika** – Suunnittelun optimointipalvelun 6.8.2021 julkaisua aiemmissa versioissa suunnittelun optimointi käyttää tätä parametria oikeiden tilaus- ja toimituspäivämäärien laskemiseen, mutta se ei tallenna itse laskettua läpimenoaikaa suunniteltuun tilaukseen. Myöhemmissä versioissa palvelu käyttää myös laskettua läpimenoaikaa **Läpimenoaika**-kentän ja **Työpäivät**-asetuksen määrittämiseen kulloisenkin suunnitellun tilauksen edellyttämällä tavalla.
  - **Työpäivät** – Suunnittelun optimointipalvelun 6.8.2021 julkaisua aiemmissa versioissa suunnittelun optimointi käyttää tätä parametria oikeiden tilaus- ja toimituspäivämäärien laskemiseen, mutta se ei tallenna itse laskettua läpimenoaikaa suunniteltuun tilaukseen. Myöhemmissä versioissa palvelu käyttää myös laskettua läpimenoaikaa **Läpimenoaika**-kentän ja **Työpäivät**-asetuksen määrittämiseen kulloisenkin suunnitellun tilauksen edellyttämällä tavalla.

## <a name="master-plans-page"></a>Pääsuunnitelmat-sivu

Suunnittelun optimointi ei käytä seuraavia parametreja tai asetuksia **Pääsuunnitelmat**-sivulla:

- **Yleinen**-pikavälilehti:

  - **Korvaa käytettävissä oleva varasto** – Odottaa *Käytettävissä olevan varaston kulutus* -asetuksen tukea.
  - **Kuluta käytettävissä olevaa varastoa** – Odottaa *Käytettävissä olevan varaston kulutus* -asetuksen tukea.
  - **Sisällytä myyntitarjoukset** – Odottaa *Myyntitarjoukset*-asetuksen tukea.
  - **Sisällytä tarjouspyyntö** – Odottaa *Tarjouspyynnöt*-asetuksen tukea.
  - **Käytä varastointiajan päivämääriä** – Odottaa *Säilyvyysaika*-asetuksen tukea.
  - **Sisällytä jatkuvuussuunnitelma** – Odottaa *Jatkuvuuden ajoitus* -asetuksen tukea.
  - **Ajoitusmenetelmä** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Rajallinen ominaisuus** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Takautuvan ajastuksen kapasiteetin aikaraja** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Rajallinen kapasiteetti** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Rajallisen kapasiteetin aikaraja** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Rajallinen kapasiteetti pullonkaularesursseille** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Kapasiteetin aikaraja pullonkaularesursseille** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Suunnitellut tilaukset** – Suunnittelun optimointi käyttää kiinteitä numerosarjoja.
  - **Istunto** – Suunnittelun optimointi käyttää kiinteitä numerosarjoja.
  - **Jatkuvuussuunnitelma** – Suunnittelun optimointi käyttää kiinteitä numerosarjoja.

- **Aikarajat päivissä** -pikavälilehti:

  - **Lukitse** – *Lukitusaikaraja*-asetusta ei aiota tukea suunnittelun optimoinnissa.
  - **Hajotus** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Ennustesuunnitelma** – Odottaa *Ennuste*-toiminnon lisätukea.
  - **Kapasiteetti** – Odottaa *Ajoitus*-toiminnon tukea.
  - **Jatkuvuussuunnitelma** – Odottaa *Jatkuvuuden ajoitus* -asetuksen tukea.
  - **Lasketut viiveet** – Odottaa *Lasketut viiveet* -asetuksen lisätukea.
  - **Järjestys** – Odottaa *Tuotanto*-asetuksen tukea.

- **Lasketut viiveet** -pikavälilehti:

  - **Varmista, että suunniteltuja tilauksia ei luoda ennen pääsuunnittelun suorituspäivää** – Odottaa *Lasketut viiveet* -asetuksen tukea.
  - **Lisää laskettu viive tarvepäivämäärään** (**Suunnitellut ostotilaukset** -osiossa) – Odottaa *Lasketut viiveet* -asetuksen tukea.
  - **Lisää laskettu viive tarvepäivämäärään** (**Suunnitellut tuotantotilaukset** -osiossa) – Odottaa *Lasketut viiveet* -asetuksen tukea.
  - **Lisää laskettu viive tarvepäivämäärään** (**Suunniteltu siirto** -osiossa) – Odottaa *Lasketut viiveet* -asetuksen tukea.
  - **Lisää laskettu viive tarvepäivämäärään** (**Suunniteltu kanban** -osiossa) – Odottaa *Lasketut viiveet* -asetuksen tukea.

- **Toimintosanoma**-pikavälilehti:

  - **Päivitä viivästyspäivämäärä tarvepäiväksi** - Tämä parametri poistetaan käytöstä suunnittelun optimoinnissa.

- **Järjestys**-pikavälilehti:

  - **Järjestä suunnitellut tilaukset pääsuunnittelun jälkeen** – Odottaa *Järjestys*-asetuksen tukea.
  - **Jakson tyyppi** – Odottaa *Järjestys*-asetuksen tukea.
  - **Kauden tyyppi** – Odottaa *Järjestys*-asetuksen tukea.
  - **Kampanjajakson jaksojen määrä** – Odottaa *Järjestys*-asetuksen tukea.

## <a name="released-product-details-page"></a>Julkaistun tuotteen tiedot -sivu

Suunnittelun optimointi ei käytä seuraavaa parametrivaihtoehtoa tai asetuksia **Vapautetun tuotteen tiedot** -sivulla:

- **Suunnittele**-pikavälilehti:

  - **Tuotantolaji** – Suunnittelun optimointi ei tue *Suunnittelunimike*-vaihtoehtoa, odottaa *Suunnittelunimikkeet*-asetuksen tukea.

## <a name="default-order-settings-page"></a>Tilauksen oletusasetukset -sivu

Suunnittelun optimointi ei käytä seuraavaa parametrivaihtoehtoa tai asetuksia **Tilauksen oletusasetukset** -sivulla:

- **Ostotilaus**-pikavälilehti:

  - **Oston läpimenoaika** – Suunnittelun optimointipalvelun 6.8.2021 julkaisua aiemmissa versioissa suunnittelun optimointi käyttää tätä parametria oikeiden tilaus- ja toimituspäivämäärien laskemiseen, mutta se ei tallenna itse laskettua läpimenoaikaa suunniteltuun tilaukseen. Myöhemmissä versioissa palvelu käyttää myös laskettua läpimenoaikaa **Läpimenoaika**-kentän ja **Työpäivät**-asetuksen määrittämiseen kulloisenkin suunnitellun tilauksen edellyttämällä tavalla.
  - **Työpäivät** – Suunnittelun optimointipalvelun 6.8.2021 julkaisua aiemmissa versioissa suunnittelun optimointi käyttää tätä parametria oikeiden tilaus- ja toimituspäivämäärien laskemiseen, mutta se ei tallenna itse laskettua läpimenoaikaa suunniteltuun tilaukseen. Myöhemmissä versioissa palvelu käyttää myös laskettua läpimenoaikaa **Läpimenoaika**-kentän ja **Työpäivät**-asetuksen määrittämiseen kulloisenkin suunnitellun tilauksen edellyttämällä tavalla.

- **Varasto**-pikavälilehti:

  - **Toimituspäivän tarkistus** – Suunnittelun optimointi ei tue *CTP*-vaihtoehtoa, odottaa *CTP*-asetuksen tukea.
  - **Varaston läpimenoaika** – Suunnittelun optimointipalvelun 6.8.2021 julkaisua aiemmissa versioissa suunnittelun optimointi käyttää tätä parametria oikeiden tilaus- ja toimituspäivämäärien laskemiseen, mutta se ei tallenna itse laskettua läpimenoaikaa suunniteltuun tilaukseen. Myöhemmissä versioissa palvelu käyttää myös laskettua läpimenoaikaa **Läpimenoaika**-kentän ja **Työpäivät**-asetuksen määrittämiseen kulloisenkin suunnitellun tilauksen edellyttämällä tavalla.
  - **Työpäivät** – Suunnittelun optimointipalvelun 6.8.2021 julkaisua aiemmissa versioissa suunnittelun optimointi käyttää tätä parametria oikeiden tilaus- ja toimituspäivämäärien laskemiseen, mutta se ei tallenna itse laskettua läpimenoaikaa suunniteltuun tilaukseen. Myöhemmissä versioissa palvelu käyttää myös laskettua läpimenoaikaa **Läpimenoaika**-kentän ja **Työpäivät**-asetuksen määrittämiseen kulloisenkin suunnitellun tilauksen edellyttämällä tavalla.

## <a name="batch-disposition-master-page"></a>Erän käsittelytiedot -sivu

Suunnittelun optimointi ei käytä seuraava parametriä **Erän käsittelytiedot** -sivulla:

- **Asetukset**-pikavälilehti:

  - **Netotettavissa** – Odottaa *Erän käsittelykoodit* -asetuksen tukea.
 
