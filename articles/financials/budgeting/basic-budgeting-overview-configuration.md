---
title: Budjetoinnin yhteenveto
description: "Lähes kaikkien yritysten, jotka käyttävät Microsoft Dynamics 365 for Finance and Operations -sovelluksen toimintoja, pitää voida luoda raportteja, joissa budjetoituja arvoja verrataan toteutuneisiin. Tässä artikkelissa kerrotaan pienin vaadittava kokoonpano budjettien luomiseen Finance and Operationsissa tai niiden lataamiseen kolmannen osapuolen ohjelmasta."
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 1d768ee6d2244a237972f7183f27a60b93eea819
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="budgeting-overview"></a>Budjetoinnin yleiskatsaus 

[!include [banner](../includes/banner.md)]

Lähes kaikkien yritysten, jotka käyttävät Microsoft Dynamics 365 for Finance and Operations -sovelluksen toimintoja, pitää voida luoda raportteja, joissa budjetoituja arvoja verrataan toteutuneisiin. Tässä artikkelissa kerrotaan pienin vaadittava kokoonpano budjettien luomiseen Finance and Operationsissa tai niiden lataamiseen kolmannen osapuolen ohjelmasta.

<a name="overview"></a>Yleiskuvaus
--------

Yrityksen hyväksyttyä budjettia ylläpidetään tiedostossa, joka tunnetaan nimellä *budjettitapahtuma*. Budjetin rekisterin merkintäasiakirjan rivejä kutsutaan *budjettitilin* tapahtumiksi, ja ne sisältävät taloushallinnon dimensiotiedot, päivämäärät ja summat hyväksytystä budjetista. Budjettirekisterin tapahtuma-asiakirja integroidaan taloushallinnon perusraportteihin ja kyselysivuihin, joissa kirjanpidon summia verrataan budjettisummiin. 

Finance and Operationsissa on useita tapoja luoda budjettitapahtumia:

-   Syötä tiedoston tiedot manuaalisesti **Budjettitapahtumat**-sivulla.
-   Käytä Microsoft Excel-mallia, jonka voit avata napsauttamalla **Avaa Excelissä** -painiketta **Budjettitapahtumat**-sivulla.
-   Tuo budjettitapahtumat Tietojen hallinnan **Budjettitiliviennit** -tietoyksikön kautta. Sinun tulisi harkita tämän menetelmän käyttämistä ja **Joukkoon perustuva** -**käsittelyn** parametrin käyttöön ottamista, kun joudut tuomaan useita budjettitilin merkintöjä järjestelmään.
-   Jos yritys käyttää Budjettisuunnittelu-toimintoa budjettitietojen valmisteluun, voit käyttää **Luo budjettitapahtuma** -kausittaista prosessia.

Budjettirekisterin tapahtumaa pidetään valmiina kun budjettisaldot on päivitetty. Valitse **Budjettirekisterimerkinnät** -sivulla **Päivitä budjettisaldot** valitulle budjettirekisterin tapahtumalle tai useille tapahtumille. Kun olet päivittänyt budjettisaldot, budjettitapahtuman tila muuttuu arvoksi **Valmis**. Valmista budjettitapahtumaa ei voida avata uudelleen muokkausta varten. Näin ollen, jos budjettitietoja täytyy korjata, sinun on luotava uusi budjettitapahtuma sen sijaan, että korjaisit valmiin budjettitapahtuman tietoja.

## <a name="configuration"></a>Määritys
Aloita budjetin määrittäminen **Budjetointiparametrit**-sivulla. Tällä sivulla sinun on määritettävä budjetin kirjauskansio, budjettitapahtumien numerosarja, ja oletustoiminnot työtiloissa.

Seuraavaksi, jos on olemassa budjettitapahtumien hyväksyntää ohjaavia käytäntöjä, budjettityypistä riippuen (esimerkiksi siirrot tai aliversiot), sinun on luotava budjettitapahtuman työnkulut **Budjetoinnin työnkulut** -sivulla. Jos on skenaarioita, joissa siirrot saattavat olla sallittuja ilman työnkulun hyväksyntää, voit määrittää budjetin siirtosäännöt, jotka tukevat näitä skenaarioita. 

Sinun on valittava **Budjetoinnin dimensiot** -sivulla budjetoinnissa käytettävät taloushallinnon dimensiot perustuen tilikartassa käytettyihin dimensioihin. Voit valita kaikki taloushallinnon dimensiot tai niiden osajoukon budjetointia varten.

