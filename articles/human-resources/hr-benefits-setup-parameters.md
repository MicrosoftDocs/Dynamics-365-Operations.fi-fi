---
title: Aseta etujenhallinnan parametrit
description: Määritä etujen hallinnan parametrit Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cb9dd6eb8ef840dab54eabab8526200a3a8e21f0
ms.sourcegitcommit: e100c1c7c8dcdacf066defc206dd2f44b8ce6100
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4057025"
---
# <a name="set-benefits-management-parameters"></a>Etujen hallinnan parametrien määrittäminen

Ennen kuin voit määrittää lomasuunnitelmia Microsoft Dynamics 365 Human Resourcesissa, sinun täytyy määrittää etujen hallintaparametrit. Nämä parametrit määrittävät oletusarvot, syykoodit ja muut asetukset.

## <a name="configure-general-parameters"></a>Konfiguroi yleiset parametrit

1. Valitse **Etujen hallinta** -työtilassa **Asetukset** -kohdassa **Henkilöstöhallinnon jaetut parametrit**.

2. Määritä **Yleiset** -välilehdelle seuraavien kenttien arvot:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Maa/alue** | **Maa/alue** -kenttä määrittää postinumeroiden/valtioiden näyttöjärjestyksen. Valittu maa näkyy ensimmäisenä avattavassa luettelossa. |
   | **Rekisteröinnin syykoodi** | Valitse oletussyykoodi, jota käytetään, kun työntekijän suunnitelmat luodaan avoimen rekisteröinnin käsittelyn aikana. |
   | **Peruutuksen syykoodi** | Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan. Se näkyy valintaikkunassa peruutusprosessin aikana. Käyttäjät voivat tarvittaessa muuttaa **peruutuksen syykoodia**. |
   | **Uudelleenavauksen syykoodi** | Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma avataan uudelleen. Se näkyy valintaikkunassa peruutusprosessin aikana. Käyttäjät voivat tarvittaessa muuttaa **uudelleen avaamisen syykoodia**. | 
   | **Elinkaaritapahtuman syykoodi** | Tapahtuma, jota käytetään elinkaaritapahtuman tapahtuessa. |
   | **Asteen muutoksen syykoodi** | Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan ja avataan uudelleen hinnan muutoksen päivitysprosessin aikana. Se ilmaisee, mitä tietuetta hinnan muutoksen päivitysprosessi on muuttanut. |
   | **Vuosittainen etupalkka** | Antaa mahdollisuuden määrittää työntekijän **Etuuksien vuosipalkka** -summan. Human Resources käyttää **Etuuksien vuosipalkka** -summaa määrittämään katetut summat kiinteän vuosittaisen kompensaatiosumman sijaan. |
   | **Uusi työntekijä on sallittu** | Määrittää, ovatko uudet työntekijät kelvollisia. |
   | **Uuden työntekijän rekisteröintikausi** | Ajanjakso, jolloin uusi osamaksu on sallittu.</br></br>**Huomautus** : Tämä asetus ohittaa uuden suunnitelman oikeutussääntöön määrittämäsi työhönottoajan jakson. |
   | **Oletusmaksutiheys** | Oletusmaksuväli, jota käytetään, kun uusia työntekijöitä lisätään. |
   | **Elinkaaritapahtumat ovat käytössä** | Mahdollistaa elinkaaritapahtumat. |
   | **Piilota vanhat etulomakkeet** | Sallii vanhojen etuuslomakkeiden piilottamisen. |

3. Valitse **Tallenna**.

## <a name="configure-employee-self-service-parameters"></a>Määritä työntekijän itsepalveluparametrit

1. Valitse **Etujen hallinta** -työtilassa **Asetukset** -kohdassa **Henkilöstöhallinnon parametrit**.

2. Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot:

   | Kenttä | kuvaus |
   | --- | --- |
   | **Edun vahvistus** | Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla. |
   | **Valitse edustajat automaattisesti** | Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella. |

3. Valitse **Tallenna**.
