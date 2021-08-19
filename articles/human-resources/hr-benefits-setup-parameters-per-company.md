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
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0c0f9f31006ca83082ddc61da5927841855077737289e31f66708ade6d66acaf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6732798"
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