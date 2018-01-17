---
title: Vanhentuneet ominaisuudet
description: "Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan."
author: sericks007
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: addd8c62ba034b47d8abbec29fa8682deb9698b1
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---

# <a name="removed-or-deprecated-features"></a>Poistetut tai vanhentuneet ominaisuudet

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu Microsoft Dynamics 365 for Finance and Operations Enterprise editionissa tai jotka ovat vanhentuneet.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

> [!Note]
> Dynamics 365 for Finance and Operations, Enterprise editionin heinäkuun 2017 ympäristöpäivityksestä 8 alkaen kunkin poistetun tai vanhentuneen ominaisuuden käyttöottotyyppi ilmoitetaan. Kaikki tässä aiheessa mainitut aiemmat versiot tukivat vain pilvikäyttöönottoja.

## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Dynamics 365 for Finance and Operations, Enterprise edition 7.3 ja ympäristöpäivitys 12

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Sähköisen raportoinnin (ER) toimintoluettelon laajennus
Mahdollisuutta käyttää mukautettuja toimintoja ER-lausekkeenmuodostimessa ei tueta enää. (Lisätietoja on kohdassa [Sähköisen raportoinnin toimintoluettelon laajentaminen](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md).) Sähköisen raportoinnin ohjelmointirajapintojen muutosten vuoksi, ohjelmointirajapinnan sisäisten toimintojen kutsuminen ER-lausekkeenmuodostimesta muuttui sisäiseksi eikä sitä voi enää laajentaa.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Koodin sulkemisaloite  |
| **Onko toinen ominaisuus korvannut?**   | Ei mitään. Aina kun uutta sisäistä tarvitaan, uusi laajennuspyyntö on osoitettava ER-kehikkotiimille.<br><br>ER-tiimi kehittää pyydettyä toimintoa, mutta ongelman voi väliaikaisesti välttää ohjelmoimalla tarvittavan logiikan mukautetun sovellusluokan menetelmänä. Tätä menetelmää voi käyttää ER-lausekkeessa mukautettuun sovellusluokkaan viittaavan **Sovellus\luokka**-tyypin lisätyn ER-tietolähteen ominaisuutena.  |
| **Tuotealueet, joihin vaikutetaan**         | Sähköisen raportoinnin kehikko                                                      |
| **Käytön asetukset**              | Kaikki                                                                                      |
| **Tila**                         | Poistettu versiosta Dynamics 365 for Finance and Operations, Enterprise edition 7.3 alkaen    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Erääntymisraportti varastoryhmittäin ja Erääntymisraportti varastodimensioittain

Finance and Operations ei enää tue raporttia. Asiakaskokemusta voi sen sijaan parantaa **Varaston erääntyminen** -raportin avulla.

|   |  |
|--------------|-----------------------|
| **Poiston syy**       | Sama toiminto  |
| **Onko toinen ominaisuus korvannut?** | Kyllä. Kaksi raporttia on korvattu **Varaston erääntyminen** -raportilla.     |
| **Tuotealueet, joihin vaikutetaan**       | Varastonhallinta, kustannushintojen hallinta        |
| **Käytön asetukset**        | Kaikki|
| **Tila**                       | Vanhentunut: kahden raportin valikkovaihtoehdot on poistettu versiossa 7.3. Raporttien koodi on kuitenkin edelleen tuotteessa. Koodi on tarkoitus poistaa tulevissa versioissa. |

