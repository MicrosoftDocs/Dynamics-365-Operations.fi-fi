---
title: Palvelunimikkeiden määrää ei voi määrittää myyntitarjouksen rivillä
description: Myyntitarjouksia käytettäessä palvelunimikkeitä oleville tuotteille ei voi määrittää myyntimäärää, koska ne eivät ole laskettavissa olevia fyysisiä nimikkeitä.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476269"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Myyntitarjousrivin palvelunimikkeen myyntimäärää ei voi muuttaa

## <a name="symptoms"></a>Oireet

Jos yrität määrittää myyntimäärää (**SalesQty**) *Palvelu*-tyypin nimikkeelle myyntitarjouksen rivillä, saat seuraavan viestin:

> Päivittäminen ei ole sallittua Määrä-kentän osalta.

## <a name="cause"></a>Syy

Tämä on suunniteltu ominaisuus. Et voi määrittää myyntimäärää tuotteille, jotka ovat palvelunimikkeitä. Jos esimerkiksi tarjoat nimikkeen asentamisen palvelua, määrän tallentaminen ei ole järkevää, koska fyysistä laskettavissa olevaa nimikettä ei ole. On vain palvelu.
