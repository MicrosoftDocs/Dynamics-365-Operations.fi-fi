---
title: Kolmisuuntaiset vastaavuuskäytännöt
description: Tässä ohjeaiheessa on esimerkkejä kolmisuuntaisesta vastaavuudesta.
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoicePostingHistory
audience: Application User
ms.reviewer: roschlom
ms.custom: 2761
ms.assetid: 70f3cb1a-18b7-4474-95ec-28b2410dd8f8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41f863d85a1ad52d8fa11a458054728728858d27
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027791"
---
# <a name="three-way-matching-policies"></a>Kolmisuuntaiset vastaavuuskäytännöt

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on esimerkkejä kolmisuuntaisesta vastaavuudesta.

<a name="example-three-way-matching-for-items"></a>Esimerkki: Kolmisuuntainen vastaavuus nimikkeille
-------------------------------------

**Yhteenveto:** Ken on vastuuhenkilö Fabrikam-nimisen yrityksen pääkonttorissa. Hän päättää, että kaikki toimittajan laskut, jotka perustuvat ostotilauksiin on yhdistettävä ostotilausriveihin (kaksisuuntainen vastaavuus). Käyttöomaisuuserinä käytettävien nimikkeiden ostolaskujen tulisi vastata sekä ostotilausrivejä että tuotteen vastaanottorivejä (kolmisuuntainen vastaavuus).

Fabrikam toimii useiden yritysten ja työntekijöiden kanssa maailmanlaajuisesti. Kun tapahtumien määrä kasvaa, ristiriidat vastaanottojen ja laskujen välillä kasvavat niiden mukana. Tämä johtaa siihen, että käyttöomaisuuseriä poistetaan kirjanpidosta. Toimittajien laskut maksetaan, mutta prosessi ei sisällä ristiriitojen tunnistamista, kun nimikkeitä vastaanotetaan vähemmän kuin mitä oli tilattu, tai kun nimikkeitä ei vastaanoteta lainkaan. Kulut kasvavat, koska työntekijät tarvitsevat joka tapauksessa työkaluja ja muita materiaaleja töidensä suorittamiseksi. Ken haluaa varmistaa, että toimittajat lähettävät tilatut tuotteet ja että Fabrikamin työntekijät vastaanottavat nimikkeet. Siksi Ken edellyttää kaksi- ja kolmisuuntaista vastaavuutta kaikilta organisaation yrityksiltä. Laskujen täsmäytys auttaa varmistamaan, että ongelmia kadonneiden tai vastaanottamattomien nimikkeiden kanssa on mahdollista seurata ja ratkaista. 

Tässä esimerkissä tarjotut laskun täsmäytyskäytännöt auttavat seuraavissa rooleissa toimivia henkilöitä saavuttamaan nämä tavoitteet:

-   Ken on Fabrikam-nimisen yrityksen vastuuhenkilö. Ken voi auttaa organisaationsa henkilöstöä tunnistamaan ja oikaisemaan toimittajien nimikkeiden, eli tavaroiden ja palveluiden tilauksiin, vastaanottoihin ja maksuihin liittyviä ongelmia.
-   Paula ja April ovat laskentapäälliköitä Fabrikamin Yhdysvaltain haaran ostoreskontraosastolla. He voivat valvoa yrityksen käytäntöjä ja varmistaa, että laskut maksetaan vasta, kun ne on täsmäytetty ostotilaukseen sekä sen ollessa aiheellista, tuotteiden ja palveluiden vastaanottoon.
-   Tony on Fabrikamin Yhdysvaltain haaran tuotantopäällikkö. Tony ja muu tuotantohenkilöstö voi varmistaa, että nimikkeet vastaanotetaan siten, miten ne on tilattu toimittajilta ja että ne ovat seurattavissa niin, että henkilökunnalla on työnsä suorittamiseen vaadittavat resurssit.

### <a name="prerequisites"></a>Edellytykset

