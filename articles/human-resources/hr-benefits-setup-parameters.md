---
title: Aseta etujenhallinnan parametrit
description: Määritä etujen hallinnan parametrit Microsoft Dynamics 365 Human Resourcesissa.
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
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008891"
---
# <a name="set-benefits-management-parameters"></a>Aseta etujenhallinnan parametrit

[!include [banner](includes/preview-feature.md)]

Ennen kuin voit määrittää lomasuunnitelmia Microsoft Dynamics 365 Human Resourcesissa, sinun on määritettävä etujen hallintaparametrit. Nämä parametrit määrittävät oletusarvot, syykoodit ja muut asetukset.

## <a name="configure-general-parameters"></a>Konfiguroi yleiset parametrit

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Parametrit**.

2. Määritä **Yleiset**-välilehdelle seuraavien kenttien arvot:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Maa/alue** | **Maa/alue**-kenttä määrittää postinumeroiden/valtioiden näyttöjärjestyksen. Valittu maa näkyy ensimmäisenä avattavassa luettelossa. |
   | **Rekisteröinnin syykoodi** | Valitse oletussyykoodi, jota käytetään, kun työntekijän suunnitelmat luodaan avoimen rekisteröinnin käsittelyn aikana. |
   | **Peruutuksen syykoodi** | Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan. Se näkyy valintaikkunassa peruutusprosessin aikana. Käyttäjät voivat tarvittaessa muuttaa **peruutuksen syykoodia**. |
   | **Uudelleenavauksen syykoodi** | Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma avataan uudelleen. Se näkyy valintaikkunassa peruutusprosessin aikana. Käyttäjät voivat tarvittaessa muuttaa **uudelleen avaamisen syykoodia**. | 
   | **Elinkaaritapahtuman syykoodi** | Tapahtuma, jota käytetään elinkaaritapahtuman tapahtuessa. |
   | **Asteen muutoksen syykoodi** | Syykoodi, jota käytetään, kun työsuhde-etuussuunnitelma peruutetaan ja avataan uudelleen hinnan muutoksen päivitysprosessin aikana. Se ilmaisee, mitä tietuetta hinnan muutoksen päivitysprosessi on muuttanut. |
   | **Uusi työntekijä on sallittu** | Määrittää, ovatko uudet työntekijät kelvollisia. |
   | **Uuden työntekijän rekisteröintikausi** | Ajanjakso, jolloin uusi osamaksu on sallittu.</br></br>**Huomautus**: Tämä asetus ohittaa uuden suunnitelman oikeutussääntöön määrittämäsi työhönottoajan jakson. | 
   | **Vuosipalkan lisäys** | Määrittää, lasketaanko **vuotuisen etuuspalkan** summa automaattisesti **työsuhteen lisätiedot** -kohdassa. Se perustuu työntekijän **Kiinteän kompensaatiotaksan**, **Keskituntien** ja **Maksutiheyden** mukaan.</br></br>**Keskimääräinen työaika** x **kiinteä taksa** x **maksutiheys** (# maksukaudet) = **vuotuinen etuuspalkka** </br></br>Jos joku **Keskimääräiset tunnit**-, **kiinteä kompensaatiotaksa**- tai **maksutiheys** -kenttien arvo muuttuu, järjestelmä laskee työntekijän **vuotuisen etuuspalkan** automaattisesti uudelleen muuttuneiden arvojen perusteella. Järjestelmä luo **päivämäärän voimaantulo** -tietueen, joka määrittää muutoksen tarkan päivämäärän ja ajan. Voit tarvittaessa muokata **vuotuisen etuuspalkan** määrää manuaalisesti. |
   | **Elinkaaritapahtumat ovat käytössä** | Mahdollistaa elinkaaritapahtumat. |
   | **Piilota vanhat etulomakkeet** | Sallii vanhojen etuuslomakkeiden piilottamisen. |

3. Valitse **Tallenna**.

## <a name="configure-employee-self-service-parameters"></a>Määritä työntekijän itsepalveluparametrit

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Parametrit**.

2. Määritä **Työntekijän itsepalvelu**-välilehdelle seuraavien kenttien arvot:

   | Kenttä | Kuvaus |
   | --- | --- |
   | **Edun vahvistus** | Itsepalvelu-etujen aikana käytettävä tarkistusteksti kassalla. |
   | **Valitse edustajat automaattisesti** | Määrittää, valitaanko huollettavat ja edunsaajat automaattisesti suunnitelmavaihtoehtojen kelpoisuuden perusteella. |

3. Valitse **Tallenna**.
