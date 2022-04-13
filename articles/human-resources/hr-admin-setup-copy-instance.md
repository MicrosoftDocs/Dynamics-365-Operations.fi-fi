---
title: Kopioi esiintymä
description: Microsoft Dynamics 365 Human Resources -tietokannan voi kopioida eristysympäristöön Microsoft Dynamics Lifecycle Servicesin (LCS) avulla.
author: twheeloc
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 04987f18542ff331124f5224e4b1240672874e83
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533961"
---
# <a name="copy-an-instance"></a>Kopioi esiintymä

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]


Microsoft Dynamics 365 Human Resources -tietokannan voi kopioida eristysympäristöön Microsoft Dynamics Lifecycle Servicesin (LCS) avulla. Jos käytössä on toinen eristysympäristö, voit kopioida myös tietokannan siitä kohde-eristysympäristöön.

Esiintymää kopioitaessa kannattaa muistaa seuraavat vinkit:

- Korvattavan Human Resources -esiintymän on oltava eristysympäristö.

- Kopioinnin lähde- ja kohdeympäristöjen on oltava samalla alueella. Et voi kopioida eri alueiden välillä.

- Sinun on oltava kohdeympäristön järjestelmänvalvoja, jotta voit kirjautua siihen, kun olet kopioinut esiintymän.

- Kun kopioit Human Resourcesin tietokannan, et kopioi elementtejä (sovelluksia tai tietoja), jotka sisältyvät Microsoft Power Apps -ympäristöön. Lisätietoja elementtien kopioinnista Power Apps-ympäristössä on kohdassa [Ympäristön kopioiminen](/power-platform/admin/copy-environment). Korvattavan Power Apps-ympäristön on oltava eristysympäristö. Sinun on oltava yleinen vuokraajan järjestelmänvalvoja, jotta voit muuttaa Power Apps-tuotantoympäristön eristysympäristöksi. Lisä tietoja Power Apps-ympäristön muuttamisesta on kohdassa [Esiintymän vaihtaminen](/dynamics365/admin/switch-instance).

