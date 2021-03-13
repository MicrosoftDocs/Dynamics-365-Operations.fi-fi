---
title: Oikeutussääntöjen ja -asetusten määrittäminen
description: Määritä oikeutussäännöt ja -vaihtoehdot Microsoftin Dynamics 365 Human Resourcesin etujen hallinnassa.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2920a03eaec226b306d03ebf8b899113128c410e
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112359"
---
# <a name="configure-eligibility-rules-and-options"></a>Oikeutussääntöjen ja -asetusten määrittäminen

Kun olet määrittänyt Microsoft Dynamics 365 Human Resourcesin etujen hallinnan edellyttämät parametrit, voit luoda oikeutussääntöjä, nippuja, kausia ja ohjelmia, jotka liität hyötysuunnitelmiisi.

## <a name="create-an-eligibility-rule"></a>Luo kelpoisuussääntö

Oikeutussäännöissä määritetään, ketkä työntekijät voivat ilmoittautua kuhunkin etuussuunnitelmaan. Kun olet määrittänyt oikeutussäännöt, voit määrittää ne etuussuunnitelmiin. Tämän jälkeen voit käsitellä rekisteröinnin kelpoisuutta nähdäksesi, mitkä työntekijät ovat oikeutettuja kuhunkin suunnitelmaan. 

Avoimessa rekisteröinnissä työntekijät voivat valita etuusjärjestelyjä. Jos ne eivät ole oikeutettuja etuusjärjestelyyn, joka perustuu kelpoisuussääntöihin sen jälkeen, kun ne on jo rekisteröity, niitä ei automaattisesti poisteta. Kun suunnitelman kelpoisuuteen vaikuttava elämäntapahtuma tapahtuu, järjestelmä aloittaa rekisteröintikauden, jonka aikana työntekijä voi valita suunnitelmat, joihin on oikeutettu. 

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Luo kelpoisuussääntö valitsemalla **kelpoisuussäännöt**-välilehdessä **Uusi**. Jos haluat nähdä kelpoisuussääntöön liittyvät suunnitelmat, valitse **liitetyt suunnitelmat**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Kelpoisuussääntö** | Kelpoisuussäännön yksilöivä tunniste. |
   | **Kuvaus** | Kelpoisuussäännön kuvaus. |
   | **Voimaantulopäivämäärä ja -aika** | Kelpoisuussäännön aloituspäivämäärä. | 
   | **Voimassaolon päättymispäivämäärä ja -aika** | Kelpoisuussäännön lopetuspäivämäärä. |
   | **Käyttäjän työntekijätyyppi** | Määrittää, käytetäänkö työntekijän työntekijätyyppiä edun oikeutussäännössä. |
   | **Työntekijätyyppi** | Työntekijän tyyppi, jos **Käytä työntekijätyyppiä** -vaihtoehdon arvoksi on määritetty **Kyllä**. |
   | **Käytä työntekijän tilaa** | Määrittää, käytetäänkö työntekijän tilaa edun oikeutussäännössä. |
   | **Tila** | Työntekijän tila, jos **Käytä työntekijän tilaa** -vaihtoehdon arvoksi on määritetty **Kyllä**. Jos **Käytä työntekijän tilaa** -vaihtoehdon arvoksi on määritetty **Ei**, kenttää ei käytetä. |
   | **Käytä työsuhdeluokkaa** | Määrittää, käytetäänkö työntekijän **Työllisyysluokka**-arvoa osana edun oikeutussääntöä. | 
   | **Työsuhdeluokka** | Työntekijän työsuhdeluokka, jos **Käytä työsuhdetta** -luokan vaihtoasetus on **Kyllä**. |
   | **Käytä uutta työhönottosääntöä** | Määrittää, käytetäänkö uuden vuokrauksen uutta työhönottokauden arvoa osana etuuksien oikeutussääntöä. |
   | **Rekisteröitymiskausi** | Ajanjakso, jolloin uusi työhönottoilmoitus on sallittu. Jos määrität tämän myös parametreissa, parametrien asetus ohittaa tämän asetuksen. |
   | **Käytä aiempaa työsuhteen tilaa** | Määrittää, käytetäänkö työntekijän edellistä työllisyysarvoa osana etujen oikeutussääntöä. Voit esimerkiksi määrittää oikeutussäännön, joka luopuu kattavuusodotusjaksosta kaikkien niiden työntekijöiden kohdalla, jotka ovat siirtyneet **Lomautus**-tilasta **Työssä**-tilaan 90 päivän kuluessa edellisen työsuhteen päättymisestä. |

