---
title: Talentin laajentaminen Power Appsin ja Power Automaten avulla
description: Tämä artikkeli käsittelee Microsoft Power Appsia ja Microsoft Power Automate'ta käyttäviä Microsoft Dynamics 365 Human Resourcesin laajennusesimerkkejä.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4036378ca70089a9978a9bf5fb48c058a2064cdc
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689491"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Laajentaminen Power Appsin ja Power Automaten avulla


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tämä artikkeli käsittelee Microsoft Power Appsia ja Microsoft Power Automate'ta käyttäviä Microsoft Dynamics 365 Human Resourcesin laajennusesimerkkejä. Voit tuoda kumpaankin esimerkkiin liitetyt ratkaisupaketin Power Apps-ympäristöön. Voit sitten käyttää paketteja joka ohjeena tai lähtökohtana, jonka avulla toteutat organisaatioon sopivia skenaarioita.

> [!IMPORTANT]
> Jos haluat käyttää tässä ohjeaiheessa kuvattuja malleja ja sovelluksia sellaisenaan, varmista testaamalla, että ne kattavat kaikki toteutukseen kuuluvat skenaariot.

## <a name="prerequisites"></a>Edellytykset

- Pakettien tuontia varten käyttäjät tarvitsevat **Ympäristön tekijä** -käyttöoikeuden.
- Sovellusten vientiä ja tuontia varten käyttäjillä on oltava Power Apps-palvelupaketin 2 käyttöoikeus tai Power Apps -palvelupaketin 2 kokeiluversion käyttöoikeus.

## <a name="integration-with-microsoft-365-power-automate"></a>Integrointi Microsoft 365:n, Power Automaten kanssa

**Microsoft 365 -integrointi** -sovelluksella voi purkaa kirjautuneiden käyttäjien tiimitiedot Microsoft 365:stä. Siinä viitataan henkilöstöhallinnon työntekijöihin, jotta työntekijöiden tunnistetyypit voidaan poimia. Esimiehet voivat tarkistaa työntekijän tunnustyyppien vanhentumispäivämäärät. He voivat myös lähettää sähköpostimuistutuksen, jos työntekijätunnuksen tyyppi on umpeutumassa. Power Automate integroituu Power Appsin kanssa tämän muistutuksen lähettämiseen. Vahvistus lähetetään takaisin Power Appsiin Power Automatesta, kun muistutus lähetetään. Tunnustyyppejä ovat ajokortti, passi ja muut hyväksyttävät henkilöllisyystodistusmuodot.

Voit laajentaa tätä sovellusta muihin tilanteisiin. Voit käyttää sitä esimerkiksi näyttämään ryhmän lomatiedot, kalenteritapahtumat ja kaikki ryhmäkohtaiset tapahtumat.

Voit ladata **Microsoft 365 -integroinnin Power Automate** -sovelluksen kohdassa [Microsoft 365 -integrointi](https://go.microsoft.com/fwlink/?linkid=2081787).

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate – SQL-yhteys ja toteutus

**Power Automate – SQL-yhteys ja toteutus** -malli muodostaa yhteyden Microsoft SQL Serveriin ja mahdollistaa SQL-kyselyjen suorittamisen.

Vaikka tämä malli lukee ja päivittää SQL-tauluja, voit laajentaa ja käyttää sitä muissa skenaarioissa. Sen avulla voit esimerkiksi täyttää valmistelutaulu Dataversessä SQL Serverin tietueilla sekä synkronoida valmistelutaulu säännöllisesti käyttämällä SQL Serverin lisäävää työntöä.

Edistynyt kysely on integroitu virtauksen kanssa, jotta tietojen muuntaminen ja lisäävä työntö voidaan ottaa käyttöön.

Voit ladata **Power Automate – SQL-yhteys ja toteutus** -mallin Microsoft Download Centerin kohdassa [Power Automate – SQL-yhteys ja toteutus](https://go.microsoft.com/fwlink/?linkid=2081789).

## <a name="additional-resources"></a>Lisäresurssit

[Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
