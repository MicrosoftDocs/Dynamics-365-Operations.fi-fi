---
title: Etujen Power BI -sisältö
description: Tässä artikkelissa käsitellään etujen Power BI -sisältöä.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.search.form: HcmBenefitWorkspace
ms.openlocfilehash: ed1fd0b86e44d022a4858e3b5bc61c83a8efd395
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206654"
---
# <a name="benefits-power-bi-content"></a>Etujen Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään **etujen** Microsoft Power BI -sisältöä. Siinä selitetään, miten sisältyvät raportit avataan, sekä kerrotaan sisältöpaketin muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
**Etujen** Power BI -sisällön edut näkyvät **Etujen hallinta** -työtilassa, jos käytössäsi on jokin seuraavista tuotteista:

- Microsoft Dynamics 365 Finance
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön
**Etujen** Power BI -sisältöön sisältyvissä raporteissa on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                      | Sisältö                                                                                       |
|-----------------------------|------------------------------------------------------------------------------------------------|
| Edun rekisteröinnin yleiskatsaus | Eniten ja vähiten rekisteröidyt suunnitelmat, työntekijäryhmäkohtainen rekisteröityminen ja valitut etusuunnitelmavaihtoehdot |
| Työsuhde-edut           | Työntekijän voimaanastuminen valitun edun mukaan                                                        |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
**Etujen** Power BI -sisällön raporteissa käytetään seuraavia tietoja. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältö perustuu.

| Kokonaisuus                   | Sisältö                                                                                                   | Suhteet muihin yksiköihin |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalenterin vastakirjaus          | Kalenterin siirtymät raporttien osittamiseen                                                                          | Aiemmin määritetty toimi, toimitrendi, työntekijätrendi, poistettu työntekijä |
| Yritys                   | Yritykset, joiden mukaan raportit suodatetaan                                                                             | Nykyinen kompensaatio, nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Kompensaatio             | Maksut ja niiden tiheys ajan myötä                                                                           | Nykyinen kompensaatio, nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Nykyinen kompensaatio     | Maksut ja niiden tiheys nykyiseen päivämäärään                                                              | Yritys, kompensaatio, demografia, työ, toimi |
| Nykyinen toimi         | Paikat nykyiseen pvm:ään asti, täysiaikaista vastaavat, avoimet paikat ja avoimista täytetyiksi -paikat | Työ, toimi |
| Nykyinen työntekijä         | Työntekijät nykyisellä päivämäärällä, ikä ja henkilöstömäärä                                                         | Yritys, kompensaatio, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, työntekijän nimike, demografia, työ, työsuhde, toimi, edut |
| Päivämäärä                     | Päiviä, viikkoja, kuukausia ja vuosia                                                                             | Aiemmin määritetty toimi, toimitrendi, poistettu työntekijä,. työntekijätrendi |
| Demografia             | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty                                                   | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työsuhde               | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                                                                  | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Maantieteellinen sijainti      | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                                                           | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työ                      | Tehtävä, tyyppi ja nimike                                                                                  | Nykyinen sijainti, nykyinen työntekijä |
| Aiemmin määritetty toimi | Työtehtävän syy, aloituspvm, loppupvm ja työ                                                           | Kalenterin vastakirjaus, päivämäärä, työ, toimi |
| Sijainti                 | Osasto, FTE, toimi, toimen tyyppi ja nimike                                                        | Nykyinen sijainti, nykyinen työntekijä |
| Toimitrendi           | Toimien ajan mukaan, FTE ja työ                                                                          | Kalenterin vastakirjaus, päivämäärä, työ, toimi |
| Raportoi:               | Etunimi , sukunimi ja koko nimi                                                                       | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Poistettu työntekijä      | Poistetut työntekijät, poistopäivämäärä, nimike, toimi ja työ                                           | Yritys, kompensaatio, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, kalenterin vastakirjaus, päivämäärä, työntekijän nimike, demografia, työsuhde, työ, toimi, edut |
| Edut                 | Voimaantulopvm, etuvaihtoehto, etusuunnitelma ja etutyyppi                                             | Nykyinen nimi, poistettu työntekijä, työntekijätrendi |
| Työntekijän nimi            | Etunimi , sukunimi ja koko nimi                                                                       | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työntekijän nimike           | Nimike ja virkaikä                                                                                   | Nykyinen työntekijä, poistettu työntekijä, työntekijätrendi |
| Työntekijätrendi           | Työntekijät ajan kuluessa, henkilöstömäärä, yritys ja toimi                                                        | Yritys, kompensaatio, maantieteellinen sijainti, työntekijän nimi, raportoinnin kohde, kalenterin vastakirjaus, päivämäärä, työntekijän nimike, demografia, työsuhde, työ, edut |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