### <a name="power-bi-content-packs-published-to-powerbicom"></a>PowerBI.comiin julkaistut Power BI -sisältöpaketit
PowerBI.com-sivustoon julkaistut **Kustannushintojen hallinta**-, **Taloudellinen suorituskyky**- ja **Vähittäismyyntikanavan suorituskyky** -sisältöpaketit ovat vanhentuneet Microsoft Power BI:n tuotepäivitysten vuoksi. Myös järjestelmän hallintalomakkeet, joilla nämä sisältöpaketit otetaan käyttöön Pack PowerBI.comissa, ovat vanhentumassa Finance and Operationsissa.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Microsoft Power BI:n tuotepäivitykset. |
| **Onko toinen ominaisuus korvannut?**   | Power BI -sisältöpaketit (julkaistu PowerBI.comiin) ollaan korvaamassa analyysisovelluksilla, joilla ratkaisuja voi integroida tietokantatasolla. Lisätietoja analyysisovelluksista on kohdassa [Embedded Power BI työtiloissa](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Tuotealueet, joihin vaikutetaan**         | Kustannushintojen hallinta, myyntitiedot ja vähittäismyynti                                                                                               |
| **Käytön asetukset**              | Vain pilvipalvelut (PowerBI.com-integraatiota ei tueta paikallisissa käyttöönotoissa).                                                                                                            |
| **Tila**                         | Vanhentunut: toiminnon poiston tavoiteajankohta on vuoden 2018 2. vuosineljännes.    |

### <a name="standard-ui-in-data-management-workspace"></a>Tietojen hallinnan työtilan vakiokäyttöliittymä

Tietojen hallinnan vakiokäyttöliittämä on käyttöliittymä, jonka käyttäjät oletusarvoisesti näkevät, kun he ovat tietojen hallinnan työtilassa.

|   |  |
|------------------|-------------------------|
| **Poiston tai vanhentumisen syy** | Panostus tehdään uuden käyttöliittymän uusiin asiakaskokemuksiin.             |
| **Onko toinen ominaisuus korvannut?**   | Uusi *laajennetuiksi näkymiksi* kutsuttu käyttöliittymä korvaa vanhan käyttöliittymän.            |
| **Tuotealueet, joihin vaikutetaan**         | Tietojen hallinnan työtila                                                     |
| **Käytön asetukset**              | Kaikki                                                                           |
| **Tila**                         | Vanhentunut: toiminnon poiston tavoiteajankohta on vuoden 2018 1. vuosineljännes. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Valmistevero, arvonlisävero, Intian palveluvero

Nämä verot on sisällytetty Intian GST-veroon.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Poiston tai vanhentumisen syy**       | Nämä verot on sisällytetty Intian GST-veroon.                          |
| **Onko toinen ominaisuus korvannut?**            | Intian GST-vero                                                              |
| **Tuotealueet, joihin vaikutetaan**                  | Vero                                                                     |
| **Käytön asetukset**                       | Kaikki moduulit                                                   |
| **Tila**                                  | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |    

### <a name="file-validation-utility-fvu-for-india"></a>Intian tiedoston tarkistuksen apuohjelma (FVU)

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Poiston tai vanhentumisen syy**       | Toimintoa ei käytetty                                                  |
| **Onko toinen ominaisuus korvannut?**            | En                                                                      |
| **Tuotealueet, joihin vaikutetaan**                  | Intian ennakonpidätys                                                  |
| **Käytön asetukset**                       | Kaikki moduulit                                                                    |
| **Tila**                                  | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.   |        

### <a name="tdstcs-certificate-for-india"></a>Intian TDS/TCS-varmenne

Käyttäjät voivat ladata tämän julkishallinnon portaalista.

|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Poiston tai vanhentumisen syy**       | Toimintoa ei käytetty                                                  |
| **Onko toinen ominaisuus korvannut?**            | En                                                                      |
| **Tuotealueet, joihin vaikutetaan**                  | Intian ennakonpidätys                                                  |
| **Käytön asetukset**                       | Kaikki moduulit                                                                   |
| **Tila**                                  | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Intian tuonnin ja viennin kannustinmalli (EXIM)


|                                             |                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Poiston tai vanhentumisen syy**       | Toimintoa ei käytetty                                                  |
| **Onko toinen ominaisuus korvannut?**            | En                                                                      |
| **Tuotealueet, joihin vaikutetaan**                  | Tuo ja vie                                                       |
| **Käytön asetukset**                       | Kaikki moduulit                                                                    |
| **Tila**                                  | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.  |    



## <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Dynamics 365 for Finance and Operations, Enterprise edition heinäkuu 2017 ja ympäristöpäivitys 8

### <a name="warehouse-mobile-devices-portal"></a>Varaston mobiililaiteportaali

Varaston mobiililaiteportaali (WMDP) oli erillinen osa, joka oli tarkoitettu paikallisesti tapahtumaan itsenäiseen käyttöönottoon. Finance and Operations ei enää tue tätä osaa. Alkuperäinen, käyttäjäkokemusta parantava sovellus, on korvannut WMDP-toiminnot.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Sama toiminto.       |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Finance and Operations – varastointi on korvannut tämän ominaisuuden. Lisätietoja asennuksesta ja ennakkoedellytyksistä on ohjeaiheessa [Microsoft Dynamics 365 for Finance and Operationsin varastointisovelluksen asentaminen ja määrittäminen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/install-configure-warehousing-app). |
| **Tuotealueet, joihin vaikutetaan**         | Varaston hallinta, kuljetusten hallinta     |
| **Käytön asetukset**              | Varaston mobiililaiteportaali (WMDP) oli erillinen osa, joka oli tarkoitettu paikallisesti tapahtumaan itsenäiseen käyttöönottoon.               |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Pankkitilin täsmäytyksen lisätoimintojen manuaalisen täsmäytyksen täsmäytyssääntö

Täsmäytyssäännöllä valittiin ja merkittiin pankkitosite, kun asiakirjat täsmäytettiin manuaalisesti täsmäytyslaskentataulukossa.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Rajoitettu käyttö.                                                                         |
| **Onko toinen ominaisuus korvannut?**   | Nro Täsmäytettäviä asiakirjoja etsitään sarakkeen suodatusominaisuuksilla. |
| **Tuotealueet, joihin vaikutetaan**         | Maksuliikenteen hallinta                                                               |
| **Käytön asetukset**              | Kaikki                                                                                    |
| **Tila**                         | Poistettu heinäkuusta 2017 alkaen.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 ja ympäristöpäivitys 3

### <a name="aeb-payment-formats-for-spain"></a>Espanjan AEB-maksumuodot

Consejo Superior Bancario -maksumuotoja käytettiin maksusuoritustiedostojen lähettämiseen pankkiin asiakkaan maksuja ja toimittajamaksuja varten. Muotojen sisällön määritti Asociación Española de Banca. Siihen sisältyy Cuaderno 19, 32, 58, 34.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Maksumuotoja ei enää käytetä.                                  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, Espanjan ISO20022-tilisiirto ja suoraveloituksen maksumuoto |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra, ostoreskontra                                    |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Liettuan pankkiohjelmamaksujen siirto

Pankkiohjelmamaksujen siirrot luotiin ja tulostettiin Liettuan maksunsiirron (LT) vientimuodon avulla. Liettuan markkina-alue aloitti LITASin, yhdistetyn sähköisen pankkijärjestelmän, käytön vuonna 2005.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Maksumuotoja ei enää käytetä.                        |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, Liettuan ISO20022-tilisiirron maksumuoto     |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra                                               |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Norjan BBS Direkte Remittering -maksumuodot

BBS Direkte Remittering -maksumuotoja ovat asiakkaan maksun perittävän vienti (suoraveloitus) ja palautussanoman tuonti.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Maksumuotoja ei enää käytetä.  |
| **Onko toinen ominaisuus korvannut?**   | Norjan AvtaleGiro- asiakkaan maksumuotoa voidaan käyttää suoraveloituksen sanomien luomiseen. Palautussanoman tuominen toteutetaan tulevissa versioissa. |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra, ostoreskontra   |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Espanjan tilikartta-työkalu

Tätä työkalua käytetään, kun Espanjan tilikartta edellyttää suuria muutoksia. Käyttäjä voi tuoda uuden tilikartan Microsoft Excel- tai tekstimuodossa ja tuoda myös raportteja.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Rajoitettu käyttö                                                  |
| **Onko toinen ominaisuus korvannut?**   | En                                                             |
| **Tuotealueet, joihin vaikutetaan**         | Kirjanpito                                                 |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="dom80-payment-format-for-belgium"></a>Belgian Dom80-maksumuoto

Vanha Belgian maksukehotuksen maksumuoto (suoraveloitus).

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tätä maksumuotoa ei enää käytetä.                          |
| **Onko toinen ominaisuus korvannut?**   | Kyllä Belgian SO 20022 -suoraveloituksen maksumuoto         |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra                                            |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>Sveitsin DTA/EZAG-maksumuodot

DTA/EZAG-muodot integroidaan ESR-järjestelmään, koska niissä voidaan käsitellä viitenumeroa. Koska viitenumero ei ole pakollinen, näitä muotoja voidaan käyttää kaikkien toimittajamaksujen käsittelyssä. Muotoja käytetään yrityksissä, joissa on pankkitili muussa kuin "Postfinance"-sijainnissa.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Maksumuotoja ei enää käytetä.                        |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, Sveitsin ISO20022-tilisiirron maksumuoto   |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra                                               |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>Itävallan ISOEDIFACT-DIRDEB-suoraveloituksen maksumuoto

Maksukehotuksen EDIFACT-DIRDEB-maksumuoto (suoraveloitus).

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tätä maksumuotoa ei enää käytetä.                          |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, Itävallan ISO 20022 -suoraveloituksen maksumuoto         |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra                                            |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="edivat-for-belgium"></a>Belgian EDIVAT

EDIVAT on Belgian vanhentunut standardi sähköiselle ilmoitukselle suojatun sähköpostin kautta. Microsoft Dynamics AX 2012 säilyttää vain luku -ratkaisun historiallisten tietojen käyttämiseksi.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tätä toimintoa ei enää käytetä.                           |
| **Onko toinen ominaisuus korvannut?**   | En                                                             |
| **Tuotealueet, joihin vaikutetaan**         | Kirjanpito                                                 |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>Norjan eGiro EDIFACT CREMUL- maksun tuontimuoto

eGiro perustuu YK:n kansainväliseen EDIFACT CREMUL (Multiple Credit Advice Message) -standardiin, jota käytetään asiakasmaksujen automaattisessa kirjauksessa. eGiro on Microsoft Dynamics AX:ssä toteutettu asiakkaan maksun tuontimuoto.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tätä maksumuotoa ei enää käytetä.                                                     |
| **Onko toinen ominaisuus korvannut?**   | Nro Muoto korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra                                                                       |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.                            |

### <a name="external-inventory-for-poland"></a>Puolan ulkoinen varasto

Tavaroiden tunnistetiedot, jotka saadaan toimittajan myynnistä ilman ostoa. Ulkoisessa varastossa käsitellyt tavarat eivät vaikuta vakiovarastoon ja ne voidaan myydä ja ostaa automaattisesti. Tämä prosessi luo todelliset varastosiirrot.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvattu toisella toiminnolla                                    |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, saapuvan tavaralähetyksen perustoiminnot                |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra, varastonhallinta                         |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Itä-Euroopan raportin muodostustoiminto

Työkalua käytetään tiedonkeruun määritykseen kirjanpitoa ja veroraportteja varten sekä tietojen viemiseksi XLS- ja DOC- raporttimalleihin.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Rajoitettu käyttö                                                                            |
| **Onko toinen ominaisuus korvannut?**   | Nro Työkalu korvataan sähköiset raportoinnin konfiguraatioilla tulevissa julkaisuversioissa. |
| **Tuotealueet, joihin vaikutetaan**         | Kirjanpito                                                                           |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Suomen asiakasmaksutapahtumien tuominen

Voit valita Suomen maksujen tuontimuodon asiakasmaksutapahtumien tuomiselle pankin antamasta ulkoisesta tiedostosta.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tätä maksumuotoa ei enää käytetä.                                                     |
| **Onko toinen ominaisuus korvannut?**   | Nro Muoto korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra                                                                       |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Suomen maksutapahtumien tuominen kirjanpidon kirjauskansioon

Suomen erityismuotoa käytetään kirjanpidon tapahtumien tuomiseksi kirjanpitoon.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tätä maksumuotoa ei enää käytetä.                                                     |
| **Onko toinen ominaisuus korvannut?**   | Nro Muoto korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra                                                                       |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Belgian Isabel-synkronoitu integrointi (CIS)

Isabel on Euroopan sähköisen maksuliikenteen ja tiedonsiirron yleinen standardi Belgiassa.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Integrointi Isabel-asiakasohjelmaan on lopetettu.   |
| **Onko toinen ominaisuus korvannut?**   | Nro Maksumuodot, joita ei voi enää käyttää, korvataan ISO20022-tilisiirron maksumuodolla Belgiassa. |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra     |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Espanjan tilikartan ja kirjanpitosääntöjen muutokset

Tätä toimintoa käytetään Espanjan tilikartan ja kirjanpitosääntöjen muutoksiin. Se yhdistää tilejä ja auttaa vanhan tilikartan muuttamisessa uudeksi tilikartaksi ja vertaa edellistä tilikautta uuteen tilikauteen, vaikka ne on kirjattu eri tilinumeroille.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Rajoitettu käyttö                                                  |
| **Onko toinen ominaisuus korvannut?**   | En                                                             |
| **Tuotealueet, joihin vaikutetaan**         | Kirjanpito                                                 |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Toimittajan Pagamento Fornittori -maksumuoto

Vanha Italian tilisiirron maksumuoto.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tätä maksumuotoa ei enää käytetä.                          |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, Italian ISO20022-tilisiirron maksumuoto         |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra                                               |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="payment-export-formats-for-estonia"></a>Viron maksun vientimuodot

Pankin maksun viennissä käytetään Telehansa- ja Teleservice-muotoja.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Maksumuotoja ei enää käytetä.                        |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, Viron ISO20022-tilisiirron maksumuoto       |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra                                               |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="payment-file-archive-for-norway"></a>Norjan maksutiedostoarkisto

Kun maksutiedostot on luotu, tiedostoarkistoon arkistoidaan kaikki luodut tiedostot, vaikka tiedostot on aiemmin kirjoitettu tai luettu.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvattu toisella toiminnolla                                        |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, sähköisen raportoinnin arkistoidut työt                            |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra, myyntireskontra, organisaation hallinto |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.     |

### <a name="payment-import-formats-for-estonia"></a>Viron maksun tuontimuodot

Pankin maksun tuonnissa käytetään Telehansa- ja TeleTeenus-muotoja.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Maksumuotoja ei enää käytetä.                                                    |
| **Onko toinen ominaisuus korvannut?**   | Nro Muodot korvataan ISO 20022- tiliotteen tuontimuodoilla tulevissa versioissa. |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra                                                                        |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.                             |

### <a name="payroll-information-in-human-resources"></a>Henkilöstöhallinnon palkanlaskentatiedot

Henkilöstöhallinnon palkanlaskentatiedot

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Palkanlaskennan ja Henkilöstöhallinnan perussivut ovat korvanneet tämän ominaisuuden.  |
| **Onko toinen ominaisuus korvannut?**   | **Edut**, **Ansiot** ja muut liittyvät Yhdysvaltojen palkanlaskenta -kohdassa olleet sivut on määritetty uudelleen ja sisältyvät nyt henkilöstöhallinnon perusmäärityksiin. Tämä auttaa tukemaan ulkoista palkanlaskennan käsittelyä. Toimintoa käytetään valitsemalla **Henkilöstöhallinta 1** \> **Palkanlaskenta**-määritysavain. |
| **Tuotealueet, joihin vaikutetaan**         | Henkilöstöhallinto, palkanlaskenta   |
| **Tila**                         | Poistettu versiosta Dynamics 365 for Operations 1611 alkaen.    |

### <a name="performance-management-goal-workflow"></a>Suorituskyvyn hallintatavoite -työnkulku

Suorituskyvyn hallinta sisältää tavoitteiden hallinnan ja integroinnin suorituskykyarvioiden kanssa.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Suorituskyvyn hallinta on suunniteltu uudelleen ja tavoitesivujen lukumäärää vähennettiin prosessin yksinkertaistamiseksi.                 |
| **Onko toinen ominaisuus korvannut?**   | Nro Tavoitteet näkyvät esimiehille esimiehen itsepalveluportaalin kautta, ja esimies voi muuttaa ja tarkastella niitä. |
| **Tuotealueet, joihin vaikutetaan**         | Henkilöstöresurssien hallinta       |
| **Tila**                         | Poistettu versiosta Dynamics 365 for Operations 1611 alkaen.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Ruotsin Postgirot- ja Postgirot Utland -maksumuodot

Ruotsin Postgirot- ja Postgirot Utland -maksumuodot.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Maksumuotoja ei enää käytetä.                        |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, Ruotsin ISO20022-tilisiirron maksumuoto        |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra                                               |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="radio-frequency-identifier"></a>Radiotaajuinen etätunnistus

Radiotaajuinen etätunnistus (RFID) on tiedonkeräysmenetelmä, jossa käytetään tunnistetietojen tallentamiseen sähköisiä tunnisteita, ja tunnistetiedot luetaan ilman näköyhteyttä.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Vähäinen käyttö ja rajoitetut toiminnot.   |
| **Onko toinen ominaisuus korvannut?**   | En                                              |
| **Tuotealueet, joihin vaikutetaan**         | Varastoinninhallinta                            |
| **Tila**                         | Poistettu versiosta Dynamics 365 for Operations 1611 alkaen. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Latvian valtion määrittämän laskujen numeroinnin raportti

Latvian lainsäädäntö sisältää myyntilaskujen numerointia koskevia erityissääntöjä. Toiminnon avulla voidaan määrittää erityiset numerot myyntilaskuille käyttäjän tai käyttäjäryhmän mukaan. Tämän jälkeen voit luoda raportin tai XML-tiedoston. Voit myös tulostaa raportin käytetyistä laskunumeroista.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Valtion määrittämää laskujen numerointia ei tarvitse enää ylläpitää. Käytettyjen laskunumeroiden raporttia ei enää vaadita. |
| **Onko toinen ominaisuus korvannut?**   | En       |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra    |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Liettuaa koskevat johtajan ja kirjanpitäjän nimien asetukset

Yrityksen johtajan ja kirjanpitäjän nimet voidaan määrittää yrityksen tietoihin ja käyttää paikallisten raporttien tulostuksessa.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Korvattu toisella toiminnolla                                     |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, viranomaisten asetuksia käytetään samaan tarkoitukseen.   |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra, myyntireskontra, maksuliikenteen hallinta |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.  |

### <a name="shipping-carrier-interface"></a>Rahdinkuljettajan liittymä

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Sama toiminto   |
| **Onko toinen ominaisuus korvannut?**   | Kuljetuksenhallinta korvaa osittain |
| **Tuotealueet, joihin vaikutetaan**         | Myynti ja markkinointi, inventoinnin- ja varastonhallinta  |
| **Tila**                         | Poistettu versiosta Dynamics 365 for Operations 1611 alkaen.  |

### <a name="telepay-payment-formats-for-norway"></a>Norjan Telepay-maksumuodot

Telepay-maksumuodot sisältävät toimittajan maksun viennin (tilisiirrolla) ja asiakkaan maksukehotuksen (suoraveloitus).

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Maksumuotoja ei enää käytetä.                                                        |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, Norjan ISO20022-tilisiirron maksumuoto ja asiakkaan maksun AvtaleGiro-muoto |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra, ostoreskontra                                                          |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Suomen toimittajan maksun vientimuodot

Kaksi eri muotoa maksujen vientiä varten käytettävissä Suomessa. LM02 (FI) käytetään kotimaan maksuille ja LUM2 (FI) ulkomaanmaksuille.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Maksumuotoja ei enää käytetä.                        |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, Suomen ISO20022-tilisiirron maksumuoto       |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra                                               |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="warehouse-management-ii"></a>Varastonhallinta II

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | **Inventoinnin- ja varastonhallintamoduuliin** sisältynyt Varastonhallinta II -ratkaisu (WMS II) oli Microsoft Dynamics AX 2012 R3:ssa julkaistun **varastonhallintamoduulin** toiminnon kaksoiskappale.                                                                         |
| **Onko toinen ominaisuus korvannut?**   | AX 2012 R3:ssa, Microsoft Dynamics AX 2012 R3 CU8:ssa ja Microsoft Dynamics AX 2012 R3 CU9:ssa julkaistu **varastonhallintamoduuli** korvaa Varastonhallinta II:n ominaisuudet. Uudessa moduulissa on kehittyneemmät ominaisuudet ja joustavammat varaston hallintaprosessit kuin Varastonhallinta II:ssa. |
| **Tuotealueet, joihin vaikutetaan**         | Varaston hallinta, myynti ja markkinointi, hankinta   |
| **Tila**                         | Poistettu versiosta Dynamics 365 for Operations 1611 alkaen.    |

### <a name="worker-reminders-in-human-resources"></a>Henkilöstöhallinnon työntekijän muistutukset

Henkilöstöhallinnon palkanlaskentatiedot

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Vähäinen käyttö                                                           |
| **Onko toinen ominaisuus korvannut?**   | En                                                                  |
| **Tuotealueet, joihin vaikutetaan**         | Henkilöstöhallinto                                                     |
| **Tila**                         | Poistettu versiosta Dynamics 365 for Operations 1611 alkaen |

### <a name="workflow-for-creating-goals"></a>Tavoitteiden luomisen työnkulku

Työntekijöiden tavoitteiden luomisen työnkulku on yksi monista työnkuluista, joita oli käytettävissä suorituskyvyn hallintaprosessin koordinoinnin apuna.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Suorituskyvyn hallinta on suunniteltu kokonaan uudelleen Microsoft Dynamics 365 for Finance and Operationsissa.     |
| **Onko toinen ominaisuus korvannut?**   | Uudelleen suunnitellulla suorituskyvyn hallintatoiminnolla voidaan seurata tarkemmin tavoitteiden sisältöä ja mittauksia, joiden avulla voidaan seurata etenemistä, sekä tukidokumentaation liittämistä. Tavoitteet voidaan tallentaa malleina ja käyttää uudelleen. Tämän toiminnon avulla voit määrittää lisätavoitteita työntekijöille entistä nopeammin. |
| **Tuotealueet, joihin vaikutetaan**         | Henkilöstöresurssien hallinta                 |
| **Tila**                         | Poistettu versiosta Dynamics 365 for Operations 1611 alkaen. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Mahdollisuus peruuttaa toimittajan laskun muutokset

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Suorituskyvyn parannus        |
| **Onko toinen ominaisuus korvannut?**   | En                             |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra               |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF-, AxD- ja AxBC-integraatiot

Application Integration Frameworkissä (AIF) tietoja voidaan vaihtaa ulkoisten järjestelmien kanssa palveluina näyttäytyvänä liiketoimintalogiikkana. Dynamics AX sisältää asiakirjoihin ja .NET Business Connectoriin (AxBC) perustuvia palveluja. Asiakirja luodaan XML-muotoisena. XML sisältää otsikkotiedot, joka lisäämällä luodaan *sanoma*, joka siirretään Dynamics AX:ään ja siitä pois. Asiakirjoja ovat esimerkiksi myynti- ja ostotilaukset. Käytännössä kuitenkin lähes mikä tahansa yksikkö, kuten asiakas, voidaan ilmaista asiakirjana. Asiakirjoihin perustuvat palvelut käyttävät **Axd\<asiakirja\>**-luokkia.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | AIF:n ja AxDs:n arkkitehtuuria ei voi skaalata pilvipalveluun. Joukkotuontiin liittyi suorituskykyongelmia.                                        |
| **Onko toinen ominaisuus korvannut?**   | Tämä ominaisuus on korvattu tietojen tuonti- ja vientiympäristöllä, joka tukee toistuvaa joukkotuontia ja -vientiä. AxBC:ssä on suositeltavaa käyttää varsinaisia tauluja. |
| **Tuotealueet, joihin vaikutetaan**         | AxDs, AxBCs ja AIF   |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.   |

### <a name="boms-without-bom-versions"></a>Tuoterakenteet ilman tuoterakenneversioita

Kun **Tuoterakenneversiot**-määritysavain poistettiin käytöstä, tuoterakenneversiot piilotettiin kaikissa lomakkeissa ja järjestelmä pakotti 1:1-suhteen vapautettujen tuotteiden ja tuoterakenteiden välille. **Tuoterakenneversiot**-määritysavainta ei voi poistaa Dynamics AX:n nykyisessä versiossa.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tuoterakenneversioiden ohjaamista määritysavaimella ei voi skaalata pilviympäristöön. |
| **Onko toinen ominaisuus korvannut?**   | En                                                                                      |
| **Tuotealueet, joihin vaikutetaan**         | Tuotetietojen hallinta, inventoinnin- ja varastonhallinta                                    |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.                                                          |

### <a name="brazilian-bordero"></a>Brasilian Bordero

Erityismaksutapa Brasilian yrityksille

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Brasilian Bordero-maksutavan tuki on lopetettu Brasilian lokalisointiversiosta |
| **Onko toinen ominaisuus korvannut?**   | En   |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra   |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="brazilian-sintegra-statement"></a>Brasilian Sintegra-raportti

Liittovaltion veroraportti ICMS-verolle

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tämä raportti ei ole enää käytettävissä joissain Brasilian osavaltioissa. |
| **Onko toinen ominaisuus korvannut?**   | Nro Käyttäjät voivat käyttää yleistä sähköistä raportointityökalua raportin määrittämiseen, jos se on pakollinen erityistilanteissa. |
| **Tuotealueet, joihin vaikutetaan**         | Verokirjat    |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasilian NF-e:n SCAN-varatila

(SCAN) varaympäristöä käytetään Nota Fiscal eletrônica (NF e) -tilan luontiin, vientiin ja tuontiin, kun Secretaria da Fazenda (SEFAZ) -ympäristö ei ole käytettävissä.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tämä varamenetelmä ei ole enää käytettävissä kaikissa Brasilian osavaltioissa |
| **Onko toinen ominaisuus korvannut?**   | En                                                                          |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra                                                         |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.              |

### <a name="business-analyzer"></a>Business Analyzer

Käyttäjät voivat tarkastella tällä mobiilisovelluksella tärkeitä liiketoiminnan mittareita.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Toinen ominaisuus on korvannut tämän toiminnon.   |
| **Onko toinen ominaisuus korvannut?**   | Microsoft PowerBI:n taloudellisen suorituskyvyn seurannan sisältöpaketti sisältää tärkeät taloudelliset mittarit, jotka sisältyivät aiemmin Business Analyzeriin. |
| **Tuotealueet, joihin vaikutetaan**         | Kirjanpito      |
| **Tila**                         | Vanhentunut: Business Analyzerin käyttö on vanhentunut.    |

### <a name="business-statistics"></a>Liiketoimintatilastot

Niiden liiketoiminnan tilastotietokyselyiden asetukset, jotka voivat auttaa organisaation suorituskyvyn analysoinnissa

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Vanha tapa käsitellä liiketoiminnan tietoja (BI), vähäinen käyttö ja rajalliset ominaisuudet |
| **Onko toinen ominaisuus korvannut?**   | Uudet BI-ratkaisut Dynamics AX:n nykyisessä versiossa                                      |
| **Tuotealueet, joihin vaikutetaan**         | Hankinta, ostoreskontra, myynti ja markkinointi, myyntireskontra         |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Hyväksyttyjen laskujen kirjauskansion tiedoston päivämäärän muutostoiminto

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Vähäinen käyttö                                                               |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Kirjatun toimittajatapahtuman tiedoston päivämäärää voidaan muuttaa. |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra                                                        |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Alankomaiden ClieOp03-maksumuoto

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Muotoa ei enää käytetä Alankomaissa, sillä SEPA-toiminto on korvannut sen. |
| **Onko toinen ominaisuus korvannut?**   | SEPA-maksujen vienti  |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit     |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.   |

### <a name="compliance-center"></a>Compliance Center

Compliance Center oli Sarbanes-Oxley-lakiin liittyvien vaatimustenmukaisuusaloitteiden asiakirjavaatimusten hallintaan tarkoitettu yritysportaalisivusto.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Toimintoa ei käytetty. Microsoft SharePoint sisältää Compliance Centerin käytössä olleet ominaisuudet. |
| **Onko toinen ominaisuus korvannut?**   | En   |
| **Tuotealueet, joihin vaikutetaan**         | Yhteensopivuus ja sisäinen valvonta  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.    |

### <a name="connector-for-microsoft-dynamics"></a>Microsoft Dynamicsin yhdistin

Tällä työkalulla integroitiin Microsoft Dynamics CRM:n tärkeitä tietoja Microsoft Dynamics ERP -sovelluksiin.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Toinen ominaisuus on korvannut tämän toiminnon. |
| **Onko toinen ominaisuus korvannut?**   | Common Data Service                                      |
| **Tuotealueet, joihin vaikutetaan**         | Microsoft Dynamicsin yhdistin                         |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Säilöyksikkö ja monidimensioinen varasto

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Sama toiminto |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. AX2012:n jälkeen tämä toiminto on korvattu konsolidoidulla erätilaustoiminnoilla. Tämä ominaisuusjoukko sisältää konsolidoidun varastonäkymän. |
| **Tuotealueet, joihin vaikutetaan**         | Tuotetietojen hallinta, tuotannonhallinta, varastonhallinta, myynti ja markkinointi  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen. |

### <a name="cue-group-metadata"></a>Pinoryhmän metatiedot

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Pinoryhmiä käytettiin näyttämään vähintään yksi pino tietoruutualueella. Toiminto oli rajallinen ja siihen liittyi suorituskykyongelmia, koska tietueen muuttuminen päälomakkeessa loi jokaiselle pinolle yhden kyselyn pinoryhmässä. |
| **Onko toinen ominaisuus korvannut?**   | En      |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit    |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.  |

### <a name="cue-metadata"></a>Pinon metatiedot

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Pinon metatiedot rajoittuivat määrä- tai summatietoihin.    |
| **Onko toinen ominaisuus korvannut?**   | Käyttöönotetut ruudun metatiedot mahdollistavat joustavamman mallinnuksen. Voit esimerkiksi mallintaa nykyiset määrät, siirtymisen ja suorituskykyilmaisimet (KPI:t). Määräruudun metatiedot korvaavat suoraan pinon metatiedot. |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit           |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen      |

### <a name="danish-check-format"></a>Tanskalainen sekkilomake

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tanskan sekkimuodon tuki on lopetettu ja raportti on poistettu tanskalaisesta lokalisoinnista. |
| **Onko toinen ominaisuus korvannut?**   | En    |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit    |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.  |

### <a name="data-partitions"></a>Tieto-osiot

Tieto-osiot erottavat Microsoft Dynamics AX:n tietokannan tiedot loogisesti.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tieto-osiot otettiin käyttöön Microsoft Dynamics AX 2012 R2:ssa tietojen eristämistä varten. Yleisessä skenaariossa yrityksellä on tytäryhtiöitä mutta tytäryhtiön tiedot eivät saisi olla toisen tytäryhtiön nähtävissä, vaikka kumpikin tytäryhtiö on saman IT-osaston alaisuudessa. Ohjelmassa oli kuitenkin otettava käyttöön ylimääräisiä komentosarjoja ja hallintakustannuksia, jotta uusia osioita voitaisiin luoda, tiedot voitaisiin lisätä ja osiotiedot voitaisiin varmuuskopioida. Pilvipalvelussa, jossa meillä on käyttöympäristövuokrattuja (PaaS-palvelu) tietokantapalveluja (Microsoft Azuren SQL-tietokanta), tietokantaa on tehokkaampaa käyttää erityssäilönä kuin tehdä eristys ohjelmassa. Riippumatta siitä, tarvitaanko tietojen osiointia tytäryhtiöitä tai useita vuokraajia varten tai koon vuoksi, skenaariot voidaan mielestämme käsitellä paremmin useissa Finance and Operations -esiintymissä. |
| **Onko toinen ominaisuus korvannut?**   | Tieto-osioita käyttävien asiakkaiden on käytettävä useita Finance and Operations -esiintymiä, jos tietokantatasoiden erottaminen on tärkeää.    |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Liitteiden tallennus tietokantaa ja jaettuun tiedostoresurssiin

Microsoft Dynamics AX 2012:ssa liitteet voitiin tallentaa tietokantaan ja jaettuihin tiedostoresursseihin. Kumpaakaan asetusta ei tueta enää.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tallennusta jaettuna tiedostoresurssina ei enää tueta, koska pilvipalveluympäristöt eivät voi viestiä paikallisten jaettujen tiedostoresurssien kanssa. Tietokantatallennus on vanhentunut Azure Blob -tallennuksen tieltä. Azure Blob -tallennus vastaa tietokantatallennusta, sillä asiakirjoja voi käyttää vain Dynamics 365 for Finance and Operations -asiakasohjelman lomakkeiden kautta. Lisäksi tällä tavoin saadaan tallennustila, joka ei heikennä tietokannan toimintaa. Blob-tallennus on asiakirjanhallinnan oletustallennusmekanismi ja toimii välittömästi. |
| **Onko toinen ominaisuus korvannut?**   | Tietokantatallennus on vanhentunut Azure Blob -tallennuksen tieltä.   |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.   |

### <a name="delimitation"></a>Rajoitus

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Toiminnolle ei ollut käyttöä. |
| **Onko toinen ominaisuus korvannut?**   | En                                     |
| **Tuotealueet, joihin vaikutetaan**         | Työajan seuranta                    |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.         |

### <a name="desktop-client"></a>Työpöytäasiakasohjelma

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Dynamics AX:n asiakasohjelmakokemus on uudistettu parantamaan käytettävyyttä kaikissa ympäristöissä ja laitteissa.                      |
| **Onko toinen ominaisuus korvannut?**   | Uusi verkkoasiakasohjelma perustuu työpöytälomakkeen metatietoihin ja ohjelmointimalliin, jota on muokattu luomaan monipuolinen verkkoympäristö. |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.   |

### <a name="direct-database-connection"></a>Suora tietokantayhteys

Dynamics AX 2012 R3 -versiossa Retail Modern POS -sovellus voi muodostaa suoran yhteyden kanavatietokantaan samalla tavalla, kuin Enterprise POS. Tämä oli lisänä Retail Modern POS -sovelluksen normaalille tietoliikenneyhteydelle, joka kulki vähittäismyynnin palvelimen välityksellä.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Suora tietokantayhteys edellytti matalamman suojauksen, ja sitä käytettiin pääasiassa korkeamman suorituskyvyn saavuttamiseen. Finance and Operationsissa tehtyjen suorituskyky- ja tietoturvaparannusten vuoksi tämä toiminnallisuus aiheuttaa enemmän ongelmia kuin mitä se ratkaisee. |
| **Onko toinen ominaisuus korvannut?**   | Nro Vain vakiomuotoinen vähittäismyynnin palvelinyhteys on enää tuettu.  |
| **Tuotealueet, joihin vaikutetaan**         | Kanavatietokanta/Retail Modern POS   |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.  |

### <a name="dutch-swift-mt940"></a>Alankomaiden SWIFT MT940

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Käytössä on nyt yleinen toiminto lokalisoidun toiminnon sijaan.                    |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Pankkitilin täsmäytyksen lisätoiminnot on korvannut tämän toiminnon. |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit                                                                              |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL Saksassa)

