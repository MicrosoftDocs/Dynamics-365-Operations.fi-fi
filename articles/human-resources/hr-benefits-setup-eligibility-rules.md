---
title: Oikeutussääntöjen ja -asetusten määrittäminen
description: Tässä artikkelissa käsitellään oikeutussääntöjen ja -asetusten määrittämistä Microsoft Dynamics 365 Human Resourcesi etujenhallinnassa.
author: twheeloc
ms.date: 09/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 916a9955327aef67ac768d4505bdb343862058a1
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644081"
---
# <a name="configure-eligibility-rules-and-options"></a>Oikeutussääntöjen ja -asetusten määrittäminen 

Kun olet määrittänyt Etujen hallinnan edellyttämät parametrit, voit luoda oikeutussäännöt, paketteja, kausia ja ohjelmia etupaketteihin liitettäviksi.

Kelpoisuussääntöjen avulla määritetään, ovatko työntekijät oikeutettuja palvelupakettiin. Työntekijän on täytettävä vähintään yhden säännön edellytys, jotta hänen voidaan katsoa olevan oikeutettu etuuteen. Palvelupakettiin voi esimerkiksi sisältyä kaksi sääntöä. Ensimmäisessä säännössä (rivi 1) todetaan, että työntekijätyypin on oltava **Työntekijä**. Toisessa säännössä (rivi 2) todetaan, että työntekijän on oltava kokopäiväisessä työsuhteessa. Näin ollen työntekijät, jotka täyttävät säännön 1, täyttävät kelpoisuusvaatimukset, vaikka he olisivat vain osa-aikaisia.

Voit kuitenkin määrittää yhden säännön, jolla on useita ehtoja. Tässä tapauksessa työntekijän on täytettävä kaikki säännön ehdot, jotta hänen voidaan katsoa olevan oikeutettu etuuteen. Sinulla on esimerkiksi sääntö, jonka nimi on **Kokopäivätyöntekijä**. Tämän säännön mukaan työntekijätyypin on oltava **Työntekijä** ja työntekijän on oltava *kokopäivätyössä*. Siten työntekijöiden on täytettävä säännön molemmat ehdot ollakseen tukikelpoisia.

> [!IMPORTANT]
> Jokaiseen etuussuunnitelmaan on liityttävä vähintään yksi kelpoisuussääntö. Voit liittää etuun useita sääntöjä.

## <a name="create-an-eligibility-rule"></a>Luo kelpoisuussääntö

Oikeutussäännöissä määritetään, ketkä työntekijät voivat ilmoittautua kuhunkin etuussuunnitelmaan. Kun olet määrittänyt oikeutussäännöt, voit määrittää ne etuussuunnitelmiin. Tämän jälkeen voit käsitellä rekisteröinnin kelpoisuutta nähdäksesi, mitkä työntekijät ovat oikeutettuja kuhunkin suunnitelmaan. 

