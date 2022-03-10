---
title: Etujen hallinnan parametrien määrittäminen yritystä kohti
description: Tässä aiheessa käsitellään yrityskohtaisten etujen hallinnan parametrien määrittämistä Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 8/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6b3f068c9d3198afa8cd10aaa14bbc7ec9ef3c4
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065815"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Etujen hallinnan parametrien määrittäminen yrityskohtaisesti


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Jokaiselle etuja tarjoavalle yritykselle on määritettävä asetukset etujen vahvistussähköposteja varten.

## <a name="configure-confirmation-email-settings"></a>Vahvistussähköpostiasetusten määrittäminen

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon parametrit**.

2. Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot: 

   | Kenttä | kuvaus |
   | --- | --- |
   | **Lähetä vahvistussähköposti** | Kun tämä toiminto on käytössä, vahvistussähköposti lähetetään työntekijöille näiden poistuessa etuihin rekisteröitymisen kokemuksesta **työntekijän itsepalvelussa**. |
   | **Vahvistussähköpostin malli** | Valitse organisaation sähköpostiviestimalli, jota käytetään rekisteröitymisvahvistuksen lähettämisessä. Jos et valitse mallia, lähetetään seuraavat yleiset sähköpostiviestit:<br><br>%EmployeeFirstName%,<br><br>Onnittelut! Etuihin rekisteröityminen onnistui.<br><br>Kiitos,<br><Yrityksen/organisaation nimi> - edut. |
   | **Lähettäjän oletussähköpostiosoite** | Sähköpostiosoite, jota käytetään vahvistussähköpostiviestin lähettämisessä. |

3. Valitse **Tallenna**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