-   Ken asettaa vastaavuuskäytännön yritystasolla kolmisuuntaiseksi.
-   Ken asettaa yritystason otsikon tilan automaattisen vastaavuuspäivityksen asetuksen tilaksi Kyllä.
-   Ken asettaa yrityksen Täsmäytä kokonaishinnat -kentän arvoksi Prosenttiosuus ja syöttää 15 % toleranssiprosentiksi.
-   Ken asettaa nimiketason vastaavuuskäytännön kolmisuuntaiseksi nimikkeelle 1500 – CNC Milicron-kone. Tämä nimike on käyttöomaisuusnimike, jota käytetään Fabrikamin tuotannossa. Tätä nimikettä koskevat laskut täsmäytetään hintojen osalta ostotilausriveihin ja määrien osalta tuotteiden vastaanottoihin.
-   Tony kirjaa ostoehdotuksen viidestä CNC Milicron-koneesta. Alicia on ostotilausten käsittelijä Fabrikamilla, joka luo ostotilauksen Contoso-nimiselle yritykselle, joka toimittaa nimikkeet.

    | Nimiketunnus                 | Määrä | Yksikköhinta | Nettosumma | Kulujen koodi        | Kulujen arvo |
    |-----------------------------|----------|------------|------------|---------------------|---------------|
    | 1500 – CNC Milicron-kone | 5        | 8 000,00   | 40 000,00  | Toimitus ja käsittely | 3,000.00      |

-   Arnie, Contoson myyntireskontrakäsittelijä, tarkistaa viikon toimitukset. Hän lähetystapahtumat, jotka laskutetaan Fabrikamilta CNC Milicron-koneiden toimituksesta. Hän lisää lähetys- ja käsittelykulut laskulle. Fabrikam ottaa toimituskulut osaksi käyttöomaisuuden kustannusta.

### <a name="scenario"></a>Skenaario

1.  Sammy, Fabrikamin vastaanotto-osaston työntekijä, vastaanottaa Contoson konetoimituksen kokonaismäärän. Sammy syöttää määräksi 5 tuotteen vastaanotossa. Koska ostotilaus on vastaanotettu kokonaisuudessaan, sen tilaksi muuttuu Vastaanotettu.
2.  Fabrikamin ostoreskontravastaava April kirjaa ja vahvistaa Contoson lähettämän laskun. Hän vahvistaa seuraavat tiedot:
    -   Nimikkeille, joiden vaatimuksena on kolmisuuntainen vastaavuus, laskurivin määrä vastaa vastaanotettua määrää. Vastaanotettu määrä näkyy laskuun kohdistetussa tuotteen vastaanotossa.
    -   Nimikkeiden, joiden vaatimuksena on kaksi- tai kolmisuuntainen vastaavuus, laskurivin hinnat ovat Microsoft Dynamics 365 Financessa asetettujen toleranssien rajoissa. Tähän kuuluvat seuraavat hinnantäsmäytykset:
        -   Nettoyksikköhinnan täsmäytys – Laskurivin nettoyksikköhinta vastaa ostotilausrivin nettoyksikköhintaa toleranssiprosentin rajoissa. Tässä esimerkissä nettoyksikköhinnan hintatoleranssi on +8 %.
        -   Kokonaishinnan täsmäytys – Laskurivin nettohinta vastaa ostotilausrivin nettohintaa toleranssiprosentin, -summan tai molempien rajoissa. Tässä esimerkissä nettohinnan hintatoleranssi on +15 %.

Contoson lähettämä paperilasku sisältää seuraavat tiedot.

| Nimike                        | Määrä | Yksikköhinta | Nettosumma |
|-----------------------------|----------|------------|------------|
| 1500 – CNC Milicron-kone | 5        | 8 100,00   | 40,500.00  |
| Toimitus ja käsittely       |          |            | 4,000.00   |
| Vero                         |          |            | 0,00       |
| Kokonaissumma                       |          |            | 44,500.00  |

Laskurivillä on seuraavat tiedot.

| Nimiketunnus                 | Määrä | Yksikköhinta | Rivin nettosumma | Täsmäytyskäytäntö    | Tuotteen vastaanoton määrän vastaavuus | Hintavastaavuus | Kokonaishintojen täsmäytys |
|-----------------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| 1500 – CNC Milicron-kone | 5        | 8 100,00   | 40 500,00       | Kolmisuuntainen vastaavuus | Hyväksytty                         | Hyväksytty      | Hyväksytty            |

Koska rivi läpäisee laskun täsmäytysprosessin, lasku on mahdollista kirjata.