Avoimessa rekisteröinnissä työntekijät voivat valita etuusjärjestelyjä. Jos he eivät ole oikeutettuja etuusjärjestelyyn, joka perustuu kelpoisuussääntöihin sen jälkeen, kun heidät on jo rekisteröity, heitä ei automaattisesti poisteta. Kun suunnitelman kelpoisuuteen vaikuttava elämäntapahtuma tapahtuu, järjestelmä aloittaa rekisteröintikauden, jonka aikana työntekijä voi valita suunnitelmat, joihin on oikeutettu. 

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Luo kelpoisuussääntö valitsemalla **kelpoisuussäännöt**-välilehdessä **Uusi**. Jos haluat nähdä kelpoisuussääntöön liittyvät suunnitelmat, valitse **liitetyt suunnitelmat**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | kuvaus |
   | --- | --- |
   | **Kelpoisuussääntö** | Kelpoisuussäännön yksilöivä tunniste. |
   | **Kuvaus** | Kelpoisuussäännön kuvaus. |
   | **Voimaantulopäivämäärä ja -aika** | Kelpoisuussäännön aloituspäivämäärä. | 
   | **Voimassaolon päättymispäivämäärä ja -aika** | Kelpoisuussäännön lopetuspäivämäärä. |
   | **Käyttäjän työntekijätyyppi** | Määrittää, käytetäänkö työntekijän työntekijätyyppiä edun oikeutussäännössä. |
   | **Työntekijätyyppi** | Työntekijän tyyppi, jos **Käytä työntekijätyyppiä** -vaihtoehdon arvoksi on määritetty **Kyllä**. |
   | **Käytä työntekijän tilaa** | Määrittää, käytetäänkö työntekijän työsuhteen tilaa edun oikeutussäännössä. |
   | **Tila** | Työntekijän tila, jos **Käytä työntekijän tilaa** -vaihtoehdon arvoksi on määritetty **Kyllä**. Jos **Käytä työntekijän tilaa** -vaihtoehdon arvoksi on määritetty **Ei**, kenttää ei käytetä. |
   | **Käytä työsuhdeluokkaa** | Määrittää, käytetäänkö työntekijän **Työllisyysluokka**-arvoa osana edun oikeutussääntöä. | 
   | **Työsuhdeluokka** | Työntekijän työsuhdeluokka, jos **Käytä työsuhdetta** -luokan vaihtoasetus on **Kyllä**. |
   | **Käytä uutta työhönottosääntöä** | Määrittää, käytetäänkö uuden työntekijän uutta työhönottokauden arvoa osana etuuksien oikeutussääntöä. |
   | **Rekisteröitymiskausi** | Ajanjakso, jolloin uusi työhönottoilmoitus on sallittu. Jos määrität tämän myös parametreissa, parametrien asetus ohittaa tämän asetuksen. |
   | **Käytä aiempaa työsuhteen tilaa** | Määrittää, käytetäänkö työntekijän edellistä työllisyysarvoa osana etujen oikeutussääntöä. Voit esimerkiksi määrittää oikeutussäännön, joka luopuu kattavuusodotusjaksosta kaikkien niiden työntekijöiden kohdalla, jotka ovat siirtyneet **Lomautus**-tilasta **Työssä**-tilaan 90 päivän kuluessa edellisen työsuhteen päättymisestä. |

4. Valitse **Lisäehdot**-kohdasta seuraavat vaihtoehdot ja lisää tarvittavat tiedot.

   | Vaihtoehto | kuvaus |
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
   | **Sallittu järjestö** | Määrittää kelpoisuussääntöä vastaavan ammattiliiton jäsenyyden. Esimerkiksi Forklift Drivers of America.</br></br>Kun käytetään liittoon perustuvaa kelpoisuussääntöä, työntekijän ammattiliiton tietueen päättymispäivämäärä on täytettävä. Et voi jättää sitä tyhjäksi. |
   | **Kelvollinen postinumero** | Määrittää kelpoisuussääntöä vastaavat postinumerot. Esimerkki: 58104. |

5. **Lisätiedot**-kohdassa voit tarkastella seuraavia lisätietoja.

   | Kenttä | kuvaus |
   | --- | --- |
   | **Sallittu käyttäjän kenttä** | Määrittää lisäkelpoisuussäännöt asiakkaan määrittämien kenttien perusteella. |
   | **Kelpoisuuden tyyppi** | Määrittää **lisäehdoissa** valitun ehtoluokan. |
   | **Kelpoisuuden viite** | Määrittää **lisäehdoissa** valitut arvot. |
   | **Kuvaus** | Määrittää **lisäehdoissa** valitun kuvauksen. |

6. Valitse **Tallenna**.

## <a name="using-custom-fields-in-eligibility-rules"></a>Mukautettujen kenttien käyttäminen oikeutussäännöissä

[Mukautettuja kenttiä](hr-developer-custom-fields.md) voidaan luoda henkilöstöhallintoon lisätietojen seuraamista varten. Nämä kentät voidaan lisätä suoraan käyttöliittymään, ja sarake lisätään dynaamisesti pohjana olevaan tauluun.  

Mukautettuja kenttiä voidaan käyttää oikeutusprosessissa. Oikeutussäännöt voivat määrittää työntekijän oikeuden käyttää yhtä tai useaa mukautettua kenttää.  Voit lisätä mukautetun kentän aiemmin luotuun sääntöön tai luoda uuden säännön kohdassa **Etujen hallinta > Linkit > Asetus > Oikeutussäännöt > Mukautetun kentän oikeutukset**. Tällä sivulla voit luoda säännön, joka käyttää yhtä tai useita mukautettuja kenttiä, ja voit määrittää kullekin mukautetulle kentälle useita arvoja oikeutuksen määrittämiseksi.

