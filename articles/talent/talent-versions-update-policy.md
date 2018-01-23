---
title: "Dynamics 365 for Talentin järjestelmävaatimukset ja päivityskäytäntö"
description: "Tässä ohjeaiheessa kerrotaan Dynamics 365 for Talentin järjestelmävaatimuksista. Lisäksi siinä käsitellään päivityskäytäntö."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-talent
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7bcc8464d34c35423e86c963c6b493fc09db4472
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="microsoft-dynamics-365-for-talent-system-requirements-and-update-policy"></a>Microsoft Dynamics 365 for Talentin järjestelmävaatimukset ja päivityskäytäntö

[!include[banner](includes/banner.md)]


Tässä ohjeaiheessa kerrotaan Microsoft Dynamics 365 for Talentin järjestelmävaatimuksista. Lisäksi siinä käsitellään päivityskäytäntö.

## <a name="supported-web-browsers"></a>Tuetut selaimet

Microsoft Dynamics 365 for Talent -verkkosovellus voidaan suorittaa seuraavissa selaimissa, joita käytetään määritetyissä käyttöjärjestelmissä: 

*   Microsoft Edge (uusin saatavana oleva versio) Windows 10 -käyttöjärjestelmässä
*   Internet Explorerin 11 Windows 10, Windows 8.1- tai Windows 7 -käyttöjärjestelmässä
*   Google Chrome (uusin saatavana oleva versio) Windows 10-, Windows 8.1-, Windows 8-, Windows 7- tai Google Nexus 10 -taulutietokoneen käyttöjärjestelmässä
*   Apple Safari (uusin saatavana oleva versio) Mac OS X 10.10 (Yosemite)-, 10.11 (El Capitan)-, 10.12 (Sierra)- tai Apple iPadin käyttöjärjestelmässä.

Ohjelmistovalmistajien sivustot sisältävät tietoja kunkin selaimen uusimmasta versiosta. 

> [!NOTE]
> * Voit tallentaa tehtävän tallennustoiminnon luomat kuvat ja sisällyttää ne Microsoft Word -asiakirjoihin, jos asennettuna on Chrome-laajennus. 
> * Työnkulkueditori käynnistetään ClickOnce-sovelluksena. Ainoastaan Microsoft Edge ja Internet Explorer (tuetussa Microsoft Windows -versiossa) tukevat ClickOnce-sovelluksia. Työnkulkueditorin ClickOnce-sovellus vaatii 64-bittisen käyttöjärjestelmän.
> * PDF-tiedostojen esikatseluun suosittelemme modernia verkkoselainta, kuten Microsoft Edgeä (uusin julkinen versio) Windows 10 -käyttöjärjestelmässä tai Google Chromea (uusin julkinen versio) Windows 10-, Windows 8.1-, Windows 8- tai Windows 7 -käyttöjärjestelmässä tai Google Nexus 10 -tabletissa.
Verkon vaatimukset
> * Dynamics 365 for Talent on suunniteltu verkkoihin, joiden viive on enintään 250–300 millisekuntia (ms). Tämä on viive selainasiakkaan ja Dynamics 365 for Talentia isännöivän Microsoft Azure -palvelinkeskuksen välillä. Verkon viive kannattaa testata osoitteessa [www.azurespeed.com] (http://www.azurespeed.com Azuren viivetesti).
> * Dynamics 365 for Talentin kaistanleveysvaatimus riippuu tilanteesta. Yleisimmät tilanteet vaativat yli 50 kilotavua sekunnissa (KBps) kaistanleveyttä.

> [!WARNING]
> Älä laske kaistanleveysvaatimuksia asiakkaan sijainnista kertomalla käyttäjien määrä kaistanleveyden vähimmäisvaatimuksella. Tietyn sijainnin samanaikainen käyttö on hyvin vaikea laskea. Asiakkaat, jotka ovat huolissaan kaistanleveyden vaatimuksista voivat käyttää Dynamics 365 for Talentin kokeiluversiota.

## <a name="supported-microsoft-office-applications"></a>Tuetut Microsoft Office -sovellukset

*   Microsoft Office 2016:n Windows- tai Mac-version on oltava asennettuna, jotta Microsoft Excel ja Word-lisäosia voi käyttää. Lisätietoja versiovaatimuksista on ohjeaiheessa [Office-integroinnin vianmääritys] (../dev-itpro/office-integration/office-integration-troubleshooting.md "Office-integroinnin vianmääritys").
*   Microsoft Office 2007 tai sitä uudempi on oltava asennettuna, jotta voit tarkastella Vie Exceliin tai Vie Wordiin -toimintojen luomia asiakirjoja.

## <a name="update-policy"></a>Päivityskäytäntö

Microsoft Dynamics 365 for Talent on pilvipalvelu. Dynamics 365 for Talentin päivitykset ovat jatkuvia ja Microsoft ottaa ne käyttöön automaattisesti.

Päivitykset julkaistaan säännöllisesti, ja ne tehdään kaikkiin ympäristöihin.  Dynamics 365 for Talentia tuetaan [Microsoft-tuen elinkaarikäytännön] (https://support.microsoft.com/en-us/gp/lifecycle#gp/OSSLpolicy Microsoft-tuen elinkaari) mukaisesti, joka ilmaisee yhdenmukaisen ja ennakoitavan ohjeistuksen tuotetuen saatavuudesta.