4. Valitse **Lisäehdot**-kohdasta seuraavat vaihtoehdot ja lisää tarvittavat tiedot:

   | Vaihtoehto | Kuvaus |
   | --- | --- |
   | **Sallittu ikä** | Määrittää kelpoisuussäännön täyttämiseen vaadittavat ikäalueet. |
   | **Sallittu osasto** | Määrittää osaston tai osastot, joihin työntekijän on kuuluttava kelpoisuussäännön täyttämiseksi. |
   | **Sallittu työsuhteen tyyppi** | Määrittää työllisyystyypin tai -tyypit, joihin työntekijä on luokiteltava kelpoisuussäännön täyttämiseksi. Esimerkiksi koko- tai osa-aikainen. |
   | **Sallittu työ** | Määrittää kelpoisuussääntöä vastaavat työt. Työt liitetään toimiin, ja toimet täytetään työntekijöillä. |
   | **Sallittu työtehtävä** | Määrittää kelpoisuussääntöä vastaavan työtehtävän tai -tehtävät. Esimerkiksi myyntityöntekijät tai teknikot. |
   | **Sallitun työn tyyppi** | Määrittää kelpoisuussääntöä vastaavan työtyypin tai -tyypit. Esimerkiksi toimisto tai johto. |
   | **Sallittu yritys** | Määrittää yrityksen tai yritykset, jotka ovat kelvollisia kelpoisuussäännölle. Esimerkiksi Contoso Entertainment System USA. |
   | **Hyväksytty kompensaatioalue** | Määrittää kelpoisuussäännön täyttävän työntekijän sijainnin. Syötä arvoksi esimerkiksi Keski-Yhdysvallat. |
   | **Sallittu toimi** | Määrittää kelpoisuussääntöä vastaavan toimen tai toimet. Esimerkiksi HR-assistentti tai henkilöstöpäällikkö. |
   | **Sallittu toimen tyyppi** | Määrittää kelpoisuussääntöä vastaavan toimityypin tai -tyypit. Esimerkiksi kokoaikainen. |
   | **Sallittu tila** | Määrittää kelpoisuussääntöä vastaavat osavaltiot tai provinssit. Esimerkiksi Pohjois-Dakota USA tai Brittiläinen Kolumbia, Kanada. |
   | **Sallitut työehdot** | Määrittää kelpoisuussäännön täyttävät työntekijän työehdot. Esimerkiksi halutessaan tai ryhmäsopimus. |
   | **Sallittu järjestö** | Määrittää kelpoisuussääntöä vastaavan ammattiliiton jäsenyyden. Esimerkiksi Forklift Drivers of America. </br></br>Kun käytetään liittoon perustuvaa kelpoisuussääntöä, työntekijän ammattiliiton tietueen päättymispäivämäärä on täytettävä. Et voi jättää sitä tyhjäksi. |
   | **Kelvollinen postinumero** | Määrittää kelpoisuussääntöä vastaavat postinumerot. Esimerkki: 58104. |

5. **Lisätiedot**-kohdassa voit tarkastella seuraavia lisätietoja:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Sallittu käyttäjän kenttä** | Määrittää lisäkelpoisuussäännöt asiakkaan määrittämien kenttien perusteella. |
   | **Kelpoisuuden tyyppi** | Määrittää **lisäehdoissa** valitun ehtoluokan. |
   | **Kelpoisuuden viite** | Määrittää **lisäehdoissa** valitut arvot. |
   | **Kuvaus** | Määrittää **lisäehdoissa** valitun kuvauksen. |

6. Valitse **Tallenna**.

## <a name="configure-bundles"></a>Määritä niput

Niput ovat liittyvien etuussuunnitelmien joukko. Etuusnippujen avulla voit ryhmitellä etuussuunnitelmia, jotka työntekijän on valittava voidakseen ilmoittautua tiettyihin etuussuunnitelmiin, jotka voivat olla riippuvaisia muista etuussuunnitelmien ilmoittautumisista. Esimerkkejä siitä, milloin nippua kannattaa käyttää, ovat esimerkiksi seuraavat:

- Terveyssuunnitelmanippu, joka sisältää korkeasti vähennyskelpoisen sairausvakuutuksen ja siihen liittyvän terveyssäästötilin (HSA).

