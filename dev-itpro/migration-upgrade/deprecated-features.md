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

# <a name="deprecated-features"></a>Vanhentuneet ominaisuudet

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan.

## <a name="features-that-have-been-deprecated-in-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a>Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivityksessä poistetut ominaisuudet

### <a name="warehouse-mobile-devices-portal"></a>Varaston mobiililaiteportaali

Varaston mobiililaiteportaali (WMDP) oli erillinen osa, joka oli tarkoitettu paikallisesti tapahtumaan itsenäiseen käyttöönottoon. Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition ei enää tue tätä komponenttia. Alkuperäinen, käyttäjäkokemusta parantava sovellus, on korvannut WMDP-toiminnot. 

|                                  |                                                 |
|----------------------------------|-------------------------------------------------|
| **Poiston syy**       | Sama toiminto.                        |
| **Onko toinen ominaisuus korvannut?** | Kyllä. Finance and Operations – varastointi on korvannut tämän ominaisuuden. Lisätietoja asennuksesta ja ennakkoedellytyksistä on ohjeaiheessa [Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen asentaminen ja määrittäminen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Vaikutuksen alaiset moduulit**             | Varaston hallinta, kuljetusten hallinta |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Pankkitilin täsmäytyksen lisätoimintojen manuaalisen täsmäytyksen täsmäytyssääntö

Täsmäytyssäännöllä valittiin ja merkittiin pankkitosite, kun asiakirjat täsmäytettiin manuaalisesti täsmäytyslaskentataulukossa.

|                                  |                                                                                        |
|----------------------------------|----------------------------------------------------------------------------------------|
| **Poiston syy**       | Rajoitettu käyttö.                                                                         |
| **Onko toinen ominaisuus korvannut?** | Nro Täsmäytettäviä asiakirjoja etsitään sarakkeen suodatusominaisuuksilla. |
| **Vaikutuksen alaiset moduulit**             | Maksuliikenteen hallinta                                                               |

### <a name="windows-8-tablet-app"></a>Windows 8 -tablettisovellus

Windows 8 -tablettisovelluksessa oli kulujen vienti- ja hyväksymistoiminnot.

|                                  |                                                                                          |
|----------------------------------|------------------------------------------------------------------------------------------|
| **Poiston syy**       | Finance and Operationsia voi käyttää tableteissa. Tablettisovellusta ei enää tarvita. |
| **Onko toinen ominaisuus korvannut?** | Nro                                                                                      |
| **Vaikutuksen alaiset moduulit**             | Matkalaskut                                                                       |


<a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Ominaisuudet, jotka on poistettu Dynamics 365 for Operations -versiosta 1611 ympäristöpäivityksessä 3
---------------------------------------------------------------------------------------------

### <a name="aeb-payment-formats-for-spain"></a>Espanjan AEB-maksumuodot

Consejo Superior Bancario -maksumuotoja käytetään maksusuoritustiedostojen lähettämiseen pankkiin asiakkaan maksuja ja toimittajamaksuja varten. Muotojen sisällön määrittää Asociación Española de Banca. Siihen sisältyy Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Espanjan ISO20022-tilisiirto ja suoraveloituksen maksumuoto |
| Vaikutuksen alaiset moduulit             | Myyntireskontra, ostoreskontra                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Liettuan pankkiohjelmamaksujen siirto

Pankkiohjelmamaksujen siirto luodaan ja tulostetaan Liettuan maksunsiirron (LT) vientimuodon avulla. Liettuan markkina-alue aloitti LITASin, yhdistetyn sähköisen pankkijärjestelmän, käytön vuonna 2005.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                    |
| Onko toinen ominaisuus korvannut? | Kyllä, Liettuan ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                           |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Norjan BBS Direkte Remittering -maksumuodot

BBS Direkte Remittering -maksumuotoja ovat asiakkaan maksun perittävän vienti (suoraveloitus) ja palautussanoman tuonti.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                                                                                                                        |
| Onko toinen ominaisuus korvannut? | Norjan AvtaleGiro- asiakkaan maksumuotoa voidaan käyttää suoraveloituksen sanomien luomiseen. Palautussanoman tuominen toteutetaan tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra, ostoreskontra                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Espanjan tilikartta-työkalu

Tätä työkalua käytetään, kun Espanjan tilikartta edellyttää suuria muutoksia. Käyttäjä voi tuoda uuden tilikartan Microsoft Excel- tai tekstimuodossa ja tuoda myös raportteja.

|                              |                |
|------------------------------|----------------|
| Poiston syy       | Rajoitettu käyttö  |
| Onko toinen ominaisuus korvannut? | Nro             |
| Vaikutuksen alaiset moduulit             | Kirjanpito |

### <a name="dom80-payment-format-for-belgium"></a>Belgian Dom80-maksumuoto

Vanha Belgian maksukehotuksen maksumuoto (suoraveloitus).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä Belgian SO 20022 -suoraveloituksen maksumuoto |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                    |

### <a name="dtaezag-payment-formats-for-switzerland"></a>Sveitsin DTA/EZAG-maksumuodot

DTA/EZAG-muodot integroidaan ESR-järjestelmään, koska niissä voidaan käsitellä viitenumeroa. Koska viitenumerot eivät ole pakollisia, näitä muotoja voidaan käyttää kaikkien toimittajamaksujen käsittelyssä. Muotoja käytetään yrityksissä, joissa on pankkitili muussa kuin "Postfinance"-sijainnissa.

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                      |
| Onko toinen ominaisuus korvannut? | Kyllä, Sveitsin ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                             |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>Itävallan ISOEDIFACT-DIRDEB-suoraveloituksen maksumuoto

Maksukehotuksen EDIFACT-DIRDEB-maksumuoto (suoraveloitus).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Itävallan ISO 20022 -suoraveloituksen maksumuoto |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                    |

### <a name="edivat-for-belgium"></a>Belgian EDIVAT

EDIVAT on Belgian vanhentunut standardi sähköiselle ilmoitukselle suojatun sähköpostin kautta. Microsoft Dynamics AX 2012 säilyttää vain luku -ratkaisun historiallisten tietojen käyttämiseksi.

|                              |                                      |
|------------------------------|--------------------------------------|
| Poiston syy       | Tätä toimintoa ei enää käytetä. |
| Onko toinen ominaisuus korvannut? | Nro                                   |
| Vaikutuksen alaiset moduulit             | Kirjanpito                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>Norjan eGiro EDIFACT CREMUL- maksun tuontimuoto

eGiro perustuu YK:n kansainväliseen EDIFACT CREMUL (Multiple Credit Advice Message) -standardiin, jota käytetään asiakasmaksujen automaattisessa kirjauksessa. eGiro on Microsoft Dynamics AX:ssä toteutettu asiakkaan maksun tuontimuoto.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                                                     |
| Onko toinen ominaisuus korvannut? | Nro Muoto korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                       |

### <a name="external-inventory-for-poland"></a>Puolan ulkoinen varasto

Tavaroiden tunnistetiedot, jotka saadaan toimittajan myynnistä ilman ostoa. Ulkoisessa varastossa käsitellyt tavarat eivät vaikuta vakiovarastoon ja ne voidaan myydä ja ostaa automaattisesti. Tämä prosessi luo todelliset varastosiirrot.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| Poiston syy       | Korvattu toisella toiminnolla                     |
| Onko toinen ominaisuus korvannut? | Kyllä, saapuvan tavaralähetyksen perustoiminnot |
| Vaikutuksen alaiset moduulit             | Ostoreskontra, varastonhallinta          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Itä-Euroopan raportin muodostustoiminto

Työkalua käytetään tiedonkeruun määritykseen kirjanpitoa ja veroraportteja varten sekä tietojen viemiseksi XLS- ja DOC- raporttimalleihin.

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| Poiston syy       | Rajoitettu käyttö                                                                            |
| Onko toinen ominaisuus korvannut? | Nro Työkalu korvataan sähköiset raportoinnin konfiguraatioilla tulevissa julkaisuversioissa. |
| Vaikutuksen alaiset moduulit             | kirjanpito                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Suomen asiakasmaksutapahtumien tuominen

Voit valita Suomen maksujen tuontimuodon asiakasmaksutapahtumien tuomiselle pankin antamasta ulkoisesta tiedostosta.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                                                     |
| Onko toinen ominaisuus korvannut? | Nro Muoto korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                       |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Suomen maksutapahtumien tuominen kirjanpidon kirjauskansioon

Suomen erityismuotoa käytetään kirjanpidon tapahtumien tuomiseksi kirjanpitoon.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                                                     |
| Onko toinen ominaisuus korvannut? | Nro Muoto korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                       |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Belgian Isabel-synkronoitu integrointi (CIS)

Isabel on Euroopan sähköisen maksuliikenteen ja tiedonsiirron yleinen standardi Belgiassa.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Integrointi Isabel-asiakasohjelmaan on lopetettu.                                                                |
| Onko toinen ominaisuus korvannut? | Nro Maksumuodot, joita ei voi enää käyttää, korvataan ISO20022-tilisiirron maksumuodolla Belgiassa. |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                                                                                     |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Espanjan tilikartan ja kirjanpitosääntöjen muutokset

Tätä toimintoa käytetään Espanjan tilikartan ja kirjanpitosääntöjen muutoksiin. Se yhdistää tilejä ja auttaa vanhan tilikartan muuttamisessa uudeksi tilikartaksi ja vertaa edellistä tilikautta uuteen tilikauteen, vaikka ne on kirjattu eri tilinumeroille.

|                              |                |
|------------------------------|----------------|
| Poiston syy       | Rajoitettu käyttö  |
| Onko toinen ominaisuus korvannut? | Nro             |
| Vaikutuksen alaiset moduulit             | Kirjanpito |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Toimittajan Pagamento Fornittori -maksumuoto

Vanha Italian tilisiirron maksumuoto.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Poiston syy       | Tätä maksumuotoa ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Italian ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                       |

### <a name="payment-export-formats-for-estonia"></a>Viron maksun vientimuodot

Pankin maksun viennissä käytetään Telehansa- ja Teleservice-muotoja.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Viron ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                         |

### <a name="payment-file-archive-for-norway"></a>Norjan maksutiedostoarkisto

Kun maksutiedostot on luotu, tiedostoarkistoon arkistoidaan kaikki luodut tiedostot, vaikka tiedostot on aiemmin kirjoitettu tai luettu.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| Poiston syy       | Korvattu toisella toiminnolla                                        |
| Onko toinen ominaisuus korvannut? | Kyllä, sähköisen raportoinnin arkistoidut työt                            |
| Vaikutuksen alaiset moduulit             | Ostoreskontra, myyntireskontra, organisaation hallinto |

### <a name="payment-import-formats-for-estonia"></a>Viron maksun tuontimuodot

Pankin maksun tuonnissa käytetään Telehansa- ja TeleTeenus-muotoja.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                                                    |
| Onko toinen ominaisuus korvannut? | Nro Muodot korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                        |

### <a name="performance-management-goal-workflow"></a>Suorituskyvyn hallintatavoite -työnkulku

Suorituskyvyn hallinta sisältää tavoitteiden hallinnan ja integroinnin suorituskykyarvioiden kanssa.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Suorituskyvyn hallinta on suunniteltu uudelleen ja tavoitesivujen lukumäärää vähennettiin prosessin yksinkertaistamiseksi.                 |
| Onko toinen ominaisuus korvannut? | Nro Tavoitteet näkyvät esimiehille esimiehen itsepalveluportaalin kautta, ja esimies voi muuttaa ja tarkastella niitä. |
| Vaikutuksen alaiset moduulit             | Henkilöstöresurssien hallinta                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Ruotsin Postgirot- ja Postgirot Utland -maksumuodot

Ruotsin Postgirot- ja Postgirot Utland -maksumuodot.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                 |
| Onko toinen ominaisuus korvannut? | Kyllä, Ruotsin ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                        |

### <a name="radio-frequency-identifier"></a>Radiotaajuinen etätunnistus

Radiotaajuinen etätunnistus (RFID) on tiedonkeräysmenetelmä, jossa käytetään tunnistetietojen tallentamiseen sähköisiä tunnisteita, ja tunnistetiedot luetaan ilman näköyhteyttä.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| Poiston syy       | Vähäinen käyttö ja rajoitetut toiminnot. |
| Onko toinen ominaisuus korvannut? | Nro                                            |
| Vaikutuksen alaiset moduulit             | Inventoinnin- ja varastonhallinta                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Latvian valtion määrittämän laskujen numeroinnin raportti

Latvian lainsäädäntö sisältää myyntilaskujen numerointia koskevia erityissääntöjä. Toiminnon avulla voidaan määrittää erityiset numerot myyntilaskuille käyttäjän tai käyttäjäryhmän mukaan. Tämän jälkeen voit luoda raportin tai XML-tiedoston. Voit myös tulostaa raportin käytetyistä laskunumeroista.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Valtion määrittämää laskujen numerointia ei tarvitse enää ylläpitää. Käytettyjen laskunumeroiden raporttia ei enää vaadita. |
| Onko toinen ominaisuus korvannut? | Nro                                                                                                                       |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                                                                      |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Liettuaa koskevat johtajan ja kirjanpitäjän nimien asetukset

Yrityksen johtajan ja kirjanpitäjän nimet voidaan määrittää yrityksen tietoihin ja käyttää paikallisten raporttien tulostuksessa.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Poiston syy       | Korvattu toisella toiminnolla                                     |
| Onko toinen ominaisuus korvannut? | Kyllä, viranomaisten asetuksia käytetään samaan tarkoitukseen.   |
| Vaikutuksen alaiset moduulit             | Ostoreskontra, myyntireskontra, maksuliikenteen hallinta |

### <a name="telepay-payment-formats-for-norway"></a>Norjan Telepay-maksumuodot

Telepay-maksumuodot sisältävät toimittajan maksun viennin (tilisiirrolla) ja asiakkaan maksukehotuksen (suoraveloitus).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                                                        |
| Onko toinen ominaisuus korvannut? | Kyllä, Norjan ISO20022-tilisiirron maksumuoto ja asiakkaan maksun AvtaleGiro-muoto |
| Vaikutuksen alaiset moduulit             | Myyntireskontra, ostoreskontra                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Suomen toimittajan maksun vientimuodot

Kaksi eri muotoa maksujen vientiä varten käytettävissä Suomessa. LM02 (FI) käytetään kotimaan maksuille ja LUM2 (FI) ulkomaanmaksuille.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Poiston syy       | Maksumuotoja ei enää käytetä.                  |
| Onko toinen ominaisuus korvannut? | Kyllä, Suomen ISO20022-tilisiirron maksumuoto |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                         |

### <a name="workflow-for-creating-goals"></a>Tavoitteiden luomisen työnkulku

Työntekijöiden tavoitteiden luomisen työnkulku on yksi monista työnkuluista, joita oli käytettävissä suorituskyvyn hallintaprosessin koordinoinnin apuna.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Suorituskyvyn hallinta on suunniteltu kokonaan uudelleen Microsoft Dynamics 365 for Finance and Operationsissa.                                                                                                                                                                                                                                        |
| Onko toinen ominaisuus korvannut? | Uudelleen suunnitellulla suorituskyvyn hallintatoiminnolla voidaan seurata tarkemmin tavoitteiden sisältöä ja mittauksia, joiden avulla voidaan seurata etenemistä, sekä tukidokumentaation liittämistä. Tavoitteet voidaan tallentaa malleina ja käyttää uudelleen. Tämän toiminnon avulla voit määrittää lisätavoitteita työntekijöille entistä nopeammin. |
| Vaikutuksen alaiset moduulit             | Henkilöstöresurssien hallinta                                                                                                                                                                                                                                                                                                               |

## <a name="features-deprecated-in-dynamics-ax-70-releases"></a>Dynamics AX:n 7.0 -julkaisuversioista poistetut ominaisuudet
### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Mahdollisuus peruuttaa toimittajan laskun muutokset

|                              |                         |
|------------------------------|-------------------------|
| Poiston syy       | Suorituskyvyn parannus |
| Onko toinen ominaisuus korvannut? | Ei                      |
| Vaikutuksen alaiset moduulit             | Ostoreskontra        |

### <a name="aif-axd-and-axbc-integrations"></a>AIF-, AxD- ja AxBC-integraatiot

Application Integration Frameworkissä (AIF) tietoja voidaan vaihtaa ulkoisten järjestelmien kanssa palveluina näyttäytyvänä liiketoimintalogiikkana. Dynamics AX sisältää asiakirjoihin ja .NET Business Connectoriin (AxBC) perustuvia palveluja. Asiakirja luodaan XML-muotoisena. XML sisältää otsikkotiedot, joka lisäämällä luodaan *sanoma*, joka siirretään Dynamics AX:ään ja siitä pois. Asiakirjoja ovat esimerkiksi myynti- ja ostotilaukset. Käytännössä kuitenkin lähes mikä tahansa yksikkö, kuten asiakas, voidaan ilmaista asiakirjana. Asiakirjoihin perustuvat palvelut käyttävät **Axd &lt;*asiakirja*&gt; -luokkia.

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | AIF:n ja AxDs:n arkkitehtuuria ei voi skaalata pilvipalveluun. Joukkotuontiin liittyi suorituskykyongelmia.                                                                               |
| Onko toinen ominaisuus korvannut? | Dynamics AX:n nykyisessä versiossa tämä ominaisuus on korvattu tietojen tuonti- ja vientiympäristöllä, joka tukee toistuvaa joukkotuontia ja -vientiä. AxBC:ssä on suositeltavaa käyttää varsinaisia tauluja. |
| Vaikutuksen alaiset moduulit             | AxDs, AxBCs ja AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>Tuoterakenteet ilman tuoterakenneversioita

Kun **Tuoterakenneversiot**-määritysavain poistettiin käytöstä, tuoterakenneversiot piilotettiin kaikissa lomakkeissa ja järjestelmä pakotti 1:1-suhteen vapautettujen tuotteiden ja tuoterakenteiden välille. **Tuoterakenneversiot**-määritysavainta ei voi poistaa Dynamics AX:n nykyisessä versiossa.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Poiston syy       | Tuoterakenneversioiden ohjaamista määritysavaimella ei voi skaalata pilviympäristöön. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                      |
| Vaikutuksen alaiset moduulit             | Tuotetietojen hallinta, inventoinnin- ja varastonhallinta                                    |

### <a name="brazilian-bordero"></a>Brasilian Bordero

Erityismaksutapa Brasilian yrityksille

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| Poiston syy       | Brasilian Bordero-maksutavan tuki on lopetettu Brasilian lokalisointiversiosta |
| Onko toinen ominaisuus korvannut? | Nro                                                                                                    |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                                                                      |

### <a name="brazilian-sintegra-statement"></a>Brasilian Sintegra-raportti

Liittovaltion veroraportti ICMS-verolle

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Tämä raportti ei ole enää käytettävissä joissain Brasilian osavaltioissa.                                                     |
| Onko toinen ominaisuus korvannut? | Nro Käyttäjät voivat käyttää yleistä sähköistä raportointityökalua raportin määrittämiseen, jos se on pakollinen erityistilanteissa. |
| Vaikutuksen alaiset moduulit             | Verokirjat                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasilian NF-e:n SCAN-varatila

(SCAN) varaympäristöä käytetään Nota Fiscal eletrônica (NF e) -tilan luontiin, vientiin ja tuontiin, kun Secretaria da Fazenda (SEFAZ) -ympäristö ei ole käytettävissä.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| Poiston syy       | Tämä varamenetelmä ei ole enää käytettävissä kaikissa Brasilian osavaltioissa |
| Onko toinen ominaisuus korvannut? | Nro                                                                          |
| Vaikutuksen alaiset moduulit             | Myyntireskontra                                                         |

### <a name="business-analyzer"></a>Business Analyzer

Käyttäjät voivat tarkastella tällä mobiilisovelluksella tärkeitä liiketoiminnan mittareita.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Toinen ominaisuus on korvannut tämän toiminnon.                                                                                                      |
| Onko toinen ominaisuus korvannut? | Microsoft PowerBI:n taloudellisen suorituskyvyn seurannan sisältöpaketti sisältää tärkeät taloudelliset mittarit, jotka sisältyivät aiemmin Business Analyzeriin. |
| Vaikutuksen alaiset moduulit             | Kirjanpito                                                                                                                                                |

### <a name="business-statistics"></a>Liiketoimintatilastot

Niiden liiketoiminnan tilastotietokyselyiden asetukset, jotka voivat auttaa organisaation suorituskyvyn analysoinnissa

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| Poiston syy       | Vanha tapa käsitellä liiketoiminnan tietoja (BI), vähäinen käyttö ja rajalliset ominaisuudet |
| Onko toinen ominaisuus korvannut? | Uudet BI-ratkaisut Dynamics AX:n nykyisessä versiossa                                      |
| Vaikutuksen alaiset moduulit             | Hankinta, ostoreskontra, myynti ja markkinointi, myyntireskontra         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Hyväksyttyjen laskujen kirjauskansion tiedoston päivämäärän muutostoiminto

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Poiston syy       | Vähäinen käyttö                                                               |
| Onko toinen ominaisuus korvannut? | Kyllä. Kirjatun toimittajatapahtuman tiedoston päivämäärää voidaan muuttaa. |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Alankomaiden ClieOp03-maksumuoto

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Muotoa ei enää käytetä Alankomaissa, sillä SEPA-toiminto on korvannut sen. |
| Onko toinen ominaisuus korvannut? | SEPA-maksujen vienti                                                                                       |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                        |

### <a name="compliance-center"></a>Compliance Center

Compliance Center oli Sarbanes-Oxley-lakiin liittyvien vaatimustenmukaisuusaloitteiden asiakirjavaatimusten hallintaan tarkoitettu yritysportaalisivusto.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Toimintoa ei käytetty. Microsoft SharePoint sisältää Compliance Centerin käytössä olleet ominaisuudet. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                     |
| Vaikutuksen alaiset moduulit             | Yhteensopivuus ja sisäinen valvonta                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Microsoft Dynamicsin yhdistin

Tällä työkalulla integroitiin Microsoft Dynamics CRM:n tärkeitä tietoja Microsoft Dynamics ERP -sovelluksiin.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Poiston syy       | Toinen ominaisuus on korvannut tämän toiminnon. |
| Onko toinen ominaisuus korvannut? | Dynamics Integrator                                      |
| Vaikutuksen alaiset moduulit             | Microsoft Dynamicsin yhdistin                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Säilöyksikkö ja monidimensioinen varasto

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Sama toiminto                                                                                                                                         |
| Onko toinen ominaisuus korvannut? | Kyllä. AX2012:n jälkeen tämä toiminto on korvattu konsolidoidulla erätilaustoiminnoilla. Tämä ominaisuusjoukko sisältää konsolidoidun varastonäkymän. |
| Vaikutuksen alaiset moduulit             | Tuotetietojen hallinta, tuotannonhallinta, varastonhallinta, myynti ja markkinointi                                                                   |

### <a name="cue-group-metadata"></a>Pinoryhmän metatiedot

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Pinoryhmiä käytettiin näyttämään vähintään yksi pino tietoruutualueella. Toiminto oli rajallinen ja siihen liittyi suorituskykyongelmia, koska tietueen muuttuminen päälomakkeessa loi jokaiselle pinolle yhden kyselyn pinoryhmässä. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                                                                                                                            |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Pinon metatiedot

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Pinon metatiedot rajoittuivat määrä- tai summatietoihin.                                                                                                                                                                                   |
| Onko toinen ominaisuus korvannut? | Käyttöönotetut ruudun metatiedot mahdollistavat joustavamman mallinnuksen. Voit esimerkiksi mallintaa nykyiset määrät, siirtymisen ja suorituskykyilmaisimet (KPI:t). Määräruudun metatiedot korvaavat suoraan pinon metatiedot. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Tanskalainen sekkilomake

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Tanskan sekkimuodon tuki on lopetettu ja raportti on poistettu tanskalaisesta lokalisoinnista. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                      |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                     |

### <a name="data-partitions"></a>Tieto-osiot

Tieto-osiot erottavat Microsoft Dynamics AX:n tietokannan tiedot loogisesti.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Tieto-osiot otettiin käyttöön Microsoft Dynamics AX 2012 R2:ssa tietojen eristämistä varten. Yleisessä skenaariossa yrityksellä on tytäryhtiöitä mutta tytäryhtiön tiedot eivät saisi olla toisen tytäryhtiön nähtävissä, vaikka kumpikin tytäryhtiö on saman IT-osaston alaisuudessa. Ohjelmassa oli kuitenkin otettava käyttöön ylimääräisiä komentosarjoja ja hallintakustannuksia, jotta uusia osioita voitaisiin luoda, tiedot voitaisiin lisätä ja osiotiedot voitaisiin varmuuskopioida. Pilvipalvelussa, jossa meillä on käyttöympäristövuokrattuja (PaaS-palvelu) tietokantapalveluja (Microsoft Azuren SQL-tietokanta), tietokantaa on tehokkaampaa käyttää erityssäilönä kuin tehdä eristys ohjelmassa. Riippumatta siitä, tarvitaanko tietojen osiointia tytäryhtiöitä tai useita vuokraajia varten tai koon vuoksi, mielestämme skenaariot voidaan käsitellä paremmin useissa tietokannoissa tai Dynamics AX:n esiintymissä. |
| Onko toinen ominaisuus korvannut? | Tieto-osiot korvataan tulevissa versioissa tukemalla useita tietokantoja tai Dynamics AX:n esiintymiä.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

### <a name="delimitation"></a>Rajoitus

|                              |                                        |
|------------------------------|----------------------------------------|
| Poiston syy       | Toiminnolle ei ollut käyttöä. |
| Onko toinen ominaisuus korvannut? | Ei                                     |
| Vaikutuksen alaiset moduulit             | Työajan seuranta                    |

### <a name="desktop-client"></a>Työpöytäasiakasohjelma

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Dynamics AX:n asiakasohjelmakokemus on uudistettu parantamaan käytettävyyttä kaikissa ympäristöissä ja laitteissa.                      |
| Onko toinen ominaisuus korvannut? | Uusi verkkoasiakasohjelma perustuu työpöytälomakkeen metatietoihin ja ohjelmointimalliin, jota on muokattu luomaan monipuolinen verkkoympäristö. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                    |

### <a name="direct-database-connection"></a>Suora tietokantayhteys

Dynamics AX 2012 R3 -versiossa Retail Modern POS -sovellus voi muodostaa suoran yhteyden kanavatietokantaan samalla tavalla, kuin Enterprise POS. Tämä oli lisänä Retail Modern POS -sovelluksen normaalille tietoliikenneyhteydelle, joka kulki vähittäismyynnin palvelimen välityksellä.  

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Poiston syy       | Suora tietokantayhteys edellytti matalamman suojauksen, ja sitä käytettiin pääasiassa korkeamman suorituskyvyn saavuttamiseen. Finance and Operationsissa tehtyjen suorituskyky- ja tietoturvaparannusten vuoksi tämä toiminnallisuus aiheuttaa enemmän ongelmia kuin mitä se ratkaisee. |
| Onko toinen ominaisuus korvannut? | Nro Vain vakiomuotoinen vähittäismyynnin palvelinyhteys on enää tuettu.    |
| Vaikutuksen alaiset moduulit             | Kanavatietokanta/Retail Modern POS                                    |

### <a name="dutch-swift-mt940"></a>Alankomaiden SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Käytössä on nyt yleinen toiminto lokalisoidun toiminnon sijaan.                                                                                                                                                                 |
| Onko toinen ominaisuus korvannut? | Kyllä. Pankkitilin täsmäytyksen lisätoiminnot on korvannut tämän toiminnon. Lisäksi camt.053 ISO20022 -tiliotteen tuonnin käyttöönottoa suunnitellaan kirjauskansioon seuraavassa Dynamics AX -päivityksessä. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL Saksassa)