Tämä toiminto mahdollisti XBRL (eXtensible Business Reporting Language) -tulostuksen, joka on tarkoitettu erityisesti Saksan eBilanz-luokitusta varten.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Toimintoa ei käytetty  |
| **Onko toinen ominaisuus korvannut?**   | Toimintoa ei korvata toisella ominaisuudella, mutta Saksan markkinoilla on saatavana useista erikoistuneita XBRL-paketteja, joissa on monipuolisia XBRL-toimintoja. |
| **Tuotealueet, joihin vaikutetaan**         | Management Reporter      |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.  |

### <a name="enterprise-portal-client"></a>Yritysportaalin asiakasohjelma

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Käytössä on yksi asiakasohjelmaympäristö.  |
| **Onko toinen ominaisuus korvannut?**   | Uusi verkkoasiakasohjelma perustuu työpöytälomakkeen metatietoihin ja ohjelmointimalliin, jota on muokattu luomaan monipuolinen verkkoympäristö. |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.   |

### <a name="environmental-sustainability"></a>Ekologinen kestävyys

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Vähäinen käyttö ja rajoitetut toiminnot  |
| **Onko toinen ominaisuus korvannut?**   | En              |
| **Tuotealueet, joihin vaikutetaan**         | Yhteensopivuus ja sisäisen tarkistus, ostoreskontra  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen. |

