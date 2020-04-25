---
title: Poistetut tai vanhentuneet Platform-ominaisuudet
description: Tässä ohjeaiheessa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan Finance and Operations -sovellusten ympäristöpäivityksissä.
author: sericks007
manager: AnnBe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0072ca507301fdb880f0595a06377ff01366ca20
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260526"
---
# <a name="removed-or-deprecated-platform-features"></a>Poistetut tai vanhentuneet Platform-ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan Finance and Operations -sovellusten ympäristöpäivityksissä.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

> [!NOTE]
> Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.

## <a name="platform-updates-for-version-10011-of-finance-and-operations-apps"></a>Finance and Operations -sovellusalustan päivitykset sovellusten versiolle 10.0.11

### <a name="field-groups-containing-invalid-field-references"></a>Virheellisiä kenttäviitteitä sisältävät kenttäryhmät

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Taulun metatietomääritysten kenttäryhmät voivat sisältää kenttäviittauksia, jotka eivät ole kelvollisia. Jos nämä kenttäryhmät otetaan käyttöön, ne voivat aiheuttaa suorituksenaikaisia virheitä talousraportoinnissa ja Microsoft SQL Server Reporting Servicesissa (SSRS). Platform Update 23 sisälsi kääntäjän *varoituksen*, joka mahdollisti tämän metatieto-ongelman käsittelemisen. Finance and Operations -sovellusten versio 10.0.11:n päivitykset luokittelevat tämän ongelman kääntäjän *virheeksi*.<p>Korjaa tämä ongelma seuraavien ohjeiden mukaisesti.</p><ol><li>Poista virheellinen kenttäviite taulun kenttäryhmämääritelmästä.</li><li>Käännä uudelleen.</li><li>Varmista, että mahdolliset virheet on korjattu.</li></ol> |
| **Onko toinen ominaisuus korvannut?**   | Tämä kääntäjän virhe korvaa kääntäjän varoituksen pysyvästi.  |
| **Tuotealueet, joihin vaikutetaan**         | Visual Studio -sovelluksen kehitystyökalut |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | **Vanhentunut:** Kääntäjävaroitus on nyt kääntäjän virhe Finance and Operations -sovellusalustan päivityksissä versiossa 10.0.11. |

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