Tämä toiminto mahdollisti XBRL (eXtensible Business Reporting Language) -tulostuksen, joka on tarkoitettu erityisesti Saksan eBilanz-luokitusta varten.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Toimintoa ei käytetty                                                                                                                                                 |
| Onko toinen ominaisuus korvannut? | Toimintoa ei korvata toisella ominaisuudella, mutta Saksan markkinoilla on saatavana useista erikoistuneita XBRL-paketteja, joissa on monipuolisia XBRL-toimintoja. |
| Vaikutuksen alaiset moduulit             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Yritysportaalin asiakasohjelma

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Käytössä on yksi asiakasohjelmaympäristö.                                                                                            |
| Onko toinen ominaisuus korvannut? | Uusi verkkoasiakasohjelma perustuu työpöytälomakkeen metatietoihin ja ohjelmointimalliin, jota on muokattu luomaan monipuolinen verkkoympäristö. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                    |

### <a name="environmental-sustainability"></a>Ekologinen kestävyys

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| Poiston syy       | Vähäinen käyttö ja rajoitetut toiminnot       |
| Onko toinen ominaisuus korvannut? | Ei                                                 |
| Vaikutuksen alaiset moduulit             | Yhteensopivuus ja sisäisen tarkistus, ostoreskontra |

### <a name="form-activex-and-managed-host-controls"></a>Lomakkeen ActiveX:n ja hallitun ylläpidon ohjausobjektit

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | ActiveX:n ja hallitun ylläpidon ohjausobjektit perustuivat vanhentuneeseen työpöytäasiakasohjelmaan.                                                                                                             |
| Onko toinen ominaisuus korvannut? | Laajennettava ohjausobjektiympäristö tukee uusien HTML-, CSS- ja JavaScript-pohjaisten ohjausobjektien luomista ja on ensimmäisen luokan ohjausobjekti Microsoft Visual Studio Tooling -ympäristössä. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Esilaskujen muodostus erätoiminnolla