- Henkivakuutussuunnitelma, jossa on pakollinen työntekijän henkivakuutussuunnitelma, johon liittyy riippuvaisen elämän suunnitelma. Näin varmistetaan, että työntekijä ei voi valita riippuvaista elämän kattavuutta kirjautumatta työntekijän kattavuus -kohtaan.

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Luo nippu valitsemalla **Niput**-välilehdessä **Uusi**. Jos haluat nähdä nippuun liittyvät suunnitelmat, valitse **liitetyt suunnitelmat**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Nippu** | Nipun yksilöivä tunniste. |
   | **Kuvaus** | Nipun kuvaus. |
   | **Päärahtikirja** | Ilmaisee, kuuluuko jokin nipun suunnitelmista merkitä pääsuunnitelmaksi. Pääsuunnitelma on valittava avoimen rekisteröinnin yhteydessä osana pakettia, ennen kuin hyödyt-järjestelmänvalvoja voi vahvistaa työntekijän etuvalinnat. |
   | **Voimaantulopäivämäärä ja -aika** | Päivämäärä ja aika, jolloin nipusta tulee aktiivinen. |
   | **Voimassaolo päättyy** | Nipun vanhentumisen päivämäärä. Oletusarvo on 12/31/2154, joka vastaa ei koskaan -arvoa. |

4. Valitse **Tallenna**.

## <a name="configure-periods"></a>Kausien konfiguroiminen

Kaudet määrittävät, milloin etuudet ovat voimassa ja milloin työntekijät voivat ilmoittautua. Voit luoda niin monta jaksoa kuin haluat, jotta hyödyt pysyvät avoimina rekisteröinnissä ja etuuksien kattavuuskausina. Etuussuunnitelmavuodet voivat olla kalenterivuoden jälkeen. 

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Luo kausi valitsemalla **kaudet**-välilehdessä **Uusi**. Jos haluat suorittaa prosessin, joka liittää kaikki kelvolliset aktiiviset hyötysuunnitelmat etuuskauteen, valitse **Liitä suunnitelmat**. Jos haluat nähdä nippuun liittyvät suunnitelmat, valitse **liitetyt suunnitelmat**. 

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Kausi** | Kauden yksilöivä tunniste. |
   | **Voimaantulopäivämäärä ja -aika** | Aloituspäivämäärä ja -aika, jona etuuskausi on aktiivinen. |
   | **Voimassaolon päättymispäivämäärä ja -aika** | Päivämäärä ja -aika, jona etuuskausi muuttuu passiiviseksi. |
   | **Rekisteröinnin aloittaminen** | Avoimen ilmoittautumisen aloituspäivämäärä. Avoin ilmoittautuminen tarkoittaa sitä, kun työntekijä voi tehdä etuusvalintoja itsepalveluetuuksissa. |
   | **Rekisteröinnin päättyminen** | Avoimen ilmoittautumisen lopetuspäivämäärä. |
   | **Avoinna** | Ilmaisee, onko kausi avoin järjestelmän päivämäärän ja voimassaolon alkamis- ja päättymispäivien sekä -aikojen perusteella. | 
   | **Edellinen jakso** | Määrittää valittua etuuskautta edeltävän etuuskauden. Näitä tietoja käytetään etuuskelpoisuuden rekisteröinnin yhteydessä, kun halutaan määrittää edellisen vuoden suunnitelmat, kattavuusasetukset ja vaihtoehdot. |
 
4. Valitse **Tallenna**.

## <a name="use-a-flex-credit-program"></a>Joustavan luotto-ohjelman käyttäminen

Joustavien luotto-ohjelmien avulla voit rekisteröidä työntekijät etuuksien mukaan ennalta määrätyn määrän joustavia luottohyvityksiä. Työntekijät voivat valita, miten he kohdistavat joustopisteensä. Jos työntekijä esimerkiksi kuuluu puolisonsa terveyenhoitosuunnitelman piiriin, hän saattaa haluta käyttää muuten terveydenhoitoon käyttämänsä pisteet muihin etuihin.

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Valitse **Kaudet**-välilehdestä **Joustoluotto-ohjelmat**.

