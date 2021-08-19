---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (22. helmikuuta 2021)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 22. helmikuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 379a902489bdccdfa3490a830cc3b0bbf7639e7f0b62079a3ff3a999b0a7c412
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721556"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (22. helmikuuta 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.3988.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Dynamics 365 Human Resources -sovellus Microsoft Teamsille | [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teamsin Human Resources -sovellus](./hr-admin-teams-leave-app.md)<br>[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.

| Ongelman numero | Varasto-otto |  kuvaus |
| --- | --- | --- |
| 529994 | **Työntekijä**-lomakkeen **Tunnetaan nimellä** -kentän muokkaaminen ei käynnistä Dataverse-päivitystä | Korjattiin ongelma, jossa Dataverse ei päivity, kun **Työntekijä**-lomakkeen **Tunnetaan nimellä** -kenttä päivitetään. |
| 532651 | Kompensaatioanalyysin PBI-raportti ei käytä valuuttamuunnosta koko yrityksen tilastojen laskennassa | Korjattiin ongelma, jossa kompensaatioanalyysin PBI-raportit eivät muuntaneet valuuttoja oikein. |
| 552226 | Elinkaaritapahtuman käsittely sulkee ja avaa suunnitelmat uudelleen useita kertoja yhdelle elinkaaritapahtumalle  | Korjattiin ongelma, jossa elinkaaritietue luotiin työntekijän jokaiselle yritykselle, jos työntekijä kuului useisiin yrityksiin elinkaaritapahtuman tapahtuessa. Käsiteltävä yritys täytyy valita elinkaaritapahtumia käsiteltäessä. Käsittelylogiikka ei kuitenkaan rajoita itseään vain tähän yritykseen. Sen sijaan se käsittelee kaikki yritykset ja sulkee ja avaa suunnitelmat uudelleen valitussa yrityksessä. Tämä toiminto käsittelee elinkaaritapahtuman useita kertoja samassa yrityksessä, jolloin kaikki suunnitelmat, joihin elinkaaritapahtuma vaikuttaa, suljetaan tai avataan uudelleen useita kertoja. |
| 518064 | Vian yksi riippuvainen edustaja valittu kelpoisuussuunnitelmissa, kun yksi tai useampi on merkitty oletusedustajiksi | Korjattiin ongelma, jossa useita oletusedustajia ei valittu automaattisesti kelpoisuussuunnitelmissa. Nyt voit myös nimittää henkilökohtaiselle yhteyshenkilölle ensisijaisen edunsaajan. Ensisijainen edunsaaja näytetään 100 %:in arvona kelpoisuussuunnitelmissa, jossa on useita edunsaajia. |
| 552365 | Tuo oma tietokantasi (BYOD) -vientityöt epäonnistuvat alustapäivityksen 40 jälkeen | Korjattiin ongelma, jossa BYOD-vientityöt epäonnistuivat, kun alustapäivitys 40 otettiin käyttöön ympäristössä. |
| 547123 | Rajoita koontinäkymän tehtäväluettelossa kyseltyjen tehtävien määrä | Tehtäväluettelossa voi näyttää nyt enintään 15 tehtävää. Tämä korjaa suorituskykyongelman, joka aiheutui liian monen tehtävän lataamisesta. |

## <a name="in-preview"></a>Esiversiossa

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Yritystenvälinen näkymä esimiesten lomia varten | [Yritystenvälinen näkymä työntekijöiden lomia varten](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Loma- ja poissaoloparametrien määrittäminen](./hr-leave-and-absence-parameters.md) |
| Etujen hallinnan työtila | [Etujen hallinnan työtila (esikatselu)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Etujen hallinnan työtila](hr-benefits-management-workspace.md) |
| Estä työntekijöitä muokkaamasta yrityksen yhteystietoja | [Estä työntekijöitä muokkaamasta yrityksen yhteystietoja](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Henkilökohtaisten tietojen muokkaamisen rajoittaminen](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Tulossa pian

| Ominaisuus | Tietoja |
| --- | --- |
| Työnkulku voi hyväksyä työntekijöidensä esimiehen syöttämät osaamisalueet automaattisesti. | Tulossa pian. |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataversen terminologiapäivitykset

Marraskuusa 2020 alkaen Common Data Servicen niimeksi on muutettu [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Lisätietoja: [virallinen ilmoitus](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) Power Apps -blogissa. Dataversen termistöä on päivitetty hieman tämän nimen muutoksen yhteydessä. Esimerkiksi *entiteetti* on nyt *taulukko* ja *kenttä* *sarake*. Lisätietoja on kohdassa [Termistön päivitykset](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Tässä versiossa Dataversen ja Dynamics 365 Human Resources -integrointiin liittyvät termit on päivitetty sovelluksen läpi näiden muutosten huomioonottamista varten. Esimerkiksi **Common Data Service -integrointi** -lomake **Microsoft Dataverse -integrointi**.

Lisätietoja Microsoft Dataversen ja Dynamics 365 Human Resourcesin integroinnista on kohdassa [Microsoft Dataverse -integroinnin määritys](./hr-admin-integration-common-data-service.md) ja [Microsoft Dataverse -virtuaalitaulujen määritys](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Palveluiden käyttöönoton päivitykset

Olemme muuttamassa alueellisten palvelupäivitysten käyttöönottoa 22. helmikuuta 2021 alkaen. Muutoksiin sisältyy Human Resources -palvelun päivitysten järjestyksen muuttaminen globaaleille alueille sekä päivityksen vaiheiden välisten odotusaikojen muutokset. Nämä muutokset sallivat meidän noudattaa paremmin turvallisia käyttöönottokäytäntöjä, joiden avulla voimme parantaa palvelun vakautta, laatua ja tukea.

Noudatamme jatkossakin kahden viikon käyttöönottotahtia. Asiakkaat saattavat kuitenkin huomata, että päivitykset otetaan tavallisesti käyttöön heidän Human Resources -ympäristöissään tässä kahden viikon syklissä eri päivänä kuin aiemmissa versioissa.

Lisätietoja palvelun päivitysprosessista on kohdassa [Päivitysprosessi](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]