Vaikka esilaskua ei voi enää muodostaa erätoimintona, käyttäjä voi edelleen luoda esilaskun.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Poiston syy       | Erätoiminnolla luodulle laskulle ei ole lomaketta, jossa luotu esilaskutiedosto voitaisiin säilyttää ja näyttää. |
| Onko toinen ominaisuus korvannut? | Esilaskuja voidaan luoda edelleen ja käyttäjä päättää sijainnin, johon tiedosto tallennetaan.   |
| Vaikutuksen alaiset moduulit             | Ostoreskontra, myyntireskontra, maksuliikenteen hallinta                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Saksan DTAUS-maksun vienti ja tiliotteen tuonti (kokonaissummat ja tapahtumat)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Muotoa ei enää käytetä Saksassa, sillä SEPA (yhtenäinen euromaksualue) -toiminto on korvannut sen.                                                                                                                                                                 |
| Onko toinen ominaisuus korvannut? | Kyllä. SEPA-maksun vienti ja pankkitilin täsmäytyksen lisätoiminnot tiliotteiden tuomiseen on korvannut tämän toiminnon. Lisäksi camt.053 ISO20022 -tiliotteen tuonnin käyttöönottoa suunnitellaan kirjauskansioon seuraavassa Dynamics AX -päivityksessä. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Saksan DTAZV-maksumuoto

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| Poiston syy       | Muotoa ei enää käytetä Saksassa, sillä SEPA-toiminto on korvannut sen. |
| Onko toinen ominaisuus korvannut? | SEPA-maksujen vienti                                                                               |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                |