## <a name="example-three-way-matching-for-item-and-vendor-combinations"></a> Esimerkki: Kolmisuuntainen vastaavuus nimike- ja toimittajayhdistelmille
Yhteenveto: Ken on vastuuhenkilö Fabrikam-nimisen yrityksen pääkonttorissa. Hän päättää, että kaikki laskut, jotka perustuvat ostotilauksiin on yhdistettävä ostotilausriveihin (kaksisuuntainen vastaavuus). Cassie on Fabrikamin Malesian-konttorin kirjanpitäjä. Hän määrittää, että valitut, tietyiltä malesialaisilta toimittajilta tilattavat nimikkeet on täsmäytettävä sekä ostotilauksen riveihin ja tuotteen vastaanottoriveihin (kolmisuuntainen vastaavuus). Hän voi myös ohittaa vastaavuuskäytännön korkeamman tason vastaavuudella haluamilleen ostotilauksille. 

Volyymi ja summat ovat pieniä, ja tiettyjen malesialaistoimittajien lähetyksissä on ollut ongelmia. Tämän vuoksi Cassie määrittää tiettyjen, Malesiasta hankittavien nimike- ja toimittajayhdistelmien hallinnan tasoksi kolmisuuntaisen vastaavuuden. 

Tässä esimerkissä tarjotut laskun täsmäytyskäytännöt auttavat seuraavissa rooleissa toimivia henkilöitä saavuttamaan nämä tavoitteet:
-   Ken on Fabrikam-nimisen yrityksen vastuuhenkilö. Ken voi auttaa organisaationsa henkilöstöä tunnistamaan ja oikaisemaan toimittajien nimikkeiden, eli tavaroiden ja palveluiden tilauksiin, vastaanottoihin ja maksuihin liittyviä ongelmia.
-   Cassie on Fabrikamin Malesian-konttorin kirjanpitäjä. Hän voi valvoa yrityksen käytäntöjä ja varmistaa, että laskut maksetaan vasta, kun ne on täsmäytetty ostotilauksen riveihin sekä tuotteiden vastaanottoihin, jotka vastaavat tuotteita ja palveluita. Hän voi myös nostaa hallinnan tason kolmisuuntaiseksi vastaavuudeksi haluamilleen nimikkeille hallitakseen toiminnan kustannuksia.

### <a name="prerequisites"></a>Edellytykset

-   Ken asettaa vastaavuuskäytännön yritystasolla kaksisuuntaiseksi.
-   Ken asettaa yrityksen Täsmäytä kokonaishinnat -kentän arvoksi Prosenttiosuus ja syöttää 10 % toleranssiprosentiksi.
-   Ken asettaa 2 %:n toleranssiprosentin kaikkiin nimikkeisiin.
-   Cassie asettaa vastaavuuskäytännön nimike- ja toimittajayhdistelmän tasolla nimikkeelle PH2500 – Tietokone ja toimittajalle Contoso kolmisuuntaiseksi vastaavuudeksi.
-   Alicia, Fabrikamin Malesian konttorissa työskentelevä ostotilausten käsittelijä lähettää Contosolle ostotilaukset kolmen nimikkeen toimittamisesta seuraavan taulukon mukaisesti. Kun hän luo ostotilauksen, hän ohittaa langattoman hiiren vastaavuuskäytännön kolmisuuntaiseksi vastaavuudeksi kaksisuuntaisuuden sijasta.

    | Nimiketunnus           | Määrä | Yksikköhinta | Nettosumma | Vastaavuuskäytäntö (oletusarvo) | Vastaavuuskäytäntö (ostotilausrivillä) |
    |-----------------------|----------|------------|------------|---------------------------------|----------------------------------------------|
    | PH2500 – Tietokone     | 2        | 2 500,00   | 5 000,00   | Kolmisuuntainen vastaavuus              | Kolmisuuntainen vastaavuus                           |
    | MM01 – Langaton hiiri | 2        | 40,00      | 80,00      | Kaksisuuntainen vastaavuus                | Kolmisuuntainen vastaavuus                           |
    | USB-muistitikku             | 200      | 10,00      | 2 000,00   | Kaksisuuntainen vastaavuus                | Kaksisuuntainen vastaavuus                             |

### <a name="scenario"></a>Skenaario