### <a name="form-activex-and-managed-host-controls"></a>Lomakkeen ActiveX:n ja hallitun ylläpidon ohjausobjektit

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | ActiveX:n ja hallitun ylläpidon ohjausobjektit perustuivat vanhentuneeseen työpöytäasiakasohjelmaan. |
| **Onko toinen ominaisuus korvannut?**   | Laajennettava ohjausobjektiympäristö tukee uusien HTML-, CSS- ja JavaScript-pohjaisten ohjausobjektien luomista ja on ensimmäisen luokan ohjausobjekti Microsoft Visual Studio Tooling -ympäristössä. |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit     |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Esilaskujen muodostus erätoiminnolla

Vaikka esilaskua ei voi enää muodostaa erätoimintona, käyttäjä voi edelleen luoda esilaskun.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Erätoiminnolla luodulle laskulle ei ole lomaketta, jossa luotu esilaskutiedosto voitaisiin säilyttää ja näyttää. |
| **Onko toinen ominaisuus korvannut?**   | Esilaskuja voidaan luoda edelleen ja käyttäjä päättää sijainnin, johon tiedosto tallennetaan.   |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra, myyntireskontra, maksuliikenteen hallinta  |
| **Tila**                         | Poistettu versiosta AX 7.0 alkaen    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Saksan DTAUS-maksun vienti ja tiliotteen tuonti (kokonaissummat ja tapahtumat)

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Muotoa ei enää käytetä Saksassa, sillä SEPA (yhtenäinen euromaksualue) -toiminto on korvannut sen.                    |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. SEPA-maksun vienti ja pankkitilin täsmäytyksen lisätoiminnot tiliotteiden tuomiseen on korvannut tämän toiminnon. |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit  |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="german-dtazv-payment-format"></a>Saksan DTAZV-maksumuoto

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Muotoa ei enää käytetä Saksassa, sillä SEPA-toiminto on korvannut sen. |
| **Onko toinen ominaisuus korvannut?**   | SEPA-maksujen vienti    |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit   |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.    |

