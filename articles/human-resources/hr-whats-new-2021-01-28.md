---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (28. tammikuuta 2021)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 28. tammikuuta 2021 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36509cc5663073fd1e3b7f41a600c7816bfbdff6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791242"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (28. tammikuuta 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia, muuttuneita tai pian tulossa olevia ominaisuuksia.

Lisätietoja päivitysprosessista ja aikataulusta on kohdassa [Päivitysprosessi](hr-admin-setup-update-process.md).

Lisätietoja uusista ominaisuuksista ja niiden odotetuista yleisen saatavuuden päivämääristä on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Tässä julkaisussa

Tämä julkaisu sisältää seuraavat uudet ominaisuudet ja ohjelmakorjaukset. Muutokset koskevat koontiversion numeroa 8.1.3906.

### <a name="new-features"></a>Uudet ominaisuudet

Seuraavat ominaisuudet ovat yleisesti saatavana tässä julkaisussa.

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Edun syykoodien integroiminen **Henkilöstöhallinta**-työtilaan | -- | [Määritä syykoodit](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Ohjelmavirhekorjaukset

Tämä julkaisu sisältää seuraavat ohjelmakorjaukset.

> [!NOTE]
> Tavoitteena on, että nämä tiedot ovat käytettävissä mahdollisimman pian. Tämän ohjeaiheen päivitys saattaa sisältää ohjelmakorjauksia, jotka on otettu käyttöön koontiversiossa tämän ohjeaiheen alkuperäisen julkaisin jälkeen.


| Ongelman numero | Varasto-otto |  kuvaus |
| --- | --- | --- |
| 539456 | Kalenterissa näkyy lomatyyppi osoitintekstissä, kun vain **Näytä vain poissaolo ilman tietoja** -parametri on otettu käyttöön. | Kun **Näytä vain poissaolo ilman tietoja** on käytössä, pyynnön päivämäärä näkyy nyt osoitettaessa. |
| 528907 | Kun työntekijäroolille myönnetään käyttöoikeus yritykselle, esimiehet eivät voi nähdä työntekijän itsepalvelun **Oma ryhmä** -alueen työntekijöiden saldoaktiviteetteja. |Kun valitset tämän vaihtoehdon, esimiehet voivat jatkaa saldotehtävän katsomista. |
| 526280 | Käyttöoikeusvirhe kohteissa HcmWorkerEntity, HcmEmployeeEntity ja HcmContractorEntity. | Käyttäjät, jotka eivät ole järjestelmänvalvojaroolissa eivät pysty viemään lueteltuja yksiköitä NationalityCountryRegion -kentän käyttöoikeusvirheen vuoksi. Tämän tiedon viemiseen tarvitaan edelleen seuraavat käyttöoikeudet: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain ja HCMContractorEntityView. |
| 542147 | **Pankkitilin numero**- ja **Pankkikoodi**-kentät ovat pakollisia lisättäessä pankkitiliä työntekijän itsepalvelun kautta. | Microsoft on korjannut virheen, jossa työntekijöiden oli annettava **Pankkitilin numero**- ja **Pankkikoodi**-kentät pankkitilitietoja lisättäessä. Nämä kentät eivät ole enää pakollisia tallennettaessa uusia pankkitilitietoja. |
| 543641 | Postinumeroa ei täytetä sähköiseen raportointiin. | Korjattu virhe, jossa postinumero ei täyty ACA-raportille kattavuuskoodeille L–Q. |
| 545402 | Poista 404-virheitä lisäämällä UserBranding.js-tiedostoon reititysmuutos. | Käyttäjän ei enää pitäisi nähdä konsolissa 404-virheitä. |

## <a name="in-preview"></a>Esiversiossa   

Seuraavat uudet ominaisuudet ovat esiversioita. Lisätietoja ominaisuuksien ottamisesta käyttöön tai poistamisesta käytöstä on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

| Ominaisuus | Julkaisusuunnitelma | Dokumentaatio |
| --- | --- | --- |
| Microsoft Teamsin Human Resources -sovellus | [Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teamsin Human Resources -sovellus](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md) |
| Yritystenvälinen näkymä esimiesten lomia varten | [Yritystenvälinen näkymä työntekijöiden lomia varten](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Loma- ja poissaoloparametrien määrittäminen](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

## <a name="coming-soon"></a>Tulossa pian

| Ominaisuus | Tietoja |
| --- | --- |
| Etujen rekisteröinnin sähköpostivahvistus | Tämä toiminto antaa mahdollisuuden lähettää vahvistussähköposti lähetetään työntekijöille näiden poistuessa etuihin rekisteröitymisen kokemuksesta työntekijän itsepalvelussa. Tämä toiminto on käytettävissä 1. helmikuuta. Lisätietoja: [Etujen hallinnan parametrien määrittäminen yritystä kohti](hr-benefits-setup-parameters-per-company.md). |
| Työnkulku voi hyväksyä työntekijöidensä esimiehen syöttämät osaamisalueet automaattisesti. | Tulossa pian. |

Täydellinen luettelo suunnitelluista ominaisuuksista ja niiden aikataulutetuista julkaisuista on kohdassa [Dynamics 365 Human Resourcesin vuoden 2021 1. julkaisuaallon yleiskatsaus](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataversen terminologiapäivitykset

Marraskuusa 2020 alkaen Common Data Servicen niimeksi on muutettu [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro). Lisätietoja: [virallinen ilmoitus](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) Power Apps -blogissa. Nimen muutoksen yhteydessä on päivitetty hieman Dataversen termistöä. Esimerkiksi *entiteetti* on nyt *taulukko* ja *kenttä* *sarake*. Lisätietoja on kohdassa [Termistön päivitykset](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Tässä versiossa Dataversen ja Dynamics 365 Human Resources -integrointiin liittyvät termit on päivitetty sovelluksen läpi näiden muutosten huomioonottamista varten. Esimerkiksi **Common Data Service -integrointi** -lomake **Microsoft Dataverse -integrointi**.

Lisätietoja Microsoft Dataversen ja Dynamics 365 Human Resourcesin integroinnista on kohdassa [Microsoft Dataverse -integroinnin määritys](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) ja [Microsoft Dataverse -virtuaalitaulujen määritys](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="see-also"></a>Lisätietoja

[Human Resourcesin uudet ja muuttuneet ominaisuudet](hr-admin-whats-new.md)</br>
[Yhteenveto Dynamics 365 Human Resourcesin vuoden 2021 julkaisuaallosta 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Päivitysprosessi](hr-admin-setup-update-process.md)</br>
[Ominaisuuksien hallinta](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]