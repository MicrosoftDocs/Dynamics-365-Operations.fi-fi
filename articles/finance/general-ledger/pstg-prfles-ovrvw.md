---
title: Kirjausprofiilien yleiskuvaus
description: Tässä aiheessa kuvataan, kuinka kirjausprofiileja käytetään Microsoft Dynamics 365 -sovellusten aikana.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c29597155e525638e7c2ded7d641017f2189c49
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734573"
---
# <a name="posting-profiles-overview"></a>Kirjausprofiilien yleiskuvaus

Taloushallinnointi- ja työvaihesovellusten termillä *kirjausprofiilit* kuvaillaan konfiguroinnit, jotka ohjaavat, miten alakirjanpitotilit muunnetaan päätileille, jotta niitä voidaan käyttää kirjanpitoon kirjattaessa. Ne ohjaavat esimerkiksi, miten asiakas muunnetaan myyntireskontran päätilille laskun kirjaamista varten.

Joillakin moduuleilla ja ominaisuuksilla on sivu, joka sisältää nimen sanat "kirjausprofiili" (esimerkiksi **asiakkaan kirjausprofiili** tai **toimittajan kirjausprofiili**). Lisäksi joillakin moduuleilla on useita asetuksia, joilla määritetään alareskontran avulla luotujen tapahtumien kirjanpitokirjaus. Voit esimerkiksi määrittää **tuotannonhallinta**-moduulissa kirjauksen tuotantoryhmän, resurssin tai resurssiryhmän mukaan.

Huomaa, että monentyyppisille tapahtumille on olemassa vaihtoehto profiilien kirjaamiselle: kirjausmääritykset. Voit käyttää tuetuissa asiakirjoissa kirjausmäärityksiä kirjausprofiilien sijaan, kun haluat luokitella kirjanpitoyksiköiden päätilit ja taloushallinnon dimensiot. Jos aiot käyttää varausten tai alustavan varauksen tilejä, kirjausmääritys on pakollinen kirjanpitomerkintöjen tilien määrittämiseksi.

Ennen kuin voit konfiguroida kirjausprofiilit, kirjausmääritykset tai **automaattisten tapahtumien tilit** -sivun, konfiguroida valitun yrityksen **kirjanpito**-sivun tilikartta on määritettävä.

## <a name="posting-types"></a>Kirjaustyypit

Rahoitus- ja toiminta -sovellusten kirjaustyypin avulla määritetään yleinen veloituksen tai hyvityksen luokka. Tämä luokka ei ole riippumaton kirjanpidon päätilistä. Kirjanpitoon on kirjaustyyppejä kutakin debet- tai kredit-kirjausta varten.

Yhdellä tositteella voi olla useita kirjaustyyppejä. Esimerkiksi tapahtuman, joka kirjataan yleisen päiväkirjan kautta, jossa tili ja vastatili on asetettu arvoon **Kirjanpito**, kirjaustyyppi on **Kirjanpidon kirjauskansio** sekä veloituksen että hyvityksen osalta. Sen sijaan toimittajan laskulla on useita kirjaustyyppejä. Kirjaustyyppeihin kuuluu yksi rivi toimittajan saldoa varten ja vastakirjauksen lisärivit, kuten **kirjanpidon kirjauskansio**.

Voit tarkastella kirjaustyyppiä **Kirjaustyyppi**-kentän tietoja **Tositetapahtumat**-sivun **Yleiset**-välilehdessä.

> [!TIP]
> **Mukauttaminen**-työkalurivin avulla voit lisätä **Kirjaustyyppi**-kentän **Yhteenveto**-välilehden ruudukkoon tai siirtää sen. Näin voit helpottaa tämän kentän käyttöä tai tarkastella tositteita katsottaessa.

## <a name="detail-settings-for-a-posting-profile"></a>Kirjausprofiilin tietoasetukset 

Kun konfiguroit kirjausprofiilit, **Tilikoodi**-kenttä määrittää asetuksen tason. Seuraavat vaihtoehdot ovat valittavissa: **Taulukko**, **Ryhmä** ja **Kaikki**. Täsmäytys päättyy ensimmäisen täsmäytyksen jälkeen, ja tilaus on yksityiskohtaisimmat tasolta vähiten erityistasolle. Vaikka Joissakin tapauksissa **Tilikoodi**-kentän nimi voi olla hieman eri, kentän toiminta ja toiminto säilyvät samana. Esimerkiksi varaston kirjausprofiiliin sisältyy **Nimikekoodi** -kenttä ja **Tilikoodi**-kenttä. Molemmissa kentissä on **Taulu**-, **Ryhmä**- ja **Kaikki**-arvot.

