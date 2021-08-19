---
title: Palkanlaskennan integraation parametrit
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin palkanlaskennan integraation parametrit.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0c489b99d5d05ddac46d222e701512288aeb10583a5e829212e0e1c924622f16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712070"
---
# <a name="payroll-integration-parameters"></a>Palkanlaskennan integraation parametrit

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sinun täytyy määrittää tässä ohjeaiheessa kuvatut parametrit ennen Dynamics 365 Human Resourcesin palkanlaskennan integraation käyttämistä.

## <a name="enable-payroll-address"></a>Ota palkanlaskennan osoite käyttöön

Jos haluat käyttää palkanlaskennan osoitetta, sinun täytyy ottaa se käyttöön Palkanlaskennan integrointi -välilehden [jaettujen parametrien lomakkeesta](hr-setup-shared-parameters.md).

## <a name="define-the-identification-type"></a>Määritä tunnistuksen tyyppi

Jos haluat näyttää tunnistuksen tyypin tunnuksen [Palkanlaskennan työntekijä -yksikössä](hr-admin-integration-payroll-api-payroll-employee.md), sinun täytyy [määrittää henkilöstöhallinnan parametrit](hr-setup-shared-parameters.md) kullekin yritykselle.

1. Valitse **Kompensaation hallinta** -työtilan linkeistä **Henkilöstöhallinnon parametrit**. 
2. Määritä **Palkanlaskennan integrointi** -välilehdessä seuraavien kenttien arvot.

| Kenttä | kuvaus |
| --- | --- |
| Käytä tunnustyyppejä palkanlaskennan käsittelyssä | Kun tämä vaihtoehto on valittuna, valittu tyypin tunnus näytetään Palkanlaskennan työntekijä -yksikössä. |
| Tunnuksen tyyppi | Tunnistuksen tyyppi, joka näytetään [Palkanlaskennan työntekijä -yksikön](hr-admin-integration-payroll-api-payroll-employee.md)  **mshr_payrollemployeeentityid**-kentässä. |

## <a name="see-also"></a>Lisätietoja

[Palkanlaskennan integroinnin ohjelmointirajapinnan esittely](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