### <a name="german-mt940-import"></a>Saksassa tuominen MT940-muodossa

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Käytössä on nyt yleinen toiminto lokalisoidun toiminnon sijaan.                                                                                                                                                                 |
| Onko toinen ominaisuus korvannut? | Kyllä. Pankkitilin täsmäytyksen lisätoiminnot on korvannut tämän toiminnon. Lisäksi camt.053 ISO20022 -tiliotteen tuonnin käyttöönottoa suunnitellaan kirjauskansioon seuraavassa Dynamics AX -päivityksessä. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>Saksan XML-muotoinen EU-myyntiluettelo

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | XML-muotoa Saksan EU:n arvonlisäveron yhteenvetoilmoitusta varten ei enää tueta. Saksan EU:n arvonlisäveron yhteenvetoilmoitus voidaan lähettää Saksan veroviranomaiselle ainoastaan ELMA5-tekstitiedostomuodossa. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                                                                                 |
| Vaikutuksen alaiset moduulit             | Vero                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>Kirjanpidon SSRS-raportit

Seuraavia valikkovaihtoehtoja sisältävät raportit on poistettu: **Pääkirjan yhteenveto**, **Yksityiskohtainen pääkirja**, **Tilikartta**, **Kirjausketju**, **Saldot** ja **Saldoluettelo**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Microsoft SQL Server Reporting Services (SSRS) -raportit on korvattu Management Reporter -toiminnoilla ja oletusraporteilla. |
| Onko toinen ominaisuus korvannut? | Management Reporter (Dynamics AX:n nykyisessä versiossa sen nimi on **Talousraportointi**)                                                  |
| Vaikutuksen alaiset moduulit             | Kirjanpito                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>InfoPart- ja FormPart-metatiedot

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | InfoPart- ja FormPart-metatietojen avulla voitiin luoda kahden eri asiakasohjelman tietoruutuja.                                                                                                                                    |
| Onko toinen ominaisuus korvannut? | InfoPart-metatiedot oli yksinkertaistettu lomakemääritelmä, ja se on muunnettu lomakkeeksi päivitystyökaluilla. Lomakkeeseen viittaavat FormPart-metatiedot on korvattu suoralla viittauksella, joka luodaan päivitystyökaluilla. |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Päätilin luettelosivu

