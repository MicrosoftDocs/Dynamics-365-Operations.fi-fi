---
title: Luo etusuunnitelma
description: Tässä artikkelissa kerrotaan, miten etuussuunnitelmia määritetään Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitPlanListPage, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7815657c4bf3f79d1a04333027cc51b496fe1820
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909814"
---
# <a name="create-a-benefit-plan"></a>Etuussuunnitelmien luominen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kerrotaan, miten etuussuunnitelmia määritetään Dynamics 365 Human Resourcesissa.

1. Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Etuussuunnitelmat**.

2. Valitse **Uusi**.

3. Määritä **Yleiset**-välilehdelle seuraavien kenttien arvot:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Suunnitelma** | Suunnitelman yksilöllinen tunnus. |
   | **Kuvaus** | Suunnitelman kuvaus. |
   | **Suunnitelman tyyppi** | Kun luot uuden suunnitelman, sinun on määritettävä suunnitelman tyyppi. Suunnitelmatyyppi on tietynlaisten etuuksien ylätason ryhmittely. Kukin suunnitelmatyyppi määrittää, voiko työntekijä rekisteröityä useisiin kyseisen tyypin suunnitelmiin, ovatko yhteyshenkilöt edunsaajia vai huollettavia sekä määrittää kattavuusasetukset. Voit luoda uusia mukautettuja suunnitelmatyyppejä, jotka vastaavat etuusvalikoimasi vaatimuksia. Etuussuunnitelmien päätyypit ovat: <ul><li>Lisäeläkemaksut (Yhdysvalloissa 401K)</li><li>ADD</li><li>Hammashoito</li><li>Kunto</li><li>FSA</li><li>Elämä</li><li>LTD</li><li>Lääkintä</li><li>PTO</li><li>STD</li><li>Näöntarkastus</li></ul> |
   | **Suunnitelman tyypin koodi** | Suunnitelmatyypin suunnitelmatyyppikoodi. |
   | **Ohjelma** | Määrittää ohjelman, jolle suunnitelma osoitetaan vaihtoehtoisesti. |
   | **Nippu** | Määrittää nipun, jolle suunnitelma osoitetaan vaihtoehtoisesti. |
   | **Päärahtikirja** | Määrittää, onko suunnitelma pääsuunnitelma, johon on liitetty nippu. |
   | **Voimaantulopäivämäärä ja -aika** | Suunnitelman alkamispäivä ja -aika. Oletusarvo on nykyinen järjestelmän päivämäärä. |
   | **Voimassaolon päättymispäivämäärä ja -aika** | Suunnitelman päättymispäivä ja -aika. Oletusarvona on 12/31/2154, joka tarkoittaa ei koskaan. |