Jos **Päätili**-kenttä jätetään tyhjäksi lähetysprofiilille, etkä ole määrittänyt päätiliä **Tilit automaattisia tapahtumia varten** -sivulla tai moduuli- tai ominaisuuskohtaisella sivulla , saat virheilmoituksen, kun lähetät tapahtuman, joka käyttää kirjaustyyppiä. Yleensä sanoma on seuraava: "\[Kirjaustyypin\] tiliä ei löydy."

### <a name="table-value"></a>Taulun arvo

**Taulun** arvo viittaa kirjausprofiiliin liittyvään päätietueeseen. Kukin taulutietue on yhden arvon kohtainen. Voit määrittää Arvon kenttään, joka tulee näkyviin **Tilikoodi**-kentän jälkeen. Yleensä tämän kentän nimi on **Tili** tai **Tili/Ryhmänumero**. Tarkka nimi vaihtelee sen mukaan, millä sivulla se esiintyy.

Jos käytät esimerkiksi asiakkaan kirjausprofiilia, **taulukon** arvo edustaa tiettyä asiakasta. Tästä syystä, jos **Tilikoodi**-kentässä valitaan **Taulukko**, asiakkaan numero on valittava **Tilin/ryhmän numero** -kentässä.

**Taulun** arvo edustaa kaikkein yksityiskohtaisinta tietuetyyppiä. Järjestelmä käyttää tätä arvoa aina, vaikka olisit konfiguroinut toisen tietueen, jossa **Ryhmä**- tai **Kaikki**-arvo on valittu. Tämä arvo ohittaa myös arvot, jotka olet luonut oletusarvoiksi **Automaattisten tapahtumien tilit** -sivulla.

**Taulun** arvoa ei ole suositeltavaa käyttää kirjausprofiilien hallinnan ensisijaisena mekanismina, koska tietojen laatuongelmat voivat ilmetä, jos kutakin perustietotietuetta varten ylläpidetään erillistä kirjausprofiilia. On myös vaikea ylläpitää ja täsmäyttää erillistä kirjausprofiilia kutakin perustietotietuetta varten. Sen sijaan tätä arvoa kannattaa käyttää kirjausprofiilien poikkeusten hallintaan.

### <a name="group-value"></a>Ryhmän arvo

**Ryhmän** arvo viittaa ryhmittelytietueeseen, jota kirjausprofiiliin liittyvä päätietue tukee. Kukin ryhmätietue on yhden arvon kohtainen. Voit määrittää Arvon kenttään, joka tulee näkyviin **Tilikoodi**-kentän jälkeen. Yleensä tämän kentän nimi on **Tili** tai **Tili/Ryhmänumero**. Tarkka nimi vaihtelee sen mukaan, millä sivulla se esiintyy.

**Ryhmä**-arvo edellyttää, että määrität ryhmän ensin ja linkität sen vähintään yhteen tilin tietueeseen. **Ryhmä**-arvo on pienempi kuin **taulun** arvo, mutta se on tarkempi kuin **Kaikki**-arvo. Jos taululle ei ole määritetty tietuetta, järjestelmä yrittää etsiä sen ryhmän tietueen, johon tietue kuuluu.

Jos esimerkiksi käytät asiakkaan kirjausprofiilia ja valitset **Tilikoodi**-kentästä **Ryhmä**, valitse asiakasryhmä **Tili/ryhmänumero**-kentästä. Asiakasryhmä on määritettävä ennalta **asiakasryhmä**-sivulla, ja asiakasryhmä on määritettävä, kun asiakas luodaan.

Jos tietyn kirjaustyypin useita päätilejä on jäljitettävä, on suositeltavaa käyttää **Ryhmä**-arvoa. Esimerkiksi kolme myyntireskontran kauppareskontran päätiliä ovat yksi tavallisille asiakkaille, yksi työntekijöille ja toinen konsernin sisäistä myyntiä varten. Tässä tapauksessa on suositeltavaa luoda kolme asiakasryhmää asiakkaiden segmentoimista varten. Liitä sitten kukin asiakasryhmä asiakkaan kirjausprofiilin oikeaan päätiliin. Seuraavassa taulukossa näkyvät tässä esimerkissä kolme asiakasryhmää.

| Asiakasryhmä | Nimi | Kuvaus |
|----------------|------|-------------|
| EXT | Ulkoinen asiakas | Tätä ryhmää käytetään kaikille ulkoisille vakioasiakkaille. |
| EMP | Omat työntekijät | Tätä ryhmää käytetään kaikille organisaatiosta ostoja tekeville työntekijöille. |
| INT | Konsernin sisäinen myynti | Tätä ryhmää käytetään kaikilla konserniyritysten välisillä asiakastileillä, joita käytetään myynti- ja ostotilausten integroinnissa. |

