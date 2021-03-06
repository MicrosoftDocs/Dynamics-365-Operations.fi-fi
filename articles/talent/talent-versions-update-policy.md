---
title: Talentin järjestelmävaatimukset
description: Tässä ohjeaiheessa kerrotaan Dynamics 365 Talentin järjestelmävaatimuksista.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461027"
---
# <a name="talent-system-requirements"></a>Talentin järjestelmävaatimukset

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kuvataan Microsoft Dynamics 365 Talent -vaatimukset, kuten Attract ja Onboard. Siinä esitellään myös Talentin käytettävissä olevat maat ja alueet sekä tiedot kielistä ja lokalisoinnissa Talentia koskevia tietoja varten. Lisäyksissä tämä ohjeaihe sisältää Talentin päivityskäytännön.

## <a name="supported-web-browsers"></a>Tuetut selaimet

Microsoft Dynamics 365 Talent toimii kaikilla seuraavilla verkkoselaimilla, joita käytetään määritetyissä käyttöjärjestelmissä: 

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
> * Dynamics 365 Talent on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms). Tämä viive on selaimen asiakasohjelman ja Talentia isännöivän Microsoft Azure -palvelinkeskuksen välillä. On suositeltavaa testata verkon viive osoitteessa [www.azurespeed.com](https://www.azurespeed.com "Azuren viivetesti").
> * Talentin kaistanleveyden vaatimukset riippuvat skenaariostasi. Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä.
> 
> [!WARNING]
> Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea. Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista voivat käyttää Talentin kokeiluversiota.

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset

* Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel- ja Word-lisäosia voi käyttää. Lisätietoja versiovaatimuksista on kohdassa [Office-integroinnin vianmääritys](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office-integroinnin vianmääritys").
* Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin- tai Vie Wordiin -toimintojen luomia asiakirjoja.

## <a name="regional-availability-languages-and-localization"></a>Alueellinen käytettävyys, kielet ja lokalisointi

Voit ladata PDF-tiedoston maista, alueista ja kielistä, joita Talent tukee kohdasta [Microsoft Dynamics 365:n kansainvälinen saatavuus](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Kun käyttöliittymä on lokalisoitu muille kielille, kaikki käyttäjätiedot tallennetaan kielellä, jolla ne on kirjoitettu. Voit luoda sähköposteja ja malleja muilla kielillä, mutta tiedot, kuten aikataulun tiedot, ovat tällä hetkellä käytettävissä vain englanniksi.

Jos olet kehittäjä, joka on kiinnostunut maa- tai aluekohtaisten mukautusten luonnista, tai kun luot ratkaisun maalle tai alueelle, jota Microsoft ei tällä hetkellä tue, Katso lisätietoja kohdasta [Globalisaatio](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).



[!INCLUDE[footer-include](../includes/footer-banner.md)]