Luettelo yrityksen tileistä ja niihin liittyvät saldotiedot

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Saldotiedot ovat saatavilla tilin ja dimension mukaisella **Pääkirja**-luettelosivulla.                                                                                      |
| Onko toinen ominaisuus korvannut? | **Päätilit** sisältää saman tililuettelon kuin **Päätili**-luettelosivu. **Päätilit**-ruudukkonäkymä näyttää myös pienemmän ruudukkomaisen näkymän. |
| Vaikutuksen alaiset moduulit             | Kirjanpito                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malesian ja Singaporen pankin kassavirtaraportti

Toiminnolla voitiin tulostaa kassavirtaraportti, joka sisältää valittujen pankkitilien saapuvien ja lähtevien kassavirtojen tapahtumat sekä tiedot määritetyltä päivämääräväliltä.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Poiston syy       | Samat tiedot saadaan pankkitapahtuman kyselyllä. |
| Onko toinen ominaisuus korvannut? | Pankkitapahtuman kysely                                            |
| Vaikutuksen alaiset moduulit             | Maksuliikenteen hallinta                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Meksikon sähköinen CFD-lasku

Tällä ominaisuudella voitiin luoda Meksikossa sähköisiä laskuja käyttämällä CFD (Comprobante Fiscal Digital) -menetelmää, jossa yritys allekirjoittaa laskun pyytämällä liittyvän valtuutuksen viranomaiselta. Tämä ominaisuus tarjoaa myös kuukausiraportin, joka koostui kaikista kyseisen kuukauden aikana tehdyistä sähköisistä laskuista.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Menetelmää ei enää käytetä. Veroviranomaiset lopettivat CFD-menetelmällä luotavat sähköiset laskut ja niiden tilalla käytetään CFDI (Comprobante Fiscal Digital a través de Internet) -menetelmää, jossa allekirjoitus on delegoitu kolmannen osapuolen palveluntarjoajalle (PAC). Kuukausiraportti on poistettu, ja käyttäjät voivat tehdä kyselyvaihtoehdolla kyselyjä historiallisista tapahtumista. |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                                                                                                                                                                                                                                                                                                        |
| Vaikutuksen alaiset moduulit             | Myyntireskontra, projekti                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Meksikon toteutunut ja toteutumaton ALV