Seuraavat taulut tukevat mukautettuja kenttiä, joita voi käyttää oikeutuksen käsittelyssä:

- Työntekijä (HcmWorker)  
- Työ (HcmJob)  
- Toimi (HcmPosition)  
- Toimen tiedot (HcmPositionDetail)  
- Toimen työntekijän toimeksianto  
- Työsuhde (HcmEmployment)  
- EmploymentDetails (HcmEmploymentDetails)  
- Työn tiedot (HcmJobDetails)  

Seuraavia mukautettuja kenttätyyppejä tuetaan oikeutuksen käsittelyssä:

- Teksti  
- Valintaluettelo  
- Numero  
- Desimaali  
- Valintaruutu  

Seuraavassa taulukossa näkyvät mukautetun kentän oikeutuslomakkeen kenttätiedot.

| Kenttä  | kuvaus |
|--------|-------------|
| Nimi | Luotavan kriteerin nimi. |
| Taulun nimi | Oikeutussäännössä käytetyn mukautetun kentän sisältävä taulun nimi. |
| Kentän nimi | Oikeutussäännössä käytettävä kenttä. |
| Operaattorin tyyppi | Näyttää mukautetussa kentän oikeutuskonfiguraatiossa käytetyn operaattorin. |
| Arvo | Näyttää mukautetussa kentän oikeutuskonfiguraatiossa käytetyn arvon. |

## <a name="eligibility-logic"></a>Oikeutuslogiikka

Seuraavissa osissa kuvataan, miten etujen oikeutus käsitellään.

### <a name="rules-assigned-to-a-plan"></a>Suunnitelmalle määritetyt säännöt 
Kun etusuunnitelmaan on liitetty useita oikeutussääntöjä, työntekijän on täytettävä vähintään yksi sääntö, jotta hän voi rekisteröityä etusuunnitelmaan.  Seuraavassa esimerkissä työntekijän on joko täytettävä **Työlaji**-säännön tai **Aktiiviset työntekijät** -säännön vaatimukset.

![Työntekijän on joko täytettävä Työlaji-säännön tai Aktiiviset työntekijät -säännön vaatimukset.](media/RulesAssignedToAPlan.png)
 
### <a name="criteria-within-an-eligibility-rule"></a>Oikeutussäännön kriteerit 
Säännön sisällä määritetään säännön muodostavat ehdot. Edellä olevassa esimerkissä **Työlaji**-säännön ehtona on, että työlaji on johtaja. Tämän vuoksi työntekijän on oltava johtaja, jotta hän voi olla oikeutettu. Tässä säännössä sääntö on vain yksi ehto.

Voit määrittää sääntöjä, joilla on useita ehtoja. Kun määrität oikeutussääntöön useita ehtoja, työntekijän on täytettävä kaikki säännön ehdot, jotta hän voi olla oikeutettu etusuunnitelmaan. 

Esimerkiksi yllä oleva **Aktiiviset työntekijät** -sääntö koostuu seuraavista ehdoista. Jotta työntekijä olisi oikeutettu **Aktiivisten työntekijöiden** säännön perusteella, työntekijän on työskenneltävä yrityksessä USMF *ja* hänen toimensa on oltava tyyppiä kokoaikainen.  

![Oikeutussäännön kriteerit.](media/CriteriaWithinAnEligibilityRule.png) 
 
### <a name="multiple-conditions-within-criteria"></a>Sääntöjen sisällä useita ehtoja

Sääntöjä voidaan laajentaa edelleen käyttämään useita ehtoja yhden ehdon sisällä. Työntekijän on täytettävä vähintään yksi ehto, jotta hän voi olla oikeutettu. Edellä olevan esimerkin perusteella **aktiivisten työntekijöiden** sääntö voidaan laajentaa niin, että siinä on myös osa-aikatyöntekijöitä. Tästä syystä työntekijän on oltava USMF:n työntekijä *ja* joko koko-aikainen tai osa-aikainen työntekijä.  

