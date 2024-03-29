---
title: Vähittäismyyntilaskelmat
description: Tässä artikkelissa kerrotaan, miten laskelmat luodaan ja kirjataan.
author: ashishmsft
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 85183
ms.assetid: df9c62a2-6f13-4a08-bdca-07d041172c1b
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0717c1198171f411e3c52233200ecfcc213dc13f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878454"
---
# <a name="retail-statements"></a>Vähittäismyyntilaskelmat

[!include [banner](includes/banner.md)]

Dynamics 365 Commercessa laskelman kirjausprosessia käytetään seuraamaan pilvimyyntipisteen tai Modern POS:n (MPOS) tapahtumia. Laskelman kirjausprosessi hakee myyntipistetapahtumajoukon Headquarters (HQ) -asiakasohjelmaan jakeluaikataulun avulla. **Kaupan parametrit**- ja **Myymälät**-sivuilla määritetyillä parametreilla valitaan yksittäisiin laskelmiin haettavat tapahtumat.

Seuraavassa kuvassa on laskelman kirjausprosessi. Tässä prosessissa myyntipisteeseen tallennetut tapahtumat lähetetään asiakkaalle Commerce-ajastuksen avulla. Kun asiakas on vastaanottanut tapahtumat, voit luoda, laskea ja kirjata myymälän tapahtumaotteen.

[![Laskelman kirjausprosessi.](./media/retail-statements.png)](./media/retail-statements.png)

## <a name="creating-and-posting-statements"></a>Laskelmien luominen ja kirjaaminen

Voit luoda laskelman manuaalisesti tai eräprosesseissa, jotka määritetään suoritettavaksi säännöllisesti koko päivän ajalta. Molemmissa tapauksissa käytetään seuraavia ohjeita, joilla voit luoda ja kirjata laskelmat.

### <a name="create-the-statement"></a>Luo laskelma

Tämä vaihe kuvaa myymälän, johon laskelma luodaan manuaalisesti. Jos määrität eräkäsittelyn, voit automaattisesti luoda raportteja myymälöille määrittämäsi aikataulun mukaan.

### <a name="calculate-the-statement"></a>Laske laskelma

Tässä vaiheessa valitaan tapahtumarivit jokaiselle myymälälle **Commercen parametrit**- ja **Myymälät**-sivuilla määritettyjen ehtojen perusteella. Voit määrittää näillä sivuilla ehdot ja tapahtumien laskentatavan. Tarkastele luetteloa laskelmaan sisältyvistä tapahtumista ennen laskelman laatimista käyttämällä **Tapahtumat**-sivulla.

Laskelman laskennassa käytetään kassanlaskennan summaa laskettuna summana. Lasketun summan voi myös syöttää manuaalisesti. Laskelma näyttää kaikkien maksutapojen tapahtumien myyntimäärän ja todellisen lasketun määrän välisen eron. Laskelma kirjataan vain, jos tämä ero on pienempi kuin suurin mahdollinen myymälälle määritetty kirjausero.

> [!NOTE]
> Laskelman laskentaprosessi käyttää yleistä numerosarjaa.

Kun lasket laskelman, laskenta sisältää seuraavat tehtävät:

- Merkitään sellaiset tapahtumat, joita ei sisällytetty edellisen raportin laskelmaan valitulla päivämääräalueella.
- Laske valittujen tapahtumien maksuvälinesummien kokonaissummat. Tulokset näkyvät laskelmariveillä laskelmamenetelmästä mukaan:

    - Jos raporttitapa on **Yhteensä**, rivi luodaan jokaiselle maksutavalle valituissa tapahtumissa.
    - Jos valittu raporttitapa on **Henkilökunta**, rivi luodaan jokaiselle maksutavalle tapahtumissa, jotka suoritti valittu työntekijä.
    - Jos valittu raporttitapa on **Kassapääte**, rivi luodaan jokaiselle maksutavalle tapahtumissa, jotka suoritettiin valitussa kassakoneessa.
    - Jos valittu raporttitapa on **Vuoro**, rivi luodaan jokaiselle maksutavalle tapahtumissa, jotka suoritettiin vuoron aikana.

Jos **Jakoperusteena laskelmatapa** -valintaruutu valitaan **Myymälät**-sivulla, erillinen laskelma luodaan **Laskelmatapa**-kentässä valitun arvon perusteella.

Jos myymälän työajat on laajennettu yli keskiyön, voit määrittää laskelman kirjauksen siten, se perustuu työpäivän päättymiseen kalenteripäivän päättymisen sijaan.

Anna **Myymälät**-sivun **Laskelma/sulkeminen**-pikavälilehden **Työpäivän päätös**-kenttään aika, jolloin viimeinen tapahtuma on kirjattava, jotta se sisältyy työpäivän tapahtumiin. Valitse **Kirjaa työpäivänä** -valintaruutu, jotta tapahtumat kirjataan saman työpäivän aikana. Kun laskelma kirjataan, saman työpäivän aikana tallennetut tapahtumat voidaan sisällyttää samaan myyntitilaukseen, vaikka osa tapahtumista tapahtuu ennen puoltayötä ja osa puolenyön jälkeen.

#### <a name="example-post-a-statement-for-a-business-day-that-extends-over-two-calendar-days"></a>Esimerkki: Kirjaa ilmoitus työpäivälle, joka ulottuu yli kahdelle kalenteripäivällle

Myymälä aukioloaika on 8.00–3.00 ja **Kirjaa työpäivänä** -valintaruutu on valittu myymälän määrityksissä. Myymälä kirjaa tapahtumia 31.5. kello 8.00–24.00. Myymälä kirjaa tapahtumia myös 1.6. kello 00.01–3.00.

Kun myymälä kirjaa tapahtumat työpäivän päätteeksi, järjestelmä muodostaa myyntitilauksen, joka sisältää kaikki tapahtumat, jotka on kirjattu työtunteina kello 8.00–3.00, vaikka tapahtumat ovat tapahtuneet toukokuun 31. ja kesäkuun 1. päivänä.

Jos sama myymälä on määritetty, kun **Kirjaa työpäivänä** -valintaruutua ei ole valittu, erillisiä myyntitilauksia luodaan, kun myymälä kirjaa sen laskelman työpäivän päätteeksi. Yksi myyntitilaus sisältää tapahtumia, jotka on kirjattu työaikana kello 8.00–24.00 31.5. ja toinen myyntitilaus sisältää tapahtumia, jotka kirjattiin 1.6. kello 00.01–3.00.

> [!NOTE]
> Laskelman ajanjaksoon sisältyvät vuorot on suljettava, ennen kuin voit luoda laskelmia.

### <a name="post-the-statement"></a>Kirjaa laskelma

Kun kirjaat laskelman, myyntitilaukset ja laskut luodaan laskelman myyntiin.

- Itsepalvelutukkumyynti yhdistetään yhdeksi myyntitilaukseksi ja laskutetaan oletusasiakkaalta, joka on määritetty myymälälle.
- Myynti, johon asiakas on lisätty tapahtumaan POS:ssa luo erillisiä myyntitilauksia ja laskuja, yksi kutakin asiakaskohtaisesti.

Maksukirjauskansioita luodaan automaattisesti lausunnon maksuille, ja varasto päivitetään myyntipistemyymälälle.


[!INCLUDE[footer-include](../includes/footer-banner.md)]