Määritä *budjettimalli*, joka vastaa kaikkia budjetteja tai joitain niistä. Voit käyttää samaa budjettimallia kaikkia budjettitapahtumia varten. Voit vaihtoehtoisesti luoda erilliset mallit, jotka perustuvat budjettityyppiin, maantieteelliseen sijaintiin tai johonkin muuhun tapaan, millä budjetti voidaan luokitella. 

> [!NOTE] 
> Jos käytetään budjettimallia, voit liittää vain yhden budjettimallin tiettyyn budjettijakson aikaväliin. 

Luo *budjettikoodit*, jotka tunnistavat tallennettavien budjettitapahtumien tyypit ja niihin liittyvän työnkulun. Budjettikoodit voivat tukea seuraavia budjettityyppejä:

-   Alkuperäinen budjetti
-   Varastosiirto
-   Aliversio
-   Varaus
-   Alustava varaus
-   Siirrettävä budjetti

Budjettikoodeja käyttämällä luot hyväksyttyjen budjettimuutosten kirjausketjun, joka kattaa koko budjettijakson. Jos työnkulkuun on liitetty budjettikoodi, työnkulkuun otetaan käyttöön kaikki budjettirekisterin tapahtumat, joissa käytetään budjettikoodia ja työnkulun vaiheet on suoritettava ennen kuin budjettirekisterimerkintä tavoittaa **Valmis**-vaiheen.  

Voit myös halutessasi määrittää *Budjetin iirtosäännöt*. Voit käyttää budjetin siirtosääntöjä valitsemalla **Käytä sääntöjä budjetin siirtoja varten** **Budjettiparametrit**-sivulla. Kun budjettisiirron säännöt ovat käytössä, jos käyttäjä luo asiakirjan käyttämällä budjettikoodia, joka on tyyppiä **Siirto**, budjettisaldoja ei päivitetä, jos budjettisiirron sääntöjä rikotaan. Voit esimerkiksi sallia Myynti- ja markkinointiosastolle budjettisiirron asiakirjat, joissa kulubudjetti siirretään päätilien välillä, mutta estää budjetin siirrot tältä osastolta tai tälle osastolle, ellei kyseisen tyyppiselle budjettitilitapahtumalle ole myönnetty työnkulun hyväksyntää.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Työntilojen ja kyselysivujen käyttäminen budjetti vs. toteutunut -lukujen seurantaan
Budjettipäällikkö voi tarkastella budjetin senhetkistä tilaa **Kirjanpitobudjetit ja ennusteet** -työtilassa. **Budjetin ylittävät kulut** ja **Budjetin alittava tuotto** -välilehdiltä löytyy pikakatsaus taloushallinnon dimensioiden yhdistelmiin, joissa tavoitebudjetteihin ei päästä tai jotka lähestyvät ko. rajaa. Voit mukauttaa näillä välilehdillä käytettävää budjetin raja-arvoprosenttia ja taloushallinnon dimensioiden joukkoa valitsemalla **Määritä oma työtila**. Voit valita **Yksikön päälliköt** nähdäksesi työntekijät, jotka ovat vastuussa tietyistä näille välilehdille valituista taloushallinnon dimensioiden yhdistelmistä. Jos esimerkiksi näet, että liiketoimintaosaston kulubudjetti on ylittämässä budjetin raja-arvoa, voit helposti löytää ja ottaa yhteyttä liiketoimintaosaston päällikköön keskustellaksesi asiasta. 

> [!NOTE] 
> **Osastopäällikkö**-kenttä **Organisaatioyksiköt**-sivulla määrittää, ketkä päälliköt ovat vastuussa määrätyistä taloushallinnon dimensioiden yhdistelmistä. Valitse kohta **Katso lisää** välilehden alareunassa avataksesi **Budjetti vs. toteutunut** -kyselysivun lisätietojen saamiseksi budjettisummista verrattuna toteutuneisiin summiin. 

**Toteutunut vs. budjetti** -kyselysivun kautta voit porautua budjetti vs. toteutunut -summien yksityiskohtaisiin tietoihin. Valitse kyselysivun rivi ja napsauta **Kauden saldot** nähdäksesi budjetoidut ja toteutuneet summat tilikausille jaettuna. **Budjettitiliviennit**-sivu porautuu budjettitapahtumien budjettisummien yksityiskohtaisiin tietoihin. **Yleisen kirjauskansion merkinnät**-sivu avaa kirjanpitotapahtumat, jotka sisältyvät laskettuun **Toteutuneet**-summaan. 

Budjettisuunnittelutoimintoa käyttävä yritys voi luoda ja käyttää *budjettiennusteita* **Kirjanpitobudjetit ja ennusteet** -työtilassa.