![Sääntöjen sisällä useita ehtoja.](media/MultipleConditionsWithinCriteria.png) 
 
### <a name="eligibility-conditions-within-a-custom-field-criterion"></a>Mukautetun kentän ehtojen oikeutusehdot 
Yllä kuvatut kentät muistuttavat sitä, että mukautettuja kenttiä voidaan käyttää luotaessa oikeutussääntöjä ja toimimalla samalla tavalla. Voit esimerkiksi tarjota Internet-hyvityksen Fargon ja Kööpenhaminan työntekijöille, jotka työskentelevät kotona, koska Internet-kustannukset ovat suuremmat näissä sijainneissa. Voit tehdä tämän luomalla kaksi mukautettua kenttää: **Toimiston sijainti** (valintaluettelo) ja **Työskentelee kotona** (valintaruutu). Luo sitten sääntö nimeltä **WFH-työntekijät**. Säännön ehtona on, että **Toimiston sijainti = Fargo** tai **Kööpenhamina** *ja* **Työskentelee kotoa = Kyllä**.

Mukautetut oikeutussäännöt on määritettävä seuraavassa kuvassa kuvatun mukaisesti. 

![Mukautetun kentän ehtojen oikeutusehdot.](media/EligibilityConditionsWithinACustomFieldCriterion.png) 
 
## <a name="configure-bundles"></a>Määritä niput

Niput ovat liittyvien etuussuunnitelmien joukko. Etuusnippujen avulla voit ryhmitellä etuussuunnitelmia, jotka työntekijän on valittava voidakseen ilmoittautua tiettyihin etuussuunnitelmiin, jotka voivat olla riippuvaisia muista etuussuunnitelmien ilmoittautumisista. Esimerkkejä siitä, milloin nippua kannattaa käyttää, ovat esimerkiksi seuraavat:

- Terveyssuunnitelmanippu, joka sisältää korkeasti vähennyskelpoisen sairausvakuutuksen ja siihen liittyvän terveyssäästötilin (HSA).

- Henkivakuutussuunnitelma, jossa on pakollinen työntekijän henkivakuutussuunnitelma, johon liittyy riippuvaisen elämän suunnitelma. Näin varmistetaan, että työntekijä ei voi valita riippuvaista elämän kattavuutta kirjautumatta työntekijän kattavuus -kohtaan.

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Luo nippu valitsemalla **Niput**-välilehdessä **Uusi**. Jos haluat nähdä nippuun liittyvät suunnitelmat, valitse **liitetyt suunnitelmat**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | kuvaus |
   | --- | --- |
   | **Nippu** | Nipun yksilöivä tunniste. |
   | **Kuvaus** | Nipun kuvaus. |
   | **Päärahtikirja** | Ilmaisee, kuuluuko jokin nipun suunnitelmista merkitä pääsuunnitelmaksi. Pääsuunnitelma on valittava avoimen rekisteröinnin yhteydessä osana pakettia, ennen kuin etujen järjestelmänvalvoja voi vahvistaa työntekijän etuvalinnat. |
   | **Vaadittu**| Osoittaa, että suunnitelma on valittava nipun minkä tahansa muun suunnitelman uloskuittaamiseksi. Useita suunnitelmia voi merkitä **pakollisiksi**. Tällöin kaikki **pakollisiksi** merkityt suunnitelmat on valittava, jotta nipusta voi kuitata ulos jonkin suunnitelman.|
   | **Voimaantulopäivämäärä ja -aika** | Päivämäärä ja aika, jolloin nipusta tulee aktiivinen. |
   | **Voimassaolo päättyy** | Nipun vanhentumisen päivämäärä. Oletusarvo on 12/31/2154, joka vastaa ei koskaan -arvoa. |

4. Valitse **Tallenna**.

## <a name="configure-periods"></a>Kausien konfiguroiminen

Kaudet määrittävät, milloin etuudet ovat voimassa ja milloin työntekijät voivat ilmoittautua. Voit luoda niin monta jaksoa kuin haluat, jotta hyödyt pysyvät avoimina rekisteröinnissä ja etuuksien kattavuuskausina. Etuussuunnitelmavuodet voivat olla kalenterivuoden jälkeen. 

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Luo kausi valitsemalla **kaudet**-välilehdessä **Uusi**. Jos haluat suorittaa prosessin, joka liittää kaikki kelvolliset aktiiviset hyötysuunnitelmat etuuskauteen, valitse **Liitä suunnitelmat**. Jos haluat nähdä nippuun liittyvät suunnitelmat, valitse **liitetyt suunnitelmat**. 

