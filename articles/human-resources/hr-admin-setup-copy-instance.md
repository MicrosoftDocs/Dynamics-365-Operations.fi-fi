---
title: Kopioi esiintymä
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008836"
---
# <a name="copy-an-instance"></a>Kopioi esiintymä

Microsoft Dynamics 365 Human Resources -tietokannan voi kopioida eristysympäristöön Microsoft Dynamics Lifecycle Servicesin (LCS) avulla. Jos käytössä on toinen eristysympäristö, voit kopioida myös tietokannan siitä kohde-eristysympäristöön.

Jos haluat kopioida esiintymän, sinun on varmistettava seuraavat asiat:

- Korvattavan Human Resources -esiintymän on oltava eristysympäristö.

- Kopioinnin lähde- ja kohdeympäristöjen on oltava samalla alueella. Et voi kopioida eri alueiden välillä.

- Sinun on oltava kohdeympäristön järjestelmänvalvoja, jotta voit kirjautua siihen, kun olet kopioinut esiintymän.

- Kun kopioit Human Resourcesin tietokannan, et kopioi elementtejä (sovelluksia tai tietoja), jotka sisältyvät Microsoft PowerApps -ympäristöön. Lisätietoja elementtien kopioinnista PowerApps-ympäristössä on kohdassa [Ympäristön kopioiminen](https://docs.microsoft.com/power-platform/admin/copy-environment). Korvattavan PowerApps-ympäristön on oltava eristysympäristö. Sinun on oltava yleinen vuokraajan järjestelmänvalvoja, jotta voit muuttaa PowerApps-tuotantoympäristön eristysympäristöksi. Lisä tietoja PowerApps-ympäristön muuttamisesta on kohdassa [Esiintymän vaihtaminen](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>Human Resources -tietokannan kopioinnin vaikutukset

Human Resources -tietokannan kopioinnin yhteydessä tapahtuu seuraavaa:

- Kopiointiprosessi poistaa aiemmin luodun tietokannan kohdeympäristöstä. Kun kopiointiprosessi on suoritettu, et voi palauttaa aiemmin luotua tietokantaa.

- Kohdeympäristö ei ole käytettävissä, ennen kuin kopiointiprosessi on valmis.

- Microsoft Azure Blob -tallennustilassa olevia asiakirjoja ei kopioida ympäristöstä toiseen. Siksi liitettyjä asiakirjoja ja malleja ei kopioida, ja ne jäävät lähdeympäristöön.

- Mitkään käyttäjät, paitsi järjestelmänvalvojakäyttäjä ja muut sisäisen palvelun käyttäjätilit eivät ole käytettävissä. Siten järjestelmänvalvojakäyttäjä voi poistaa tietoja tai piilottaa niitä näkyvistä, ennen kuin muut käyttäjät pääsevät takaisin järjestelmään.

- Järjestelmänvalvojakäyttäjän on suoritettava vaadittavat muutokset määrityksiin, kuten yhdistettävä integroinnin päätepisteet uudelleen tiettyihin palveluihin tai URL-osoitteisiin.

## <a name="copy-the-human-resources-database"></a>Human Resources -tietokannan kopiointi

Jos haluat suorittaa tämän tehtävän, kopioi ensin esiintymä ja kirjaudu sitten Microsoft Power Platform -hallintakeskukseen ja kopioi PowerApps-ympäristösi.

> [!WARNING]
> Kun kopioit esiintymän, tietokanta poistetaan kohde-esiintymästä. Kohde-esiintymä ei ole käytettävissä tämän prosessin aikana.

1. Kirjaudu LCS:ään ja valitse LCS-projekti, joka sisältää kopioitavan esiintymän.

2. Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.

3. Valitse kopioitava esiintymä ja sitten **Kopioi**.

4. Valitse korvattava esiintymä **Kopioi esiintymä** -tehtäväruudusta ja valitse sitten **Kopioi**. Odota, että **Kopioi tila** -kentän arvoksi päivittyy **Valmis**.

   ![[Valitse korvattava esiintymä](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Valitse **Power Platform** ja kirjaudu Microsoft Power Platform -hallintakeskukseen.

   ![[Valitse Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Valitse kopioitava PowerApps-ympäristö ja sitten **Kopioi**.

7. Kun kopiointiprosessi on valmis, kirjaudu kohde-esiintymään ja ota Common Data Service -integrointi käyttöön. Lisätietoja ja -ohjeita on kohdassa [Common Data Service -integroinnin määrittäminen](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

## <a name="data-elements-and-statuses"></a>Tietoelementit ja tilat

Seuraavia tietoelementtejä ei kopioida, kun kopioit Human Resources -esiintymän:

- Sähköpostiosoitteet **LogisticsElectronicAddress**-taulukossa

- Erätyöhistoria taulukoissa **BatchJobHistory**, **BatchHistory** ja **BatchConstraintHistory**

- Simple Mail Transfer Protocol (SMTP) -salasanaa **SysEmailSMTPPassword**-taulukossa

- SMTP-välityspalvelin **SysEmailParameters**-taulukossa

- Tulostuksenhallinta-asetukset taulukoissa **PrintMgmtSettings** ja **PrintMgmtDocInstance**

- Ympäristökohtaiset tietueet taulukoissa **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ja **BatchServerGroup**

- Asiakirjojen liitteet DocuValue-taulukossa. Nämä liitteet sisältävät kaikki lähdeympäristössä korvatut Microsoft Office -mallit

- Yhteysmerkkijono taulukossa **PersonnelIntegrationConfiguration**

Osaa näistä elementeistä ei kopioida, koska ne ovat ympäristökohtaisia. Esimerkkejä tästä ovat tietueet **BatchServerConfig** ja **SysCorpNetPrinters**. Toisia elementtejä ei kopioida palvelupyyntöjen suuren määrän vuoksi. Esimerkiksi sähköpostien kaksoiskappaleita saatetaan lähettää, koska SMTP on edelleen käytössä käyttäjän hyväksyntätestauksen ympäristössä (eristys), virheellisiä integrointisanomia saatetaan lähettää, koska erätyöt ovat yhä käytössä ja käyttäjät saattavat olla käytössä, ennen kuin järjestelmänvalvojat voivat suorittaa päivityksen jälkeiset puhdistustoiminnot.

Lisäksi seuraavat tilat muuttuvat, kun esiintymä kopioidaan:

- Kaikkien käyttäjien tilaksi järjestelmänvalvojaa lukuun ottamatta asetetaan **Pois käytöstä**.

- Kaikki erätyöt joitakin järjestelmätöitä lukuun ottamatta asetetaan tilaan **Pidätä**.

## <a name="environment-admin"></a>Ympäristön järjestelmänvalvoja

Kaikki eristetyn kohdeympäristön käyttäjät, myös järjestelmänvalvojat, korvataan lähdeympäristön käyttäjillä. Varmista ennen esiintymän kopioimista, että olet kohdeympäristön järjestelmänvalvoja. Jos et ole, et voi kirjautua eristettyyn kohdeympäristöön, kun kopiointi on valmis.

Kaikki muut kuin järjestelmänvalvojakäyttäjät poistetaan käytöstä eristetyssä kohdeympäristössä, jotta estetään ei-toivotut kirjautumiset siihen. Järjestelmänvalvojat voivat tarvittaessa ottaa käyttäjiä uudelleen käyttöön.
