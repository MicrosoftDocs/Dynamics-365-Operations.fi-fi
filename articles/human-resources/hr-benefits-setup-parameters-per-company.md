---
title: Etujen hallinnan parametrien määrittäminen yrityskohtaisesti
description: Määritä etujen hallinnan parametrit yrityskohtaisesti Microsoft Dynamics 365 Human Resourcesissa.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2943d0095e4c9421725b90e579b7cbb841038ab7
ms.sourcegitcommit: fd097f6f76f0d8428038fa3655b3188bf093b517
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692742"
---
# <a name="configure-benefits-management-parameters-per-company"></a>Etujen hallinnan parametrien määrittäminen yrityskohtaisesti

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