3. Valitse käytettävä joustoluotto-ohjelma. Kentät sisältävät seuraavat tiedot:

   | Kenttä | Kuvaus |
   | --- | --- |
   | Etuhyvityksen tunnus | Joustavien pisteiden ohjelman yksilöllinen tunnus. |
   | Kuvaus | Joustavien pisteiden ohjelman kuvaus. | 
   | Päivämäärästä | Päivämäärä ja aika, jolloin joustavien pisteiden ohjelma tulee voimaan. |
   | Päivämäärään | Joustavien pisteiden järjestelmän päättymispäivä. Voit jättää säilyttää oletusarvon (12/31/2154) osoittamaan, että joustavien pisteiden järjestelmän päättymispäivää ei ole aikataulutettu. |
   | Hyvityksen arvo yhteensä | Niiden pisteiden määrä, joka jokaisella työntekijällä on käytettävissään etujaan varten. |
   | Suhteellisen jaon sääntö | Sääntö, jota käytetään joustavien pisteiden suhteelliseen laskentaan, kun työntekijä palkataan keskellä joustavien pisteiden jaksoa. </br></br><ul><li>**Ei yhtään** – Työntekijä ei saa joustavia pisteitä, jos hänet palkataan joustavien pisteiden ohjelmajakson alkamisen jälkeen.</li><li>**Täydet pisteet** – Työntekijä saa täyden määrän joustavia pistetiä riippumatta hänen palkkaushetkestään.</li><li>**Suhteellinen** – Työntekijä saa aloituspäiväänsä perustuvan suhteellisen määrän joustavia pisteitä.</li></ul> |
   | Joustavien pisteiden suhteellisen laskennan kaava | Sääntö, jota käytetään joustavien pisteiden suhteelliseen laskentaan, kun työntekijä palkataan keskellä joustavien pisteiden ohjelman etuusjaksoa. Suhteellinen laskenta perustuu työsuhteen alkamispäivään. Tämä kenttä on käytettävissä vain, jos valitset **Suhteellinen** kentässä **Suhteellisuussääntö**. </br></br><ul><li>**Päivittäin** – Laskee työntekijän saamien joustavien pisteiden suhteellisen määrän päivätasolla. Joustavien pisteiden kokonaismäärä jaetaan jakson päivien määrällä. Jos etuusjakso esimerkiksi on 400 päivää, järjestelmä jakaa joustavien pisteiden kokonaismäärän luvulla 400 laskeakseen työntekijöiden päivittäin saamien joustavien pisteiden määrän.</li><li>**Kuluva kuukausi** – Laskee työntekijän saamien joustavien pisteiden suhteellisen määrän kuukausitasolla kuluvaan kuukauteen pyöristettynä. Joustavien pisteiden kokonaismäärä jaetaan jakson kuukausien määrällä. Jos etuusjakso esimerkiksi on 15 kuukautta, järjestelmä jakaa joustavien pisteiden kokonaismäärän luvulla 15 laskeakseen työntekijöiden kuukausittain saamien joustavien pisteiden määrän.</li><li>**Seuraava kuukausi** – Laskee työntekijän saamien joustavien pisteiden suhteellisen määrän kuukausitasolla seuraavaan kuukauteen pyöristettynä. Joustavien pisteiden kokonaismäärä jaetaan jakson kuukausien määrällä. Jos etuusjakso esimerkiksi on 15 kuukautta, järjestelmä jakaa joustavien pisteiden kokonaismäärän luvulla 15 laskeakseen työntekijöiden kuukausittain saamien joustavien pisteiden määrän.</li></ul> |
   
   Varmista, että kukin etuussuunnitelma on rekisteröity vain yhteen joustoluotto-ohjelmaan kutakin etuusjaksoa kohden. Muussa tapauksessa järjestelmä ei tiedä, mitä joustoluotto-ohjelmaa tulee käyttää joustoluottohyvitysten myöntämiseen, ja kohtaat ongelmia. 

## <a name="configure-programs"></a>Ohjelmien määrittäminen

Ohjelmat ovat joukko etuussuunnitelmia, joilla on yhteiset kelpoisuussäännöt. Voit määrittää koko ohjelman kelpoisuussäännöt kunkin erillisen suunnitelman asemesta. Esimerkki: Contoso Canada FTE-ohjelma tai Contoso Europen johtotason ohjelma. 

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Luo ohjelma valitsemalla **Ohjelmat**-välilehdessä **Uusi**. Jos haluat tehdä poikkeuksia niille työntekijöille, jotka eivät täytä kelpoisuussäännön vaatimuksia, valitse **Oikeutussäännön ohitus**. Jos haluat nähdä ohjelmaan liittyvät suunnitelmat, valitse **Liitetyt suunnitelmat**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Ohjelma** | Ohjelman yksilöivä tunniste. |
   | **Kuvaus** | Ohjelman kuvaus. | 
   | **Voimaantulopäivämäärä ja -aika** | Päivämäärä ja aika, jolloin ohjelmasta tulee aktiivinen. |
   | **Voimassaolon päättymispäivämäärä ja -aika** | Päivämäärä ja aika, jolloin ohjelma vanhenee. Oletusarvo on 12/31/2154, joka vastaa ei koskaan -arvoa. |
   | **Kattavuuden odotusaika** | Aika, jonka työntekijän on odotettava, ennen kuin etuusohjelman kattavuus alkaa. |
   | **Vähennyksen odotusaika** | Aika, jonka työntekijä odottaa, ennen kuin etuusohjelman vähennykset alkavat. |
   | **Oikeutussäännöt** | Valitse etuuksia koskevaan ohjelmaan sovellettavat kelpoisuussäännöt. Voit määrittää kelpoisuussäännöt tämän sivun **Kelpoisuussäännöt**-välilehdessä. |
   
4. Valitse **Tallenna**.
