---
title: Poistetut tai vanhentuneet Platform-ominaisuudet
description: Tässä ohjeaiheessa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan Finance and Operations -sovellusten ympäristöpäivityksissä.
author: sericks007
manager: AnnBe
ms.date: 03/03/2020
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
ms.openlocfilehash: d394f5ca84efc5beb943d349e45a3d2c9639d83c
ms.sourcegitcommit: 75974ae567bb0eacf0f65cac992b34ce5c680b93
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095771"
---
# <a name="removed-or-deprecated-platform-features"></a>Poistetut tai vanhentuneet Platform-ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään toimintoja, jotka on poistettu tai joiden poistoa suunnitellaan Finance and Operations -sovellusten ympäristöpäivityksissä.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

> [!NOTE]
> Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.

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