Microsoft Dynamics AX 2012:lla hallittiin toteutumatonta arvonlisäveroa (ALV:tä) käyttämällä vain Meksikoa koskevaa toteutumattoman veron toimintoa.

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Sama toiminto                                                                                             |
| Onko toinen ominaisuus korvannut? | Kyllä. Tämä toiminto on korvattu ydintoimintojen tavallisessa suoritusperusteisella arvonlisäverotoiminnolla. |
| Vaikutuksen alaiset moduulit             | Vero                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook -integrointi

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| Poiston syy       | Tämä ominaisuus on korvattu Microsoft Exchange Server -integroinnilla. |
| Onko toinen ominaisuus korvannut? | Kyllä                                                                            |
| Vaikutuksen alaiset moduulit             | Myynti ja markkinointi                                                            |

### <a name="payroll-information-in-human-resources"></a>Henkilöstöhallinnon palkanlaskentatiedot

Henkilöstöhallinnon palkanlaskentatiedot

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Palkanlaskennan ja Henkilöstöhallinnan perussivut ovat korvanneet tämän ominaisuuden.                                                                                                                                                                                                                                              |
| Onko toinen ominaisuus korvannut? | **Edut**, **Ansiot** ja muut liittyvät Yhdysvaltojen palkanlaskenta -kohdassa olleet sivut on määritetty uudelleen ja sisältyvät nyt henkilöstöhallinnon perusmäärityksiin. Tämä auttaa tukemaan ulkoista palkanlaskennan käsittelyä. Toimintoa käytetään valitsemalla **Henkilöstöhallinta 1** &gt; **Palkanlaskenta**-määritysavain. |
| Vaikutuksen alaiset moduulit             | Henkilöstöhallinto, palkanlaskenta                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Varastonhallinnan kirjauskansioiden yksityinen esto