3. Määritä seuraavien kenttien arvot.

   | Kenttä | kuvaus |
   | --- | --- |
   | **Jakso** | Kauden yksilöivä tunniste. |
   | **Voimaantulopäivämäärä ja -aika** | Aloituspäivämäärä ja -aika, jona etuuskausi on aktiivinen. |
   | **Voimassaolon päättymispäivämäärä ja -aika** | Päivämäärä ja -aika, jona etuuskausi muuttuu passiiviseksi. |
   | **Rekisteröinnin aloittaminen** | Avoimen ilmoittautumisen aloituspäivämäärä. Avoin ilmoittautuminen tarkoittaa sitä, kun työntekijä voi tehdä etuusvalintoja itsepalveluetuuksissa. |
   | **Rekisteröinnin päättyminen** | Avoimen ilmoittautumisen lopetuspäivämäärä. |
   | **Avoinna** | Ilmaisee, onko kausi avoin järjestelmän päivämäärän ja voimassaolon alkamis- ja päättymispäivien sekä -aikojen perusteella. | 
   | **Edellinen jakso** | Määrittää valittua etuuskautta edeltävän etuuskauden. Näitä tietoja käytetään etuuskelpoisuuden rekisteröinnin yhteydessä, kun halutaan määrittää edellisen vuoden suunnitelmat, kattavuusasetukset ja vaihtoehdot. |
 
4. Valitse **Tallenna**.

## <a name="use-a-flex-credit-program"></a>Joustavan luotto-ohjelman käyttäminen

Joustavien luotto-ohjelmien avulla voit rekisteröidä työntekijät etuuksien mukaan ennalta määrätyn määrän joustavia luottohyvityksiä. Työntekijät voivat valita, miten he kohdistavat joustopisteensä. Jos työntekijä esimerkiksi kuuluu puolisonsa terveydenhoitosuunnitelman piiriin, hän saattaa haluta käyttää muuten terveydenhoitoon käyttämänsä pisteet muihin etuihin.

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Valitse **Kaudet**-välilehdestä **Joustoluotto-ohjelmat**.