### <a name="german-mt940-import"></a>Saksassa tuominen MT940-muodossa

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Käytössä on nyt yleinen toiminto lokalisoidun toiminnon sijaan.                    |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Pankkitilin täsmäytyksen lisätoiminnot on korvannut tämän toiminnon. |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit                                                                              |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.                           |

### <a name="german-xml-eu-sales-list"></a>Saksan XML-muotoinen EU-myyntiluettelo

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | XML-muotoa Saksan EU:n arvonlisäveron yhteenvetoilmoitusta varten ei enää tueta. Saksan EU:n arvonlisäveron yhteenvetoilmoitus voidaan lähettää Saksan veroviranomaiselle ainoastaan ELMA5-tekstitiedostomuodossa. |
| **Onko toinen ominaisuus korvannut?**   | En         |
| **Tuotealueet, joihin vaikutetaan**         | Vero        |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.   |

### <a name="gl-ssrs-reports"></a>Kirjanpidon SSRS-raportit

Seuraavia valikkovaihtoehtoja sisältävät raportit on poistettu: **Pääkirjan yhteenveto**, **Yksityiskohtainen pääkirja**, **Tilikartta**, **Kirjausketju**, **Saldot** ja **Saldoluettelo**.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Microsoft SQL Server Reporting Services (SSRS) -raportit on korvattu Management Reporter -toiminnoilla ja oletusraporteilla. |
| **Onko toinen ominaisuus korvannut?**   | Management Reporter (Dynamics AX:n nykyisessä versiossa sen nimi on **Talousraportointi**)    |
| **Tuotealueet, joihin vaikutetaan**         | Kirjanpito   |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart- ja FormPart-metatiedot

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | InfoPart- ja FormPart-metatietojen avulla voitiin luoda kahden eri asiakasohjelman tietoruutuja. |
| **Onko toinen ominaisuus korvannut?**   | InfoPart-metatiedot oli yksinkertaistettu lomakemääritelmä, ja se on muunnettu lomakkeeksi päivitystyökaluilla. Lomakkeeseen viittaavat FormPart-metatiedot on korvattu suoralla viittauksella, joka luodaan päivitystyökaluilla. |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit    |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.        |

