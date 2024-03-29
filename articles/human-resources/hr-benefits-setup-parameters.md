---
title: Etujen hallinnan ja työntekijän itsepalveluparametrien määrittäminen kaikille yrityksille
description: Etujen hallinnan ja työntekijän itsepalveluparametrien määrittäminen Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1bae79e47c3fa695ac239320eeee17b1a480f18
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336894"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Etujen hallinnan ja työntekijän itsepalveluparametrien määrittäminen kaikille yrityksille



Ennen kuin voit määrittää etusuunnitelmat Microsoft Dynamics 365 Human Resourcesissa, sinun täytyy määrittää etujen hallintaparametrit. Nämä parametrit määrittävät oletusarvot, syykoodit ja muut asetukset. 

## <a name="configure-general-parameters"></a>Konfiguroi yleiset parametrit

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon jaetut parametrit**.

2. Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot:

   | Kenttä | kuvaus |
   | --- | --- |
   | **Maa/alue** | **Maa/alue**-kenttä määrittää postinumeroiden/valtioiden näyttöjärjestyksen. Valittu maa näkyy ensimmäisenä avattavassa luettelossa. |
   | **Rekisteröinnin syykoodi** | Valitse oletussyykoodi, jota käytetään, kun työntekijän suunnitelmat luodaan avoimen rekisteröinnin käsittelyn aikana. |
   | **Peruutuksen syykoodi** | Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan. Se näkyy valintaikkunassa peruutusprosessin aikana. Käyttäjät voivat tarvittaessa muuttaa **peruutuksen syykoodia**. |
   | **Uudelleenavauksen syykoodi** | Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma avataan uudelleen. Se näkyy valintaikkunassa peruutusprosessin aikana. Käyttäjät voivat tarvittaessa muuttaa **uudelleen avaamisen syykoodia**. | 
   | **Elinkaaritapahtuman syykoodi** | Tapahtuma, jota käytetään elinkaaritapahtuman tapahtuessa. |
   | **Asteen muutoksen syykoodi** | Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan ja avataan uudelleen hinnan muutoksen päivitysprosessin aikana. Se ilmaisee, mitä tietuetta hinnan muutoksen päivitysprosessi on muuttanut. |
   | **Vuosittainen etupalkka** | Antaa mahdollisuuden määrittää työntekijän **Etuuksien vuosipalkka** -summan. Human Resources käyttää **Etuuksien vuosipalkka** -summaa määrittämään katetut summat kiinteän vuosittaisen kompensaatiosumman sijaan. |
   | **Uusi työntekijä on sallittu** | Määrittää, ovatko uudet työntekijät kelvollisia. |
   | **Uuden työntekijän rekisteröintikausi** | Ajanjakso, jolloin uusi osamaksu on sallittu.</br></br>**Huomautus**: Tämä asetus ohittaa uuden suunnitelman oikeutussääntöön määrittämäsi työhönottoajan jakson. |
   | **Oletusmaksutiheys** | Oletusmaksuväli, jota käytetään, kun uusia työntekijöitä lisätään. |
   | **Elinkaaritapahtumat ovat käytössä** | Mahdollistaa elinkaaritapahtumat. |
   | **Piilota vanhat etulomakkeet** | Sallii vanhojen etuuslomakkeiden piilottamisen. |
   | **Edun vahvistus** | Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla. |
   | **Valitse edustajat automaattisesti** | Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella. |

3. Valitse **Tallenna**.

## <a name="configure-employee-self-service-parameters"></a>Määritä työntekijän itsepalveluparametrit

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon parametrit**.

2. Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot:

   | Kenttä | kuvaus |
   | --- | --- |
   | **Edun vahvistus** | Etuuksien itsepalvelun kassalla käytettävä tarkistusteksti. |
   | **Valitse edustajat automaattisesti** | Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella. |

3. Valitse **Tallenna**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