Tämän jälkeen määrität kirjausprofiilissa kolme riviä. Jokaisella rivillä valitaan **ryhmä**-arvo ja liittyvä päätili.

### <a name="all-value"></a>Kaikki arvot

**Kaikki**-arvo ilmaisee, että asetukset koskevat kaikkia tietueita. Jos valitset **Tilikoodi**-kentästä **Kaikki**-arvon, **Tili/ryhmänumero**-kenttä ei ole käytettävissä etkä voi ottaa konfiguraatiota käyttöön valitsemalla tiettyä tietuetta.

**Kaikki**-arvo on vähiten spesifinen arvo. Sitä käytetään vain, jos järjestelmä ei löydä vastinetta **taulu**- tai **ryhmä**-arvolle. Valitse **Kaikki**-arvo, kun tiettyä kirjaustyyppiä varten on vain yksi päätili.

Kun esimerkiksi käytät asiakkaan kirjausprofiilia, määritettävät päätilit koskevat kaikkia muita asiakkaita ja asiakasryhmiä, joilla ei ole tietuetta tiettyä taulua (asiakasta) tai ryhmää (asiakasryhmää) varten.

### <a name="category"></a>Luokka

Varaston kirjausprofiileilla on myynti- tai hankintaluokkakohtainen lisäarvo. Arvo muistuttaa **taulun** arvoa siinä tapauksessa, että sitä käytetään vain tiettyyn myynti- tai hankintaluokkaan.

### <a name="default-value"></a>Oletusarvo

Jos kirjausprofiilin kirjaustyypille ei luoda tietuetta, jossa **Tilikoodi**-kentän arvoksi on määritetty **Kaikki** eikä järjestelmä löydä vastaavaa kirjausprofiilitietuetta **ryhmä**- tai **taulu** arvolle, järjestelmä palauttaa oletusarvoksi oletusarvon, joka voidaan määrittää **Automaattisten tapahtumien tilit** -sivulla. Lisätietoja on kohdassa [Automaattisten tapahtumien tilit](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Selvitystilit

*Selvitystiliä* käytetään usein kirjanpidossa. Jotkin Microsoft Dynamics 365 -sovellusten kirjaustyypit ovat selvitystilejä. Toisin sanoen tilin saldo tyhjennetään tai peruutetaan, kun toinen tapahtuma kirjataan. Kun esimerkiksi kirjaat ostotilauksen tuotteen vastaanoton, tuotteiden arvioitujen kustannusten summa sekä verot ja ostotilausrivien mahdolliset kulut kirjataan oston jaksotuskirjaustyyppiin velkana. Kun laskutat ostotilauksen, saldo palautetaan myöhemmin oston jaksotuksen kirjaustyypistä ja siirretään ostoreskontran kauppatilille.

## <a name="additional-resources"></a>Lisäresurssit

Monissa Dynamics 365 Finance-, Dynamics 365 Supply Chain Management-, Dynamics 365 Commerce- ja Dynamics 365 Project Operations -järjestelmän moduuleissa on kirjausprofiili tai lisäkonfiguraatio, joka ohjaa kirjanpidon kirjausta. Seuraavissa ohjeaiheissa on lisätietoja kunkin moduulin kirjausprofiileista ja kirjausasetuksista:

- [Automaattisten tapahtumien tilit](accounts-for-auto-transactions.md)
- [Ostoreskontran kirjaus](accts-payble-posting.md)
- [Myyntireskontran kirjaus](accts-recvble-posting.md)
- [Resurssin vuokrauksen kirjaus](../asset-leasing/set-up-lease-posting-accts.md)
- Käyttöomaisuuden hallinnan kirjaaminen (tulossa pian)
- Maksuliikennetiedot (Tulossa pian)
- Valuutan uudelleenarvostuksen kirjaustilit (Tulossa pian)
- Kulujen hallinnan kirjaaminen (Tulossa pian)
- [Käyttöomaisuuserän kirjausprofiili](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Konserniyritysten välisen laskennan kirjaaminen (Tulossa pian)
- Varaston kirjausprofiili (tulossa pian)
- [Aiheutuneiden kustannusten kirjaaminen](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Kirjausmääritysten yleiskatsaus](posting-definitions.md)
- Tuotannonohjauksen kirjaaminen (Tulossa pian)
- Projektinhallinnan ja kirjanpidon kirjaaminen (Tulossa pian)
- Palvelujen hallinnan kirjaaminen (Tulossa pian)
- Verojen kirjaaminen (Tulossa pian)
- Aika- ja läsnäolokirjaus (Tulossa pian)
- Kuljetuksen hallinnan kirjaaminen (Tulossa pian)
- Ostohyvitysten hallinnan kirjausprofiilit (Tulossa pian)
