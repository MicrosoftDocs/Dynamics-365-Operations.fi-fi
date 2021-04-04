---
title: Järjestelmävaatimukset
description: Tässä artikkelissa kuvataan Microsoft Dynamics 365 Human Resourcesin vaatimukset.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8b94c1844470938d5e53423f045f5af4c1793d3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466805"
---
# <a name="system-requirements"></a>Järjestelmävaatimukset

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä artikkelissa kuvataan Microsoft Dynamics 365 Human Resourcesin vaatimukset. Siinä esitellään myös maat ja alueet, joissa Human Resources on käytettävissä sekä Human Resources -tietojen kielistä ja lokalisoinnista.

## <a name="supported-web-browsers"></a>Tuetut selaimet

Human Resources toimii kaikilla seuraavilla verkkoselaimilla, joita käytetään määritetyissä käyttöjärjestelmissä: 

*   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
*   Internet Explorer 11 Windows 10-, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
*   Google Chrome (uusin saatavana oleva versio)
*   Apple Safari (uusin saatavana oleva versio)

Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta. 

> [!NOTE]
> * Voit tallentaa tehtävän tallennustoiminnon luomat kuvat ja sisällyttää ne Microsoft Word -asiakirjoihin, jos asennettuna on Chrome-laajennus. 
> * Työnkulkueditori käynnistetään ClickOnce-sovelluksena. Vain Microsoft Edge ja Internet Explorer (tuetuissa Microsoft Windows -versioissa) tukevat ClickOnce-sovelluksia. Työnkulkueditorin ClickOnce-sovellus vaatii 64-bittisen käyttöjärjestelmän.
> * PDF-tiedostojen esikatseluun suosittelemme modernia verkkoselainta, kuten Microsoft Edgeä (uusin julkinen versio) Windows 10 -käyttöjärjestelmässä tai Google Chromea (uusin julkinen versio) Windows 10-, Windows 8.1-, Windows 8- tai Windows 7 -käyttöjärjestelmässä tai Google Nexus 10 -tabletissa.
>   Verkon vaatimukset
> * Human Resources on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms). Tämä viive on selaimen asiakasohjelman ja Human Resourcesia isännöivän Microsoft Azure -palvelinkeskuksen välillä. On suositeltavaa testata verkon viive osoitteessa [www.azurespeed.com](https://www.azurespeed.com "Azuren viivetesti").
> * Human Resourcesin kaistanleveyden vaatimukset riippuvat skenaariostasi. Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä.
> 
> [!WARNING]
> Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea. Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista voivat käyttää Human Resourcesin kokeiluversiota.

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset

* Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel- ja Word-lisäosia voi käyttää. Lisätietoja versiovaatimuksista on kohdassa [Office-integroinnin vianmääritys](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office-integroinnin vianmääritys").
* Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin- tai Vie Wordiin -toimintojen luomia asiakirjoja.

## <a name="regional-availability-languages-and-localization"></a>Alueellinen käytettävyys, kielet ja lokalisointi

Voit ladata PDF-tiedoston maista, alueista ja kielistä, joita Human Resources tukee kohdasta [Microsoft Dynamics 365:n kansainvälinen saatavuus](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Kun käyttöliittymä on lokalisoitu muille kielille, kaikki käyttäjätiedot tallennetaan kielellä, jolla ne on kirjoitettu. Voit luoda sähköposteja ja malleja muilla kielillä, mutta tiedot, kuten aikataulun tiedot, ovat tällä hetkellä käytettävissä vain englanniksi.

Jos olet kehittäjä, joka on kiinnostunut maa- tai aluekohtaisten mukautusten luonnista, tai kun luot ratkaisun maalle tai alueelle, jota Microsoft ei tällä hetkellä tue, Katso lisätietoja kohdasta [Globalisaatio](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).


[!INCLUDE[footer-include](../includes/footer-banner.md)]