4. Määritä **Määritys**-välilehdessä seuraavien kenttien arvot luotavan suunnitelman tyypin mukaan:

   | Suunnitelman tyyppi | Kenttä | Kuvaus |
   | --- | --- | --- |
   | Terveydenhuolto (terveydenhuolto, hammashoito, näkö, HMO) | COBRA | Määrittää, onko suunnitelma COBRA-oikeutettu (Consolidated Omnibus Budget Reconciliation Act) oikeutettu. |
   | Terveydenhuolto (terveydenhuolto, hammashoito, näkö, HMO) | HIPAA | Määrittää, onko suunnitelma HIPAA-oikeutettu (Health Insurance Portability and Accountability Act). |
   | Terveydenhuolto (terveydenhuolto, hammashoito, näkö, HMO)<br><br>Muu (PTO, kunto)<br><br>Muu<br><br>Pitkäaikainen vamma<br><br>ADD (perushenki, vapaaehtoinen henki)<br><br>Säästö (esimerkiksi 401(k))<br><br>FSA | Ennen veroja, sallittu | Määrittää, voiko suunnitelmaan tehdä maksuja ennen verojen soveltamista. |
   | Terveydenhuolto (terveydenhuolto, hammashoito, näkö, HMO)<br><br>Muu (PTO, kunto)<br><br>Pitkäaikainen vamma<br><br>ADD (perushenki, vapaaehtoinen henki)<br><br>Säästö (esimerkiksi 401(k))<br><br>FSA | Verojen jälkeen, sallittu | Määrittää, voiko suunnitelmaan tehdä maksuja verojen soveltamisen jälkeen. |
   | Terveydenhuolto (terveydenhuolto, hammashoito, näkö, HMO)<br><br>Muu (PTO, kunto)<br><br>Pitkäaikainen vamma<br><br>ADD (perushenki, vapaaehtoinen henki)<br><br>Säästö (esimerkiksi 401(k))<br><br>FSA | Osallistuja | Määrittää, kuka tekee maksuja suunnitelmaan – työntekijään, työnantaja vai molemmat. |
   | Pitkäaikainen vamma<br><br>ADD (perushenki, vapaaehtoinen henki) | Vähimmäiskattavuus | Suunnitelman vaatima vakuutuksen vähimmäiskattavuus. |
   | Pitkäaikainen vamma<br><br>ADD (perushenki, vapaaehtoinen henki) | Enimmäiskattavuus | Suunnitelman vaatima vakuutuksen enimmäiskattavuus. |
   | Pitkäaikainen vamma<br><br>ADD (perushenki, vapaaehtoinen henki) | Käytä kattavuuden lisäyksiä | Määrittää, vahvistetaanko, että kattavuus vastaa kelvollista lisämäärää. |
   | Pitkäaikainen vamma<br><br>ADD (perushenki, vapaaehtoinen henki) | Lisäävä summa | Suunnitelman vakuutuskattavuuden lisämäärä. Jos lisämäärä esimerkiksi on 1 000, työntekijällä ei voi olla vakuutusta 200 500 dollarin edestä, vaan summa on pyöristettävä arvoon 201 000 tai 200 000. |
   | Pitkäaikainen vamma<br><br>ADD (perushenki, vapaaehtoinen henki) | Lisäävä suunta | Määrittää pyöristyksen suunnan joko ylös- tai alaspäin, kun kattavuussumma ei täytä lisäyssumman arvoa. |
   | ADD (perushenki, vapaaehtoinen henki) | Todiste vakuutuskelpoisuudesta | Määrittää, onko työntekijän todistettava vakuutettavuutensa. |
   | ADD (perushenki, vapaaehtoinen henki) | Määrä | Summa kirjanpitovaluuttana. Tämä kenttä on aktiivinen vain, jos Todisteet vakuutettavuudesta -valintaruutu on valittuna. |
   | Säästö (esimerkiksi 401(k))<br><br>FSA | Vuosittainen vähimmäisosuus | Suunnitelman vaatima vähimmäismaksu. |
   | Säästö (esimerkiksi 401(k))<br><br>FSA | Vuosittainen enimmäisosuus | Suunnitelman vaatima enimmäismaksu. |
   | Säästö (esimerkiksi 401(k)) | Työnantajan vuosittainen enimmäissumma | Enimmäissumma, jonka työntekijä voi maksaa työntekijän säästösuunnitelmaa varten etuusjakson aikana. Tämän kentän käyttö edellyttää Työnantajan vastaus -valintaruudun valitsemista. |
   | Säästö (esimerkiksi 401(k)) | Työnantajan vastaavuus | Määrittää, osallistuuko työnantaja työntekijän säästösuunnitelmaan. |
   | Säästö (esimerkiksi 401(k)) | Työnantajan vastaavuusprosentti | Prosenttiosuus työntekijän maksumäärästä, jonka myös työnantaja maksaa. |
   | Säästö (esimerkiksi 401(k)) | Työnantajan vastaavuuden yläraja | Suurin prosenttiosuus, jonka myös työnantaja maksaa. Jos työnantaja esimerkiksi maksaa 100 % työntekijän maksuista aina 6 %:iin työntekijän palkasta asti, työnantajan vastaavuuden yläraja on 6 %. |

