---
title: Työhönoton Power BI -sisältö
description: Tässä ohjeaiheessa käsitellään työhönoton Power BI -sisältöä.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 36ea9f204b50b3d7a6c8e33e69a9c3fd7d82cd79d466e2b9547c6733aa294aea
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765119"
---
# <a name="recruiting-power-bi-content"></a>Työhönoton Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään **työhönoton** Microsoft Power BI -sisältöä. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
**Työhönoton** Power BI -sisältö näkyy **Työhönoton hallinta** -työtilassa.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Työhönoton hallinnan työtilan raportit ja visualisoinnit
**Työhönoton hallinta** -työtilassa on **Analytiikka**-välilehti. Välilehti sisältää työhönoton upotetun Power BI -sisällön. Sisällön yhdessä välilehdessä on yleiskatsaus ja muissa välilehdissä tarkempia tietoja. Seuraavassa taulukossa esitellään kunkin välilehden raportit.

| Raportti               | Sisältö |
|----------------------|----------|
| Työhönoton yleiskatsaus | Raporttien yhteenveto |
| Hakijan analyysi   | Hakijoiden kokonaismäärä, hakijat työn mukaan, hakijan lähteet, mies- ja naishakijoiden suhde sekä hakijat sijainnin mukaan |
| Hakijan tila     | Hakijat tyypin ja tilan mukaan sekä hakijan tila |
| Työhönoton analyysi  | Työhönoton nettosuhde, palkkaukseen kuluvat keskimääräiset päivät, epäonnistuneiden palkkausten prosenttiosuus, työhönoton kustannukset, työnoton ja hakeneiden suhde sekä hakijoiden ja työpaikkojen suhde työhönottoprojektin mukaan |

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Seuraavassa taulukossa on esitetty yksiköt, joihin **työhönoton** Power BI -sisältö on perustunut.

| Kokonaisuus               | Sisältö                                                         | Suhteet muihin yksiköihin |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Hakija            | Hakijat, palkatut hakijat, palkkauksen nettosuhde ja kustannukset          | Hakijan nimi, yritys, kalenterin vastakirjaus, päivämäärä, maantieteellinen sijainti, demografia, työ, media, työhönottoprojekti |
| Hakijan nimi       | Hakijan etunimi, sukunimi ja koko nimi                   | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Kalenterin vastakirjaus      | Kalenterin siirtymät raporttien osittamiseen                                | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Yritys               | Yritykset, joiden mukaan raportit suodatetaan                                   | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Päivämäärä                 | Päiviä, viikkoja, kuukausia ja vuosia                                   | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Demografia         | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty         | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Työsuhteessa oleva hakija   | Hakija, suorituskyky, alkupäivämäärä ja hakijan tyyppi           | Yritys, kalenterin vastakirjaus, päivämäärä, maantieteellinen sijainti, hakijan nimi, työsuhde, suoritus, työ, media, työhönottoprojekti |
| Työsuhde           | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                        | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Maantieteellinen sijainti  | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                 | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Työ                  | Tehtävä, tyyppi ja nimike                                        | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Mediat                | Hakijoiden lähde                                             | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Suoritus          | Pisteytys, kuvaus arviointimalli                            | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Työhönottoprojekti  | Projektin kuvaus, projektin tila ja avoimet paikat                | Hakijan, työsuhteessa oleva hakija, irtisanottu hakija |
| Irtisanottu hakija | Työntekijät, joiden työsuhde on päätetty, syy, suorituskyky ja työsuhteen päättymispäivä | Yritys, kalenterin vastakirjaus, päivämäärä, maantieteellinen sijainti, suoritus, demografia, työsuhde, media, työhönottoprojekti, hakijan nimi |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]