- Jos kopioit esiintymään eristysympäristöön ja haluat integroida eristysympäristön Dataversen kanssa, mukautetut kentät on otettava uudelleen Dataverse-taulukoissa. Lisätietoja on kohdassa [Mukautettujen kenttien käyttäminen Dataversessä](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Human Resources -tietokannan kopioinnin vaikutukset

Human Resources -tietokannan kopioinnin yhteydessä tapahtuu seuraavaa:

- Kopiointiprosessi poistaa aiemmin luodun tietokannan kohdeympäristöstä. Kun kopiointiprosessi on suoritettu, et voi palauttaa aiemmin luotua tietokantaa.

- Kohdeympäristö ei ole käytettävissä, ennen kuin kopiointiprosessi on valmis.

- Microsoft Azure Blob -tallennustilassa olevia asiakirjoja ei kopioida ympäristöstä toiseen. Tämän vuoksi liitettyjä asiakirjoja ja malleja ei kopioida, ja ne jäävät lähdeympäristöön.

- Mitkään käyttäjät, paitsi käyttäjät, joilla on järjestelmänvalvojan käyttöoikeusrooli ja muu sisäisen palvelun käyttäjätili, eivät ole käytettävissä. Järjestelmänvalvojakäyttäjä voi poistaa tietoja tai piilottaa niitä näkyvistä, ennen kuin muut käyttäjät pääsevät takaisin järjestelmään.

- Käyttäjän, jolla on järjestelmänvalvojan käyttöoikeusrooli, on suoritettava vaadittavat muutokset määrityksiin, kuten yhdistettävä integroinnin päätepisteet uudelleen tiettyihin palveluihin tai URL-osoitteisiin.

## <a name="copy-the-human-resources-database"></a>Human Resources -tietokannan kopiointi

Jos haluat suorittaa tämän tehtävän, kopioi ensin esiintymä ja kirjaudu sitten Microsoft Power Platform -hallintakeskukseen ja kopioi Power Apps-ympäristösi.

> [!WARNING]
> Kun kopioit esiintymän, tietokanta poistetaan kohde-esiintymästä. Kohde-esiintymä ei ole käytettävissä tämän prosessin aikana.

1. Kirjaudu LCS:ään ja valitse LCS-projekti, joka sisältää kopioitavan esiintymän.

2. Valitse LCS-projektin **Human Resources -sovelluksen hallinta** -ruutu.

3. Valitse kopioitava esiintymä ja sitten **Kopioi**.

4. Valitse korvattava esiintymä **Kopioi esiintymä** -tehtäväruudusta ja valitse sitten **Kopioi**. Odota, että **Kopioi tila** -kentän arvoksi päivittyy **Valmis**.

   ![[Valitse korvattava esiintymä.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Valitse **Power Platform** ja kirjaudu Microsoft Power Platform -hallintakeskukseen.

   ![[Valitse Power Platform.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Valitse kopioitava Power Apps-ympäristö ja sitten **Kopioi**.

7. Kun kopiointiprosessi on valmis, kirjaudu kohde-esiintymään ja ota Dataverse -integrointi käyttöön. Lisätietoja ja -ohjeita on kohdassa [Dataverse -integroinnin määrittäminen](./hr-admin-integration-common-data-service.md).

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

Osaa näistä elementeistä ei kopioida, koska ne ovat ympäristökohtaisia. Esimerkkejä tästä ovat tietueet **BatchServerConfig** ja **SysCorpNetPrinters**. Toisia elementtejä ei kopioida palvelupyyntöjen suuren määrän vuoksi. Esimerkki:

- Sähköpostien kaksoiskappaleita saatetaan lähettää, koska SMTP on edelleen käytössä käyttäjän hyväksyntätestauksen ympäristössä (eristys).

- Virheellisiä integrointisanomia saatetaan lähettää, koska erätyöt ovat yhä käytössä.

- Käyttäjät saattavat olla käytössä, ennen kuin järjestelmänvalvojat voivat suorittaa päivityksen jälkeiset puhdistustoiminnot.

Myös seuraavat tilat muuttuvat, kun esiintymä kopioidaan:

- Kaikille muille käyttäjille paitsi käyttäjille, joilla on järjestelmänvalvojan käyttöoikeusrooli, määritetään asetukseksi **Ei käytössä**.

- Kaikki erätyöt joitakin järjestelmätöitä lukuun ottamatta asetetaan tilaan **Pidätä**.

## <a name="environment-admin"></a>Ympäristön järjestelmänvalvoja

Kaikki eristetyn kohdeympäristön käyttäjät, myös järjestelmänvalvojat, korvataan lähdeympäristön käyttäjillä. Varmista ennen esiintymän kopioimista, että olet lähdeympäristön järjestelmänvalvoja. Jos et ole, et voi kirjautua eristettyyn kohdeympäristöön, kun kopiointi on valmis.

Kaikki muut kuin järjestelmänvalvojakäyttäjät poistetaan käytöstä eristetyssä kohdeympäristössä, jotta estetään ei-toivotut kirjautumiset siihen. Järjestelmänvalvojat voivat tarvittaessa ottaa käyttäjiä uudelleen käyttöön.

## <a name="apply-custom-fields-to-dataverse"></a>Mukautettujen kenttien käyttäminen Dataversessä

Jos kopioit esiintymään eristysympäristöön ja haluat integroida eristysympäristön Dataversen kanssa, mukautetut kentät on otettava uudelleen Dataverse-taulukoissa.

Tee seuraavat jokaisen Dataverse-taulukoissa näkyvän mukautetun kentän kohdalla:

1. Siirry mukautettuun kenttään ja valitse **Muokkaa**.

2. Poista kunkin sellaisen cdm_*-entiteetin **Käytössä**-kentän valinta, jossa mukautettu kenttä on otettu käyttöön.

3. Valitse **Ota muutokset käyttöön**.

4. Valitse **Muokkaa** uudelleen.

5. Valitse kunkin sellaisen cdm_*-entiteetin **Käytössä**-kenttä, jossa mukautettu kenttä on otettu käyttöön.

6. Valitse **Ota muutokset käyttöön** uudelleen.

Valinnan poistamisprosessi, muutosten käyttöönottaminen, uudelleen valitseminen ja muutosten ottaminen uudelleen käyttöön saa rakenteen päivittämään Dataversen sisällyttämään mukautetut kentät.

Lisätietoja mukautetuista kentistä on kohdassa [Mukautettujen kenttien luonti ja käyttö](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>Lisätietoja

[Valmistele Human Resources](hr-admin-setup-provision.md)</br>
[Poista esiintymä](hr-admin-setup-remove-instance.md)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