### <a name="main-account-list-page"></a>Päätilin luettelosivu

Luettelo yrityksen tileistä ja niihin liittyvät saldotiedot

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Saldotiedot ovat saatavilla tilin ja dimension mukaisella **Pääkirja**-luettelosivulla.  |
| **Onko toinen ominaisuus korvannut?**   | **Päätilit** sisältää saman tililuettelon kuin **Päätili**-luettelosivu. **Päätilit**-ruudukkonäkymä näyttää myös pienemmän ruudukkomaisen näkymän. |
| **Tuotealueet, joihin vaikutetaan**         | Kirjanpito      |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malesian ja Singaporen pankin kassavirtaraportti

Toiminnolla voitiin tulostaa kassavirtaraportti, joka sisältää valittujen pankkitilien saapuvien ja lähtevien kassavirtojen tapahtumat sekä tiedot määritetyltä päivämääräväliltä.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Samat tiedot saadaan pankkitapahtuman kyselyllä. |
| **Onko toinen ominaisuus korvannut?**   | Pankkitapahtuman kysely                                            |
| **Tuotealueet, joihin vaikutetaan**         | Maksuliikenteen hallinta                                                |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty.          |

### <a name="mexican-cfd-electronic-invoice"></a>Meksikon sähköinen CFD-lasku

