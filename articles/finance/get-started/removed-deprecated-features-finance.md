---
title: Poistetut tai vanhentuneet Dynamics 365 Finance -ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Financesta.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127974"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Poistetut tai vanhentuneet Dynamics 365 Finance -ominaisuudet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Financesta.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi. 

> [!NOTE]
> Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Financen version 10.0.12 poistetut tai vanhentuneet ominaisuudet

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Puolan SSRS-raportit, maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri - toimintojen viite PL-00014

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Ei lakisääteistä edellytystä.  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä (Excel-muoto vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa - JPK_VDEK) |
| **Tuotealueet, joihin vaikutetaan**         | Sovellus |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: 1.7.2021 jälkeen emme enää tue SSRS-raportteja: **Maksettavan veron rekisteri, vähennettävän veron rekisteri, EU-yhteenveto, ALV-rekisteri – toimintojen viite PL-00014**. Excel-muodon esimerkki vakiomuotoista tarkistustiedostoa varten ALV-ilmoituksessa (JPK_VDEK) otetaan sen sijaan käyttöön. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Financen version 10.0.7 poistetut tai vanhentuneet ominaisuudet

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Työnkulun pyynnön muutoksen valintaikkuna ei enää sisällä käyttäjän valinnan avattavaa luetteloa
|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Siirrytty ominaisuuteen, jossa on tiliryhmävalinta.  |
| **Onko toinen ominaisuus korvannut?**   | Kyllä |
| **Tuotealueet, joihin vaikutetaan**         | Työnkulku |
| **Käytön asetukset**              | Kaikki |
| **Tila**                         | Vanhentunut: Suunnittelemme lopettavamme Kiinalaisten tositetyyppimäärityksen tukemisen ilman tiliryhmävalintaa 1.12.2020 mennessä. Lisätietoja uudesta suunnitelmasta on kohdassa [Uutta versiossa 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset
Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