5. Määritä **Määritys**-välilehdelle seuraavien kenttien arvot:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Salli rekisteröinti tai jatka sitä** | Määrittää, voivatko työntekijät rekisteröityä suunnitelmaan, jos he täyttävät kelpoisuusvaatimukset.</br></br>Jos arvoksi on määritetty Ei, suunnitelma ei ole työntekijöiden käytettävissä, kun kelpoisuus käsitellään. |
   | **Rekisteröi automaattisesti edellisestä vuodesta** | Määrittää, voiko kelvollisen työntekijän rekisteröidä automaattisesti suunnitelmaan, jos työntekijä on rekisteröity edellisen vuoden aikana. |
   | **Automaattinen rekisteröinti oletusarvoisesti** | Määrittää, valitaanko suunnitelma oletusarvoiseen rekisteröintiin. Suunnitelma ei ole pakollinen, joten työntekijä voi muuttaa oletusvalintaa. |
   | **Suljettu, ei uusia rekisteröintejä** | Määrittää, rajoittuuko suunnitelma vain kelpoisiin työntekijöihin, jotka olivat rekisteröityneet suunnitelmaan edellisenä vuonna. |
   | **Pakollinen suunnitelma** | Määrittää, rekisteröidäänkö työntekijät automaattisesti suunnitelmaan. Työntekijät eivät voi muuttaa rekisteröitymisvalintaa. |
   | **Aloituspäivämäärä** | Päivämäärä, jona suunnitelma on luotu yrityksessä. |
   | **Toimittajatili** (edun toimittaja) | Toimittaja, jolle yritys maksaa suunnitelman maksut. |
   | **Nimi** (edun toimittaja) | Toimittajan nimi. |
   | **Toimittajaviite** (edun toimittaja) | Toimittajan viite suunnitelmalle. Esimerkiksi yrityksen ryhmäsuunnitelmanumero. |
   | **Vaihtoehtoinen viite** (edun toimittaja) | Toimittajan vaihtoehtoinen viite suunnitelmalle. Esimerkiksi yrityksen tilinumero. |
   | **Valuutta** (edun toimittaja) | Valuutta, jota käytetään maksujen suorittamisessa toimittajalle. |
   | **Kulutili** (edun toimittaja) | yleinen kirjanpitotili, jota käytetään suunnitelman maksujen kulutilinä. |
   | **Toimittajatili** (edun ylläpitäjä) | Toimittaja, jolle yritys maksaa suunnitelman ylläpitämisestä. Jos suunnitelmaa ylläpidetään itse, jätä tämä kenttä tyhjäksi. |
   | **Nimi** (edun ylläpitäjä) | Edut ylläpidon toimittajan nimi. |
   | **Toimittajaviite** (edun ylläpitäjä) | Ylläpidon toimittajan viite suunnitelmalle. |
   | **Vaihtoehtoinen viite** (edun ylläpitäjä) | Ylläpidon toimittajan vaihtoehtoinen viite suunnitelmalle. |
   | **Valuutta** (edun ylläpitäjä) | Valuutta, jota käytetään etujen ylläpitäjälle maksamiseen. |
   | **Kulutili** (edun ylläpitäjä) | Yleinen kirjanpitotili, jota käytetään suunnitelman ylläpitoon liittyvien kulujen kulutilinä. |

6. Tarvittaessa **Suodattimet**-välilehdessä. Voit suodattaa seuraavien kenttien perusteella:

   - **Liiketoimintayksikkö**
   - **Osasto**
   - **Oikeushenkilö**
   - **Toimipaikka**
   - **Sijainti**

