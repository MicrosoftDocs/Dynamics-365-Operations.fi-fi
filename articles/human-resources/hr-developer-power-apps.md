---
title: Talentin laajentaminen Power Appsin ja Power Automaten avulla
description: Tässä artikkelissa käsitellään Microsoft Power Appsia ja Microsoft Power Automatea käyttäviä Microsoft Dynamics 365 Human Resourcesin laajennusesimerkkejä.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1c5bc0776174960af6cb8a62f00e3fd7d56b1676
ms.sourcegitcommit: 58d7133ae9909fa205730e3cf4c7fd5a1d5d0b75
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/10/2020
ms.locfileid: "3793608"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Laajentaminen Power Appsin ja Power Automaten avulla

Tässä artikkelissa käsitellään Microsoft Power Appsia ja Microsoft Power Automatea käyttäviä Microsoft Dynamics 365 Human Resourcesin laajennusesimerkkejä. Voit tuoda kumpaankin esimerkkiin liitetyt ratkaisupaketin Power Apps-ympäristöön. Voit sitten käyttää paketteja joka ohjeena tai lähtökohtana, jonka avulla toteutat organisaatioon sopivia skenaarioita.

> [!IMPORTANT]
> Jos haluat käyttää tässä ohjeaiheessa kuvattuja malleja ja sovelluksia sellaisenaan, varmista testaamalla, että ne kattavat kaikki toteutukseen kuuluvat skenaariot.

## <a name="prerequisites"></a>Edellytykset

- Pakettien tuontia varten käyttäjät tarvitsevat **Ympäristön tekijä** -käyttöoikeuden.
- Sovellusten vientiä ja tuontia varten käyttäjillä on oltava Power Apps-palvelupaketin 2 käyttöoikeus tai Power Apps -palvelupaketin 2 kokeiluversion käyttöoikeus.

## <a name="integration-with-office-365-power-automate"></a>Integrointi Office 365:n, Power Automaten kanssa

**Office 365 -integrointi** -sovelluksella voi purkaa kirjautuneiden käyttäjien tiimitiedot Microsoft Office 365:stä. Siinä viitataan henkilöstöhallinnon työntekijöihin, jotta työntekijöiden tunnistetyypit voidaan poimia. Esimiehet voivat tarkistaa työntekijän tunnustyyppien vanhentumispäivämäärät. He voivat myös lähettää sähköpostimuistutuksen, jos työntekijätunnuksen tyyppi on umpeutumassa. Power Automate integroituu Power Appsin kanssa tämän muistutuksen lähettämiseen. Vahvistus lähetetään takaisin Power Appsiin Power Automatesta, kun muistutus lähetetään. Tunnustyyppejä ovat ajokortti, passi ja muut hyväksyttävät henkilöllisyystodistusmuodot.

Voit laajentaa tätä sovellusta muihin tilanteisiin. Voit käyttää sitä esimerkiksi näyttämään ryhmän lomatiedot, kalenteritapahtumat ja kaikki ryhmäkohtaiset tapahtumat.

Voit ladata **Office 365 -integroinnin Power Automate** -sovelluksen kohdassa [Office 365 -integrointi](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL-yhteys ja toteutus

**Power Automate – SQL-yhteys ja toteutus** -malli muodostaa yhteyden Microsoft SQL Serveriin ja mahdollistaa SQL-kyselyjen suorittamisen.

Vaikka tämä malli lukee ja päivittää SQL-tauluja, voit laajentaa ja käyttää sitä muissa skenaarioissa. Sen avulla voit esimerkiksi täyttää valmistelutaulu Common Data Servicessä SQL Serverin tietueilla sekä synkronoida valmistelutaulu säännöllisesti käyttämällä SQL Serverin lisäävää työntöä.

Edistynyt kysely on integroitu virtauksen kanssa, jotta tietojen muuntaminen ja lisäävä työntö voidaan ottaa käyttöön.

Voit ladata **Power Automate – SQL-yhteys ja toteutus** -mallin Microsoft Download Centerin kohdassa [Power Automate – SQL-yhteys ja toteutus](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="additional-resources"></a>Lisäresurssit

[Microsoft Power Platform](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>