3. Valitse käytettävä joustoluotto-ohjelma. Kentät sisältävät seuraavat tiedot.

   | Kenttä | kuvaus |
   | --- | --- |
   | **Etuhyvityksen tunnus** | Joustavien pisteiden ohjelman yksilöllinen tunnus. |
   | **Kuvaus** | Joustavien pisteiden ohjelman kuvaus. | 
   | **Päivämäärästä** | Päivämäärä ja aika, jolloin joustavien pisteiden ohjelma tulee voimaan. |
   | **Päivämäärään** | Joustavien pisteiden järjestelmän päättymispäivä. Voit jättää säilyttää oletusarvon (12/31/2154) osoittamaan, että joustavien pisteiden järjestelmän päättymispäivää ei ole aikataulutettu. |
   | **Hyvityksen arvo yhteensä** | Niiden pisteiden määrä, joka jokaisella työntekijällä on käytettävissään etujaan varten. |
   | **Suhteellisen jaon sääntö** | Sääntö, jota käytetään joustavien pisteiden suhteelliseen laskentaan, kun työntekijä palkataan keskellä joustavien pisteiden jaksoa. </br></br><ul><li>**Ei yhtään** – Työntekijä ei saa joustavia pisteitä, jos hänet palkataan joustavien pisteiden ohjelmajakson alkamisen jälkeen.</li><li>**Täydet pisteet** – Työntekijä saa täyden määrän joustavia pistetiä riippumatta hänen palkkaushetkestään.</li><li>**Suhteellinen** – Työntekijä saa aloituspäiväänsä perustuvan suhteellisen määrän joustavia pisteitä.</li></ul> |
   | **Joustavien pisteiden suhteellisen laskennan kaava** | Sääntö, jota käytetään joustavien pisteiden suhteelliseen laskentaan, kun työntekijä palkataan keskellä joustavien pisteiden ohjelman etuusjaksoa. Suhteellinen laskenta perustuu työsuhteen alkamispäivään. Tämä kenttä on käytettävissä vain, jos valitset **Suhteellinen** kentässä **Suhteellisuussääntö**. </br></br><ul><li>**Päivittäin** – Laskee työntekijän saamien joustavien pisteiden suhteellisen määrän päivätasolla. Joustavien pisteiden kokonaismäärä jaetaan jakson päivien määrällä. Jos etuusjakso esimerkiksi on 400 päivää, järjestelmä jakaa joustavien pisteiden kokonaismäärän luvulla 400 laskeakseen työntekijöiden päivittäin saamien joustavien pisteiden määrän.</li><li>**Kuluva kuukausi** – Laskee työntekijän saamien joustavien pisteiden suhteellisen määrän kuukausitasolla kuluvaan kuukauteen pyöristettynä. Joustavien pisteiden kokonaismäärä jaetaan jakson kuukausien määrällä. Jos etuusjakso esimerkiksi on 15 kuukautta, järjestelmä jakaa joustavien pisteiden kokonaismäärän luvulla 15 laskeakseen työntekijöiden kuukausittain saamien joustavien pisteiden määrän.</li><li>**Seuraava kuukausi** – Laskee työntekijän saamien joustavien pisteiden suhteellisen määrän kuukausitasolla seuraavaan kuukauteen pyöristettynä. Joustavien pisteiden kokonaismäärä jaetaan jakson kuukausien määrällä. Jos etuusjakso esimerkiksi on 15 kuukautta, järjestelmä jakaa joustavien pisteiden kokonaismäärän luvulla 15 laskeakseen työntekijöiden kuukausittain saamien joustavien pisteiden määrän.</li></ul> |
   
   Varmista, että kukin etuussuunnitelma on rekisteröity vain yhteen joustoluotto-ohjelmaan kutakin etuusjaksoa kohden. Muussa tapauksessa järjestelmä ei tiedä, mitä joustopisteohjelmaa tulee käyttää joustohyvitysten myöntämiseen, ja kohdataan ongelmia. 

## <a name="configure-programs"></a>Ohjelmien määrittäminen

Ohjelmat ovat joukko etuussuunnitelmia, joilla on yhteiset kelpoisuussäännöt. Voit määrittää koko ohjelman kelpoisuussäännöt kunkin erillisen suunnitelman asemesta. Esimerkki: Contoso Canada FTE-ohjelma tai Contoso Europen johtotason ohjelma. 

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Oikeutussäännöt ja -asetukset**.

2. Luo ohjelma valitsemalla **Ohjelmat**-välilehdessä **Uusi**. Jos haluat tehdä poikkeuksia niille työntekijöille, jotka eivät täytä kelpoisuussäännön vaatimuksia, valitse **Oikeutussäännön ohitus**. Jos haluat nähdä ohjelmaan liittyvät suunnitelmat, valitse **Liitetyt suunnitelmat**.

3. Määritä seuraavien kenttien arvot.

   | Kenttä | kuvaus |
   | --- | --- |
   | **Ohjelma** | Ohjelman yksilöivä tunniste. |
   | **Kuvaus** | Ohjelman kuvaus. | 
   | **Voimaantulopäivämäärä ja -aika** | Päivämäärä ja aika, jolloin ohjelmasta tulee aktiivinen. |
   | **Voimassaolon päättymispäivämäärä ja -aika** | Päivämäärä ja aika, jolloin ohjelma vanhenee. Oletusarvo on 12/31/2154, joka vastaa ei koskaan -arvoa. |
   | **Kattavuuden odotusaika** | Aika, jonka työntekijän on odotettava, ennen kuin etuusohjelman kattavuus alkaa. |
   | **Vähennyksen odotusaika** | Aika, jonka työntekijä odottaa, ennen kuin etuusohjelman vähennykset alkavat. |
   | **Oikeutussäännöt** | Valitse etuuksia koskevaan ohjelmaan sovellettavat kelpoisuussäännöt. Voit määrittää kelpoisuussäännöt tämän sivun **Kelpoisuussäännöt**-välilehdessä. |
   
4. Valitse **Tallenna**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
