---
title: Vanhentuneet ominaisuudet
description: "Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Platform
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 6
ms.translationtype: Human Translation
ms.sourcegitcommit: 3267bd1cbd738b5ced9996fc3b28eee211627591
ms.openlocfilehash: 8feffb27b5d08a9c90e97ac0d7e00abf0448d0df
ms.contentlocale: fi-fi
ms.lasthandoff: 06/16/2017


---

# Vanhentuneet ominaisuudet
<a id="deprecated-features" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan.

## Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivityksessä poistetut ominaisuudet
<a id="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update" class="xliff"></a>

### Varaston mobiililaiteportaali
<a id="warehouse-mobile-devices-portal" class="xliff"></a>

Varaston mobiililaiteportaali (WMDP) oli erillinen osa, joka oli tarkoitettu paikallisesti tapahtumaan itsenäiseen käyttöönottoon. Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ei enää tue tätä komponenttia. Alkuperäinen, käyttäjäkokemusta parantava sovellus, on korvannut WMDP-toiminnot. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Poiston syy**       | Sama toiminto.                        |
| **Onko toinen ominaisuus korvannut?** | Kyllä. Finance and Operations – varastointi on korvannut tämän ominaisuuden. Lisätietoja asennuksesta ja ennakkoedellytyksistä on ohjeaiheessa [Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen asentaminen ja määrittäminen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Vaikutuksen alaiset moduulit**             | Varaston hallinta, kuljetusten hallinta |

### Pankkitilin täsmäytyksen lisätoimintojen manuaalisen täsmäytyksen täsmäytyssääntö
<a id="advanced-bank-reconciliation-matching-rule-for-manual-matching" class="xliff"></a>

Täsmäytyssäännöllä valittiin ja merkittiin pankkitosite, kun asiakirjat täsmäytettiin manuaalisesti täsmäytyslaskentataulukossa.

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Poiston syy**       | Rajoitettu käyttö.                                                                         |
| **Onko toinen ominaisuus korvannut?** | Nro Täsmäytettäviä asiakirjoja etsitään sarakkeen suodatusominaisuuksilla. |
| **Vaikutuksen alaiset moduulit**             | Maksuliikenteen hallinta                                                               |

### Windows 8 -tablettisovellus
<a id="windows-8-tablet-app" class="xliff"></a>

Windows 8 -tablettisovelluksessa oli kulujen vienti- ja hyväksymistoiminnot.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Poiston syy**       | Finance and Operationsia voi käyttää tableteissa. Tablettisovellusta ei enää tarvita. |
| **Onko toinen ominaisuus korvannut?** | Nro                                                                                      |
| **Vaikutuksen alaiset moduulit**             | Matkalaskut                                                                       |


Ominaisuudet, jotka on poistettu Dynamics 365 for Operations -versiosta 1611 ympäristöpäivityksessä 3
<a id="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3" class="xliff"></a>
---------------------------------------------------------------------------------------------

### Espanjan AEB-maksumuodot
<a id="aeb-payment-formats-for-spain" class="xliff"></a>

Consejo Superior Bancario -maksumuotoja käytetään maksusuoritustiedostojen lähettämiseen pankkiin asiakkaan maksuja ja toimittajamaksuja varten. Muotojen sisällön määrittää Asociación Española de Banca. Siihen sisältyy Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Espanjan ISO20022-tilisiirto ja suoraveloituksen maksumuoto |
| Vaikutuksen alaiset moduulit             | Myyntireskontra, ostoreskontra                                    |

### Liettuan pankkiohjelmamaksujen siirto
<a id="bank-payments-transfer-for-lithuania" class="xliff"></a>

Pankkiohjelmamaksujen siirto luodaan ja tulostetaan Liettuan maksunsiirron (LT) vientimuodon avulla. Liettuan markkina-alue aloitti LITASin, yhdistetyn sähköisen pankkijärjestelmän, käytön vuonna 2005.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                    |
| Onko toinen ominaisuus korvannut? | Kyllä, Liettuan ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                           |

### Norjan BBS Direkte Remittering -maksumuodot
<a id="bbs-direkte-remittering-payment-formats-for-norway" class="xliff"></a>

BBS Direkte Remittering -maksumuotoja ovat asiakkaan maksun perittävän vienti (suoraveloitus) ja palautussanoman tuonti.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                                                                                                                        |
| Onko toinen ominaisuus korvannut? | Norjan AvtaleGiro- asiakkaan maksumuotoa voidaan käyttää suoraveloituksen sanomien luomiseen. Palautussanoman tuominen toteutetaan tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra, ostoreskontra                                                                                                                          |

### Espanjan tilikartta-työkalu
<a id="chart-of-accounts-tool-for-spain" class="xliff"></a>

Tätä työkalua käytetään, kun Espanjan tilikartta edellyttää suuria muutoksia. Käyttäjä voi tuoda uuden tilikartan Microsoft Excel- tai tekstimuodossa ja tuoda myös raportteja.

|                              |                |
|------------------------------|----------------|
| Poiston syy       | Rajoitettu käyttö  |
| Onko toinen ominaisuus korvannut? | Nro             |
| Vaikutuksen alaiset moduulit             | Kirjanpito |

### Belgian Dom80-maksumuoto
<a id="dom80-payment-format-for-belgium" class="xliff"></a>

Vanha Belgian maksukehotuksen maksumuoto (suoraveloitus).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä Belgian SO 20022 -suoraveloituksen maksumuoto |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                    |

### Sveitsin DTA/EZAG-maksumuodot
<a id="dtaezag-payment-formats-for-switzerland" class="xliff"></a>

DTA/EZAG-muodot integroidaan ESR-järjestelmään, koska niissä voidaan käsitellä viitenumeroa. Koska viitenumerot eivät ole pakollisia, näitä muotoja voidaan käyttää kaikkien toimittajamaksujen käsittelyssä. Muotoja käytetään yrityksissä, joissa on pankkitili muussa kuin "Postfinance"-sijainnissa.

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                      |
| Onko toinen ominaisuus korvannut? | Kyllä, Sveitsin ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                             |

### Itävallan ISOEDIFACT-DIRDEB-suoraveloituksen maksumuoto
<a id="edifact-dirdeb-payment-format-for-austria" class="xliff"></a>

Maksukehotuksen EDIFACT-DIRDEB-maksumuoto (suoraveloitus).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Itävallan ISO 20022 -suoraveloituksen maksumuoto |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                    |

### Belgian EDIVAT
<a id="edivat-for-belgium" class="xliff"></a>

EDIVAT on Belgian vanhentunut standardi sähköiselle ilmoitukselle suojatun sähköpostin kautta. Microsoft Dynamics AX 2012 säilyttää vain luku -ratkaisun historiallisten tietojen käyttämiseksi.

|                              |                                      |
|------------------------------|--------------------------------------|
| Poiston syy       | Tätä toimintoa ei enää käytetä. |
| Onko toinen ominaisuus korvannut? | Nro                                   |
| Vaikutuksen alaiset moduulit             | Kirjanpito                       |

### Norjan eGiro EDIFACT CREMUL- maksun tuontimuoto
<a id="egiro-edifact-cremul-payment-import-format-for-norway" class="xliff"></a>

eGiro perustuu YK:n kansainväliseen EDIFACT CREMUL (Multiple Credit Advice Message) -standardiin, jota käytetään asiakasmaksujen automaattisessa kirjauksessa. eGiro on Microsoft Dynamics AX:ssä toteutettu asiakkaan maksun tuontimuoto.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                                                     |
| Onko toinen ominaisuus korvannut? | Nro Muoto korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                       |

### Puolan ulkoinen varasto
<a id="external-inventory-for-poland" class="xliff"></a>

Tavaroiden tunnistetiedot, jotka saadaan toimittajan myynnistä ilman ostoa. Ulkoisessa varastossa käsitellyt tavarat eivät vaikuta vakiovarastoon ja ne voidaan myydä ja ostaa automaattisesti. Tämä prosessi luo todelliset varastosiirrot.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| Poiston syy       | Korvattu toisella toiminnolla                     |
| Onko toinen ominaisuus korvannut? | Kyllä, saapuvan tavaralähetyksen perustoiminnot |
| Vaikutuksen alaiset moduulit             | Ostoreskontra, varastonhallinta          |

### Itä-Euroopan raportin muodostustoiminto
<a id="financial-reports-generator-for-eastern-europe" class="xliff"></a>

Työkalua käytetään tiedonkeruun määritykseen kirjanpitoa ja veroraportteja varten sekä tietojen viemiseksi XLS- ja DOC- raporttimalleihin.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| Poiston syy       | Rajoitettu käyttö                                                                            |
| Onko toinen ominaisuus korvannut? | Nro Työkalu korvataan sähköiset raportoinnin konfiguraatioilla tulevissa julkaisuversioissa. |
| Vaikutuksen alaiset moduulit             | kirjanpito                                                                           |

### Suomen asiakasmaksutapahtumien tuominen
<a id="import-of-customer-payment-transactions-for-finland" class="xliff"></a>

Voit valita Suomen maksujen tuontimuodon asiakasmaksutapahtumien tuomiselle pankin antamasta ulkoisesta tiedostosta.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                                                     |
| Onko toinen ominaisuus korvannut? | Nro Muoto korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                       |

### Suomen maksutapahtumien tuominen kirjanpidon kirjauskansioon
<a id="import-of-payment-transactions-into-a-general-ledger-journal-for-finland" class="xliff"></a>

Suomen erityismuotoa käytetään kirjanpidon tapahtumien tuomiseksi kirjanpitoon.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                                                     |
| Onko toinen ominaisuus korvannut? | Nro Muoto korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                       |

### Belgian Isabel-synkronoitu integrointi (CIS)
<a id="integration-with-isabel-synchronized-cis-for-belgium" class="xliff"></a>

Isabel on Euroopan sähköisen maksuliikenteen ja tiedonsiirron yleinen standardi Belgiassa.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Integrointi Isabel-asiakasohjelmaan on lopetettu.                                                                |
| Onko toinen ominaisuus korvannut? | Nro Maksumuodot, joita ei voi enää käyttää, korvataan ISO20022-tilisiirron maksumuodolla Belgiassa. |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                                                                                     |

### Espanjan tilikartan ja kirjanpitosääntöjen muutokset
<a id="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain" class="xliff"></a>

Tätä toimintoa käytetään Espanjan tilikartan ja kirjanpitosääntöjen muutoksiin. Se yhdistää tilejä ja auttaa vanhan tilikartan muuttamisessa uudeksi tilikartaksi ja vertaa edellistä tilikautta uuteen tilikauteen, vaikka ne on kirjattu eri tilinumeroille.

|                              |                |
|------------------------------|----------------|
| Poiston syy       | Rajoitettu käyttö  |
| Onko toinen ominaisuus korvannut? | Nro             |
| Vaikutuksen alaiset moduulit             | Kirjanpito |

### Toimittajan Pagamento Fornittori -maksumuoto
<a id="pagamento-fornittori-vendor-payment-format" class="xliff"></a>

Vanha Italian tilisiirron maksumuoto.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Italian ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                       |

### Viron maksun vientimuodot
<a id="payment-export-formats-for-estonia" class="xliff"></a>

Pankin maksun viennissä käytetään Telehansa- ja Teleservice-muotoja.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Viron ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                         |

### Norjan maksutiedostoarkisto
<a id="payment-file-archive-for-norway" class="xliff"></a>

Kun maksutiedostot on luotu, tiedostoarkistoon arkistoidaan kaikki luodut tiedostot, vaikka tiedostot on aiemmin kirjoitettu tai luettu.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| Poiston syy       | Korvattu toisella toiminnolla                                        |
| Onko toinen ominaisuus korvannut? | Kyllä, sähköisen raportoinnin arkistoidut työt                            |
| Vaikutuksen alaiset moduulit             | Ostoreskontra, myyntireskontra, organisaation hallinto |

### Viron maksun tuontimuodot
<a id="payment-import-formats-for-estonia" class="xliff"></a>

Pankin maksun tuonnissa käytetään Telehansa- ja TeleTeenus-muotoja.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                                                    |
| Onko toinen ominaisuus korvannut? | Nro Muodot korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                        |

### Suorituskyvyn hallintatavoite -työnkulku
<a id="performance-management-goal-workflow" class="xliff"></a>

Suorituskyvyn hallinta sisältää tavoitteiden hallinnan ja integroinnin suorituskykyarvioiden kanssa.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Suorituskyvyn hallinta on suunniteltu uudelleen ja tavoitesivujen lukumäärää vähennettiin prosessin yksinkertaistamiseksi.                 |
| Onko toinen ominaisuus korvannut? | Nro Tavoitteet näkyvät esimiehille esimiehen itsepalveluportaalin kautta, ja esimies voi muuttaa ja tarkastella niitä. |
| Vaikutuksen alaiset moduulit             | Henkilöstöresurssien hallinta                                                                                                 |

### Ruotsin Postgirot- ja Postgirot Utland -maksumuodot
<a id="postgirot-and-postgirot-utland-payment-formats-for-sweden" class="xliff"></a>

Ruotsin Postgirot- ja Postgirot Utland -maksumuodot.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                 |
| Onko toinen ominaisuus korvannut? | Kyllä, Ruotsin ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                        |

### Radiotaajuinen etätunnistus
<a id="radio-frequency-identifier" class="xliff"></a>

Radiotaajuinen etätunnistus (RFID) on tiedonkeräysmenetelmä, jossa käytetään tunnistetietojen tallentamiseen sähköisiä tunnisteita, ja tunnistetiedot luetaan ilman näköyhteyttä.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| Poiston syy       | Vähäinen käyttö ja rajoitetut toiminnot. |
| Onko toinen ominaisuus korvannut? | Nro                                            |
| Vaikutuksen alaiset moduulit             | Inventoinnin- ja varastonhallinta                          |

### Latvian valtion määrittämän laskujen numeroinnin raportti
<a id="report-about-state-invoices-numbering-for-latvia" class="xliff"></a>

Latvian lainsäädäntö sisältää myyntilaskujen numerointia koskevia erityissääntöjä. Toiminnon avulla voidaan määrittää erityiset numerot myyntilaskuille käyttäjän tai käyttäjäryhmän mukaan. Tämän jälkeen voit luoda raportin tai XML-tiedoston. Voit myös tulostaa raportin käytetyistä laskunumeroista.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Valtion määrittämää laskujen numerointia ei tarvitse enää ylläpitää. Käytettyjen laskunumeroiden raporttia ei enää vaadita. |
| Onko toinen ominaisuus korvannut? | Nro                                                                                                                       |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                                                      |

### Liettuaa koskevat johtajan ja kirjanpitäjän nimien asetukset
<a id="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania" class="xliff"></a>

Yrityksen johtajan ja kirjanpitäjän nimet voidaan määrittää yrityksen tietoihin ja käyttää paikallisten raporttien tulostuksessa.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Poiston syy       | Korvattu toisella toiminnolla                                     |
| Onko toinen ominaisuus korvannut? | Kyllä, viranomaisten asetuksia käytetään samaan tarkoitukseen.   |
| Vaikutuksen alaiset moduulit             | Ostoreskontra, myyntireskontra, maksuliikenteen hallinta |

### Norjan Telepay-maksumuodot
<a id="telepay-payment-formats-for-norway" class="xliff"></a>

Telepay-maksumuodot sisältävät toimittajan maksun viennin (tilisiirrolla) ja asiakkaan maksukehotuksen (suoraveloitus).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                                                        |
| Onko toinen ominaisuus korvannut? | Kyllä, Norjan ISO20022-tilisiirron maksumuoto ja asiakkaan maksun AvtaleGiro-muoto |
| Vaikutuksen alaiset moduulit             | Myyntireskontra, ostoreskontra                                                          |

### Suomen toimittajan maksun vientimuodot
<a id="vendor-payment-export-formats-for-finland" class="xliff"></a>

Kaksi eri muotoa maksujen vientiä varten käytettävissä Suomessa. LM02 (FI) käytetään kotimaan maksuille ja LUM2 (FI) ulkomaanmaksuille.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Suomen ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                         |

### Tavoitteiden luomisen työnkulku
<a id="workflow-for-creating-goals" class="xliff"></a>

Työntekijöiden tavoitteiden luomisen työnkulku on yksi monista työnkuluista, joita oli käytettävissä suorituskyvyn hallintaprosessin koordinoinnin apuna.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Suorituskyvyn hallinta on suunniteltu kokonaan uudelleen Microsoft Dynamics 365 for Finance and Operationsissa.                                                                                                                                                                                                                                        |
| Onko toinen ominaisuus korvannut? | Uudelleen suunnitellulla suorituskyvyn hallintatoiminnolla voidaan seurata tarkemmin tavoitteiden sisältöä ja mittauksia, joiden avulla voidaan seurata etenemistä, sekä tukidokumentaation liittämistä. Tavoitteet voidaan tallentaa malleina ja käyttää uudelleen. Tämän toiminnon avulla voit määrittää lisätavoitteita työntekijöille entistä nopeammin. |
| Vaikutuksen alaiset moduulit             | Henkilöstöresurssien hallinta                                                                                                                                                                                                                                                                                                               |

## Dynamics AX:n 7.0 -julkaisuversioista poistetut ominaisuudet
<a id="features-deprecated-in-dynamics-ax-70-releases" class="xliff"></a>
### Mahdollisuus peruuttaa toimittajan laskun muutokset
<a id="ability-to-cancel-changes-to-a-vendor-invoice" class="xliff"></a>

|                              |                         |
|------------------------------|-------------------------|
| Poiston syy       | Suorituskyvyn parannus |
| Onko toinen ominaisuus korvannut? | Ei                      |
| Vaikutuksen alaiset moduulit             | Ostoreskontra        |

### AIF-, AxD- ja AxBC-integraatiot
<a id="aif-axd-and-axbc-integrations" class="xliff"></a>

Application Integration Frameworkissä (AIF) tietoja voidaan vaihtaa ulkoisten järjestelmien kanssa palveluina näyttäytyvänä liiketoimintalogiikkana. Dynamics AX sisältää asiakirjoihin ja .NET Business Connectoriin (AxBC) perustuvia palveluja. Asiakirja luodaan XML-muotoisena. XML sisältää otsikkotiedot, joka lisäämällä luodaan *sanoma*, joka siirretään Dynamics AX:ään ja siitä pois. Asiakirjoja ovat esimerkiksi myynti- ja ostotilaukset. Käytännössä kuitenkin lähes mikä tahansa yksikkö, kuten asiakas, voidaan ilmaista asiakirjana. Asiakirjoihin perustuvat palvelut käyttävät **Axd &lt;*asiakirja*&gt; -luokkia.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | AIF:n ja AxDs:n arkkitehtuuria ei voi skaalata pilvipalveluun. Joukkotuontiin liittyi suorituskykyongelmia.                                                                               |
| Onko toinen ominaisuus korvannut? | Dynamics AX:n nykyisessä versiossa tämä ominaisuus on korvattu tietojen tuonti- ja vientiympäristöllä, joka tukee toistuvaa joukkotuontia ja -vientiä. AxBC:ssä on suositeltavaa käyttää varsinaisia tauluja. |
| Vaikutuksen alaiset moduulit             | AxDs, AxBCs ja AIF                                                                                                                                                                                     |

### Tuoterakenteet ilman tuoterakenneversioita
<a id="boms-without-bom-versions" class="xliff"></a>

Kun **Tuoterakenneversiot**-määritysavain poistettiin käytöstä, tuoterakenneversiot piilotettiin kaikissa lomakkeissa ja järjestelmä pakotti 1:1-suhteen vapautettujen tuotteiden ja tuoterakenteiden välille. **Tuoterakenneversiot**-määritysavainta ei voi poistaa Dynamics AX:n nykyisessä versiossa.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Poiston syy       | Tuoterakenneversioiden ohjaamista määritysavaimella ei voi skaalata pilviympäristöön. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                      |
| Vaikutuksen alaiset moduulit             | Tuotetietojen hallinta, inventoinnin- ja varastonhallinta                                    |

### Brasilian Bordero
<a id="brazilian-bordero" class="xliff"></a>

Erityismaksutapa Brasilian yrityksille

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| Poiston syy       | Brasilian Bordero-maksutavan tuki on lopetettu Brasilian lokalisointiversiosta |
| Onko toinen ominaisuus korvannut? | Nro                                                                                                    |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                                                                      |

### Brasilian Sintegra-raportti
<a id="brazilian-sintegra-statement" class="xliff"></a>

Liittovaltion veroraportti ICMS-verolle

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Tämä raportti ei ole enää käytettävissä joissain Brasilian osavaltioissa.                                                     |
| Onko toinen ominaisuus korvannut? | Nro Käyttäjät voivat käyttää yleistä sähköistä raportointityökalua raportin määrittämiseen, jos se on pakollinen erityistilanteissa. |
| Vaikutuksen alaiset moduulit             | Verokirjat                                                                                                          |

### Brasilian NF-e:n SCAN-varatila
<a id="brazilian-scan-contingency-mode-for-nf-e" class="xliff"></a>

(SCAN) varaympäristöä käytetään Nota Fiscal eletrônica (NF e) -tilan luontiin, vientiin ja tuontiin, kun Secretaria da Fazenda (SEFAZ) -ympäristö ei ole käytettävissä.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| Poiston syy       | Tämä varamenetelmä ei ole enää käytettävissä kaikissa Brasilian osavaltioissa |
| Onko toinen ominaisuus korvannut? | Nro                                                                          |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                         |

### Business Analyzer
<a id="business-analyzer" class="xliff"></a>

Käyttäjät voivat tarkastella tällä mobiilisovelluksella tärkeitä liiketoiminnan mittareita.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Toinen ominaisuus on korvannut tämän toiminnon.                                                                                                      |
| Onko toinen ominaisuus korvannut? | Microsoft PowerBI:n taloudellisen suorituskyvyn seurannan sisältöpaketti sisältää tärkeät taloudelliset mittarit, jotka sisältyivät aiemmin Business Analyzeriin. |
| Vaikutuksen alaiset moduulit             | Kirjanpito                                                                                                                                                |

### Liiketoimintatilastot
<a id="business-statistics" class="xliff"></a>

Niiden liiketoiminnan tilastotietokyselyiden asetukset, jotka voivat auttaa organisaation suorituskyvyn analysoinnissa

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| Poiston syy       | Vanha tapa käsitellä liiketoiminnan tietoja (BI), vähäinen käyttö ja rajalliset ominaisuudet |
| Onko toinen ominaisuus korvannut? | Uudet BI-ratkaisut Dynamics AX:n nykyisessä versiossa                                      |
| Vaikutuksen alaiset moduulit             | Hankinta, ostoreskontra, myynti ja markkinointi, myyntireskontra         |

### Hyväksyttyjen laskujen kirjauskansion tiedoston päivämäärän muutostoiminto
<a id="change-document-date-function-in-invoice-approval-journal" class="xliff"></a>

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Poiston syy       | Vähäinen käyttö                                                               |
| Onko toinen ominaisuus korvannut? | Kyllä. Kirjatun toimittajatapahtuman tiedoston päivämäärää voidaan muuttaa. |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                                        |

### Alankomaiden ClieOp03-maksumuoto
<a id="clieop03-payment-format-for-the-netherlands" class="xliff"></a>

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Muotoa ei enää käytetä Alankomaissa, sillä SEPA-toiminto on korvannut sen. |
| Onko toinen ominaisuus korvannut? | SEPA-maksujen vienti                                                                                       |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                        |

### Compliance Center
<a id="compliance-center" class="xliff"></a>

Compliance Center oli Sarbanes-Oxley-lakiin liittyvien vaatimustenmukaisuusaloitteiden asiakirjavaatimusten hallintaan tarkoitettu yritysportaalisivusto.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Toimintoa ei käytetty. Microsoft SharePoint sisältää Compliance Centerin käytössä olleet ominaisuudet. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                     |
| Vaikutuksen alaiset moduulit             | Yhteensopivuus ja sisäinen valvonta                                                                                       |

### Microsoft Dynamicsin yhdistin
<a id="connector-for-microsoft-dynamics" class="xliff"></a>

Tällä työkalulla integroitiin Microsoft Dynamics CRM:n tärkeitä tietoja Microsoft Dynamics ERP -sovelluksiin.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Poiston syy       | Toinen ominaisuus on korvannut tämän toiminnon. |
| Onko toinen ominaisuus korvannut? | Dynamics Integrator                                      |
| Vaikutuksen alaiset moduulit             | Microsoft Dynamicsin yhdistin                         |

### Säilöyksikkö ja monidimensioinen varasto
<a id="container-unit-and-multi-dimension-on-hand" class="xliff"></a>

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Sama toiminto                                                                                                                                         |
| Onko toinen ominaisuus korvannut? | Kyllä. AX2012:n jälkeen tämä toiminto on korvattu konsolidoidulla erätilaustoiminnoilla. Tämä ominaisuusjoukko sisältää konsolidoidun varastonäkymän. |
| Vaikutuksen alaiset moduulit             | Tuotetietojen hallinta, tuotannonhallinta, varastonhallinta, myynti ja markkinointi                                                                   |

### Pinoryhmän metatiedot
<a id="cue-group-metadata" class="xliff"></a>

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Pinoryhmiä käytettiin näyttämään vähintään yksi pino tietoruutualueella. Toiminto oli rajallinen ja siihen liittyi suorituskykyongelmia, koska tietueen muuttuminen päälomakkeessa loi jokaiselle pinolle yhden kyselyn pinoryhmässä. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                                                                                                                            |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                           |

### Pinon metatiedot
<a id="cue-metadata" class="xliff"></a>

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Pinon metatiedot rajoittuivat määrä- tai summatietoihin.                                                                                                                                                                                   |
| Onko toinen ominaisuus korvannut? | Käyttöönotetut ruudun metatiedot mahdollistavat joustavamman mallinnuksen. Voit esimerkiksi mallintaa nykyiset määrät, siirtymisen ja suorituskykyilmaisimet (KPI:t). Määräruudun metatiedot korvaavat suoraan pinon metatiedot. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                     |

### Tanskalainen sekkilomake
<a id="danish-check-format" class="xliff"></a>

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Tanskan sekkimuodon tuki on lopetettu ja raportti on poistettu tanskalaisesta lokalisoinnista. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                      |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                     |

### Tieto-osiot
<a id="data-partitions" class="xliff"></a>

Tieto-osiot erottavat Microsoft Dynamics AX:n tietokannan tiedot loogisesti.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Tieto-osiot otettiin käyttöön Microsoft Dynamics AX 2012 R2:ssa tietojen eristämistä varten. Yleisessä skenaariossa yrityksellä on tytäryhtiöitä mutta tytäryhtiön tiedot eivät saisi olla toisen tytäryhtiön nähtävissä, vaikka kumpikin tytäryhtiö on saman IT-osaston alaisuudessa. Ohjelmassa oli kuitenkin otettava käyttöön ylimääräisiä komentosarjoja ja hallintakustannuksia, jotta uusia osioita voitaisiin luoda, tiedot voitaisiin lisätä ja osiotiedot voitaisiin varmuuskopioida. Pilvipalvelussa, jossa meillä on käyttöympäristövuokrattuja (PaaS-palvelu) tietokantapalveluja (Microsoft Azuren SQL-tietokanta), tietokantaa on tehokkaampaa käyttää erityssäilönä kuin tehdä eristys ohjelmassa. Riippumatta siitä, tarvitaanko tietojen osiointia tytäryhtiöitä tai useita vuokraajia varten tai koon vuoksi, mielestämme skenaariot voidaan käsitellä paremmin useissa tietokannoissa tai Dynamics AX:n esiintymissä. |
| Onko toinen ominaisuus korvannut? | Tieto-osiot korvataan tulevissa versioissa tukemalla useita tietokantoja tai Dynamics AX:n esiintymiä.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

### Rajoitus
<a id="delimitation" class="xliff"></a>

|                              |                                        |
|------------------------------|----------------------------------------|
| Poiston syy       | Toiminnolle ei ollut käyttöä. |
| Onko toinen ominaisuus korvannut? | Ei                                     |
| Vaikutuksen alaiset moduulit             | Työajan seuranta                    |

### Työpöytäasiakasohjelma
<a id="desktop-client" class="xliff"></a>

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Dynamics AX:n asiakasohjelmakokemus on uudistettu parantamaan käytettävyyttä kaikissa ympäristöissä ja laitteissa.                      |
| Onko toinen ominaisuus korvannut? | Uusi verkkoasiakasohjelma perustuu työpöytälomakkeen metatietoihin ja ohjelmointimalliin, jota on muokattu luomaan monipuolinen verkkoympäristö. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                    |

### Suora tietokantayhteys
<a id="direct-database-connection" class="xliff"></a>

Dynamics AX 2012 R3 -versiossa Retail Modern POS -sovellus voi muodostaa suoran yhteyden kanavatietokantaan samalla tavalla, kuin Enterprise POS. Tämä oli lisänä Retail Modern POS -sovelluksen normaalille tietoliikenneyhteydelle, joka kulki vähittäismyynnin palvelimen välityksellä.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Poiston syy       | Suora tietokantayhteys edellytti matalamman suojauksen, ja sitä käytettiin pääasiassa korkeamman suorituskyvyn saavuttamiseen. Finance and Operationsissa tehtyjen suorituskyky- ja tietoturvaparannusten vuoksi tämä toiminnallisuus aiheuttaa enemmän ongelmia kuin mitä se ratkaisee. |
| Onko toinen ominaisuus korvannut? | Nro Vain vakiomuotoinen vähittäismyynnin palvelinyhteys on enää tuettu.    |
| Vaikutuksen alaiset moduulit             | Kanavatietokanta/Retail Modern POS                                    |

### Alankomaiden SWIFT MT940
<a id="dutch-swift-mt940" class="xliff"></a>

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Käytössä on nyt yleinen toiminto lokalisoidun toiminnon sijaan.                                                                                                                                                                 |
| Onko toinen ominaisuus korvannut? | Kyllä. Pankkitilin täsmäytyksen lisätoiminnot on korvannut tämän toiminnon. Lisäksi camt.053 ISO20022 -tiliotteen tuonnin käyttöönottoa suunnitellaan kirjauskansioon seuraavassa Dynamics AX -päivityksessä. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                   |

### eBilanz (XBRL Saksassa)
<a id="ebilanz-xbrl-for-germany" class="xliff"></a>

Tämä toiminto mahdollisti XBRL (eXtensible Business Reporting Language) -tulostuksen, joka on tarkoitettu erityisesti Saksan eBilanz-luokitusta varten.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Toimintoa ei käytetty                                                                                                                                                 |
| Onko toinen ominaisuus korvannut? | Toimintoa ei korvata toisella ominaisuudella, mutta Saksan markkinoilla on saatavana useista erikoistuneita XBRL-paketteja, joissa on monipuolisia XBRL-toimintoja. |
| Vaikutuksen alaiset moduulit             | Management Reporter                                                                                                                                                    |

### Yritysportaalin asiakasohjelma
<a id="enterprise-portal-client" class="xliff"></a>

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Käytössä on yksi asiakasohjelmaympäristö.                                                                                            |
| Onko toinen ominaisuus korvannut? | Uusi verkkoasiakasohjelma perustuu työpöytälomakkeen metatietoihin ja ohjelmointimalliin, jota on muokattu luomaan monipuolinen verkkoympäristö. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                    |

### Ekologinen kestävyys
<a id="environmental-sustainability" class="xliff"></a>

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| Poiston syy       | Vähäinen käyttö ja rajoitetut toiminnot       |
| Onko toinen ominaisuus korvannut? | Ei                                                 |
| Vaikutuksen alaiset moduulit             | Yhteensopivuus ja sisäisen tarkistus, ostoreskontra |

### Lomakkeen ActiveX:n ja hallitun ylläpidon ohjausobjektit
<a id="form-activex-and-managed-host-controls" class="xliff"></a>

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | ActiveX:n ja hallitun ylläpidon ohjausobjektit perustuivat vanhentuneeseen työpöytäasiakasohjelmaan.                                                                                                             |
| Onko toinen ominaisuus korvannut? | Laajennettava ohjausobjektiympäristö tukee uusien HTML-, CSS- ja JavaScript-pohjaisten ohjausobjektien luomista ja on ensimmäisen luokan ohjausobjekti Microsoft Visual Studio Tooling -ympäristössä. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                           |

### Esilaskujen muodostus erätoiminnolla
<a id="generate-prenotes-by-using-a-batch" class="xliff"></a>

Vaikka esilaskua ei voi enää muodostaa erätoimintona, käyttäjä voi edelleen luoda esilaskun.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Poiston syy       | Erätoiminnolla luodulle laskulle ei ole lomaketta, jossa luotu esilaskutiedosto voitaisiin säilyttää ja näyttää. |
| Onko toinen ominaisuus korvannut? | Esilaskuja voidaan luoda edelleen ja käyttäjä päättää sijainnin, johon tiedosto tallennetaan.   |
| Vaikutuksen alaiset moduulit             | Ostoreskontra, myyntireskontra, maksuliikenteen hallinta                                        |

### Saksan DTAUS-maksun vienti ja tiliotteen tuonti (kokonaissummat ja tapahtumat)
<a id="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions" class="xliff"></a>

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Muotoa ei enää käytetä Saksassa, sillä SEPA (yhtenäinen euromaksualue) -toiminto on korvannut sen.                                                                                                                                                                 |
| Onko toinen ominaisuus korvannut? | Kyllä. SEPA-maksun vienti ja pankkitilin täsmäytyksen lisätoiminnot tiliotteiden tuomiseen on korvannut tämän toiminnon. Lisäksi camt.053 ISO20022 -tiliotteen tuonnin käyttöönottoa suunnitellaan kirjauskansioon seuraavassa Dynamics AX -päivityksessä. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                                                                            |

### Saksan DTAZV-maksumuoto
<a id="german-dtazv-payment-format" class="xliff"></a>

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| Poiston syy       | Muotoa ei enää käytetä Saksassa, sillä SEPA-toiminto on korvannut sen. |
| Onko toinen ominaisuus korvannut? | SEPA-maksujen vienti                                                                               |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                |

### Saksassa tuominen MT940-muodossa
<a id="german-mt940-import" class="xliff"></a>

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Käytössä on nyt yleinen toiminto lokalisoidun toiminnon sijaan.                                                                                                                                                                 |
| Onko toinen ominaisuus korvannut? | Kyllä. Pankkitilin täsmäytyksen lisätoiminnot on korvannut tämän toiminnon. Lisäksi camt.053 ISO20022 -tiliotteen tuonnin käyttöönottoa suunnitellaan kirjauskansioon seuraavassa Dynamics AX -päivityksessä. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                   |

### Saksan XML-muotoinen EU-myyntiluettelo
<a id="german-xml-eu-sales-list" class="xliff"></a>

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | XML-muotoa Saksan EU:n arvonlisäveron yhteenvetoilmoitusta varten ei enää tueta. Saksan EU:n arvonlisäveron yhteenvetoilmoitus voidaan lähettää Saksan veroviranomaiselle ainoastaan ELMA5-tekstitiedostomuodossa. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                                                                                 |
| Vaikutuksen alaiset moduulit             | Vero                                                                                                                                                                                |

### Kirjanpidon SSRS-raportit
<a id="gl-ssrs-reports" class="xliff"></a>

Seuraavia valikkovaihtoehtoja sisältävät raportit on poistettu: **Pääkirjan yhteenveto**, **Yksityiskohtainen pääkirja**, **Tilikartta**, **Kirjausketju**, **Saldot** ja **Saldoluettelo**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Microsoft SQL Server Reporting Services (SSRS) -raportit on korvattu Management Reporter -toiminnoilla ja oletusraporteilla. |
| Onko toinen ominaisuus korvannut? | Management Reporter (Dynamics AX:n nykyisessä versiossa sen nimi on **Talousraportointi**)                                                  |
| Vaikutuksen alaiset moduulit             | Kirjanpito                                                                                                                               |

### InfoPart- ja FormPart-metatiedot
<a id="infopart-and-formpart-metadata" class="xliff"></a>

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | InfoPart- ja FormPart-metatietojen avulla voitiin luoda kahden eri asiakasohjelman tietoruutuja.                                                                                                                                    |
| Onko toinen ominaisuus korvannut? | InfoPart-metatiedot oli yksinkertaistettu lomakemääritelmä, ja se on muunnettu lomakkeeksi päivitystyökaluilla. Lomakkeeseen viittaavat FormPart-metatiedot on korvattu suoralla viittauksella, joka luodaan päivitystyökaluilla. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                            |

### Päätilin luettelosivu
<a id="main-account-list-page" class="xliff"></a>

Luettelo yrityksen tileistä ja niihin liittyvät saldotiedot

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Saldotiedot ovat saatavilla tilin ja dimension mukaisella **Pääkirja**-luettelosivulla.                                                                                      |
| Onko toinen ominaisuus korvannut? | **Päätilit** sisältää saman tililuettelon kuin **Päätili**-luettelosivu. **Päätilit**-ruudukkonäkymä näyttää myös pienemmän ruudukkomaisen näkymän. |
| Vaikutuksen alaiset moduulit             | Kirjanpito                                                                                                                                                                     |

### Malesian ja Singaporen pankin kassavirtaraportti
<a id="malaysia-and-singapore-bank-cash-flow-report" class="xliff"></a>

Toiminnolla voitiin tulostaa kassavirtaraportti, joka sisältää valittujen pankkitilien saapuvien ja lähtevien kassavirtojen tapahtumat sekä tiedot määritetyltä päivämääräväliltä.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Poiston syy       | Samat tiedot saadaan pankkitapahtuman kyselyllä. |
| Onko toinen ominaisuus korvannut? | Pankkitapahtuman kysely                                            |
| Vaikutuksen alaiset moduulit             | Maksuliikenteen hallinta                                                |

### Meksikon sähköinen CFD-lasku
<a id="mexican-cfd-electronic-invoice" class="xliff"></a>

Tällä ominaisuudella voitiin luoda Meksikossa sähköisiä laskuja käyttämällä CFD (Comprobante Fiscal Digital) -menetelmää, jossa yritys allekirjoittaa laskun pyytämällä liittyvän valtuutuksen viranomaiselta. Tämä ominaisuus tarjoaa myös kuukausiraportin, joka koostui kaikista kyseisen kuukauden aikana tehdyistä sähköisistä laskuista.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Menetelmää ei enää käytetä. Veroviranomaiset lopettivat CFD-menetelmällä luotavat sähköiset laskut ja niiden tilalla käytetään CFDI (Comprobante Fiscal Digital a través de Internet) -menetelmää, jossa allekirjoitus on delegoitu kolmannen osapuolen palveluntarjoajalle (PAC). Kuukausiraportti on poistettu, ja käyttäjät voivat tehdä kyselyvaihtoehdolla kyselyjä historiallisista tapahtumista. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                                                                                                                                                                                                                                                                                                        |
| Vaikutuksen alaiset moduulit             | Myyntireskontra, projekti                                                                                                                                                                                                                                                                                                                                                                              |

### Meksikon toteutunut ja toteutumaton ALV
<a id="mexico-realized-and-unrealized-vat" class="xliff"></a>

Microsoft Dynamics AX 2012:lla hallittiin toteutumatonta arvonlisäveroa (ALV:tä) käyttämällä vain Meksikoa koskevaa toteutumattoman veron toimintoa.

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Sama toiminto                                                                                             |
| Onko toinen ominaisuus korvannut? | Kyllä. Tämä toiminto on korvattu ydintoimintojen tavallisessa suoritusperusteisella arvonlisäverotoiminnolla. |
| Vaikutuksen alaiset moduulit             | Vero                                                                                                                 |

### Microsoft Outlook -integrointi
<a id="microsoft-outlook-integration" class="xliff"></a>

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| Poiston syy       | Tämä ominaisuus on korvattu Microsoft Exchange Server -integroinnilla. |
| Onko toinen ominaisuus korvannut? | Kyllä                                                                            |
| Vaikutuksen alaiset moduulit             | Myynti ja markkinointi                                                            |

### Henkilöstöhallinnon palkanlaskentatiedot
<a id="payroll-information-in-human-resources" class="xliff"></a>

Henkilöstöhallinnon palkanlaskentatiedot

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Palkanlaskennan ja Henkilöstöhallinnan perussivut ovat korvanneet tämän ominaisuuden.                                                                                                                                                                                                                                              |
| Onko toinen ominaisuus korvannut? | **Edut**, **Ansiot** ja muut liittyvät Yhdysvaltojen palkanlaskenta -kohdassa olleet sivut on määritetty uudelleen ja sisältyvät nyt henkilöstöhallinnon perusmäärityksiin. Tämä auttaa tukemaan ulkoista palkanlaskennan käsittelyä. Toimintoa käytetään valitsemalla **Henkilöstöhallinta 1** &gt; **Palkanlaskenta**-määritysavain. |
| Vaikutuksen alaiset moduulit             | Henkilöstöhallinto, palkanlaskenta                                                                                                                                                                                                                                                                                                     |

### Varastonhallinnan kirjauskansioiden yksityinen esto
<a id="private-blocking-of-inventory-and-warehouse-management-journals" class="xliff"></a>

Varastokirjauskansiot eivät enää tue kirjauskansion merkitsemistä yksityiseksi valitulle käyttäjälle. Vain käyttäjäryhmien käyttämää kirjauskansioiden yksityistä estoa ja estoa muokkauksen aikana tuetaan.

|                              |                                        |
|------------------------------|----------------------------------------|
| Poiston syy       | Toiminnolle ei ollut käyttöä. |
| Onko toinen ominaisuus korvannut? | Ei                                     |
| Vaikutuksen alaiset moduulit             | Varastonhallinta                   |

### Tuotekonfiguraattori
<a id="product-builder" class="xliff"></a>

Tuotekonfiguraattoria käytettiin määrittämään dynaamisesti nimikkeitä myyntitilauksesta, ostotilauksesta, tuotantotilauksesta, myyntitarjouksesta, projektitarjouksesta tai nimiketarpeesta. Käyttäjä voi valita asiakkaan vaatimusten mukaisia arvoja mallinnusmuuttujia sisältävän tuotemallin perusteella ja saada näin yksilöllisen tuotevariantin, jolla on tuoterakenne ja reitti.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Tuotekonfiguraattori paljasti X ++-koodin loppukäyttäjille eikä sitä tueta Dynamics AX:n nykyisessä versiossa. Se on poistettu, jotta päällekkäisissä suurissa koodikannoissa ei tarvitsisi tehdä kaksinkertaista ylläpitoa. |
| Onko toinen ominaisuus korvannut? | Tuotekonfiguraatio                                                                                                                                                                                   |
| Vaikutuksen alaiset moduulit             | Tuotetietojen hallinta, myynti ja markkinointi                                                                                                                                                     |

### Nimeä tuotedimensio uudelleen
<a id="rename-product-dimension" class="xliff"></a>

Tällä toiminnolla voi vaihtaa yhden kolmesta vakiotuotedimension nimestä (koko, väri tai tyyli) liiketoiminnan vaatimuksiin paremmin sopivaan nimeen. Uudelleennimeäminen koski kaikkia otsikoita, joissa tuotedimension nimeä käytettiin.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Poiston syy       | Dynamics AX:n nykyinen versio ei tue suorituksen aikaisia otsikkomuutoksia. |
| Onko toinen ominaisuus korvannut? | Nro                                                                            |
| Vaikutuksen alaiset moduulit             | Tuotetietojen hallinta                                                |

### Vähittäismyynnin palvelinyhteys HTTP-protokollalla
<a id="retail-server-connectivity-using-http" class="xliff"></a>

Dynamics AX 2012 R3 -versiossa vähittäismyynnin palvelinyhteyttä oli mahdollista käyttää (suojaamattomalla) HTTP-yhteydellä. Tämä oli lisänä vakioyhteyteen HTTPS-protokollalla.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Poiston syy       | Uusien suojausvaatimusten vuoksi tietoliikenneyhteys on sallittua ainoastaan TLS 1.2 -suojausta (tai uudempaa) käyttäen. Omatoiminen asennusohjelma määrittää yhteystavan tietokoneelle automaattisesti. |
| Onko toinen ominaisuus korvannut? | Nro Vain vakiomuotoinen HTTPS-yhteys on enää tuettu.                                                                           |
| Vaikutuksen alaiset moduulit             | Vähittäismyynnin palvelin                                                |

### Roolikeskus-sivut
<a id="role-center-pages" class="xliff"></a>

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Roolikeskus-sivut perustuivat vanhentuneeseen yritysportaaliympäristöön, joka on korvattu uudella verkkoasiakasympäristöllä Dynamics AX:n nykyisessä versiossa. |
| Onko toinen ominaisuus korvannut? | Uusi Työtila-lomakemalli käyttäjille prosessikeskeisen rakenteen, jonka kautta on helppo käyttää kyseisen prosessin usein käytettyjä tehtäviä.                       |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                      |

### Arvonlisäveroviranomaiset
<a id="sales-tax-jurisdictions" class="xliff"></a>

|                              |                                              |
|------------------------------|----------------------------------------------|
| Poiston syy       | Vähäinen käyttö ja rajoitetut toiminnot |
| Onko toinen ominaisuus korvannut? | Ei                                           |
| Vaikutuksen alaiset moduulit             | Yhdysvaltojen arvonlisävero                                 |

### Rahdinkuljettajan liittymä
<a id="shipping-carrier-interface" class="xliff"></a>

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Sama toiminto                                                                                                                         |
| Onko toinen ominaisuus korvannut? | Kyllä. Kuljetustenhallinta korvaa tämän toiminnon osittain, mutta perusvarastonhallinta (WMS I) ei ole vielä korvannut. |
| Vaikutuksen alaiset moduulit             | Myynti ja markkinointi, inventoinnin- ja varastonhallinta                                                                                                       |

### Sites Services -palvelut
<a id="sites-services" class="xliff"></a>

Sites Services -palveluiden avulla voit luoda sivustoja, jotka laajentavat liiketoimintaprosesseja Internetiin.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Dynamics AX:n käyttämässä Microsoft Azuren infrastruktuurissa on uusia korvaavia ominaisuuksia (esimerkiksi Azure-sivustot). |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                                       |
| Vaikutuksen alaiset moduulit             | Henkilön työhönotto, Palvelupyynnön hallinta, Tarjouspyynnöt, Toimittajan rekisteröinti                                                                  |

### SSAS – kysynnän ennustestrategia
<a id="ssas-demand-forecasting-strategy" class="xliff"></a>

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| Poiston syy       | Uusi pilviarkkitehtuuri ei voi tukea toiminnon rakennetta. |
| Onko toinen ominaisuus korvannut? | Azure Machine Learningin kysynnän ennusteen strategia                           |
| Vaikutuksen alaiset moduulit             | Suunnittelu                                                                     |

### Matkahankinnat
<a id="travel-requisitions" class="xliff"></a>

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Poiston syy       | Vähäinen käyttö ja suurin osa toiminnoista oli yritysportaalissa. |
| Onko toinen ominaisuus korvannut? | Ei                                                              |
| Vaikutuksen alaiset moduulit             | Matkalaskut                                              |

### Toimittajan laskupooli, ei sisällä kirjaustietoja
<a id="vendor-invoice-pool-excluding-posting-details" class="xliff"></a>

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| Poiston syy       | Vähäinen käyttö. Toiminto on korvattu laskun kirjauskansiolla, joka sisältää työnkulkutoiminnon. |
| Onko toinen ominaisuus korvannut? | Laskun kirjauskansion työnkulkutoiminnot                                                           |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                                                                        |

### Virtuaaliyritykset
<a id="virtual-company-accounts" class="xliff"></a>

Dynamics AX ei enää tue virtuaaliyritystoimintoa. Virtuaaliyritystoiminnon avulla käyttäjät pystyivät määrittämään tauluja yritysjoukon jaettavaksi. Toiminnon kuvaus on artikkelissa [Yrityksen tilit ja virtuaaliyrityksen tilit](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Toiminto ryhmittää virtuaaliyrityksille määritetyiksi tauluiksi. Virtuaaliyritykset ovat olemassa olevien "oikeiden" yritysten ryhmiä. Kyselyjä luomalla kaikki virtuaaliyrityksen yritykset voivat käyttää liitettyjen taulukokoelmien taulujen tietoja.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Poiston syy</td>
<td><ul>
<li>Virtuaaliyritykset on määritettävä, ennen kuin tiedot tallennetaan tauluihin. Virtuaaliyritysten sovittaminen jälkikäteen aiemmin luotuihin toteutuksiin on erittäin hankalaa.</li>
<li>Koska Dynamics AX:n nykyisessä versiossa on niin paljon tietojen normalisointia, taulukokoelmiin lisättävän tiedon hahmottamisesta on tullut erittäin hankalaa. Esimerkiksi on vaikea hahmottaa, mitä taulut tulee jakaa. Lisäksi kaikki taulut, joihin virtuaaliyrityksessä olevat taulut viitataan, on lisättävä. Taulun normalisoinnin vuoksi yksinkertaisimmankin useissa taulukoissa olevan päätiedon on oltava myös virtuaaliyrityksen osa. Tässä yhteydessä tehdyt mahdolliset virheet aiheuttavat toimintaongelmia.</li>
<li>Kun taulu on osa virtuaaliyritystä, se menettää tiedot tiedon alkuperästä ja vain virtuaaliyritys kirjataan.</li>
</ul></td>
</tr>
<tr class="even">
<td>Onko toinen ominaisuus korvannut?</td>
<td>Yleisiä tauluja käyttämällä taulut ovat kaikkien yritysten käytettävissä. Tällä hetkellä korvaavaa toimintoa ei ole.</td>
</tr>
<tr class="odd">
<td>Vaikutuksen alaiset moduulit</td>
<td>Ei käytettävissä</td>
</tr>
</tbody>
</table>

### Varastonhallinta II
<a id="warehouse-management-ii" class="xliff"></a>

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | **Inventoinnin- ja varastonhallintamoduuliin** sisältynyt Varastonhallinta II -ratkaisu (WMS II) oli Microsoft Dynamics AX 2012 R3:ssa julkaistun **varastonhallintamoduulin** toiminnon kaksoiskappale.                                                                         |
| Onko toinen ominaisuus korvannut? | AX 2012 R3:ssa, Microsoft Dynamics AX 2012 R3 CU8:ssa ja Microsoft Dynamics AX 2012 R3 CU9:ssa julkaistu **varastonhallintamoduuli** korvaa Varastonhallinta II:n ominaisuudet. Uudessa moduulissa on kehittyneemmät ominaisuudet ja joustavammat varaston hallintaprosessit kuin Varastonhallinta II:ssa. |
| Vaikutuksen alaiset moduulit             | Varaston hallinta, myynti ja markkinointi, hankinta                                                                                                                                                                                                                                         |

### Henkilöstöhallinnon työntekijän muistutukset
<a id="worker-reminders-in-human-resources" class="xliff"></a>

Henkilöstöhallinnon palkanlaskentatiedot

|                              |                 |
|------------------------------|-----------------|
| Poiston syy       | Vähäinen käyttö       |
| Onko toinen ominaisuus korvannut? | Ei              |
| Vaikutuksen alaiset moduulit             | Henkilöstö |

### Työn suunnittelu
<a id="workplanner" class="xliff"></a>

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Vähäinen käyttö                                                                                                                                                            |
| Onko toinen ominaisuus korvannut? | Ei, mutta **Profiilirelaatio**-sivu, joka avautuu **Profiiliryhmät**-sivulta, tukee samoja liiketoimintaskenaarioita mitä vanhentuneella **Työn suunnittelu**-sivulla käytettiin. |
| Vaikutuksen alaiset moduulit             | Työajan seuranta                                                                                                                                                  |

### X++-raportit
<a id="x-financial-statements" class="xliff"></a>

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| Poiston syy       | Toinen ominaisuus on korvannut tämän toiminnon.                                    |
| Onko toinen ominaisuus korvannut? | Management Reporter (Dynamics AX:n nykyisessä versiossa sen nimi on **Talousraportointi**) |
| Vaikutuksen alaiset moduulit             | Kirjanpito                                                                              |