7. Määritä **Kelpoisuussäännöt**-välilehdelle seuraavien kenttien arvot:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Rivinumero** | Kelpoisuussäännön rivinumero. |
   | **Kelpoisuussääntö** | Etuussuunnitelmaan sovellettava kelpoisuussääntö. Tätä kelpoisuussääntöä sovelletaan vastaavaan toimintotyyppiin ja kohdistetaan määritettyihin kattavuuden odotusaikaan ja vähennyksiin. |
   | **Toimenpidetyyppi** | Toiminto, johon kelpoisuussääntöä sovelletaan: etuuksiin rekisteröityminen vai etuuksien vanheneminen. |
   | **Kattavuuden odotusaika** | Arvo odotusjaksojen lomakkeesta. Kattavuuden odotusaika määrittää, kuinka monta päivää tai kuukautta työntekijä odottaa etuuden kattavuutta tai edun vanhentumista kelpoisuussäännön kriteereiden ja toimintotyypin mukaan. |
   | **Vähennyksen odotusaika** | Arvo odotusjaksojen lomakkeesta. Vähennyksen odotusaika määrittää, kuinka monta päivää tai kuukautta työntekijä odottaa etuuden vähennysten tekemistä palkastaan kelpoisuussäännön kriteereiden ja toimintotyypin mukaan. |

8. Valitse **Tallenna**.

## <a name="view-enrolled-workers"></a>Rekisteröityneiden työntekijöiden tarkasteleminen

Voit tarkastella työntekijöitä, jotka ovat rekisteröityneet valittuun etuussuunnitelmaan.

1. Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Etuussuunnitelmat**.

2. Valitse siirtymispalkin **Edut**-välilehdessä **Rekisteröidyt työntekijät**.

## <a name="attach-coverage-options"></a>Liitä kattavuusvaihtoehdot

Voit lisätä valittuun etuussuunnitelmaan kattavuusasetuksia. Kattavuusasetusten liittäminen tuo kattavuusvaihtoehdon maksu- ja vähennysmääritykset yhteen.  Esimerkki: Terveydenhuoltosuunnitelman osalta käyttäjä valitsisi perhekattavuusvaihtoehdon.  Silloin hänen on valittava liittyvän suunnitelman perhemaksu (määritetään maksumäärityksessä) ja liittyvän suunnitelman vähennys (määritetään maksumäärityksessä). Tämä määrittää valitun kattavuuden kustannukset työnantajalle ja työntekijälle. Tämän jälkeen prosessi toistettaisiin kattavuudelle Työntekijä+1 tai Työntekijä.

1. Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Etuussuunnitelmat**.

2. Valitse siirtymispalkin **Edut**-välilehdessä **Liitä kattavuusvaihtoehdot**.

## <a name="override-eligibility-rules"></a>Kelpoisuussääntöjen ohitus

Voit lisätä työntekijöitä suunnitelmaan kelpoisuussääntöjen poikkeuksina. Jokainen lisäämäsi työntekijä on oikeutettu etuussuunnitelmaan.

1. Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Etuussuunnitelmat**.

2. Valitse siirtymispalkin **Edut**-välilehdessä **Kelpoisuussääntöjen ohitus**.

## <a name="view-attached-periods"></a>Liitettyjen jaksojen tarkastelu

Voit nähdä luettelon käytettävissä olevista etuisuusjaksoista.

1. Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Etuussuunnitelmat**.

2. Valitse sivunavigointipalkista **Kaudet**-välilehti.

## <a name="view-plan-description"></a>Näytä suunnitelman kuvaus

Voit antaa kuvauksen suunnitelmasta auttaaksesi työntekijöitä etuusvalinnoissaan. Tässä antamasi suunnitelman kuvaus näkyy työntekijän itsepalvelussa, kun suunnitelmaa osoitetaan kattavuusvaihtoehtoluettelossa.

1. Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Etuussuunnitelmat**.

2. Valitse siirtymispalkin **Edut**-välilehdessä **Suunnitelman kuvaus**.

## <a name="view-flex-credit-programs"></a>Näytä bonushyvitysohjelmat

1. Valitse **Etujen hallinta** -työtilassa **Suunnitelmat**-kohdasta **Etuussuunnitelmat**.

2. Valitse siirtymispalkin **Edut**-välilehdessä **Bonushyvitysohjelmat**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
