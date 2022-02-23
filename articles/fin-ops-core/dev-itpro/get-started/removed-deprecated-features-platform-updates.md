---
title: Poistetut tai vanhentuneet Platform-ominaisuudet
description: Tässä ohjeaiheessa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan Finance and Operations -sovellusten ympäristöpäivityksissä.
author: sericks007
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ffd98016079ccab47864c821116c821b5df22e3b
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689563"
---
# <a name="removed-or-deprecated-platform-features"></a>Poistetut tai vanhentuneet Platform-ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan Finance and Operations -sovellusten ympäristöpäivityksissä.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.

## <a name="platform-updates-for-version-10015-of-finance-and-operations-apps"></a>Finance and Operations -sovellusalustan päivitykset sovellusten versiolle 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11:n Dynamics 365 -tuki on vanhentunut

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Joulukuusta 2020 alkaen kaikkien Dynamics 365 -tuotteiden Microsoft Internet Explorer 11 -tuki vanhenee eikä Internet Explorer 11:tä tueta elokuun 2021 jälkeen.<br><br>Tämä vaikuttaa sellaisiin Dynamics 365 -tuotteita käyttäviin asiakkaisiin, jotka on suunniteltu käytettäviksi Internet Explorer 11 -liittymässä. Elokuun 2021 jälkeen Internet Explorer 11:tä ei tueta kyseisissä Dynamics 365 -tuotteissa. |
| **Onko toinen ominaisuus korvannut?**   | Asiakkaiden kannattaa siirtyä Microsoft Edgeen.|
| **Tuotealueet, joihin vaikutetaan**         | Kaikki Dynamics 365 -tuotteet |
| **Käytön asetukset**              | Kaikki|
| **Tila**                         | Vanhentunut. Internet Explorer 11:tä ei tueta elokuun 2021 jälkeen.|


### <a name="visual-studio-add-in-to-apply-metadata-hotfixes"></a>Visual Studio -apuohjelma metatietojen hotfix-korjausten käyttämiseen

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Metatietojen hotfix-korjauksia ei enää tueta [One Version](../../fin-ops/get-started/one-version.md) -palvelupäivityksissä, jotka otettiin käyttöön heinäkuussa 2018 versiossa 8.1. |
| **Onko toinen ominaisuus korvannut?**   | Yksittäiset metatietojen hotfix-korjaukset eivät ole saatavana tuettuihin versioihin. Sen sijaan käytetään kumulatiivisia laatupäivityksiä. |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -apuohjelmat |
| **Käytön asetukset**              | Kehityksen virtuaalikoneet |
| **Tila**                         | Versiossa 10.0.15 myötä apuohjelma ei enää sisälly Visual Studio Toolsiin. |


## <a name="platform-updates-for-version-10014-of-finance-and-operations-apps"></a>Finance and Operations -sovellusalustan päivitykset sovellusten versiolle 10.0.14

### <a name="online-users-page"></a>Online-käyttäjien sivu 

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tämä on vanha sivu, joka on luotu aiemmalle asiakas-/palvelinarkkitehtuurille. Tällä sivulla olevat tiedot eivät aina ole oikein, mikä voi olla hämmentävää ja harhaanjohtavaa. |
| **Onko toinen ominaisuus korvannut?**   | Julkaisemme uuden sivun tulevassa päivityksessä.|
| **Tuotealueet, joihin vaikutetaan**         | Järjestelmän hallinta |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Tämä lomake poistetaan lokakuuhun 2021 mennessä.   |


## <a name="platform-updates-for-version-10013-of-finance-and-operations-apps"></a>Finance and Operations -sovellusalustan päivitykset sovellusten versiolle 10.0.13


