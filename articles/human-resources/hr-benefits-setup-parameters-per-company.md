---
title: Etujen hallinnan parametrien määrittäminen yrityskohtaisesti
description: Määritä etujen hallinnan parametrit yrityskohtaisesti Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87d4f1e7580b333fd17d3b779aafa47c5baed424
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805655"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Etujen hallinnan parametrien määrittäminen yrityskohtaisesti

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Jokaiselle etuja tarjoavalle yritykselle on määritettävä asetukset etujen vahvistussähköposteja varten.

## <a name="configure-confirmation-email-settings"></a>Vahvistussähköpostiasetusten määrittäminen

1. Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdassa **Henkilöstöhallinnon parametrit**.

2. Määritä **Etujen hallinta** -välilehdessä seuraavien kenttien arvot: 

   | Kenttä | kuvaus |
   | --- | --- |
   | **Lähetä vahvistussähköposti** | Kun tämä toiminto on käytössä, vahvistussähköposti lähetetään työntekijöille näiden poistuessa etuihin rekisteröitymisen kokemuksesta työntekijän itsepalvelussa. |
   | **Vahvistussähköpostin malli** | Valitse organisaation sähköpostiviestimalli, jota käytetään rekisteröitymisvahvistuksen lähettämisessä. Jos et valitse mallia, lähetetään seuraavat yleiset sähköpostiviestit:<br><br>%EmployeeFirstName%,<br><br>Onnittelut! Etuihin rekisteröityminen onnistui.<br><br>Kiitos,<br><Yrityksen/organisaation nimi> - edut. |
   | **Lähettäjän oletussähköpostiosoite** | Sähköpostiosoite, jota käytetään vahvistussähköpostiviestin lähettämisessä. |

3. Valitse **Tallenna**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]