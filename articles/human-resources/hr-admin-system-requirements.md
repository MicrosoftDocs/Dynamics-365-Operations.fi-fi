---
title: Järjestelmävaatimukset
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin järjestelmävaatimuksista.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b07d14dfe0e6b53c9489c284520a24b97d9887fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879334"
---
# <a name="system-requirements"></a>Järjestelmävaatimukset

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin järjestelmävaatimuksista. Siinä esitellään myös maat ja alueet, joissa Human Resources on käytettävissä sekä Human Resources -tietojen kielistä ja lokalisoinnista.

## <a name="supported-web-browsers"></a>Tuetut selaimet

Käyttäjät voivat käyttää Microsoft Dynamics 365 Human Resources seuraavilla selaimilla, joita käytetään määritetyissä käyttöjärjestelmissä: 

*   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
*   Internet Explorer 11 Windows 10-, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
*   Google Chrome (uusin saatavana oleva versio)
*   Apple Safari (uusin saatavana oleva versio)

Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta. 

## <a name="special-considerations"></a>Erityiset huomioitavat asiat

* Chrome-laajennuksen ennakkojulkaisuversio on asennettava, jotta tehtävien tallennustoiminto voi siepata luodut kuvat ja sisällyttää ne Microsoft Word -asiakirjoihin.
* Työnkulkueditori käynnistetään ClickOnce-sovelluksena. Vain Microsoft Edge ja Internet Explorer (tuetuissa Microsoft Windows -versioissa) tukevat ClickOnce-sovelluksia. Työnkulkueditorin ClickOnce-sovellus vaatii 64-bittisen käyttöjärjestelmän.
* PDF-tiedostojen esikatseluun suosittelemme modernia verkkoselainta, kuten Microsoft Edgeä (uusin julkinen versio) Windows 10 -käyttöjärjestelmässä tai Google Chromea (uusin julkinen versio) Windows 10-, Windows 8.1-, Windows 8- tai Windows 7 -käyttöjärjestelmässä tai Google Nexus 10 -tabletissa.

## <a name="network-requirements"></a>Verkon vaatimukset

* Human Resources on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms). Tämä viive on selaimen asiakasohjelman ja Human Resourcesia isännöivän Microsoft Azure -palvelinkeskuksen välillä. On suositeltavaa testata verkon viive osoitteessa [www.azurespeed.com](https://www.azurespeed.com "Azuren viivetesti").
* Human Resourcesin kaistanleveyden vaatimukset riippuvat skenaariostasi. Tyypillisissä skenaarioissa tarvittava kaistanleveys on yli 50 kilotavua sekunnissa (kb/s).
 
> [!WARNING]
> Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea. Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista voivat käyttää Human Resourcesin kokeiluversiota.

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset

* Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel- ja Word-lisäosia voi käyttää. Lisätietoja versiovaatimuksista on kohdassa [Office-integroinnin vianmääritys](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Office-integroinnin vianmääritys").
* Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin- tai Vie Wordiin -toimintojen luomia asiakirjoja.

## <a name="regional-availability-languages-and-localization"></a>Alueellinen käytettävyys, kielet ja lokalisointi

Voit ladata PDF-tiedoston maista, alueista ja kielistä, joita Human Resources tukee kohdasta [Microsoft Dynamics 365:n kansainvälinen saatavuus](/dynamics365/get-started/availability). 

> [!NOTE]
> Kun käyttöliittymä on lokalisoitu muille kielille, kaikki käyttäjätiedot tallennetaan kielellä, jolla ne on kirjoitettu. Voit luoda sähköposteja ja malleja muilla kielillä, mutta tiedot, kuten aikataulun tiedot, ovat tällä hetkellä käytettävissä vain englanniksi.

Jos olet kehittäjä, joka on kiinnostunut maa- tai aluekohtaisten mukautusten luonnista, tai kun luot ratkaisun maalle tai alueelle, jota Microsoft ei tällä hetkellä tue, Katso lisätietoja kohdasta [Globalisaatio](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