### <a name="custom-code-defined-in-ssrs-report-properties"></a>SSRS-raportin ominaisuuksissa määritetty mukautettu koodi 

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Yleensä mukautettu koodi tarjoaa rajoitettuja etuja samaan aikaan ja edellyttää huomattavaa resursointi- ja käsittelytukea. Mukautettua koodia käytetään ensisijaisesti raportin laatijoiden kutsussa julkisiin menetelmiin mukautetusta koodikokoonpanosta. Pilvipohjainen palvelu ei kuitenkaan tue SSRS-raporttien mukautettujen kokoonpanojen viittauksia. |
| **Onko toinen ominaisuus korvannut?**   | Raporttien laatijat voivat halutessaan jatkaa julkisten .NET-API-liittymien vertailemista mistä tahansa tekstiruudun lausekkeesta. Lisätietoja on kohdassa [Koodin lisääminen raporttiin (SSRS)](https://docs.microsoft.comsql/reporting-services/report-design/add-code-to-a-report-ssrs?view=sql-server-ver15).  |
| **Tuotealueet, joihin vaikutetaan**         | RDL:ssä määritetyn sovellusraporttimallin alijoukko, joka sisältää mukautettua koodia. |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versiolla 10.0.13, kääntäjä alkaa antaa varoituksen tapauksissa, joissa mukautettua koodia havaitaan SSRS-raportti määritelmässä. Voit korjata ongelman avaamalla raportin rakennemäärityksen ja poistamalla kaikki mukautetut koodiartefaktit. Tämä varoitus korvataan kääntäjän virheellä tulevassa päivityksessä.   |

### <a name="upgrade-of-three-jquery-component-libraries"></a>Kolmen jQuery-osakirjaston päivitys 

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Kolmea jQuery-osakirjastoa päivitetään suojauskorjausten vuoksi ja valuutan ylläpitoa varten.   
| **Onko toinen ominaisuus korvannut?**   | Kyse on seuraavista kirjastoista: jQuery (versioon 3.5.0 versiosta 2.1.4), jQuery UI (versioon 1.12.1 versiosta 1.11.4), jQuery qTip (versioon 3.0.3 versiosta 2.2.1). jQuerylla on verkossa ohjeet siirtoa varten.  |
| **Tuotealueet, joihin vaikutetaan**         | Laajennettavat ohjausobjektit, etenkin vanhentuneita tai poistettuja ohjelmointirajapintoja käyttävä mukautettu JavaScript-koodi |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versiossa 10.0.13 / Platform update 37:ssä asiakkailla on mahdollisuus siirtyä uusimpiin kirjastoihin ottamalla Kolmen jQuery-osakirjaston päivitys -toiminto käyttöön. Uusiin kirjastoihin siirtyminen tulee pakolliseksi huhtikuun 2021 -version myötä, jotta kyseisten ohjelmointirajapintojen siirtoon jää aikaa.   |

### <a name="existing-grid-controlforcelegacygrid-api"></a>Olemassa oleva ruudukon ohjausobjekti / forceLegacyGrid()-ohjelmistorajapinta

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uusi ruudukon ohjausobjekti korvaa aiemmin luodun ruudukon ohjausobjektin. |
| **Onko toinen ominaisuus korvannut?**   | [Uusi ruudukon ohjausobjekti](../..//fin-ops/get-started/grid-capabilities.md) |
| **Tuotealueet, joihin vaikutetaan**         | WWW-asiakasohjelma |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versiossa 10.0.13 uusi ruudukon ohjausobjekti on yleisesti saatavilla. Asiakkaat voivat halutessaan ottaa ominaisuuden käyttöön. Uusi ruudukon ohjausobjekti on pakollinen lokakuun 2021 julkaisussa. Kun uusi ruudukon ohjausobjekti on pakollinen, **forceLegacyGrid()**-ohjelmointirajapintaa ei enää käytetä. |

### <a name="personalization-without-saved-views"></a>Mukauttaminen ilman tallennettuja näkymiä 

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Mukautuksen alijärjestelmä on uudistettu. Se sisältää tallennettujen näkymien ominaisuuden, joten suorituskyky on parempi ja se sisältää uusia ominaisuuksia. |
| **Onko toinen ominaisuus korvannut?**   | Tallennetut näkymät |
| **Tuotealueet, joihin vaikutetaan**         | WWW-asiakasohjelma |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versiossa 10.0.13 / Platform update 37 tallennettujen näkymien ominaisuus on yleisesti käytettävissä. Asiakkaat voivat halutessaan ottaa tämän ominaisuuden käyttöön. Tallennettujen näkymien ominaisuus on pakollinen lokakuun 2021 julkaisussa. |


## <a name="platform-updates-for-version-10012-of-finance-and-operations-apps"></a>Finance and Operations -sovellusalustan päivitykset sovellusten versiolle 10.0.12

### <a name="grid-or-group-control-form-extensions-containing-invalid-field-references"></a>Ruudukko- tai ryhmäohjausobjektin lomakelaajennukset, jotka sisältävät virheellisiä kenttäviittauksia

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Ruudukko- tai ryhmäohjausobjektien tietoryhmäominaisuuden avulla voidaan automaattisesti näyttää kaikki kenttäryhmän kentät. Laajennuksessa lisätty ruudukko tai ryhmäohjausobjekti voi sisältää kenttiä, joita ei ole enää määritetty kenttäryhmässä, tai kenttäryhmään määritettyjä kenttiä ei ehkä löydy. Tämä voi aiheuttaa epäjohdonmukaista käyttäytymistä suorituksen aikana. Finance and Operations -sovellusten versio 10.0.12:n päivitykset luokittelevat nyt tämän ongelman kääntäjän *varoitukseksi*. Voit korjata tämän ongelman avaamalla lomakelaajennuksen ja tallentamalla sen.
| **Onko toinen ominaisuus korvannut?**   | Tämä kääntäjän varoitus korvataan kääntäjän virheellä tulevassa päivityksessä. |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Kääntäjävaroitus esiintyy Finance and Operations -sovellusalustan päivityksissä versiossa 10.0.12. |

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Finance and Operations -sovellusalustan päivitykset sovellusten versiolle 10.0.11

### <a name="explicit-safe-lists-for-self-service-environments"></a>Selkeä turvallisten osoitteiden luettelo itsepalveluympäristöissä

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | IP-osoitteiden turvallisiin osoitteisiin siirtymisprosessi on muuttunut. Itsepalvelu ei enää tue turvallisia IP-osoitteita. |
| **Onko toinen ominaisuus korvannut?**   | Lisätietoja on kohdassa [Azure Active Directoryn ehdollisen käytön konfigurointi](https://docs.microsoft.com/appcenter/general/configuring-aad-conditional-access).|
| **Tuotealueet, joihin vaikutetaan**         | Suojaus |
| **Käytön asetukset**              | Pilvi |
| **Tila**                         | **Vanhentunut:** Tämä ominaisuus on täysin vanhentunut itsepalvelukäyttöönotoissa. |

### <a name="visual-studio-2015"></a>Visual Studio 2015

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Uusimpien Visual Studio -versioiden tueksi on tehtävä joitakin muutoksia Visual Studion X + +-laajennuksiin. Nämä muutokset eivät ole yhteensopivia Visual Studio 2015:n kanssa. |
| **Onko toinen ominaisuus korvannut?**   | Visual Studio 2017 korvaa Visual Studio 2015:n käyttöönotettuna ja vaaditussa muodossa. |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Versio 10.0.13 (Alustapäivitys 37) tai uudemmassa versiossa käyttöön otetut virtuaalikoneet sisältävät Visual Studio 2017:n. Versio 10.0.16 (Alustapäivitys 40) on viimeinen julkaisu, joka tukee Visual Studio 2015:ta. Virtuaalikoneita, joissa on vain Visual Studio 2015, ei voi päivittää versioon 10.0.17 (Alustapäivitys 41). |

### <a name="field-groups-containing-invalid-field-references"></a>Virheellisiä kenttäviitteitä sisältävät kenttäryhmät

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Taulun metatietomääritysten kenttäryhmät voivat sisältää kenttäviittauksia, jotka eivät ole kelvollisia. Jos nämä kenttäryhmät otetaan käyttöön, ne voivat aiheuttaa suorituksenaikaisia virheitä talousraportoinnissa ja Microsoft SQL Server Reporting Servicesissa (SSRS). Platform Update 23 sisälsi kääntäjän *varoituksen*, joka mahdollisti tämän metatieto-ongelman käsittelemisen. Finance and Operations -sovellusten versio 10.0.11:n päivitykset luokittelevat tämän ongelman kääntäjän *virheeksi*.<p>Korjaa tämä ongelma seuraavien ohjeiden mukaisesti.</p><ol><li>Poista virheellinen kenttäviite taulun kenttäryhmämääritelmästä.</li><li>Käännä uudelleen.</li><li>Varmista, että mahdolliset virheet on korjattu.</li></ol> |
| **Onko toinen ominaisuus korvannut?**   | Tämä kääntäjän virhe korvaa kääntäjän varoituksen pysyvästi.  |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | **Vanhentunut:** Kääntäjävaroitus on kääntäjän virhe Finance and Operations -sovellusalustan päivityksissä versiossa 10.0.11. |

### <a name="isv-licenses-created-by-using-the-sha1-hashing-algorithm"></a>SHA1-hajautusalgoritmin avulla luodut ohjelmistotoimittajien lisenssit

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Riippumattoman ohjelmistotoimittajan käyttöoikeuksien luontiprosessi on muuttunut. Lisätietoja on kohdassa [Riippumaton ohjelmistotoimittajien (ISV) lisensointi](../dev-tools/isv-licensing.md#appendix-create-self-signed-certificates-for-test-purposes). |
| **Onko toinen ominaisuus korvannut?**   | Kyllä. Luo lisenssejä Windows PowerShellin avulla. |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | <strong>Vanhentunut:</strong> Ohjelmistotoimittajien käyttöoikeudet, jotka luotiin SHA1-hajautusalgoritmin avulla. Tämä algoritmi riippui MakeCert-apuohjelman avulla luoduista sertifikaateista, ja tämä apuohjelma on syrjäytetty.<p><strong>Vanhentunut:</strong> SHA1 käyttösuojaus- tai hajautustarkoituksiin. SHA1 lakkaa toimimasta vuoden 2021 alussa. Siksi sitä ei pitäisi enää käyttää.<p><strong>Poistettu:</strong> Transport Layer Securityn tuki (TLS) 1.0 ja TLS 1.1 saapuville tai lähteville pyynnöille. |

## <a name="platform-update-32"></a>Ympäristön update 32 -päivitys

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Työnkulun pyynnön muutoksen valintaikkuna ei enää sisällä käyttäjän valinnan avattavaa luetteloa
|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Tämä oli tietoturvaongelma, koska muutospyyntö voitiin lähettää väärälle käyttäjälle. Tämä oli myös käytettävyysongelma, koska se pakotti käyttäjän määrittämään, kuka työnkulun aloittaja on, ja manuaalisesti valitsemaan tämän.  |
| **Onko toinen ominaisuus korvannut?**   | Ei |
| **Tuotealueet, joihin vaikutetaan**         | Työnkulku |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Käyttäjän valinnan avattava luettelo poistettiin pyynnön muutoksen valintaikkunasta Platform update 32 -päivityksessä. Pyynnön muutospyynnöt lähetetään automaattisesti aloittajalle aiemmin määritetyllä tavalla. Lisätietoja tästä toiminnosta on kohdassa [Toiminnot työnkulun hyväksyntäprosesseissa](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

### <a name="embedded-drill-through-links-are-no-longer-supported-in-paginated-documents-rendered-by-the-cloud-hosted-service"></a>Upotetut porautumiseen käytettäviä linkkejä ei enää tueta sivutetuissa asiakirjoissa, jotka pilvipohjainen palvelu hahmontaa 
|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Palvelun hahmontamat asiakirjoihin upotetut siirtymisen URL-osoitteet voivat sisältää luottamuksellista liiketoimintatietoa. Kaikkien upotettujen porautumislinkkien tuki asiakirjoissa poistetaan. Näin turvataan asiakastiedot jatkossa. Käyttäjät hyötyvät myös paremmasta suorituskyvystä samalla, kun asiakirjoja tuotetaan interaktiivisesti tämän muutoksen seurauksena.  |
| **Onko toinen ominaisuus korvannut?**   | Nro |
| **Tuotealueet, joihin vaikutetaan**         | Raportointi |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Tämä toiminto poistetaan käytöstä palvelusta.<br><br>Uusi asiakasohjelma tarjoaa useita vaihtoehtoja näkymien tuottamiseen. Se luo myös linkkejä automaattisesti sovelluksessa siirtymistä varten. Palvelun hahmontamia sivutettuja asiakirjoja suositellaan ulkoista viestintää varten sähköpostissa, arkistoinnissa ja vastaanottajien tulostuksissa. Asiakirjojen esikatselua suoraan selaimessa on parannettu. Näin voidaan käyttää paikallisia tulostimia suoraan. Lisätietoja on kohdassa [PDF-asiakirjojen esikatselu upotetussa katseluohjelmassa](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/preview-pdf-documents). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset
Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../migration-upgrade/deprecated-features.md).