Tällä ominaisuudella voitiin luoda Meksikossa sähköisiä laskuja käyttämällä CFD (Comprobante Fiscal Digital) -menetelmää, jossa yritys allekirjoittaa laskun pyytämällä liittyvän valtuutuksen viranomaiselta. Tämä ominaisuus tarjoaa myös kuukausiraportin, joka koostui kaikista kyseisen kuukauden aikana tehdyistä sähköisistä laskuista.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Menetelmää ei enää käytetä. Veroviranomaiset lopettivat CFD-menetelmällä luotavat sähköiset laskut ja niiden tilalla käytetään CFDI (Comprobante Fiscal Digital a través de Internet) -menetelmää, jossa allekirjoitus on delegoitu kolmannen osapuolen palveluntarjoajalle (PAC). Kuukausiraportti on poistettu, ja käyttäjät voivat tehdä kyselyvaihtoehdolla kyselyjä historiallisista tapahtumista. |
| **Onko toinen ominaisuus korvannut?**   | En    |
| **Tuotealueet, joihin vaikutetaan**         | Myyntireskontra, projekti   |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="mexico-realized-and-unrealized-vat"></a>Meksikon toteutunut ja toteutumaton ALV

Microsoft Dynamics AX 2012:lla hallittiin toteutumatonta arvonlisäveroa (ALV:tä) käyttämällä vain Meksikoa koskevaa toteutumattoman veron toimintoa.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Sama toiminto  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Tämä toiminto on korvattu ydintoimintojen tavallisessa suoritusperusteisella arvonlisäverotoiminnolla. |
| **Tuotealueet, joihin vaikutetaan**         | Vero   |
| **Tila**                         | Vanhentunut: tämän ominaisuuden poistopäivämäärää ei ole määritetty. |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook -integrointi


|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tämä ominaisuus on korvattu Microsoft Exchange Server -integroinnilla. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä                                                                            |
| **Tuotealueet, joihin vaikutetaan**         | Myynti ja markkinointi                                                            |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Varastonhallinnan kirjauskansioiden yksityinen esto

Varastokirjauskansiot eivät enää tue kirjauskansion merkitsemistä yksityiseksi valitulle käyttäjälle. Vain käyttäjäryhmien käyttämää kirjauskansioiden yksityistä estoa ja estoa muokkauksen aikana tuetaan.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Toiminnolle ei ollut käyttöä. |
| **Onko toinen ominaisuus korvannut?**   | En                                     |
| **Tuotealueet, joihin vaikutetaan**         | Varastoinninhallinta                   |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.         |

### <a name="product-builder"></a>Tuotekonfiguraattori

Tuotekonfiguraattoria käytettiin määrittämään dynaamisesti nimikkeitä myyntitilauksesta, ostotilauksesta, tuotantotilauksesta, myyntitarjouksesta, projektitarjouksesta tai nimiketarpeesta. Käyttäjä voi valita asiakkaan vaatimusten mukaisia arvoja mallinnusmuuttujia sisältävän tuotemallin perusteella ja saada näin yksilöllisen tuotevariantin, jolla on tuoterakenne ja reitti.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tuotekonfiguraattori paljasti X ++-koodin loppukäyttäjille eikä sitä tueta Dynamics AX:n nykyisessä versiossa. Se on poistettu, jotta päällekkäisissä suurissa koodikannoissa ei tarvitsisi tehdä kaksinkertaista ylläpitoa.  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Poissulkeva konfiguraatio otettiin käyttöön Dynamics AX 2012:ssä, jossa tuotekonfiguraattorin vanhentuminen tulevissa versioissa oli jo ilmoitettu. Poissulkeva konfiguraatiomenetelmä valitaan päätuotteessa ottamaan konfiguraatio käyttöön. Lisätietoja on kohdassa [Tuotemääritysmallin luominen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/pim/build-product-configuration-model). |
| **Tuotealueet, joihin vaikutetaan**         | Tuotetietojen hallinta, myynti ja markkinointi  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.      |

### <a name="rename-product-dimension"></a>Nimeä tuotedimensio uudelleen

Tällä toiminnolla voi vaihtaa yhden kolmesta vakiotuotedimension nimestä (koko, väri tai tyyli) liiketoiminnan vaatimuksiin paremmin sopivaan nimeen. Uudelleennimeäminen koski kaikkia otsikoita, joissa tuotedimension nimeä käytettiin.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Dynamics AX:n nykyinen versio ei tue suorituksen aikaisia otsikkomuutoksia. |
| **Onko toinen ominaisuus korvannut?**   | En                                                                            |
| **Tuotealueet, joihin vaikutetaan**         | Tuotetietojen hallinta                                                |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.                                                |