Varastokirjauskansiot eivät enää tue kirjauskansion merkitsemistä yksityiseksi valitulle käyttäjälle. Vain käyttäjäryhmien käyttämää kirjauskansioiden yksityistä estoa ja estoa muokkauksen aikana tuetaan.

|                              |                                        |
|------------------------------|----------------------------------------|
| Poiston syy       | Toiminnolle ei ollut käyttöä. |
| Onko toinen ominaisuus korvannut? | Ei                                     |
| Vaikutuksen alaiset moduulit             | Varastonhallinta                   |

### <a name="product-builder"></a>Tuotekonfiguraattori

Tuotekonfiguraattoria käytettiin määrittämään dynaamisesti nimikkeitä myyntitilauksesta, ostotilauksesta, tuotantotilauksesta, myyntitarjouksesta, projektitarjouksesta tai nimiketarpeesta. Käyttäjä voi valita asiakkaan vaatimusten mukaisia arvoja mallinnusmuuttujia sisältävän tuotemallin perusteella ja saada näin yksilöllisen tuotevariantin, jolla on tuoterakenne ja reitti.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Tuotekonfiguraattori paljasti X ++-koodin loppukäyttäjille eikä sitä tueta Dynamics AX:n nykyisessä versiossa. Se on poistettu, jotta päällekkäisissä suurissa koodikannoissa ei tarvitsisi tehdä kaksinkertaista ylläpitoa. |
| Onko toinen ominaisuus korvannut? | Tuotekonfiguraatio                                                                                                                                                                                   |
| Vaikutuksen alaiset moduulit             | Tuotetietojen hallinta, myynti ja markkinointi                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Nimeä tuotedimensio uudelleen

Tällä toiminnolla voi vaihtaa yhden kolmesta vakiotuotedimension nimestä (koko, väri tai tyyli) liiketoiminnan vaatimuksiin paremmin sopivaan nimeen. Uudelleennimeäminen koski kaikkia otsikoita, joissa tuotedimension nimeä käytettiin.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Poiston syy       | Dynamics AX:n nykyinen versio ei tue suorituksen aikaisia otsikkomuutoksia. |
| Onko toinen ominaisuus korvannut? | Nro                                                                            |
| Vaikutuksen alaiset moduulit             | Tuotetietojen hallinta                                                |

### <a name="retail-server-connectivity-using-http"></a>Vähittäismyynnin palvelinyhteys HTTP-protokollalla

