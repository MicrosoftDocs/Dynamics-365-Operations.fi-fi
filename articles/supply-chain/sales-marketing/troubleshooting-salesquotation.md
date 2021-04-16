---
title: Myyntitarjousten vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 09529ba729170be7281e2ae04008d3ba4a58e060
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824747"
---
# <a name="troubleshoot-sales-quotations"></a>Myyntitarjousten vianmääritys

Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita myyntitarjousten käytössä voi esiintyä.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>En saa muutettua palvelunimikkeen myyntitarjouksen myyntimäärää.

### <a name="issue-description"></a>Ongelman kuvaus

Jos yrität määrittää myyntimäärää (**SalesQty**) *Palvelu*-tyypin nimikkeelle myyntitarjouksen rivillä, saat viestin "Päivittäminen ei ole sallittua Määrä-kentän osalta".

### <a name="issue-resolution"></a>Ongelman ratkaisu

Et voi määrittää myyntimäärää tuotteille, jotka ovat palvelunimikkeitä. Jos esimerkiksi tarjoat nimikkeen asentamisen palvelua, määrän tallentaminen ei ole järkevää, koska fyysistä nimikettä ei ole. On vain palvelu.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]