### <a name="retail-server-connectivity-using-http"></a>Vähittäismyynnin palvelinyhteys HTTP-protokollalla

Dynamics AX 2012 R3 -versiossa vähittäismyynnin palvelinyhteyttä oli mahdollista käyttää (suojaamattomalla) HTTP-yhteydellä. Tämä oli lisänä vakioyhteyteen HTTPS-protokollalla.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uusien suojausvaatimusten vuoksi tietoliikenneyhteys on sallittua ainoastaan TLS 1.2 -suojausta (tai uudempaa) käyttäen. Omatoiminen asennusohjelma määrittää yhteystavan tietokoneelle automaattisesti. |
| **Onko toinen ominaisuus korvannut?**   | Nro Vain vakiomuotoinen HTTPS-yhteys on enää tuettu. |
| **Tuotealueet, joihin vaikutetaan**         | Retail Server  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen. |

### <a name="role-center-pages"></a>Roolikeskus-sivut

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Roolikeskus-sivut perustuivat vanhentuneeseen yritysportaaliympäristöön, joka on korvattu uudella verkkoasiakasympäristöllä Dynamics AX:n nykyisessä versiossa. |
| **Onko toinen ominaisuus korvannut?**   | Uusi Työtila-lomakemalli käyttäjille prosessikeskeisen rakenteen, jonka kautta on helppo käyttää kyseisen prosessin usein käytettyjä tehtäviä.                       |
| **Tuotealueet, joihin vaikutetaan**         | Kaikki moduulit    |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen   |

### <a name="sales-tax-jurisdictions"></a>Arvonlisäveroviranomaiset

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Vähäinen käyttö ja rajoitetut toiminnot |
| **Onko toinen ominaisuus korvannut?**   | En                                           |
| **Tuotealueet, joihin vaikutetaan**         | Yhdysvaltojen arvonlisävero                                 |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.               |

### <a name="sites-services"></a>Sites Services -palvelut

Sites Services -palveluiden avulla voit luoda sivustoja, jotka laajentavat liiketoimintaprosesseja Internetiin.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Dynamics AX:n käyttämässä Microsoft Azuren infrastruktuurissa on uusia korvaavia ominaisuuksia (esimerkiksi Azure-sivustot). |
| **Onko toinen ominaisuus korvannut?**   | En   |
| **Tuotealueet, joihin vaikutetaan**         | Henkilön työhönotto, palvelupyynnön hallinta, tarjouspyynnöt, toimittajan rekisteröinti, mahdollisuuksien ja kampanjoiden yhteistyötyötila  |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS – kysynnän ennustestrategia

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uusi pilviarkkitehtuuri ei voi tukea toiminnon rakennetta. |
| **Onko toinen ominaisuus korvannut?**   | Azure Machine Learningin kysynnän ennusteen strategia                           |
| **Tuotealueet, joihin vaikutetaan**         | Pääsuunnittelu                                                              |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Toimittajan laskupooli, ei sisällä kirjaustietoja

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Vähäinen käyttö. Toiminto on korvattu laskun kirjauskansiolla, joka sisältää työnkulkutoiminnon. |
| **Onko toinen ominaisuus korvannut?**   | Laskun kirjauskansion työnkulkutoiminnot     |
| **Tuotealueet, joihin vaikutetaan**         | Ostoreskontra |
| **Tila**                         | Poistettu versiosta Dynamics AX 7.0 alkaen.    |


### <a name="virtual-company-accounts"></a>Virtuaaliyritykset

Dynamics AX ei enää tue virtuaaliyritystoimintoa. Virtuaaliyritystoiminnon avulla käyttäjät pystyivät määrittämään tauluja yritysjoukon jaettavaksi. Toiminnon kuvaus on artikkelissa [Yrityksen tilit ja virtuaaliyrityksen tilit](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). Toiminto ryhmittää virtuaaliyrityksille määritetyiksi tauluiksi. Virtuaaliyritykset ovat olemassa olevien "oikeiden" yritysten ryhmiä. Kyselyjä luomalla kaikki virtuaaliyrityksen yritykset voivat käyttää liitettyjen taulukokoelmien taulujen tietoja.

|   |  | 
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | - Virtuaaliyritykset on määritettävä, ennen kuin tiedot tallennetaan tauluihin. Virtuaaliyritysten sovittaminen jälkikäteen aiemmin luotuihin toteutuksiin on erittäin hankalaa.<br><br>- Koska Dynamics AX:n nykyisessä versiossa on niin paljon tietojen normalisointia, taulukokoelmiin lisättävän tiedon hahmottamisesta on tullut erittäin hankalaa. Esimerkiksi on vaikea hahmottaa, mitä taulut tulee jakaa. Lisäksi kaikki taulut, joihin virtuaaliyrityksessä olevat taulut viitataan, on lisättävä. Taulun normalisoinnin vuoksi yksinkertaisimmankin useissa taulukoissa olevan päätiedon on oltava myös virtuaaliyrityksen osa. Tässä yhteydessä tehdyt mahdolliset virheet aiheuttavat toimintaongelmia.<br><br>- Kun taulu on osa virtuaaliyritystä, se menettää tiedot tiedon alkuperästä ja vain virtuaaliyritys kirjataan.   |
| **Onko toinen ominaisuus korvannut?** | Yleisiä tauluja käyttämällä taulut ovat kaikkien yritysten käytettävissä. Tällä hetkellä korvaavaa toimintoa ei ole. |   
| **Tuotealueet, joihin vaikutetaan**       | Kaikki moduulit |   
| **Tila**                       | Poistettu versiosta Dynamics AX 7.0 alkaen.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 -tablettisovellus

Windows 8 -tablettisovelluksessa oli kulujen vienti- ja hyväksymistoiminnot.

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Finance and Operationsia voi käyttää tableteissa. Tablettisovellusta ei enää tarvita.    |
| **Onko toinen ominaisuus korvannut?**   | Nro          |
| **Tuotealueet, joihin vaikutetaan**         | Kulujen hallinta   |
| **Tila**                         | Poistettu: Tämä toiminto on käytössä vain Dynamics AX 2012 R3:ssa. |

### <a name="workplanner"></a>Työn suunnittelu

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Vähäinen käyttö |
| **Onko toinen ominaisuus korvannut?**   | Ei, mutta **Profiilirelaatio**-sivu, joka avautuu **Profiiliryhmät**-sivulta, tukee samoja liiketoimintaskenaarioita mitä vanhentuneella **Työn suunnittelu**-sivulla käytettiin. |
| **Tuotealueet, joihin vaikutetaan**         | Työajan seuranta     |
| **Tila**                         | Koodia ei ole poistettu. Lomaketta, JmgWorkPlanner, ei kuitenkaan siirretty.    |

### <a name="x-financial-statements"></a>X++-raportit

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Toinen ominaisuus on korvannut tämän toiminnon.                                    |
| **Onko toinen ominaisuus korvannut?**   | Management Reporter (Dynamics AX:n nykyisessä versiossa sen nimi on **Talousraportointi**) |
| **Tuotealueet, joihin vaikutetaan**         | Kirjanpito                                                                              |
| **Tila**                         | Poistettu versiosta Dynamics AX 2012 alkaen                                                              |