1.  Nimikkeet saapuvat. Sammy, työntekijä Fabrikamin Malesian konttorin vastaanotossa keskeytetään työssään eikä kirjaa tuotteen vastaanottoa välittömästi.
2.  Fabrikamin ostoreskontravastaava April kirjaa ja vahvistaa Contoson lähettämän laskun. Hän vahvistaa seuraavat tiedot:
    -   Nimikkeille, joiden vaatimuksena on kolmisuuntainen vastaavuus, laskurivin määrä vastaa vastaanotettua määrää. Vastaanotettu määrä näkyy laskuun kohdistetussa tuotteen vastaanotossa.
    -   Nimikkeiden, joiden vaatimuksena on kaksi- tai kolmisuuntainen vastaavuus, laskurivin hinnat ovat sovelluksessa asetettujen toleranssien rajoissa. Tähän kuuluvat seuraavat hinnantäsmäytykset:
        -   Nettoyksikköhinnan täsmäytys – Laskurivin nettoyksikköhinta vastaa ostotilausrivin nettoyksikköhintaa toleranssiprosentin rajoissa. Tässä esimerkissä nettoyksikköhinnan hintatoleranssi on +2 %.
        -   Kokonaishinnan täsmäytys – Laskurivin nettohinta vastaa ostotilausrivin nettohintaa toleranssiprosentin, -summan tai molempien rajoissa. Tässä esimerkissä nettohinnan hintatoleranssi on +10 %.

Contoson lähettämä paperilasku sisältää seuraavat tiedot.

| Nimike                  | Määrä | Yksikköhinta | Nettosumma |
|-----------------------|----------|------------|------------|
| PH2500 – Tietokone     | 2        | 2 500,00   | 5 000,00   |
| MM01 – Langaton hiiri | 2        | 41.00      | 82.00      |
| USB-muistitikku             | 200      | 10.05      | 2,010.00   |
| Kokonaislasku         |          |            | 7,092.00   |

Laskurivillä on seuraavat tiedot.

| Nimiketunnus           | Määrä | Yksikköhinta | Rivin nettosumma | Täsmäytyskäytäntö    | Tuotteen vastaanoton määrän vastaavuus | Hintavastaavuus | Kokonaishintojen täsmäytys |
|-----------------------|----------|------------|-----------------|--------------------|--------------------------------|-------------|-------------------|
| PH2500 – Tietokone     | 2        | 2 500,00   | 5 000,00        | Kolmisuuntainen vastaavuus | Epäonnistui                         | Hyväksytty      | Hyväksytty            |
| MM01 – Langaton hiiri | 2        | 41,00      | 82,00           | Kolmisuuntainen vastaavuus | Epäonnistui                         | Epäonnistui      | Hyväksytty            |
| USB-muistitikku             | 200      | 10,05      | 2 010,00         | Kaksisuuntainen vastaavuus   |                                | Hyväksytty      | Hyväksytty            |

Huomaa seuraavat nimikkeet:
-   PH2500 – Tietokone -rivin tuotteen vastaanottomäärän vastaavuussarakkeessa on varoituskuvake, koska laskuriviä ei ole täsmäytetty tuotteen vastaanottoon.
-   MM01 – Langaton hiiri -rivin tuotteen vastaanottomäärän vastaavuussarakkeessa on varoituskuvake, koska laskuriviä ei ole täsmäytetty tuotteen vastaanottoon. Yksikköhinnan täsmäytys -sarakkeessa on varoituskuvake, koska nettoyksikköhinnan 2 prosentin hintatoleranssi on ylittynyt.
-   USB-muistitikun rivin tuotteen vastaanottomäärän vastaavuussarake on tyhjä, koska kaksisuuntaisessa vastaavuudessa ei täsmäytetä laskurivin ja tuotteen vastaanottorivin määriä.

Jos laskuille, joilla on laskun täsmäytysristiriitoja vaaditaan hyväksyntä, laskun täsmäytystietojen sivulta on otettava käyttöön Hyväksy kirjaus, jos on täsmäytysristiriitoja -asetus ennen kuin laskun, jolla on hinnan- ja määräntäsmäytysristiriitoja voi kirjata. Jos hyväksyntää ei tarvita, laskun käsittelyä voi jatkaa jos muita kirjausvirheitä ei ole.


Lisätietoja on kohdassa [Ostoreskontran laskujen täsmäytyksen yleiskatsaus](accounts-payable-invoice-matching.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]