Dynamics AX 2012 R3 -versiossa vähittäismyynnin palvelinyhteyttä oli mahdollista käyttää (suojaamattomalla) HTTP-yhteydellä. Tämä oli lisänä vakioyhteyteen HTTPS-protokollalla.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Poiston syy       | Uusien suojausvaatimusten vuoksi tietoliikenneyhteys on sallittua ainoastaan TLS 1.2 -suojausta (tai uudempaa) käyttäen. Omatoiminen asennusohjelma määrittää yhteystavan tietokoneelle automaattisesti. |
| Onko toinen ominaisuus korvannut? | Nro Vain vakiomuotoinen HTTPS-yhteys on enää tuettu.                                                                           |
| Vaikutuksen alaiset moduulit             | Vähittäismyynnin palvelin                                                |

### <a name="role-center-pages"></a>Roolikeskus-sivut

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Roolikeskus-sivut perustuivat vanhentuneeseen yritysportaaliympäristöön, joka on korvattu uudella verkkoasiakasympäristöllä Dynamics AX:n nykyisessä versiossa. |
| Onko toinen ominaisuus korvannut? | Uusi Työtila-lomakemalli käyttäjille prosessikeskeisen rakenteen, jonka kautta on helppo käyttää kyseisen prosessin usein käytettyjä tehtäviä.                       |
| Vaikutuksen alaiset moduulit             | Kaikki                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>Arvonlisäveroviranomaiset

|                              |                                              |
|------------------------------|----------------------------------------------|
| Poiston syy       | Vähäinen käyttö ja rajoitetut toiminnot |
| Onko toinen ominaisuus korvannut? | Ei                                           |
| Vaikutuksen alaiset moduulit             | Yhdysvaltojen arvonlisävero                                 |

### <a name="shipping-carrier-interface"></a>Rahdinkuljettajan liittymä

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Sama toiminto                                                                                                                         |
| Onko toinen ominaisuus korvannut? | Kyllä. Kuljetustenhallinta korvaa tämän toiminnon osittain, mutta perusvarastonhallinta (WMS I) ei ole vielä korvannut. |
| Vaikutuksen alaiset moduulit             | Myynti ja markkinointi, inventoinnin- ja varastonhallinta                                                                                                       |

### <a name="sites-services"></a>Sites Services -palvelut

Sites Services -palveluiden avulla voit luoda sivustoja, jotka laajentavat liiketoimintaprosesseja Internetiin.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Dynamics AX:n käyttämässä Microsoft Azuren infrastruktuurissa on uusia korvaavia ominaisuuksia (esimerkiksi Azure-sivustot). |
| Onko toinen ominaisuus korvannut? | Ei                                                                                                                                       |
| Vaikutuksen alaiset moduulit             | Henkilön työhönotto, Palvelupyynnön hallinta, Tarjouspyynnöt, Toimittajan rekisteröinti                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS – kysynnän ennustestrategia

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| Poiston syy       | Uusi pilviarkkitehtuuri ei voi tukea toiminnon rakennetta. |
| Onko toinen ominaisuus korvannut? | Azure Machine Learningin kysynnän ennusteen strategia                           |
| Vaikutuksen alaiset moduulit             | Suunnittelu                                                                     |

### <a name="travel-requisitions"></a>Matkahankinnat

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Poiston syy       | Vähäinen käyttö ja suurin osa toiminnoista oli yritysportaalissa. |
| Onko toinen ominaisuus korvannut? | Ei                                                              |
| Vaikutuksen alaiset moduulit             | Matkalaskut                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Toimittajan laskupooli, ei sisällä kirjaustietoja

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| Poiston syy       | Vähäinen käyttö. Toiminto on korvattu laskun kirjauskansiolla, joka sisältää työnkulkutoiminnon. |
| Onko toinen ominaisuus korvannut? | Laskun kirjauskansion työnkulkutoiminnot                                                           |
| Vaikutuksen alaiset moduulit             | Ostoreskontra                                                                                        |

### <a name="virtual-company-accounts"></a>Virtuaaliyritykset

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

### <a name="warehouse-management-ii"></a>Varastonhallinta II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | **Inventoinnin- ja varastonhallintamoduuliin** sisältynyt Varastonhallinta II -ratkaisu (WMS II) oli Microsoft Dynamics AX 2012 R3:ssa julkaistun **varastonhallintamoduulin** toiminnon kaksoiskappale.                                                                         |
| Onko toinen ominaisuus korvannut? | AX 2012 R3:ssa, Microsoft Dynamics AX 2012 R3 CU8:ssa ja Microsoft Dynamics AX 2012 R3 CU9:ssa julkaistu **varastonhallintamoduuli** korvaa Varastonhallinta II:n ominaisuudet. Uudessa moduulissa on kehittyneemmät ominaisuudet ja joustavammat varaston hallintaprosessit kuin Varastonhallinta II:ssa. |
| Vaikutuksen alaiset moduulit             | Varaston hallinta, myynti ja markkinointi, hankinta                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Henkilöstöhallinnon työntekijän muistutukset

Henkilöstöhallinnon palkanlaskentatiedot

|                              |                 |
|------------------------------|-----------------|
| Poiston syy       | Vähäinen käyttö       |
| Onko toinen ominaisuus korvannut? | Ei              |
| Vaikutuksen alaiset moduulit             | Henkilöstö |

### <a name="workplanner"></a>Työn suunnittelu

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Poiston syy       | Vähäinen käyttö                                                                                                                                                            |
| Onko toinen ominaisuus korvannut? | Ei, mutta **Profiilirelaatio**-sivu, joka avautuu **Profiiliryhmät**-sivulta, tukee samoja liiketoimintaskenaarioita mitä vanhentuneella **Työn suunnittelu**-sivulla käytettiin. |
| Vaikutuksen alaiset moduulit             | Työajan seuranta                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++-raportit

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| Poiston syy       | Toinen ominaisuus on korvannut tämän toiminnon.                                    |
| Onko toinen ominaisuus korvannut? | Management Reporter (Dynamics AX:n nykyisessä versiossa sen nimi on **Talousraportointi**) |
| Vaikutuksen alaiset moduulit             | Kirjanpito                                                                              |


